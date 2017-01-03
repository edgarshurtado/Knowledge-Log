## Comands

## Controllers
### Obtain parameters passed with the http request

```php
use Symfony\Component\HttpFoundation\Request;

public function updateAction(Request $request)
{
    // $_GET parameters
    $request->query->get('name');

    // $_POST parameters
    $request->request->get('name');
}
```
### Redirect response among controllers

```php
//Symfony controller

public function someController(Request $request)
{
	$requestParams = array("param1" => "some value");
	return $this->redirectToRoute('controller_name', $requestParams);
}
```
[more info](https://symfony.com/doc/master/controller.html#redirecting)

## Bundles
### Create a new bundle

```bash
php app/console generate:bundle
```

## Doctrine
### Console

* Generate getters and setters of the entities of a bundle

```bash
php app/console doctrine:generate:entities ExampleBundle
```

* See the sqls that would be applied for a schema update

```bash
php app/console doctrine:schema:update --dump-sql
```

* Update the database with the doctrine entities schema

```bash
php app/console doctrine:schema:update --force
```

* Create a new Entity

```bash
php app/console doctrine:generate:entity
```

> We'll be prompted for some data as the name. The name of the entity has to
follow the rule of `ExampleBundle:EntityName`


### Default value for fields in doctrine
Example:

```php
/**
 * @ORM\Column(name="campoId", type="string", length=255, options={"default":"id"})
 */
```

### Relationships between entities

#### Many to one relationships
* On the many side:

```php
/**
 * @ORM\ManyToOne(targetEntity="Encuesta", inversedBy="encuestaRespuestas")
 */
private $encuesta;
```

* On the one side:

```php
/**
 * @ORM\OneToMany(targetEntity="EncuestaRespuesta", mappedBy="encuesta")
 */
private $encuestaRespuestas;
```

> If the relationship is with an Entity from other bundle, we
use the namespace of the entity. (e.g: `AdminBundle\Entity\Cliente`)

### Allow cascade persist

> This only applies to properties of an entity with a relation with other one

This is useful if an object has a foreign key to another and we want to persist
both at the same time. This means that if the referenced object isn't at the DB
it will be created and inserted.

For doing this we add the following anottation `cascade={"persist"}` as in the
example:

```php
    /*
     * @ORM\ManyToOne(targetEntity="AdminBundle\Entity\Zona", inversedBy="encuestas", cascade={"persist"})
     */
```


### Using comparative conditions

```php
$criteria = new \Doctrine\Common\Collections\Criteria();
$criteria->where($criteria->expr()->gt('prize', 200));

$result = $entityRepository->matching($criteria);
```

### How to use the WHERE variable IN array

```php
$queryBuilder = $em->createQueryBuilder();
$queryBuilder->andWhere('r.winner IN (:ids)')
             ->setParameter('ids', $ids);
```
[resource1](http://stackoverflow.com/a/11874278)
[resource2](http://stackoverflow.com/a/14790069)

### Raw sql on Symfony2
This is the way for retrieving an array with the results of a sql:

```php
$conn = $em->getConecction();
$sql = "SELECT * FROM table_name";
$r = $conn->executeQuery($sql)
          ->fetchAll();
```

With fecthAll we get the whole result array. Otherway we would have to iterate
over the pointer executeQuery returns in order to access the data.

```php
$conn = $em->getConecction();
$sql = "SELECT * FROM table_name";
$r = $conn->executeQuery($sql)

foreach($r as $result){
    var_dump($result); echo "<br";
}
```

Execute query doesn't return an array, so the following code would give us an
error

```php
$conn = $em->getConecction();
$sql = "SELECT * FROM table_name";
$r = $conn->executeQuery($sql)

var_dump($r[0]);

```

### Resources

* [Some Doctrine2 best practices](https://www.uvd.co.uk/blog/some-doctrine-2-best-practices/)

### Errors gotten

#### `Attribute "length" of ... expects a(n) integer, but got string.`

This is due when in the annotation for the attribute length we put the number
between quotes.

This is wrong:

```php
/**
 * @ORM\Column(name="ser4", type="string", length="255")
 */
private $ser4;
```

Whereas this is right

```php
/**
 * @ORM\Column(name="ser4", type="string", length=255)
 */
private $ser4;
```

> Notice the diference in the value passed to length

> [reference](http://stackoverflow.com/a/33241263)

#### `Could not convert database value "" to Doctrine Type array`
This was due of having a column as type array in doctrine and having the
value on the database as `""`. I just had to set as value for the column:
`"a:0:{}"`.

```mysql
UPDATE table SET column="a:0:{}" WHERE column = "";
```

> [source](http://stackoverflow.com/a/8819929)

#### References to the same object persisted in diferent batches

If the persistance of several objects in doctrine is done in batches (this is
inside some kind of loop that counts a maximum of objects to call `persist`
before executing `flush`) if a new object is persisted in a different batch than
a following object that has a foreign key to te former, the object would not be
the same and doctrine will either create a new one or throw a cascade persist
error if the entity with the foreign key doesn't allow to persist in cascade;

## Symfony commands

### Built in commands

* `php app\console router:debug`

* `php app\console cache:clear`

* `php app/console cache:clear --env=prod --no-debug`


#### Install assets

This process will take the assets put on the **Resources>Public** of each bundle
in **web/bundles**. Being **web** the folder where files are served directly.

* `php app\console assets:install` (as hard copies)
* `php app\console assets:install -symlink web` (as symbolic links)

Intall assets for production
* `php app/console cache:clear --env=prod --no-debug`

### Create your own
For creating a symfony command, create a file in the Command folder of the Bundle

it has to have the followin namespace and imports:

```php
namespace Madison\RutinasBundle\Command;

use Symfony\Bundle\FrameworkBundle\Command\ContainerAwareCommand;
use Symfony\Component\Console\Style\SymfonyStyle;
use Symfony\Component\Console\Output\OutputInterface;
use Symfony\Component\Console\Input\InputInterface;
```

Create a `configure` function where the name we'll be set and a `execute`
function that will contain the main business logic:

```php
protected function configure()
{
    $this->setName('namspace:nombre');
}

protected function execute(InputInterface $input, OutputInterface $output)
{
    // Bussiness logic
}
```

In the `BundleName.php` file, import your new command

```php
use BundleName\Command\CommandFile

// ...
    public function registerCommands(Application $application)
    {
        $application->add(new CommandFile());
    }

// ...
```

The injection of `InputInterface` and `OutputInterface` is compulsary

### Add Arguments or/and Options

Example:

```php
protected function configure()
{
    $this
        ->setName('name:command') // Nombre para su ejecución
        ->setDescription(' Description for your comand')
        ->addOption(
            "name", // The name of the option
            "t",    // Single char. This allows us to refer to the option as -t
            InputOption::VALUE_NONE, // The Option doesn't have stored value
            "Info about the option"
        );

    // ...

    $optionSet = $this->getOption("name");

    if($optionSet) // Do some stuff.
}
```

[resource](https://symfony.com/doc/2.8/console/input.html);

### Call command within a command
```php
    //...
    use Symfony\Component\Console\Input\ArrayInput;

    //...
    $output->writeln("Initial message ");
    $command = $this->getApplication()->find('assets:install');
    $arguments = array();

    $input = new ArrayInput($arguments);
    $returnCode = $command->run($input, $output);
```

## Assetic

### Installation

1. Install the AsseticBundle
2. Register it to *AppKernel*
3. Configure assetic in *app/config/config.yml*

For detailed info see [the symfony docs](http://symfony.com/doc/current/assetic/asset_management.html)

### Using Assetic

```twig
{# Javascript Imports from the bundle #}
{% javascripts '@AppBundle/Resources/public/js/*' %}
    <script src="{{ asset_url }}"></script>
{% endjavascripts %}

{#
    CSS imports from the bundle. Notice that the filters have to be configured
    before
#}
{% stylesheets 'bundles/app/css/*' filter='cssrewrite' %}
    <link rel="stylesheet" href="{{ asset_url }}" />
{% endstylesheets %}
```

### Prepare Assetic for production

For the production enviroment is needed to dump all the files managed by
assetic

* `php app/console assetic:dump --env=prod --no-debug`

### Errors encountered
I got the following error after configuring assetic to work from twig:

> Unable to generate a URL for the named route ...

To solve it I just cleared the cache

`php app\console cache:clear`

----

Broken references when using assetic for css that it's inside a bundle

We have to reference directly to the installed assets. So whenever we have some
assets we should do the following

1. `php app\console assets:install -symlink web`
2. The references when loading the css have to be directly having in mind that
our assets are in **web/bundles/my-bundle/**

```twig
{% stylesheets 'bundles/front/css/bootstrap-datetimepicker.min.css'
                'bundles/front/css/dataTables.bootstrap.min.css'
                'bundles/front/css/multiselectcss.css'
                'bundles/front/css/jquery-ui-1.10.3.custom.css'
                'bundles/front/css/jquerymultiselectcss.css'
                filter="cssrewrite"
%}
    <link rel="stylesheet" type="text/css" href="{{ asset_url }}">
{% endstylesheets %}
```

> Normally we reference an asset in a bundle by `@MyBundle/MyAsset`, however this
will break all internal links in css files to other assets such as images

[reference](http://www.craftitonline.com/2011/06/symfony2-beautify-with-assetic-and-a-template-part-ii/)

### YML

#### YML service names are normalized

When referencing to a service, doesn't matter if the name has underscores or
capital letters, symfony will read it correctly anyway. For example:

```yml
exampleService:
    class: DefaultBundle\Service\ExampleService
    arguments: []
```

Now, at any point where we have access to the `Container` we can get the service
with any of these combinations.

```php
$this->get("example_service");
$this->get("exampleService");
$this->get("eXamPlesErvIce");
```

I find this useful when generating the service names for the get method dinamically

### Export Data to a File in CSV

[resource](https://vauly.com/symfony2-export-csv);

and add the line: just before returning the response

```php
echo "\xEF\xBB\xBF"; // UTF-8 BOM
```

### Preparing for production enviroment a Symfony project

```bash
php app\console assets:install
php app\console assetic:dump --env=prod --no-debug
php app\console cache:clear --env=prod --no-debug
```

### Inyect security.token_storage in a service

```yml
# service.yml
service:
    class:  ...
    arguments: ["@security.token_storage"]
```

```php
use Symfony\Component\Security\Core\Authentication\Token\Storage\TokenStorage;

class Service {
    // ... logic
}
```

## FOSUserBundle

* [role hierarchical roles](http://symfony.com/doc/current/security.html#hierarchical-roles);
* [add several roles to a path](http://stackoverflow.com/a/19453541)
* [checking authentication](http://stackoverflow.com/a/12984413)
* [command line tools](http://symfony.com/doc/current/bundles/FOSUserBundle/command_line_tools.html)

### Call assets:install from Controller

`assets:install` is supposed to be called from the project root. That's why if
called from a controller, it won't be able to find the `web` folder. Thus, a
hack for being able to execute `assets:install` from a controller is changing
the php current directory. To change to the project root folder write at the
beginning or your controller:

```php

$projectRootDir = $this->get('kernel')->getRootDir() . "/../";
chdir($projectRootDir);
```

> I had to use this hack because of I couldn't specify the path to web as when
you execute the command from the console `php app\console assets:install path`

## Change execution time for the app

You have to use the ini_set('max_execution_time', 0);

If you set it in a controller it'll only afect to that controller process, if
you set it in `app.php` or `app_dev.php` it will afect the whole project.

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

### Errors got previously

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

## Symfony commands

### Built in commands

* `php app\console router:debug`

* `php app\console cache:clear`

#### Install assets

This process will take the assets put on the **Resources>Public** of each bundle
in **web/bundles**. Being **web** the folder where files are served directly.

* `php app\console assets:install` (as hard copies)
* `php app\console assets:install -symlink web` (as symbolic links)

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

The injection of `InputInterface` and `OutputInterface` is compulsary

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
# Install packages in a different dir

`composer require <package> -d <dir_route>`

# Run Scripts in a Symfony enviroment

Before runing a composer comand, just run:

```
export SYMFONY_ENV=your_enviroment
```

this will make all console commands to run with that enviroment, and composer
is one of them.

E.G: 

```
export SYMFONY_ENV=your_enviroment
composer update 
```

For more information [see this link](https://github.com/symfony/symfony/issues/11704)

###27/10/2015

* Talking with Juan Riquelme
  * NeoVim is a new VIM implementation, however it's still in alpha
  * [Koding](https://koding.com/): VM hosting plataform. For getting an VM to run projects on them
  * [Floobits](https://floobits.com/): plugguin for pair-programming works with several IDEs

* You’re not so smart Podcast
  * Mental reframing is on of the simplest and more effective ways to change bad thoughts
  * [itskoko.com](http://itskoko.com/) web page project like StackOverflow but for sharing thoughts that the community help you to *debug* into good thoughts. Created by Robert R. Morris

* Clase CodeIgnite
  * Borrar index.php de la ruta url:
    * en config.php tener la siguiente línea
    * en .htaccess escribir:

      ```
      RewriteEngine on
      RewriteCond $1 !^(index\.php|resources|robots\.txt)
      RewriteCond %{REQUEST_FILENAME} !-f
      RewriteCond %{REQUEST_FILENAME} !-d
      RewriteRule ^(.*)$ index.php/$1 [L,QSA]
      ```

    * backoffice : Sistema para el mantenimiento de la página web al estilo de wp-admin
    * En las vistas se ponen sólo los documentos .php y .html. Los CSS, JS, etc. van en otra carpeta llamada assets

* Revert all the last changes made since last commit `git reset --hard HEAD `

###28/10/2015
* EOI homework
  * Every other <day/month/year> -> Cada 2 <días/meses/años>
  * hoot -> Tocar la bocina
  * worn out -> agotado/a
  * *in* pijamas (not *on* pijamas)
  * p130 of the book is in the page 74 of the pdf

* Clase de interfaces web
  * *Carga cognitiva* se refiere a la cantidad de información que debe procesar el usuario para poder usar la aplicación.

* Reading *Appretince patterns*
  * Suggests having a list of books to read and books I already read.
    * With this idea I think it could be great having a MOOC's list as well
  * Create a meetup group
  * You don't have to read every book in a linear way. You can jump over chapters.

##29/10/2015
* Emilcar Daily
  * Roaming is going to be banished
  * El confidencial has an article talking about the current state of the net neutrality in europe
* EOI
  * fancy-dresses : disfraces
  * Halloween : All Hallows' Eve
  * to carve : tallar
  * to play a trick: hacer una jugarreta.
  * sweets or chocolates: dulces o bombones/chocolatinas.
  * clove of garlic: Diente de ajo.
  * out of my depth: Quedarse sin respiración
  * trainee soliciter : aprendiz de abogado
  * to tell off: to reprimand/ reñir
  * put your foot in it : meter la pata
  *relief : asistencia/socorro o alivio.
* Gitter spanish chat
  * How to conciliate the big amount of things we should do it's not easy. You can try do a bit of each every day o be proyect focus (you don't do other thing until you finished the previous one)
  * I'm going to put a list of blog's I've read and recommend and blog posts to read
* I could write the chapters of every book I've read instead of waiting for having read all of it
* Self-executing functions in JavaScript:
  ```javascript
  (function foo(){
    // some code…
  })()
  ```
* BackEnd DAW
  * .htaccess nos permite la utilización de urls amigables.
* There's something called Coffe Script
  * the CodeNewbie fellow piecedigital it's not fond of it because it's whitspaces sensitive. 

### 30/10/2015
* Reading How to Write a Git Commit Message
  * There's something called *commit squasing* which I should search for later
  * The 7 rules for idiomatic commit messages:
    1. Separate subject from body with blank line
    2. Limit the subject line to 50 characters
    3. Capitalize the subject line
    4. Do not end the subject line with a period
    5. Use the imperative mood in the subject line
      * I think I read about this on the Git MOOC I took
    6. Wrap the body at 72 characters
    7. Use the body to explain what and why vs. how
* Clase JavaScript
  * Hay 2 tipos de claves para la pulsación de teclas
    * código del carácter y código de tecla. Esto es porque no todos los teclados tienen la mísma disposición de los carácteres, entonces puede interesarnos más una cosa u otra.
* Clase PHP
  * añadido en la base de los href `<?php echo base_url()?>`
  * Para encriptar:
    * en el constructor del controlador cargar la librería

```php
$this->load->library('encrytp');
```

    * en el archivo config.php

```php
$config['encryption_key'] = ''; //poner una clave de encriptación
```

* FreeCodeCamp Gitter Chat
  * [Parallax scrolling](https://en.wikipedia.org/wiki/Parallax_scrolling):

> Parallax scrolling is a technique in computer graphics and web design, where background images move by the camera slower than foreground images, creating an illusion of depth in a 2D scene and adding to the immersion

### 2/11/2015
* EOI
  * drought -> sequía
  * famine -> hambruna
  * drunkenness -> de borrachos/ borracho/a
  * appeal -> llamamiento/súplica
  * project -> predecir
  * law-abiding -> que obedece las leyes
  * deterrent -> disuasorio/disuasivo
  * surveillance -> vigilancia
  * hand over -> entregar

* Center a object exactly in the middle of the screen: [explanation post](https://css-tricks.com/quick-css-trick-how-to-center-an-object-exactly-in-the-center/)

```css
  .center {
    position: fixed;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
```

* Reading Pragmatic Programmer:
  * Relentless -> Implacable
  * preclude -> excluir
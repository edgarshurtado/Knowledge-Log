###27/10/2015

* Talking with Juan Riquelme
    * NeoVim is a new VIM implementation, however it's still in alpha
    * [Koding](https://koding.com/): VM hosting plataform. For getting an VM to
      run projects on them
    * [Floobits](https://floobits.com/): plugguin for pair-programming works
      with several IDEs

* You’re not so smart Podcast
    * Mental reframing is on of the simplest and more effective ways to change
      bad thoughts
    * [itskoko.com](http://itskoko.com/) web page project like StackOverflow but
      for sharing thoughts that the community help you to *debug* into good
thoughts. Created by Robert R. Morris

* Clase CodeIgnite
    * Borrar index.php de la ruta url:
        * en config.php tener la siguiente línea
        * en .htaccess escribir:

```
RewriteEngine on RewriteCond $1 !^(index\.php|resources|robots\.txt)
RewriteCond %{REQUEST_FILENAME} !-f RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ index.php/$1 [L,QSA] 
```

    * backoffice : Sistema para el mantenimiento de la página web al estilo de
      wp-admin
    * En las vistas se ponen sólo los documentos .php y .html. Los CSS, JS, etc.
      van en otra carpeta llamada assets

* Revert all the last changes made since last commit `git reset --hard HEAD `

### 28/10/2015

* EOI homework
    * Every other day/month/year -> Cada 2 días/meses/años
    * hoot -> Tocar la bocina
    * worn out -> agotado/a
    * in pijamas (not *on* pijamas)
    * p130 of the book is in the page 74 of the pdf

* Clase de interfaces web
    * Carga cognitiva se refiere a la cantidad de información que debe procesar
      el usuario para poder usar la aplicación.

* Reading Appretince patterns
    * Suggests having a list of books to read and books I already read.
        * With this idea I think it could be great having a MOOC's list as well
    * Create a meetup group
    * You don't have to read every book in a linear way. You can jump over
      chapters.

##29/10/2015
* Emilcar Daily
    * Roaming is going to be banished
    * El confidencial has an article talking about the current state of the net
      neutrality in europe
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
    * relief : asistencia/socorro o alivio.
* Gitter spanish chat
    * How to conciliate the big amount of things we should do it's not easy. You
      can try do a bit of each every day o be proyect focus (you don't do other
thing until you finished the previous one)
    * I'm going to put a list of blog's I've read and recommend and blog posts
      to read
* I could write the chapters of every book I've read instead of waiting for
  having read all of it
* Self-executing functions in JavaScript

```javascript

 (function foo(){ 
 // some code… 
 });

```

* BackEnd DAW
    * .htaccess nos permite la utilización de urls amigables.
* There's something called Coffe Script
    * the CodeNewbie fellow piecedigital it's not fond of it because it's
      whitspaces sensitive. 

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
    * código del carácter y código de tecla. Esto es porque no todos los
      teclados tienen la mísma disposición de los carácteres, entonces puede
interesarnos más una cosa u otra.
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

> Parallax scrolling is a technique in computer graphics and web design, where
> background images move by the camera slower than foreground images, creating
> an illusion of depth in a 2D scene and adding to the immersion
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

* Center an object exactly in the middle of the screen: [explanation
  post](https://css-tricks.com/quick-css-trick-how-to-center-an-object-exactly-in-the-center/)

```css
.center {
     position: fixed; 
     left: 50%;
     top: 50%;
     transform: translate(-50%, -50%);
 }
 ```

#### Pragmatic Programmer:
  * Relentless -> Implacable
  * preclude -> excluir

### 3/11/2015

* EOI

    * Ask and answer in groups
        * Do you shop at Charity shops?
        * Do you take into consideration which charity shops do you go to?
        * Do you shop at charity shops for that fell good feeling you have
          helped somebody out?
        * Do you simply go to charity shops to look for a bargain?

    * Charity:
        * FairTrade
        * Caritas
        * The Red Cross
        * Save the Children
        * Alma de Acero
        * RSPCA -> Royal Society for the Prevention of Cruelty to Animals
          (Protectora de animales)
          * Kennel -> perrera
        * OXFAM
          * Famine = hanger = hambruna

    * Things people can do for charity
      * Give money to people collecting in the street
      * Buy/Give clothes
      * Go to events that raise money
      * Give/buy food
      * Harley Davidson event Every Km counts
      * Participate in race that raise money
      * Give toys
      * Sell/buy lotery tickets
      * Be a volunteer
      * T.V. or radio programmes to raise money

    * Handicraft -> manualidades

    * State Verbs
      1. Emotion -> love, hate, want, need
      2. Possession -> have, own, belong
      3. Sense -> see, hear, smell, seem
      4. Thoughts -> know believe, remember, understand...

    * Listening exercise
        * How long have you been working here?
        * How many chocolates have you eaten?
        * What have you been doing?

* CodeNewbie thread [Windows vs Mac for
  coding](http://discourse.codenewbie.org/t/windows-vs-mac-for-coding/1317/5)

> If you do webdev, having easy access to software which works similar to the
> vast majority of servers out there is handy. Additionally, if you need to
> debug / code for iPhone / iPad, you're going to need a Mac to debug properly.
>
>[Cory_Underwood](http://discourse.codenewbie.org/users/Cory_Underwood)

#### Pragmatic programmer
    * Unforeseen -> imprevisto
    * shortcomings -> defectos
    * My cat Ate my Code
    * When a problem appears don't make excuses but posible solutions
    * Don't blame others work if there was something you could have done to
      prevent it
    * Whenever you're going to report a problem make sure you have tried all the
      posible solutions that came to your mind first. Try to think what your
colleges would ask you
        * First mention of the rubber duck =).

    * Software Entropy

> When disorder increases in software, programmers call it "software rot"

    * setback -> revés/contratiempo
    * We have to repair any bad piece of code as soon as posible. If we let the
      bad implementations or decitions gather, the software will deteriorate
(Broken Window Theory)

* Clase cliente (Forms)
    * Existe el array `form` en JS nada más cargar la página, pero esta forma de
      programar no está recomendada porque hay que acceder a los distintos
formularios mediante index. La manera correcta sería mediante ID 
    * Al final de la sección 7.1 hay un grupo de funciones útiles para
      validación de formularios.

    * [pForm](www.phpform.org) Para la creación automática de formularios en
      html

### 4/11/2015

Pushbullet chrome plugin causes a [pasteboard
issue](https://discussions.apple.com/message/27250427#27250427)

Delete all files without extension from bash ```bash $ find . -type f  ! -name
"*.*"  -delete ``` 

Compile and execute C from terminal ```bash $ gcc -o compiled_file_name
source_file.c $ ./compiled_file_name ```

Resize a tmux split to full window `ctr-B + z`

Close files in vim without quiting vim `:bd` 

Know if the web browser es Internet Explorer ```javascript var ie =
navigator.userAgent.toLowerCase().indexOf('msie')!=-1; ```

Big fail done by mysefl: `var x-coords = ...` instead of `var x_coords = ...` I
lost too much time debuggin this =(

#### EiE Inflación : aumento del coste de vida con respecto al aumento de la
productividad del país

Puede ser que queramos buscar a la competencia. Eso es porque estando ahí la
gente seguro que pasará ya sea para comprarme a mí o a la competencia, pero se
crea así una "zona" donde los clientes pueden fácilmente encontrar un producto
que están buscando.

No confundir imagen corporativa con cultura corporativa:
    * Cultura corporativa: Cómo és la empresa
    * Imagen corporativa: Cómo la sociedad ve la empresa

[Dark Horse](https://en.wikipedia.org/wiki/Dark_horse) Alguien del que no se
esperaba grandes resultados y al final acaba destacando.

#### Despliege WEB

El router es el encargado de mandar la petición de dns del usuario a un servidor
dns

La comunicación con el servidor dns se hace mediante ip

El router ante un conflicto entre el servidor objetivo configurado en el router
y la configuración del ordenador, manda el router en última instancia 

el archivo `host` es un archivo local que sirve de "servidor dns"

El cliente pide y recibe información por protocolo `tcp` pero el servidor por
`udp`
* tcp orientado a la conexión
    * Esto significa que el ordenador gasta recursos y no se produce la
      comunicación a no ser que la conexión se establezca
* udp no-orientado a la conexión
    * Se realiza el envío sin asegurar la recepción.
    * No obstante este es más rápido que el tcp y gasta menos recursos

#### Pragmatic programmer
* Quality as one of the proyect requirements. Look for the Good Enough Software
* Don't do big changes all at once but gradually implement them
* Don't lose the big picture and react quickly to the signs of something going
  wrong
* Invest in your knowledge portfolio:
    * Read technical books and non-technical books
    * Learn new languages.
    * Balance between safe investments (popular technologies today) and risky
      investments (be an early adopter)
    * Seek for challenges. One think you're asked about and you don't know the
      solution is a challenge to seek and find the answer.

### 5/11/2015

#### EOI

* goods --> products (bienes)
* spokesman --> portavoz
* *badly* always before the adjective: be badly hurt (not be hurt badly)

#### Slack CodeNewbie
* Guido van Rossum --> Creador de Python

#### Pragmatic programmer

* look over -> echar un vistazo
* overlook -> pasar por alto

> Too many developers concentrate solely on content when producing written
> documents. We think this is a mistake

* Dave generated tests from the document?
>

### 6/11/2015

#### CRUD PDO Project

For being able to work with utf-8 characters, when stablishing the connection
add:

```php <?php $dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass);
?> ```

This add `dbname=test` to the `dsn` example in the PDO docs whitch doesn't work
for retrieving data in utf-8 [source](http://stackoverflow.com/a/11249695)


### 8/11/2015

#### EOI

* taxpayers --> contribuyentes
* pursue -> discutir
* blur -> hacer borroso
* prompt -> rápido/a

#### CodeNewbie Slack

* pip -> Package managment for python.

#### The pragmatic Programmer

* Refactoring
> Look for any opportunities to reorganize the code to improve its structure and
> orthogonality.

### 9/11/2015

#### The pragmatic Programmer
* Make critical no reversible decisions. Implement things to dependent of the
  caracteristics at the time of development

>“The mistake lies in assuming that any decision is cast in stone—and in not
>preparing for the contingencies that might arise”
>
>Fragmento de: Hunt, Andrew;Thomas, David. “The Pragmatic Programmer: From
>Journeyman to Master”.

* Use *tracer bullets*: rudimentary software that works for giving a real user
  experience. This technique is based on implementing a not fully functional
program. Once we got the basic stuff runing satisfactory, the further
development consists in adding functionality around it. It defers from
Prototyping because prototypes just give a glance of the user experience and are
completely disposable. But the tracer bullets keeps at the codebase.

> “The distinction is important enough to warrant repeating. Prototyping
> generates disposable code. Tracer code is lean but complete, and forms part of
> the skeleton of the final system. Think of prototyping as the reconnaissance
> and intelligence gathering that takes place before a single tracer bullet is
> fired.”
> 
> Fragmento de: Hunt, Andrew;Thomas, David. “The Pragmatic Programmer: From
> Journeyman to Master”. iBooks. 

### 10/11/2015

#### EOI

* They gave me some present (ACTIVE)
    * Some presents were fiven to me.
    * I was given some presents (more common)

* On or at:
    * I was given some presents on Christmas' eve. (Use *on* for specific time)
    * I was given any presents at Christmas.

* stunt -> very exciting action

#### The Pragmatic Programmer

* clay -> barro

> Prototyping is a learning experience. Its value lies not in the code produced,
>but in the lessons learned. That's really the point of prototyping.”
>
>Fragmento de: Hunt, Andrew;Thomas, David. “The Pragmatic Programmer: From
>Journeyman to Master”.

* Things that can be ignored in prototyping:
    * Correctness (use dummy data)
    * Completness
    * Robustness
    * Style

* high-level scripting program languages as glue for low-level code

### 11/11/2015

#### Despliegue de Aplicaciones Web
2 tipos de modelos para la resolución de nombres DNS
* Iterativa
* Recursiva

#### Eli Video
* Direct your learning problem solve based
* Informatics is a massive field to learn everything
* Is a field where you learn through dive into the middle and learn from it
* Cisco ??
* Virtual Hybrid Infraestructure ??
* Certifications just if you have several years in experience

### 12/11/2015
#### EOI
* Correcting the letter exercise
    * with regard for --> with regard to
    * properly wahsed --> properly cleaned
    * Second --> Secondly.
    * Lastly --> Finally
    * Persuaded --> Pursued
    * order to dissolve this matter --> order ro resolve this matter
    * fund --> refund
    * contract --> contact
    * convince that this step has been taken. --> confirm that this step has
      been taken
    * Thanks for your promply attention to ths matter --> prompt
    * Yours faithlessly --> Yours faithfully

* Vocabulary
    * Electric kettle
    * CC -> enclosed
    * lines = wrinkes
    * to do the bads -> quitarse las bolsas de los ojos
    * cosmetic surgery -> cirugía estética
    * botox (to fill the lines)
    * tho have your legs waxed -> depilarse las pierna
    * pedestrianized area -> zona peatonal
    * boobs job --> aumento de pecho
    * to be for --> in favour

* Desarrollo de Interfaces Web
    * webGL: Renderizado ??
    * APIs para HTML5
        - Geolocalización
        - Almacenamiento
        - Sockets
    * Etiquetas añadidas:
        - Header
        - Audio
        - Embed
        - header
        - nav
        - footer
    * Página para saber las características que soporta cada navegador 
    [Can I Use](http://caniuse.com/)
    * HTML5 tiene soporte nativo para calendario y color-pick
    * placeholder es de HTML5

* Cliente
    * Tooltip -> recuadros de ayuda
        * Librería de tooltips -> [OpenTip](http://www.opentip.org/)

# 13/11/2015
## Pragmatic Programmer
* Buzzword -> Palabra de moda
* *Domain Languages* -> Pseudo or mini languages that are used to abstract the
implementation of a program but indicate the steps that are needed for the real
solution
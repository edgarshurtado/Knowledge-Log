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

* CodeNewbie thread [Windows vs Mac for coding](http://discourse.codenewbie.org/t/windows-vs-mac-for-coding/1317/5)

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

Pushbullet chrome plugin causes a [pasteboard issue](https://discussions.apple.com/message/27250427#27250427)

Delete all files without extension from bash 

```bash
bash $ find . -type f  ! -name
"*.*"  -delete 
```

Compile and execute C from terminal 

```

bash $ gcc -o compiled_file_name
source_file.c $ ./compiled_file_name 
```

Resize a tmux split to full window `ctr-B + z`

Close files in vim without quiting vim `:bd` 

Know if the web browser es Internet Explorer 

```javascript

var ie = navigator.userAgent.toLowerCase().indexOf('msie')!=-1; 

```

Big fail done by mysefl: `var x-coords = ...` instead of `var x_coords = ...` I
lost too much time debuggin this =(

#### EiE Inflación : aumento del coste de vida con respecto al aumento de la productividad del país

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

```php
<?php $dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass); ?>
 ```

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

> “The mistake lies in assuming that any decision is cast in stone—and in not
> preparing for the contingencies that might arise”
>
> Fragmento de: Hunt, Andrew;Thomas, David. “The Pragmatic Programmer: From
> Journeyman to Master”.

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
> but in the lessons learned. That's really the point of prototyping.”
>
> Fragmento de: Hunt, Andrew;Thomas, David. “The Pragmatic Programmer: From
> Journeyman to Master”.

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

## Bug with wifi share
* It happened to me that because of I was in class sharing wifi. Then, at home
my wifi connection didn't work. To fix it I had to connect the rj45, then go to
wifi share and disable it.

#16/11/2015
## Despliegue de aplicaciones
* El SMTP es un canal de comunicación bidireccional entre servidores.
* El IMAP/POP3 es el canal de comunicación entre servidor y cliente.
* La história de HOTMAIL:
    - Cuál fué la idea inicial?
        * Poder acceder a el inbox desde cualquier parte del mundo
    - En qué año?
        * Fue lanzado en 1996
    - Cuantos trabajaban en el ppi?
        * Sólo 2. Sabeer Bhatia y Jack Smith
    - Quién, cuanto y por cuanto se compró?
        * Microsoft lo compró en 1997 por 400 millones de $
    - Cuáles crees que fueron las causas del éxito?
        * Acceso al inbox desde cualquier punto del mundo, y después su
        integración con todo el ecosistema MSN de Microsoft.

[The Single Biggest Mistake Programmers Make Every Day](https://medium.com/javascript-scene/the-single-biggest-mistake-programmers-make-every-day-62366b432308)
* The process for developing should be: *Make it work, make it right, make it
fast*

[5 Reasons Why Swift is Perfect for Beginners](http://learn.onemonth.com/5-reasons-swift-is-perfect-for-beginners?utm_source=twitter&utm_medium=social&utm_campaign=sumome_share)
* Apple is going to make Swift open-source

# 17/11/2015
## EOI
* electrical appliances = hosehold appliances = white goods -->
Electrodomésticos
* instalment -> Episode
* to pay by instalments -> Pagar a plazos
* leisure -> free time

#18/11/2015
## Trouble-shooting solarized broken color in tmux

I had a problem that made vim represent solarized colors badly when running
in tmux. To fix it I just need to create a *.tmux.conf* file with the following
line:

```
set -g default-terminal "screen-256color"
```

For more information and other solutions you can read this 
[github issue](https://github.com/altercation/solarized/issues/159)

## Set mailx to send emails with gmail account
* Follow the instructions on [this post](http://owleon.blogspot.com.es/2014/11/command-line-mail-with-gmail-smtp-on.html)

#19/11/2015
##EOI
* scenary = landscape = paisaje.
* you're always dragging your children = Simpre llevas a los niños arrastrándo
* get away from it all! -> Escaparse
* unwind -> desconectar
*Board Games*
* draughts -> damas
* ludo -> Parchis
* snakes and ladders = juego de la oca

#20/11/2015
## get the css properties from an external css file

```javascript
    var style = window.getComputedStyle(element, pseudoElt);
```
* [Docs](https://developer.mozilla.org/es/docs/Web/API/Window/getComputedStylehll)

other solution (more reliable):

```javascript
var style = window.getBoundingClientRect();
```


## Despliegue de aplicaciones web
### Pasar un dominio de una empresa registradora a otra
1. Pedir el **autocode** en la registradora origen
    - Hay que hacerlo antes de que empiece el periodo de autorenovación
2. Darte de alta en la destinataria pasándole tus datos junto al autocode

### Sockets
Ventajas:
* Necesidad de instalar únicamente una vez el servidor
* Flexibilidad

La parte de Java que se baja y ejecuta en la parte cliente es conocida como 
applet. Es **bytecode** descargado desde el servidor.

Al crear el socket servidor diremos el puerto por el que trabajaremos y cuando
creemos el socket del servidor especificamos también el ip del servidor.

Los socket consumen recursos, motivo por el cual se realizan los ataques ddos.
Se basan en crear sockets hasta desbordar el servidor.

Las 2 principales librerías para hacer sockets:
* java.io
* java.net

#24/11/2015
## EOI
hooked on = adicted to.

###Used to/would:
* when I was a child I **used to** + **infinitive**
* My grandfather would sit in front of the T.V. every Sunday to watch
bullfighting

* When I was a child I used to read a hole book while my mother and grandmother
where shopping

###Be used to + **ing**
* I'm used to getting up early.

* I'm used to working mostly on my computer

###To get used to
* I am getting used to **eating** healthy food

* My grandmother has got used to sending whatsapps whith her friends.

* The internet
    - Don't forget the article **the**

* Niche holiday
    - Holidays for people with particular interest
* Flopout holiday
    - Holidays in which you do nothing but relax
        * Like sunbathing (lying in the sun)

#26/11/2015
##EOI
Like-minded people: People with similar interest

Self-catering accomodation : You provide food for yourself, and you have to cook it.

Travelling broadens the mind -> Viajar abre la mente

* Palm tree holidays -> vacaciones de playa
* Package holidays -> Vacaciones de todo incluído
* Camp-site holidays -> Acampada
* Potholing -> espeleología
* Scuba diving -> buceo
* Bungee-jumping -> Puenting

unspoilt place -> virgin place

**Travel** is a verb and a noun, but as a noun it is a general word usually
uncountable. We can't say **a travel**

Leaflet -> panfleto (propaganda)

Full-boarding -> pensión completa

###p36 ex 4a

2. Are you going to do// Yes we're going to 
3. The plane lands// we get
4. It's likely to rain//It'll be//I'll check
5. We might go // we could stop off
6. Is thinking in going // He's hopping to ask

###p37 6B
* Ecotour
* Location
    - National Park of Monfrague
* Arrange little buses for little groups
* Easter holiday
* 1 night in a rural house and 1 night camping in the wildness
* Bird-watching, hicking, night songs

#29-11-2015
## Match whitespace in RegExp in JS
```
new RegExp("\\s", "g")
```

I have to use \\s instead of \s when using this constructor

#30/12/2015
## Grocery_CRUD issue with set_relation
Can't have 2 tables with a field named the same way used with set_relation
[explanation](http://www.grocerycrud.com/forums/topic/254-set-relation-breaks-processing-of-field-with-same-name-returned/#entry10005)

## Pragmatic programer
Use codegenerators and textprocesors


#2/12/2015
# Create globally executable python scripts
[source](http://stackoverflow.com/questions/15587877/run-a-python-script-in-terminal-without-the-python-command)

## Make python run gitignore.io (to test)
sudo vim /usr/local/bin/gi
curl -L -s https://www.gitignore.io/api/\$@
Permisos y ale. Y si ahí no va, pues en /usr/bin/

#6/12/2015
## Config apache for override urls
[apache.org](http://httpd.apache.org/docs/2.4/mod/core.html#allowoverride)
set AllowOverride from none to all

#8/12/2015
## Code Igniter Error: No input file specified
add the ? sign after index.php in the .htaccess file
[source](http://stackoverflow.com/questions/6118740/codeigniter-no-input-file-specified)

#9/12/2015
## Barcelona abre un grado en Bioinformática
[fuente](http://www.bsc.es/sites/default/files/public/about/news/bib-10052015-lavanguardia.pdf)

#11/12/2015
## Pragmatic Programer
* Don't turn off assertions when ship code. If it's needed a better performance
in the code just turn off the assertions you need, but don't every of them.

#13/12/2015
## Pragmatic Programmer
* Deallocate resources in the opposite order to that in which you allocate them. That way you won't orphan resources if one resource contains references to another.”

# 2015-12-17

## EOI
Even gift ourselves with **wrong**
Even treat ourselves **right**

It's just cloth ... **wrong**
it's just a piece of cloth **wright**

surrogate daughter --> hija adoptiva
to steer --> conducir
gap year --> año sabático
rusty --> oxidado

## Mirando cursos del CIPF
* 6-04-2016 -> Job opportunities / Carrers in science
* 11-04-2016 -> Proteomics
* 13-04-2016 -> Statistical graphics.
* 11-05-2016 -> Genomics
* 23-05-2016 -> Developing statistical intuition


# 2015-12-18
## Pragmatic Programmer
* Architecture the programs as independent services and plan for concurrency.
Even though we don't need to do this it makes possible the scalability of the
application and gives a cleaner code.

# 2016-1-09
## Pragmatic Programmer
`cron` it's a unix command to schedule processes 
[wikipedia](https://en.wikipedia.org/wiki/Cron)

# 2016-1-11
##EOI
* stretch (as noun) -> tramo
* tide -> marea
* strolling -> paseando
* as time and again -> una y otra vez
* stranded -> varado (sirve también para decir que alguien se ha quedado tirado
por ejemplo si el vuelo del avión se cancela)
* dried up -> seco

## Despliegue de aplicaciones web
La *capa de enlace* se encarga de garantizar que el canal de transmisión es
correcto
Además la capa de enlace sincroniza la velocidad de envío de información

El cómo es con los protocolos, el qué es con las capas

# 2016-1-12
#EOI
* New Years Resolution -> Propósitos de año nuevo
* Drew nearer -> se acercó
* Heads or Tails -> Cara o cruz
* Toss up a coin -> lanzar una moneda
* Safe and sound -> Sano y salvo
* Pulling my leg -> Tomándome el pelo
* A bird in the hand is worth two in the bush -> Más vale págaro en mano que
ciento volando

# 2016-1-13
## EOI
* wade -> andar por el agua
* sail -> vela
* dejectedly -> con desánimo

## Servidor
* jsp -> **Java Server Page** página web generada dinámicamente que combina
html con java
* scriplet -> código java presente en un documento jsp
* directives jsp -> JSP directives provide directions and instructions to the 
container, telling it how to handle certain aspects of JSP processing. A JSP 
directive affects the overall structure of the servlet class

## VIM
Write timestamp quickly on VIM
```
:r! date
```
[More info](http://superuser.com/questions/451340/how-to-insert-the-date-into-vim)


# jueves, 14 de enero de 2016, 09:23:29 CET
## EOI

* Birds of a feather flock together -> Dios los cría y ellos se juntan
* When the cat's away the mice will play -> Cuando no está el *jefe* los empleados
hacen lo que quieren
* Don't put the cart before the horses -> No empieces la casa por el tejado
* Don't count your chicken before ther are hatched -> No cantes victoria andtes
de tiempo
* Out of sight out of mind -> Ojos que no ven, corazón que no siente.
* A stich in time saves nine -> Más vale prevenir que curar.
* There's no smoke without fire -> Cuando el río suena, agua lleva 
* People who live in glass houses shouldn't throw stones -> Don't say bad things
about others because it could come back
* It's no use crying over split milk -> A lo hecho pecho
* In for a penny in for a pound -> De perdidos al río

## Servidor: Servlets
* CGI: solicitar datos de un programa ejecutado en un servidor web. CGI 
especifica un estándar para transferir datos entre el cliente y el programa


# viernes, 15 de enero de 2016, 13:51:46 CET
## Least Common Multiple in python

```python
from fractions import gcd

def lcm(numbers):
    return reduce(lambda x, y: (x*y)/gcd(x,y), numbers, 1)
```
[source](http://www.enrico-franchi.org/2010/09/nice-functional-lcm-in-python.html)


# Mon Jan 18 16:51:43 CET 2016
## Despliegue aplicaciones Web
Principal tarea del protocolo IP es el enrutamiento
Información necesaria para la conexión de 2 ordenadores IP, máscara de subred,
puerta de enlace (el router).

La información en internet viaja en forma de paquetes (troceada). De esta forma,
cada paquete puede buscar rutas diferentes para llegar al destino. Así no hay
líneas dedicadas. Si en algún momento un nodo callera, el protocolo ip es capaz
de redirigir los paquetes (siempre en la ruta que menos congestione la red). 
Además, una vez en el destino, el protocolo IP se encarga de reordenar los 
paquetes para que formar el archivo que ha sido enviado.


La negociación de una clave de sesión depende de la capa de presentación.

El concepto de **procesos** aparece en la capa de transporte, ya que un puerto
es la forma de identificar un proceso en una IP determinada.

Aunque parezca que las capas hablan entre ellas de forma horizontal, no es
cierto, sino que es vertical.

En una conexión tipo TCP, cada paquete recibido genera un mensaje respuesta 
desde el cliente (ACK).

Cuando se manda información, a medida que bajamos en la arquitectura TCP/IP se
le va añadiendo información que necesitan (los headers).


# Wed Jan 20 00:23:35 CET 2016

## Avoid jslint error message when using jquery
Add this to the top of the js file
```
/*jslint browser: true*/
/*global $, jQuery, alert*/
```

# Wed Jan 20 18:14:55 CET 2016
## EIE

La SA ha de tener un grupo designado para la revisión de las cuentas de la
empresa.

## Despliegue de Aplicaciones
### Arquitecturas de conexión
* *OSI* Modelo abierto y estándard de interconexión
* *SNA* Utilizada por algunos organismos debido a motivos de seguridad (entre
los motivos es porque es poco conocida).
* *TCP/IP*
* *ARCNET*
* *DNA*
### Nombre de las unidades de datos en cada capa OSI
* *Física* : Bits
* *Enlace* : Frames/Tramas
* *Red*: Packages/Paquetes
* *Transporte*: Segments/Segmentos
* *Sesión, presentación y aplicación*: Data

### Protocolos
Aunque también se puede hablar de protocolos en la capa física, los protocolos
propiamente dichos empiezan en la capa de enlace.

* Enlace -> Ethernet, Wifi, Fast Ethernet, Gigabit Ethernet, PPP, ATM, HDLC
* Red -> IP, Appletalk, NetBEUI (Microsoft), IPX
* Transporte -> TCP, UDP, SPX
* Sesion -> NetBIOS

# Thu Jan 21 09:22:36 CET 2016
## EOI
### Grammar photocopy to practice wishes and regrets
* Start
    * I whish I hadn't stayied that long on David's.
    * I whish I could have seen an elephant.
    * I whish I didn't have to work today.
    * I whish you wouldn't be always late.
    * I wish I was taller.
* I wish I haven't accepted to run with my classmate.
    - I wish I wasn't talked like that.
    - I wish I had fixed the door.
    - I wish I had someone to went tracking with.
    - I wish I could dance salsa.
    - I wish I had another seat.
* I wish I had started to code earlier .
    - If only I had brought with me something to eat.
    - If only those photos had burnt.
    - If only I had a flatmate who pull his weight.
    - If only I had saved enought money to pay the taxes.
    - If only I had learnt to play the guitar.
* I wish I could live with my girlfriend.
    - I wish I had done a backup of my files.
    - If only I had been born in America.
    - I should've saved more money.
    - I should've brought my umbrella.
*
    - If only I had felt ill other day.
    - I wish he had already washed his hair.
    - I wish I had taken the elevator.
    - I wish I had thrown something heavier at him.
    - If only my partner wouldn't be such a coward.
* 
    - If only I had enjoyed life more.
    - I should've been more sociable when I was young.
    - I should've bought an extra battery.

### Other
* multi-word phrases -> phrasal verbs
    
## Cliente
* Cuando hacemos un método *get* la información se manda por la **URL**, cuando el 
método es POST la información se manda por la **cabecera HTML**

# Mon Jan 25 16:39:24 CET 2016
## Despliegue aplicaciones web
### Práctica Apache

Los archivos que son pedidos con una extensión php o phtml, el servidor apache lo
envía al intérprete php que tenga el servidor instalado y cuando este le devuelve
al apache el html, esto es lo que se envía al cliente que haya hecho la petición.

# Tue Jan 26 10:03:47 CET 2016
## EOI
* A british sitcom -> situational comedy -> soap opera
* sends shivers up my spine -> me da escalofríos
* pull aside -> lo aparta / echar a un lado
* blink -> parpadear
* wink at me -> guiñar un ojo
* gutted -> disappointed


# Mon Feb  1 18:48:12 CET 2016
## EOI
### Vocabulary about films
* Predictable
* Poignant -> conmovedor
* Moving -> emotivo
* Touching -> emotivo
* chilling --> escalofriante
* gripping --> fascinante/apasionante
* creepy -> de terror/ de miedo
* dull -> aburrido/soso
* electrifying
* brilliant
* horrific -> horrible/espantoso
* fast-paced
* weak
* unforgettable

# Tue Feb  2 09:46:37 CET 2016
## EOI
### Vocabulary
* I had my leg in plaster -> tener la pierna escayolada.

## Design
* [Color Scheme Designer](http://colorschemedesigner.com/csd-3.5/). Web para ayudar en la elección de colores a la hora de diseñar.

# Thu Feb  4 10:11:57 CET 2016
## EOI
* When want to know the sex of an animal -> *Is it a he or a she?*
* Sheik -> Jeque Árabe
* Setting of -> Dónde está situado?
* Box-office hit -> Éxito de taquilla

## Angular Course
### Angular Scaffolding
* app
    - styles        //Contiene los documentos CSS de la aplicación
    - images        // Contiene las imágenes de la aplicación
    - scripts
        - controllers   //Contiene los controladores de AngularJS
        - directives    //Contiene los directives de AngularJS
        - filter        //Contiene los filters de AngularJS
        - services      // Contiene los servicios de AngularJS
        - app.js        // Definición y configuración de la aplicación
        - values/constants      // Settings del proyecto. Esta carpeta es opcional
    - vendor    //Contiene las librerías de terceros
    - views     //Contiene las vistas HTML
    - index.html        // Punto de entradda de la aplicación

# Tue Feb  9 09:32:20 CET 2016
## EOI
### Vocabulary
* V.A.T -> Value Added Tax (IVA)
* Yacht -> Yate
* Interestingly -> Curiosamente
* freebies -> regalos
* outlook -> actitud/opinión/pronóstico
* money launderers -> blanqueadores de dinero
* launderette -> lavandería
* hecklers -> provocadores/ persona que interrumpe con preguntas
* have a knack -> tener maña para algo

##EIE
### T6
* Ventana única empresarial: Facilita las tramitaciones para la creacion de empresas, permitiendo entregar toda la documentación en un único sito y ya son los 
* Las empresas han de tener de forma obligatoria la razón social, el nombre comercial es un nombre que pueden o no tener

## PHP - AJAX
### How to retrieve a php return as a xml file:

Insert this before any echo:

```php
header('Content-Type: text/xml');
```
# Mon Feb 15 09:45:28 CET 2016
## J2EE - Hibernate. Pasos a seguir.
1. Crear una web aplication nueva, elegir el directorio y tener marcada la opción de tener una carpeta dedicada para las librerías en el proyecto
2. Elegimos servidor (En este caso Tomcat)
3. Importamos librería Hibernate 4.3.1 y seleccionamos conexión.(Si la conexión no está creada le daremos a crear nueva conexión.) 
    1. Elegir MySQL Driver
    2. rellenar datos de la base de datos. (Podemos clickar en "Test Connection" para comprobar que la conexión se realiza correctamente);
    3. Click Finish
4. Una vez creado el proyecto nos aseguramos de contar con las librerías (Hibernate 4.3.x, Persistence JPA2.1 y MySQL JDBC Driver). Las que no tengamos las importamos.
5. Creamos el paquete entity y dentro una class que representará la tabla de la BD que queramos persistir.
6. La clase ha de implementar Serializable.
7. Creamos todos los atributos que necesitemos junto a sus setter, getter y un constructor vacío. Cada atributo será una columna de la tabla a persistir, y además podemos crear un constructor con parámetros para facilitar la instanciación del objeto.
### Mapeo con xml
8. Click en el paquete entity y seleccionar new > Hibernate Mapping Wizard
9. Seleccionamos la clase y la tabla de la base de datos.
10. en el archivo generado xml debemos definir todos los atributos referenciando la columna de la BD a la que apuntan y la propiedad de la clase equivalente. Así nuestro ejemplo quedaría de la siguiente forma:

Original
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE hibernate-mapping PUBLIC "-//Hibernate/Hibernate Mapping DTD 3.0//EN" "http://hibernate.sourceforge.net/hibernate-mapping-3.0.dtd">
<hibernate-mapping>
  <class name="entity.CgStore" table="cg_store"/>
</hibernate-mapping>
```

Configurado
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE hibernate-mapping PUBLIC "-//Hibernate/Hibernate Mapping DTD 3.0//EN" "http://hibernate.sourceforge.net/hibernate-mapping-3.0.dtd">
<hibernate-mapping>
    <class name="entity.CgStore" table="cg_store">
        <id column="store_id" name="store_id" type="integer" />
        <property column="store_address" name="store_address" />
        <property column="store_name" name="store_name" />
        <property column="store_phone" name="store_phone" /> 
    </class>
</hibernate-mapping>
```
### Mapeo con anotaciones
8. Se modifica la clase de Java a persistir, añadiendo anotaciones JSP a las definiciones de las propiedades y a la propia clase, quedando así:
```
@Entity
@Table(name="cg_store")
public class CgStore implements Serializable{
    @Id
    @Column(name="store_id")
    private int store_id;
    @Column
    private String store_name;
    @Column
    private String store_address;
    @Column
    private String store_phone;

    public CgStore() {}

    //...Getters and Setters

}
```
El `Column` del id está puesto como ejemplo de cómo se debería escribir en caso de que el nombre de la propiedad no coincida con el nombre de la tabla

9. Añadimos la clase al mapeo en hibernate.cfg.xml añadiendo la línea siguiente dentro de `session-factory`
```
<mapping class="entity.CgStore" />
```


### Siguientes pasos
11. Creamos HibernateUtils en un paquete `utils`
12. Creamos una clase donde definir todas las funciones que necesitemos para trabajar con la clase en un paquete `dao`. En esta primera prueba vamos a listar todas las tiendas, por lo que nuestra clase queda:
```
package dao;

import entity.CgStore;
import java.util.ArrayList;
import org.hibernate.Session;
import org.hibernate.SessionFactory;
import utils.HibernateUtil;

public class CgStoreDAO {
	private static final SessionFactory sf = HibernateUtil.getSessionFactory();
	public static ArrayList<CgStore> listarTiendas(){
		Session session = sf.openSession();

		ArrayList<CgStore> listaTiendas = new ArrayList<>();
		String hql = "SELECT t FROM CgStore t";

		try {
			listaTiendas = (ArrayList<CgStore>)session.createQuery(hql).list();
			
		} catch (Exception e) {
			e.printStackTrace();
		}

		return listaTiendas;
	}
	
}
```
13. Creamos un cotroller en el paquete `controllers` que se encargará de ser el que coja la información de la base de datos y mandarla a la vista. Ha de ser un Servlet. Ojo con añadirlo a el archivo `web.xml`

```
package controllers;

import dao.CgStoreDAO;
import entity.CgStore;
import java.io.IOException;
import java.util.ArrayList;
import javax.servlet.ServletException;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

/**
 *
 * @author Rumil
 */
public class ListarTiendasController extends HttpServlet {

    /**
     * Processes requests for both HTTP <code>GET</code> and
     * <code>POST</code> methods.
     *
     * @param request servlet request
     * @param response servlet response
     * @throws ServletException if a servlet-specific error occurs
     * @throws IOException if an I/O error occurs
     */
    protected void processRequest(HttpServletRequest request, HttpServletResponse response)
        throws ServletException, IOException {
        response.setContentType("text/html;charset=UTF-8");

        ArrayList<CgStore> listaTiendas = CgStoreDAO.listarTiendas();

        request.setAttribute("listaTiendas", listaTiendas);
        request.getRequestDispatcher("/listadoTiendas.jsp").forward(request, response);
    
        }

    //...

}
```


14. creamos la vista (jsp) a donde redirigimos la salida del controlador anterior
15. Programamos una tabla para que imprima todos los datos.

## Despliegue Aplicaciones Web
### Ficheros relacionados con el mundo de las redes en LINUX
* `/etc/hosts`
    - Registros de direcciones IP
* `/etc/ethers`
    - MAC y nombre de la tarjeta de internet
    - No es un fichero que esté comúnmente por defecto en el SO
* `/etc/services`
    - Estructura:
        - Nombre servicio   puerto/protocolo    alias   Comentarios
    - Listado de todos los servicios
*  `/etc/protocolos`
    - Estructura
        - Nombre servicio   Numero Protocolo(no es número de puerto)
* `/etc/hosts.equiv`
    - Listado de máquinas confiables.
* `/etc/inted.conf`
    - No está en Mac
    - Es el archivo de configuración del gestor de todos los servicios en red
    - Servicio  Tipo de Socket(Puede ser stream(TCP) y dgram(UDP))  Tipo de protocolo(TCP/UDP/RPC)    Concurrencia  Usuario propietario del servicio
    - Explicación en [este post](http://ibiblio.org/pub/Linux/docs/LuCaS/Manuales-LuCAS/doc-unixsec/unixsec-html/node196.html)


#Tue Feb 16 10:00:31 CET 2016
##EOI
* sue -> demandar == filled a lawsuit.
* trailed behind-> sigue
* everything is a click away -> todo está a un click de distancia.
* adverts == advertisements == commercials
### Verbs:
* Sound /id/:
    - verbs ending in d or t: end > ended; start > started

#Wed Feb 17 17:07:28 CET 2016
##EIE
* Ventanilla Única Empresarial(VUE)
    - Facilita la creación de una empresa
        - Empresario Individual
        - 
* Punto de Atención al Emprendedor (PAE)
    - La VUE se a integrado aquí.
    - Absorbe a la PAIT
    - Incluye la información y formularios necesarios.
    - Prenstar documentación
    - Estado solicitud

* Punto de Asesoramiento e Inicio de Tramitación (PAIT)
    - Constituida en 2006
    - En 2013 pasa a llamarse PAE
    
* Centro de Información y Red de Creación de Empresas(CIRCE)
    - Sistema informático para realizar los trámites para la creación de  un empresa de forma telemática

* Documento Único Electrónico
    - Es el documento que se utiliza en el sistema electrónico CIRCE

## Despliegue aplicaciones Web
### NETSTAT
* Scaneador de puertos en el ordenador que lo ejecuta
    - Scaneo: `> netstat -r`
* Está a nivel de socket
### NMAP
* Scaneador de puertos en el ordenador que lo ejecuta, ordenadores de la red local e incluso de un dns externo a la red local.

#Thu Feb 18 09:39:39 CET 2016
## EOI
* whimsical -> caprichoso

### Conditional
#### Zero Conditional
 If you heat(S.Pres) water to 100ºC, it boils(S.pres)
#### First Conditional
If the weather is(S.Pres) good, we'll go(Fut) for a walk
#### Second Conditional
If I knew(S. Past) the answer, I woutld tell (should, could...) you
* Variation-> If i **were to** offer you the job, would you accept it?
                    =offered

#### Third Conditional
If I had studied(Past Pf) more, I would have passed (would+have+Past Participle) the exam.

If I **had seen** her, I would have told her.


# Mon Feb 22 17:17:12 CET 2016
## Despliegue aplicaciones
### nmap
6. `nmap 192.168.4.40 -p20-30`
7. `nmap -sV insecure.org`
8. `nmpa -sv localhost` y miramos el puerto 80
9. `nmap -O www.elpais.es`


#Wed Feb 24 19:09:36 CET 2016
##Despliegue aplicaciones
###Archivos de Apache

* ServerRoot
* pidfile

* /etc/init.d es el daemon supervisor del sistema operativo
* Apache gasta 80 y 483, el 443 es el puerto para información 

* Todos los hosts virtuales van por el 80 también.
    - En tu site puedes tener varios dns


# Mon Mar 28 13:53:50 CEST 2016
## R statics

### Create an empty data.frame
```
nodata <- data.frame(x= numeric(0), y= integer(0), z = character(0))
str(nodata)

## 'data.frame':    0 obs. of  3 variables:
##  $ x: num 
##  $ y: int 
##  $ z: Factor w/ 0 levels: 
```

### List of files in current wd
```
list.files()
```

### Add rows to a data.frame
Create a new data frame and use rbind

## Node
* [upgrade node](http://theholmesoffice.com/node-js-fundamentals-how-to-upgrade-the-node-js-version/)


# Thu Apr 14 23:14:42 CEST 2016

## JS
* `domElement.getBoundaryClientRect()` this method asures you the real css properties of the dom element
* `document.querySelector('cssSelector')` Way of selecting dom elements natively. No jQuery needed


# Sun Apr 17 19:07:23 CEST 2016
# SVG
They are a kind of file writen in xml that can be copy-pasted from an editor 
such as inkscape to the html document. This allows to have some shapes that would
be very complicated to achive (or even imposible) with css

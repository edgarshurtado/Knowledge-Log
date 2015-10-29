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

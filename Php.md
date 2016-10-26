## Range from a to zz

A normal for-loop incrementing in one the letter wouldn't work when you hit the
2 letters (works fine from 'a' to 'z' but has a weird behaviour if you hit 'zz')

```php
$letters = array();
$letter = "A";
while($letter !== "AAA") {
    $letters[] = $letter++;
}
```

[source](http://stackoverflow.com/a/14278795)

## Get Multiple Values from a select

If a select is allowed to have multiple values and we want to get all of them
in php, we just have to change the `name` attribute to have `[]` at the end.
This way php will consider the element as an array and we'll be able to get
all the values

```html
<form action="">
    <select name="myMultipleSelec[]">
        <option value="1">Value 1</option>
        <option value="2">Value 2</option>
        <option value="3">Value 3</option>
    </select>
    <input type="submit" value="send">
</form>
```

> If we don't do this, php will have available just the las selected value because
it considers the whole form as an array of information. That for, when a select
has multiple selected values, the keynames collide and the info is overwritten

## Scape single and double quotes

These functions are usefull overall when recieving a string from the user that
you want to persist on the DB.

```php
$stringWithQuotes = "This ' is a single quote";
$stringWithScapedQuotes = addslashes($stringWithQuotes);
    // "This \' is a single quote"
```

This string is now ready to be inserted in the DB. For doing the reverse
operation:

```php
$stringWithScapedQuotes =  "This \' is a single quote";
$stringWithNoSlashes = stripslashes($stringWithScapedQuotes);

    //  "This ' is a single quote"
```

## Writting UTF-8 in a CSV compatible with excel
Funny enough, if you write utf-8 chars in a csv, even though the codification is
right, if the csv is opened with Excel, all the special chars will be broken.

To prevent this we have just to do a UTF-8 BOM before sending the file

```php
header('Content-Encoding: UTF-8');
header('Content-type: text/csv; charset=UTF-8');
header('Content-Disposition: attachment; filename=Customers_Export.csv');
echo "\xEF\xBB\xBF"; // UTF-8 BOM
```

[credits](http://stackoverflow.com/a/4440143)
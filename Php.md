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


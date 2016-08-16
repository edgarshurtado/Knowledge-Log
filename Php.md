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

[source](http://stackoverflow.com/a/14278795);
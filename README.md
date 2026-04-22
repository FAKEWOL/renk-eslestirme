# renk-eslestirme

## Description
The "renk-eslestirme" repository contains PHP scripts for finding common and unique elements in arrays, as well as removing duplicates from an array.

## Features
- Find common elements among multiple arrays.
- Identify unique elements within a single array.
- Remove duplicate elements from an array.

## Installation
To use the scripts, simply download the files `renk`, `renk-fark`, and `renk-tekrar` to your local environment. Ensure that PHP is installed on your server or development machine.

## Usage
### renk
This script finds common elements among three arrays (`$renk1`, `$renk2`, `$renk3`) and displays them.
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <?php
     $renk1=array("Kırmızı","Mavi","Sarı","Siyah","Beyaz","Gri");
     $renk2=array("Yeşil","Mav","kırmızı","siyah","Beyaz","gri");
     $renk3=array("yeşil","Mavi","Sarı","siyah","Beyaz","Gri");
     $son_renk=array_intersect($renk1,$renk2,$renk3);
     echo"<pre>";
     print_r($son_renk);
    ?>
</body>
</html>
```

### renk-fark
This script identifies unique elements within the first array (`$renk1`) and removes them if they exist in the other arrays (`$renk2` and `$renk3`).
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <?php
     $renk1=array("Kırmızı","Mavi","Sarı","Siyah","Beyaz","Gri");
     $renk2=array("Yeşil","Mav","kırmızı","siyah","Beyaz","gri");
     $renk3=array("yeşil","Mavi","Sarı","siyah","Beyaz","Gri");
     $son_renk=array_diff($renk1,$renk2,$renk3);
     echo"<pre>";
     print_r($son_renk)
    ?>
</body>
</html>
```

## Tech Stack
- PHP

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
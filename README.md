# php

#### Generate a random number between 1 and 100

**Method 1:**
```php
<?php
    $num2 = rand(1, 100);
    echo "Random number in range (1, 100): ", $num2;
?>
```

**Method 2: Using `random_int()` function**
```php
<?php
    $num1 = random_int(1, 100);
    echo "Random number in range (1, 100): " . $num;
?>
```

#### Modify above program to accept range of the random number from HTML interface

```php
<?php
$num1 = $_POST['num1'];
$num2 = $_POST['num2'];
?>

<html>
    <form action="" method="POST">
        Enter Min number: <input type="text" name="num1">
        Enter Max number: <input type="text" name="num2">
        Click the submit button below:
        <input type="submit" value="submit">
    </form
</html>

<?php
$random = rand($num1, $num2);
echo "The random number is: $random";
```

#### Programs involving various control structures (Example program)

```php
<?php
$number = 10;
if ($number > 0) {
    echo "The number is positive.";
} elseif ($number < 0) {
    echo "The number is negative.";
} else {
    echo "The number is zero.";
}
?>
```

#### Demonstrating program using break and continue (Exmple program)

```php
<?php
for ($i = 1; $i <= 10; $i++) {
    if ($i == 5) {
        continue;
    }
    if ($i == 8) {
        break;
    }
    echo $i . " ";
}
?>
```

#### Demonstrating program using looping statements (Example program)

```php
<?php
for ($i = 1; $i <= 5; $i++) {
    echo "Loop iteration: " . $i . "<br>";
}
?>
```

#### PHP Array functions - Sorting

```php
<?php
echo "Associative array: Ascending order sort by value <br>";
$array1 = array("Sophia" => "31", "Jacob" => "41", "William" => "39", "Ramesh" => "40");
asort($array1);
foreach ($array1 as $x => $x_value) {
    echo "Age of $x is: $x_value <br>";
}

echo "Associative array: Ascending order sort by key <br>";
$array2 = array("Sophia" => "31", "Jacob" => "41", "William" => "39", "Ramesh" => "40");
ksort($array2);
foreach ($array2 as $x => $x_value) {
    echo "Age of $x is: $x_value <br>";
}

echo "Associative array: Descending order sort by value <br>";
$array3 = array("Sophia" => "31", "Jacob" => "41", "William" => "39", "Ramesh" => "40");
arsort($array3);
foreach ($array3 as $x => $x_value) {
    echo "Age of $x is: $x_value <br>";
}

echo "Associative array: Descending order sort by key <br>";
$array4 = array("Sophia" => "31", "Jacob" => "41", "William" => "39", "Ramesh" => "40");
krsort($array4);
foreach ($array4 as $x => $x_value) {
    echo "Age of $x is: $x_value <br>";
}
?>
```

#### PHP Array functions - Reverse sorting, array to string conversion

**Reverse Sorting:**
```php
<?php
$a = array("a" => "array", "b" => "reverse", "c" => "sorting");
print_r(array_reverse($a));
?>
```

**Array to string conversion:**
```php
<?php
$a = array("This", "Array", "Will", "Be", "Converted", "To", "A", "String");
print_r($a);
echo "<br>Converted array:<br>";
echo implode(" ", $a);
?>
```

#### PHP Array functions - Implode() and Explode()

**Implode():**
```php
<?php
$arr = array('Hello', 'World!', 'Beautiful', 'Day!');
echo implode(" ", $arr);
?>
```

**Explode():**
```php
<?php
$str = "Hello world. It's a beautiful day.";
print_r(explode(" ", $str));
?>
```

#### Remove duplicate values

```php
<?php
$a = array("a" => "red", "b" => "green", "c" => "red");
print_r(array_unique($a));
?>
```

#### PHP Array functions - Array Search, Array Replace

**Array Search:**
```php
<?php
$a = array("a" => "red", "b" => "green", "c" => "blue");
echo array_search("red", $a);
?>
```

**Array Replace:**
```php
<?php
$a1 = array("red", "green");
$a2 = array("blue", "yellow");
print_r(array_replace($a1, $a2));
?>
```

#### Extract the file name from the string

```php
<?php
$path = 'www.example.com/public/index.php';
$file_name = substr(strrchr($path, "/"), 1);
echo $file_name;
?>
```

#### Find whether the given number is a prime or not (Example Program)

```php
<?php
function is_primt($number) {
    if ($number <= 1) return false;
    for ($i = 2; $i <= sqrt($number); $i++) {
        if ($number % $i == 0) return false;
    }
    return true;
}

$number = 29;
if (is_primt($number)) {
    echo $number . " is a prime number.";
} else {
    echo $number . " is not a prime number.";
}
?>
```

#### Display the Fibonacci sequence with HTML page (Example Program)

```php
<?php
function fibonacci($n) {
    $fib = array(0, 1);
    while (count($fib) < $n) {
        $fib[] = $fib[count($fib) - 1] + $fib[count($fib) - 2];
    }
    return $fib;
}

$sequence = fibonacci(10);

foreach ($sequence as $num) {
    echo $num . " ";
}
?>
```

#### Create a chess board

```php
<html>
  <body>
    <h3>Chess Board using Nested for loop</h3>
    <table width="270px" cellspacing="0px" cellpadding="0px" border="1px">
      <?php
      for ($row = 1; $row <= 8; $row++) {
        echo "<tr>";
        for ($col = 1; $col <= 8; $col++) {
          $total = $row + $col;
          if ($total % 2 == 0) {
            echo "<td height=30px width=30px bgcolor=#ffffff></td>";
          } else {
            echo "<td height=30px width=30px bgcolor=#000000></td>";
          }
        }
        echo "</tr>";
      }
      ?>
    </table>
  </body>
</html>
```

#### Using built-in string functions

**strstr():**
```php
<?php
echo strstr("Hello world!", "world");
?>
```

**strpos():**
```php
<?php
echo strpos("I love php, I love php too!", "php");
?>
```

**substr_count():**
```php
<?php
echo substr_count("Hello world. The world is nice", "world");
?>
```

#### Transform a string to uppercase, lowercase letters, and make the first character uppercase

```php
<?php
print(stringtoupper("hello world.") . "<br>")
print(strtolower("HELLO WORLD.") . "<br>")
print(ucfirst("hello world.") . "<br>")
?>
```

#### Check whether all array values are strings

```php
<?php
function check_strings_in_array($arr) {
    return array_sum(array_map('is_string', $arr)) == count($arr);
}
$arr1 = array('PHP', 'JS', 'Python');
$arr2 = array('SQL', 200, 'MySQL');
var_dump(check_strings_in_array($arr1));
var_dump(check_strings_in_array($arr2));
?>
```

#### Count number of elements in an array

```php
<?php
$ele = array("count", "number", "elements", "array");
$no_of_ele = count($ele);
echo "Number of elements present in the array: " . $no_of_ele;
?>
```

#### Create a new image

```php
<?php
$image = imagecreatetruecolor(200, 100);
$background_color = imagecolorallocate($image, 255, 255, 255);
imagefill($image, 0, 0, $background_color);
header("Content-type: image/png"); 
imagepng($image); 
?>
```

#### Draw a polygon

```php
<?php
$image = imagecreatetruecolor(200, 200);
$background_color = imagecolorallocate($image, 255, 255, 255);
$polygon_color = imagecolorallocate($image, 0, 0, 255);
imagefill($image, 0, 0, $background_color);
$points = [50, 150, 150, 100, 50];
imagepolygon($image, $points, 3, $polygon_color);
header("Content-type: image/png"); 
imagepng($image); 
?>
```

#### Draw an ellipse

```php
<?php
$image = imagecreatetruecolor(200, 200);
$background_color = imagecolorallocate($image, 255, 255, 255);
$ellipse_color = imagecolorallocate($image, 0, 0, 255);
imagefill($image, 0, 0, $background_color);
imageellipse($image, 100, 100, 150, 100, $ellipse_color);
header("Content-type: image/png"); 
imagepng($image); 
?>
```

#### Perform file read

```php
<?php
$fileName = "C:/xampp/htdocs/s3.txt";
$fileResource = fopen($fileName, 'r');
print $fileResource . "<br>";
$fileSize = filesize($fileName);
print $fileSize . "<br>";
print fread($fileResource, $fileSize);
fclose($fileResource);
?>
```

#### Perform file write

```php
<?php
$fileName = "C:/xampp/htdocs/s3.txt";
$fileResource = fopen($fileName, 'w');
print $fileResource . "<br>";
fwrite($fileResource, "This is my first text to be written to the file.");
$fileSize = filesize($fileName);
print $fileSize . "<br>";
fclose($fileResource);
?>
```

#### Perform file append

```php
<?php
$fileName = "C:/xampp/htdocs/s3.txt";
$fileResource = fopen($fileName, 'a');
print $fileResource . "<br>";
fwrite($fileResource, "This is my second text to be written to the file.");
$fileSize = filesize($fileName);
print $fileSize . "<br>";
fclose($fileResource);
?>
```

#### Perform form validaion

```php
<html>
    <body>
        <?php
        $name = $email = $gender = $comment = $website = "";
        if ($_SERVER["REQUEST_METHOD"] == "POST") {
            $name = test_input($_POST["name"]);
            $email = test_input($_POST["email"]);
            $website = test_input($_POST["website"]);
            $comment = test_input($_POST["comment"]);
            $gender = test_input($_POST["gender"]);
        }
        function test_input($data) {
            $data = trim($data);
            $data = stripslashes($data);
            $data = htmlspecialchars($data);
            return $data;
        }
        ?>
        <h2>PHP Form Validation Example</h2>
        <form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
            Name: <input type="text" name="name">
            <br><br>
            E-mail: <input type="text" name="email">
            <br><br>
            Website: <input type="text" name="website">
            <br><br>
            Comment: <textarea name="comment" rows="5" cols="40"></textarea>
            <br><br>
            Gender:
            <input type="radio" name="gender" value="female">Female
            <input type="radio" name="gender" value="male">Male
            <input type="radio" name="gender" value="other">Other
            <br><br>
            <input type="submit" name="submit" value="Submit">
        </form>
        <?php
        echo "<h2>Your Output:</h2>";
        echo $name;
        echo "<br>";
        echo $email;
        echo "<br>";
        echo $website;
        echo "<br>";
        echo $comment;
        echo "<br>";
        echo $gender;
        ?>
    </body>
</html>
```

#### Connecting to MySQL database

```php
<html>
    <body>
        <?php 
        $host_name = "localhost";
        $user_name = "admin";
        $password = "";
        $db = "test";
        
        $conn = mysqli_connect($host_name, $user_name, $password, $db);
        if (!$conn) {
            echo "Connection Failed";
        } else {
            $sql = "CREATE TABLE Stud(sl_no INT, name VARCHAR(30), dept VARCHAR(30))";
            if ($conn->query($sql) === TRUE) {
                echo "Table Stud created successfully <br>";
            } else {
                echo "Error creating table: <br>";
            }
            $sql = "INSERT INTO Stud VALUES (1, 'Flicson', 'CS'), (2, 'Vishnu', 'CS'), (3, 'Nihal', 'Stat')"
            if ($conn->query($sql) === TRUE) {
                echo "New records created successfully<br>";
            } else {
                echo "Error Inserting Values <br>";
            }
            $sql = "SELECT sl_no, name, dept FROM Stud";
            $result = $conn->query($sql);
            if ($result->num_rows > 0) {
                while ($row = $result->fetch_assoc()) {
                    echo "<b>sl_no:</b> $row['sl_no'] - <b>Name:</b> $row['name'] - <b>Dept:</b> $row['dept'] <br>";
                }
            } else {
                echo "0 results<br>";
            }
            $conn->close();
        }
        ?>
    </body>
</html>
```


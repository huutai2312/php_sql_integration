## php sql integration
##### Preview:
```php
<?php
$servername = "localhost";
$username = "root";
$password = "";

// create connection
$conn = new mysqli($servername, $username, $password);
// check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

// create database
$sql = "USE <tablename>;"; // replace tablename with your table's name

if (!$conn->query($sql) === TRUE) {
    echo "Error using database: " . $conn->error;
}

// save your variable
// example
$example = $_POST["example"];

// define your query
$query = "";
$result = $conn->query($query);

// check if there are rows to display
if ($result->num_rows > 0) {
    // output data of each row
    while($row = $result->fetch_assoc()) {
        echo $row["example"];
    }
} else {
    echo "0 results";
}

$conn->close();
?>
```
| Associated Context                         |                                          |
| ------------------------------------------ | ---------------------------------------- |
| Type | Code Snippet  ( ***.php***  )  |
| Associated Tags | `Database management` `Console output` `Fetching rows` `SQL query` `PHP` `Data retrieval` `Connection creation` `Error handling` `MySQL database` |
| 💡 Smart Description | This PHP code creates a MySQL connection, then checks if there are rows to display. It also prints out data of each row.<br> |
| 🔎 Suggested Searches  | How to create a connection using mysqli ?<br>How to handle error handling?<br>What is the syntax for creating a database with MySQL ?<br>How to use PDO  to query and display data in PHP? |
| Related Links | [https://www.w3schools.com/php/php_mysql_prepared_statements.asp](https://www.w3schools.com/php/php_mysql_prepared_statements.asp)<br>[https://www.php.net/manual/en/mysqli.quickstart.prepared-statements.php](https://www.php.net/manual/en/mysqli.quickstart.prepared-statements.php)<br>[https://www.w3schools.com/php/php_mysql_select.asp](https://www.w3schools.com/php/php_mysql_select.asp)<br>[https://www.w3schools.com/php/func_mysqli_connect.asp](https://www.w3schools.com/php/func_mysqli_connect.asp)<br>[https://www.tutorialrepublic.com/php-tutorial/php-mysql-prepared-statements.php](https://www.tutorialrepublic.com/php-tutorial/php-mysql-prepared-statements.php)<br>[https://www.tutorialrepublic.com/php-tutorial/php-mysql-select-query.php](https://www.tutorialrepublic.com/php-tutorial/php-mysql-select-query.php) |
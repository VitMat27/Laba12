# Laba12
<p align = "center">МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ<br>
РОССИЙСКОЙ ФЕДЕРАЦИИ<br>
ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ<br>
ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ<br>
«САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</p>
<br><br><br><br><br><br>
<p align = "center">Институт естественных наук и техносферной безопасности<br>Кафедра информатики<br>Иванюшин Виталий Петрович</p>
<br><br><br>
<p align = "center"><br><strong>Лабораторная работа №12.«PHP»</strong><br>01.03.02 Прикладная математика и информатика</p>
<br><br><br><br><br><br><br><br><br><br><br><br>
<p align = "right">Научный руководитель<br>
Соболев Евгений Игоревич</p>
<br><br><br>
<p align = "center">г. Южно-Сахалинск<br>2024 г.</p>
<br><br><br><br><br><br><br><br><br><br><br><br>

<h1 align = "center">Введение</h1>

<p><b>HTML</b> —  стандартизированный язык гипертекстовой разметки документов для просмотра веб-страниц в браузере. Веб-браузеры получают HTML документ от сервера по протоколам HTTP/HTTPS или открывают с локального диска, далее интерпретируют код в интерфейс, который будет отображаться на экране монитора.</p>
<p><b>CSS</b> — формальный язык описания внешнего вида документа, написанного с использованием языка разметки. Также может применяться к любым XML-документам, например, к SVG или XUL.</p>


<h1 style="text-align: center">Задачи php</h1>
<ol> Выполнить задания по PHP </ol>  


<h1 style="text-align: center">Решения PHP</h1>

<h2 style="text-align: center">Файл 1.php</h2>

```php
<?php

// 1. Создаем массив, заполненный числами от 1 до 100 и находим сумму элементов
$numbers = range(1, 100);
$sum = array_sum($numbers);
echo "Сумма элементов массива: $sum\n";

// 2. Преобразуем массив 'a', 'b', 'c', 'd', 'e' в массив 'A', 'B', 'C', 'D', 'E'
$letters = ['a', 'b', 'c', 'd', 'e'];
$capitalLetters = array_map('strtoupper', $letters);
print_r($capitalLetters);

// 3. Подсчитываем количество элементов массива
$arr = [1, 2, 3, 4, 5];
$count = count($arr);
echo "Количество элементов массива: $count\n";

// 4. Выводим последний элемент массива
$lastElement = end($arr);
echo "Последний элемент массива: $lastElement\n";

// 5. Проверяем наличие элемента со значением 3 в массиве
$numbersArray = [1, 2, 3, 4, 5];
if (in_array(3, $numbersArray)) {
    echo "Элемент со значением 3 найден в массиве\n";
} else {
    echo "Элемент со значением 3 не найден в массиве\n";
}

// 6. Находим сумму элементов массива [1, 2, 3, 4, 5]
$numbers = [1, 2, 3, 4, 5];
$sum = array_sum($numbers);
echo "Сумма элементов массива: $sum\n";

// 7. Находим произведение элементов массива [1, 2, 3, 4, 5]
$product = array_product($numbers);
echo "Произведение элементов массива: $product\n";

// 8. Находим среднее арифметическое элементов массива $arr
$average = array_sum($arr) / count($arr);
echo "Среднее арифметическое элементов массива: $average\n";

// 9. Создаем массив, заполненный числами от 1 до 100
$numbers = range(1, 100);
print_r($numbers);

// 10. Создаем массив, заполненный буквами от 'a' до 'z'
$letters = range('a', 'z');
print_r($letters);

//11
$str = implode('-', range(1, 9));
echo $str; // Вывод: 1-2-3-4-5-6-7-8-9

//12
$sum = array_sum(range(1, 100));
echo $sum; // Вывод: 5050
//13
$prod = array_product(range(1, 10));
echo $prod; // Вывод: 3628800
//14
$arr1 = [1, 2, 3];
$arr2 = ['a', 'b', 'c'];
$result = array_merge($arr1, $arr2);
print_r($result); // Вывод: Array ( [0] => 1 [1] => 2 [2] => 3 [3] => a [4] => b [5] => c )
//15
$arr = [1, 2, 3, 4, 5];
$result = array_slice($arr, 1, 3);
print_r($result); // Вывод: Array ( [0] => 2 [1] => 3 [2] => 4 )
//16
$arr = [1, 2, 3, 4, 5];
array_splice($arr, 1, 2);
print_r($arr); // Вывод: Array ( [0] => 1 [1] => 4 [2] => 5 )
//17
$arr = [1, 2, 3, 4, 5];
$newArr = array_splice($arr, 1, 3);
print_r($newArr); // Вывод: Array ( [0] => 2 [1] => 3 [2] => 4 )
//18
$arr = [1, 2, 3, 4, 5];
array_splice($arr, 3, 0, ['a', 'b', 'c']);
print_r($arr); // Вывод: Array ( [0] => 1 [1] => 2 [2] => 3 [3] => a [4] => b [5] => c [6] => 4 [7] => 5 )
//19
$arr = [1, 2, 3, 4, 5];
array_splice($arr, 1, 0, ['a', 'b']);
array_splice($arr, 6, 0, ['c']);
array_splice($arr, 8, 0, ['e']);
print_r($arr); // Вывод: Array ( [0] => 1 [1] => a [2] => b [3] => 2 [4] => 3 [5] => 4 [6] => c [7] => 5 [8] => e )
//20
$arr = ['a' => 1, 'b' => 2, 'c' => 3];
$keys = array_keys($arr);
$values = array_values($arr);
print_r($keys); // Вывод: Array ( [0] => a [1] => b [2] => c )
print_r($values); // Вывод: Array ( [0] => 1 [1] => 2 [2] => 3 )

//21
$array1 = ['a', 'b', 'c'];
$array2 = [1, 2, 3];
$result = array_combine($array1, $array2);
print_r($result);
//22
$array = ['a'=>1, 'b'=>2, 'c'=>3];
$result = array_flip($array);
print_r($result);
//23
$array = [1, 2, 3, 4, 5];
$result = array_reverse($array);
print_r($result);
//24
$array = ['a', '-', 'b', '-', 'c', '-', 'd'];
$position = array_search('-', $array);
echo $position;
//25
$array = ['a', '-', 'b', '-', 'c', '-', 'd'];
$position = array_search('-', $array);
if ($position !== false) {
    array_splice($array, $position, 1);
}
print_r($array);
//26
$array = ['a', 'b', 'c', 'd', 'e'];
$array[0] = '!';
$array[3] = '!!';
print_r($array);
//27
$array = ['3'=>'a', '1'=>'c', '2'=>'e', '4'=>'b'];
ksort($array); // Сортировка по ключу
asort($array); // Сортировка по значению
print_r($array);
//28
$array = ['a'=>1, 'b'=>2, 'c'=>3];
$randomKey = array_rand($array);
echo $randomKey;
//29
$array = ['a'=>1, 'b'=>2, 'c'=>3];
$randomValue = array_rand($array, 1);
echo $array[$randomValue];
//30
$array = ['a'=>1, 'b'=>2, 'c'=>3];
$randomValue = array_rand($array, 1);
echo $array[$randomValue];
// 31
$numbers = range(1, 25);
shuffle($numbers);

// 32
$letters = range('a', 'z');
shuffle($letters);
$randomLetters = array_slice($letters, 0, 26);

// 33
$randomString = str_shuffle(substr(str_shuffle('abcdefghijklmnopqrstuvwxyz'), 0, 6));

// 34
$array = ['a', 'b', 'c', 'b', 'a'];
$uniqueArray = array_unique($array);

// 35
$array = [1, 2, 3, 4, 5];
$firstElement = array_shift($array);
$lastElement = array_pop($array);

// 36
$array = [1, 2, 3, 4, 5];
array_unshift($array, 0);
array_push($array, 6);

// 37
$array = [1, 2, 3, 4, 5, 6, 7, 8];
$result = '';
while (!empty($array)) {
    $result .= array_shift($array) . array_pop($array);
}

// 38
$array = ['a', 'b', 'c'];
$extendedArray = array_merge($array, array_fill(0, 3, '-'));

// 39
$lettersArray = array_fill(0, 10, 'x');

// 40
$numbersArray = range(1, 20);
$chunkedArray = array_chunk($numbersArray, 4);

?>

```

<h1 align = "center">Вывод</h1>
<p>В ходе выполнения лабораторной работы по php были рассмотрены различные способы работы с переменными и строками.</p>

# 3df
For 3d-fabrik
# HTML ``` <table> ``` Tag
***
[Таблицы-ссылка на сайт](https://html5book.ru/html-table/)
[test](Test.md)
Таблица создаётся при помощи парного тега `<table></table>`. Данный тег является контейнером для элементов таблицы и все элементы должны находиться внутри него. Например, с помощью данной разметки можно создать таблицу, состоящую из двух столбцов и двух строк:
```
<table>
<tr><th>текст заголовка</th><th>текст заголовка</th></tr> <!--ряд с ячейками заголовков-->
<tr><td>данные</td><td>данные</td></tr> <!--ряд с ячейками тела таблицы-->
</table>
```
По умолчанию таблица и ячейки не имеют видимых границ. Границы задаются с помощью свойства `border`:
```
/* внешние границы таблицы серого цвета толщиной 1px */
table {border: 1px solid grey;} 
/* границы ячеек первого ряда таблицы */
th {border: 1px solid grey;}
/* границы ячеек тела таблицы */
td {border: 1px solid grey;} 
```
## Стили для таблицы
С помощью стандартных способов оформления можно задать стиль для таблицы и всех её строк. Но как быть, если требуется, например, выделить отдельную ячейку? Чтобы не задавать для ячейки class, можно воспользоваться комбинацией селекторов и псевдоклассов.
В данном уроке приведены различные варианты отбора элементов таблицы с помощью структурных псевдоклассов.

**Разметка HTML**
```
<table>
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>
```
 
### Table1:Первая строка таблицы.
```
th {background: #C9E3FE;}
table {border: 1px solid grey;} 
```

<table class="table1">
<tr>
  <th style="background: #C9E3FE;">Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>


### Table2:Последняя строка таблицы.
```
tr:last-child {background: #C9E3FE}
```
<table class="table2">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

### Table3:Третья строка таблицы.
```
tr:nth-child(3){background:#C9E3FE}
```
<table class="table3">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

### Table4:Таблица-зебра. Каждая четная строка.
```
tr:nth-child(even) {background: #C9E3FE}
```
<table class="table4">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

### Table5:Таблица-зебра. Каждая нечетная строка таблицы.
```
tr:nth-child(odd) {background: #C9E3FE}
```
<table class="table5">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

### Table6:Первая ячейка первой строки таблицы.
```
th:first-child {background: #c9e3fe;}
```
<table class="table6">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

### Table7:Последняя ячейка первой строки таблицы. 
```
th:last-child {background: #C9E3FE}
```
<table class="table7">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>


### Table8:Первая ячейка последней строки таблицы. 
```
tr:last-child td:first-child {background: #C9E3FE}
```
<table class="table8">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>


### Table9:Последняя ячейка последней строки таблицы. 
```
tr:last-child td:last-child {background: #C9E3FE}
```
<table class="table9">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>


### Table10:Третья ячейка третьей строки таблицы. 
```
tr:nth-child(3) td:nth-child(3) {background: #C9E3FE}
```
<table class="table10">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>


### Table11:Первый столбец таблицы. 
```
th:first-child, td:first-child {background: #C9E3FE}
```
<table class="table11">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>


### Table12:Третий столбец таблицы. 
```
td:nth-child(3), th:nth-child(3) {background: #C9E3FE}
```
<table class="table12">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>


### Table13:Последний столбец таблицы. 
```
th:last-child, td:last-child {background: #C9E3FE}
```
<table class="table13">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>






<style>
 
 .table1 th {background: #C9E3FE;
      }
 .table1 {border: 1px solid grey;
      } 
 .table1 td {border: 1px solid grey;
      } 
 .table2 tr:last-child {background: #C9E3FE;
      }
 .table3 tr:nth-child(3){background:#C9E3FE;
      }
 .table4 tr:nth-child(even) {background: #C9E3FE;
      }
 .table5 tr:nth-child(odd) {background: #C9E3FE;
      }
 .table6 th:first-child {background: #c9e3fe;
      }
 .table7 th:last-child {background: #C9E3FE;
      }
 .table8 tr:last-child td:first-child {background: #C9E3FE;
      }
 .table9 tr:last-child td:last-child {background: #C9E3FE;
      }
 .table10 tr:nth-child(3) td:nth-child(3) {background: #C9E3FE;
      }
 .table11 th:first-child, .table11 td:first-child {background: #C9E3FE;
      }
 .table12 td:nth-child(3), .table12 th:nth-child(3) {background: #C9E3FE;
      }
 .table13 th:last-child, .table13 td:last-child {background: #C9E3FE;
      }
</style>

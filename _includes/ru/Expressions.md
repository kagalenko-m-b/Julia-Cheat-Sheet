Julia является гомоиконическим языком программирования: программы имеют ту же структуру, что и данные самого языка. Фактически, всё является выражением `Expr`.


Символы являются <a class="tooltip" href="#">внутренними строками<span>Хранится только одна копия каждого отдельного (неизменяемого) значения строки. </span></a> после двоеточия. Символы более эффективны и обычно используются в качестве идентификаторов,
ключей (в словарях) или столбцов в фреймах данных. Символы не могут быть объединены.

Цитирование `:( ... )` или `quote ... end` создаёт выражение, в точности как <a class="tooltip" href="#">`Meta.parse(str)` <span> Эта форма, вероятно, наиболее понятна
тем, кто знаком с динамическим SQL. Фунция `Meta.parse` аналогична оператору
`EXECUTE IMMEDIATE` в Oracle и PostgreSQL, а также процедуре `sp_executesql()` в SQL Server.</span></a> , и `Expr(:call, ...)`.

```
x = 1
line = "1 + $x"         # какие-либо операторы
expr = Meta.parse(line) # создать объект Expr
typeof(expr) == Expr    # true
dump(expr)              # генерировать абстрактное синтаксическое дерево
eval(expr) == 2         # интерпретировать объект Expr: true
```
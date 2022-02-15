Об инструментах, подобных `dplyr`, см.
[DataFramesMeta.jl.](https://github.com/JuliaStats/DataFramesMeta.jl)

|                                  |                                           |
| -------------------------------- | ----------------------------------------- |
| Читать Stata, SPSS, etc.         | Пакет `StatFiles`                       |
| <a class="tooltip" href="#">Описать<span>Похоже на `summary(df)` в R.</span></a> фрейм данных | `describe(df)` |
| Преобразовать `col` в вектор     | `v = df[:col]`                            |
| Отсортировать по  `col`          | `sort!(df, [:col])`                       |
| <a class="tooltip" href="#">Categorical<span>Похоже на `df$col = as.factor(df$col)` в R.</span> `col` | `categorical!(df, [:col])` |
| Перечислить уровни `col`         | `levels(df[:col])`                        |
| Все наблюдения с `col==val`      | `df[df[:col] .== val, :]`                 |
| Переформатировать с широкого на длинный | `stack(df, [1:n; ])`<br>`stack(df, [:col1, :col2, ...])`<br>`melt(df, [:col1, :col2])` |
| Переформатировать с длинного на широкий | `unstack(df, :id, :val)`                  |
| Создать `Nullable`                  | `allowmissing!(df)` or `allowmissing!(df, :col)` |
| Цикл по строкам                  | `for r in eachrow(df)`<br>`    # выполнить действия.`<br>`    # r является Struct с полями имён col.`<br>`end` |
| Цикл по столбцам                 | `for c in eachcol(df)`<br>`    # выполнить действия.`<br>`    # c - кортеж с именем и вектором `<br>`end` |
| Применить func к группам         | `by(df, :group_col, func)`                |
| Запрос                           | `using Query`<br>`query = @from r in df begin`<br>`    @where r.col1 > 40`<br>`    @select {new_name=r.col1, r.col2}`<br>`    @collect DataFrame # Default: iterator`<br>`end` |

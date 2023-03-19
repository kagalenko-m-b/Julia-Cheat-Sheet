
|                                |                                                                  |
| ------------------------------ | ---------------------------------------------------------------- |
| Словарь    | `d = Dict(key1 => val1, key2 => val2, ...)`<br>`d = Dict(:key1 => val1, :key2 => val2, ...)` |
| Все ключи (итератор)           | `keys(d)`                                                        |
| Все значения (итератор)        | `values(d)`                                                      |
| Цикл по парам ключ-значение    | `for (k,v) in d`<br>`    println("key: $k, value: $v")`<br>`end` |
| Проверить наличие ключа `:k`   | `haskey(d, :k)`                                                  |
| Коспировать ключи (или значения) в массив | `arr = collect(keys(d))`<br>`arr = [k for (k,v) in d]`           |

Словари являются изменяемыми; когда в качестве ключей используются символы, ключи являются неизменяемыми.
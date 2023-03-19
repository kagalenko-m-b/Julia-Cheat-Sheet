Многие функции  случайных чисел требуют `using Random`.

|                                  |                                                               |
| -------------------------------- | ------------------------------------------------------------- |
| Установить состояние генератора  | `seed!(seed)`                                                 |
| Случайные числа                  | `rand()   # равномерно на [0,1)`<br>`randn()  # нормально распределённые на (-Inf, Inf)` |
| Случайные числа из других распределений | `using Distributions`<br>`my_dist = Bernoulli(0.2) # Например`<br>`rand(my_dist)` |
| Случайная выборка элементов из A с вероятностью p | `randsubseq(A, p)`               |
| Случайная перестановка элементов A | `shuffle(A)`                                                  |
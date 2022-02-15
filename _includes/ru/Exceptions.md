|                           |                                                 |
| ------------------------- | ----------------------------------------------- |
| Вызвать SomeExcep         | `throw(SomeExcep())`                            |
| Повторно вызвать текущее исключение | `rethrow()`                                     |
| Определить NewExcep       | `struct NewExcep <: Exception`<br>`    v::String`<br>`end`<br><br>`Base.showerror(io::IO, e::NewExcep) = print(io, "Проблема с $(e.v)!")`<br><br>`throw(NewExcep("x"))` |
| Вызвать ошибку с текстом msg | `error(msg)`                                    |
| Обработчик                | `try`<br>`    # проделать небезопасную операцию`<br>`catch ex`<br>`    if isa(ex, SomeExcep)`<br>`        # handle SomeExcep`<br>`    elseif isa(ex, AnotherExcep)`<br>`        # обработать AnotherExcep`<br>`    else`<br>`        # обработать остальные`<br>`    end`<br>`finally`<br>`    # выполнить во всех случаях`<br>`end` |

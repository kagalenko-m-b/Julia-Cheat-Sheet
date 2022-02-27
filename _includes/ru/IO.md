|                   |                                                                                 |
| ----------------- | ------------------------------------------------------------------------------- |
| Читать поток данных | `stream = stdin`<br>`for line in eachline(stream)`<br>`    # do stuff`<br>`end` |
| Читать файл       | `open(filename) do file`<br>`    for line in eachline(file)`<br>`        # do stuff`<br>`    end`<br>`end` |
| Читать файл CSV   | `using CSV`<br>`data = CSV.read(filename)`                                      |
| Записать в файл CSV | `using CSV`<br>`CSV.write(filename, data)`                                      |
| Сохранить объект Julia | `using JLD`<br>`save(filename, "object_key", object, ...)`                      |
| Загрузить объект Julia | `using JLD`<br>`d = load(filename) # Returns a dict of objects`                 |
| Сохранить HDF5    | `using HDF5`<br>`h5write(filename, "key", object)`                              |
| Загрузить HDF5    | `using HDF5`<br>`h5read(filename, "key")`                                       |

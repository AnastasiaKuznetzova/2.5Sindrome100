**Счетчики покрытия кода JACOCO**

**INSTRUCTION**

**INSTRUCTION** — это счетчик, который считает байт-код Java; наименьшая единица, которую обрабатывет JaCoCo. Охват инструкций предоставляет информацию о количестве кода, который был выполнен или пропущен. Этот показатель полностью независим от исходного форматирования и всегда доступен даже при отсутствии отладочной информации в файлах классов.

**LINE**

Для всех файлов классов, которые были скомпилированы с отладочной информацией, можно рассчитать информацию покрытия для отдельных строк. Строка источника считается выполненной, когда выполнена хотя бы одна инструкция, назначенная этой строке. В связи с тем, что одна строка обычно компилируется в байт-код, выделение исходного кода показывает три разных состояния для каждой строки, содержащей исходный код:

* Нет покрытия: не было выполнено ни одной инструкции в строке (красный фон);
* Частичное покрытие: только часть инструкции в строке была выполнена (желтый фон);
* Полное покрытие: все инструкции в строке выполнены (зеленый фон).

**BRANCH**

JaCoCo также рассчитывает покрытие ветвей для всех операторов if и switch. Эта метрика подсчитывает общее количество таких ветвей в методе и определяет количество выполненных или пропущенных ветвей. Покрытие ветвей всегда доступно, даже в отсутствие отладочной информации в файлах классов. Обратите внимание, что обработка исключений не рассматривается как ветви в контексте этого определения счетчика. Если файлы классов были скомпилированы с отладочной информацией, точки принятия решения могут быть сопоставлены с исходными строками и выделены соответствующим образом:

* Нет покрытия: не было выполнено ни одной ветви в строке (красный ромб);
* Частичное покрытие: была выполнена только часть ветвей в линии (желтый ромб);
* Полное покрытие: все ветви в линии были выполнены (зеленый бриллиант).

**COMPLEXITY**

JaCoCo также вычисляет цикломатическую сложность для каждого неабстрактного метода и суммирует сложность для классов, пакетов и групп. Согласно определению McCabe1996 цикломатическая сложность - это минимальное количество путей, которые в (линейной) комбинации могут генерировать все возможные пути через метод. Таким образом, значение сложности может служить индикатором для количества случаев модульного тестирования, чтобы полностью охватить определенную часть программного обеспечения. Показатели сложности всегда можно рассчитать даже при отсутствии отладочной информации в файлах классов
README для проекта SAUSE DEMO
______________________________
Данный проект создан для тестирования с помощью Selenium

Selenium - это набор инструментов для end-to-end (или e2e) тестирования.
Он используется для того, чтобы "притворяться" пользователем в каком-то определенном браузере,
позволяет записать действия "пользователя" и воспроизводить их неограниченное количество раз по требованию,
то есть автоматизирует процесс проверки работоспособности сайта в разных браузерах при помощи инструмента иструмент Selenium Webdriver.
Selenium Webdriver - это специальная программа, которая эмулирует конкретный браузер, и набор библиотек для разных языков программирования
(сам Selenium написан на Java, но писать тесты можно не только на Java, но и на JS, Ruby, Python, ...), которые позволяют писать тесты в виде кода.
Когда файл с такими тестами запускается, он обращается к Selenium, чтобы открыть окно браузера, изменить его размеры,
загрузить нужную страницу, найти на ней элементы и т.д. Чтобы запустить такие тесты, нужно установить драйвер для соответствующего браузера
(например, для Chrome или EDGE, OPERA и т.д...) - важно понимать, что вся логика реализована в этом драйвере.

ПРОЕКТ
______________________________

Процесс тестирования просходит на сайте https://www.saucedemo.com.
В проекте реализовано 15 тестов, которые в свою очередь, находятся в соответствующих java-классах и расположены по следующему пути:
SauseDemo/scr/test/java/tests

- CartPageTest
- ContextMenuTest
- DynamicControlTest
- FileUploaderTest
- FramesTest
- ProduttCriticalPathTest
______________________________

POM.xml

В проекте содержится POM.xml файл.
POM (Project Object Model) является базовым модулем Maven. Это специальный XML-файл, который всегда хранится в базовой директории проекта.
Файл POM содержит информацию о проекте и различных деталях конфигурации, включающих в себя различные библиотеки отвечающие за реализацию тестов,
которые используются Maven для создания проекта.
POM.xml файл расположен по следующему пути:
SauseDemo/POM.xml

Существует несколько вариантов обновления библиотек:

* В зависимых проектах pom.xml выполните команду: mvn versions:use-latest-releases для автоматического обновления версий зависимостей.

* Если все проекты наследуются от одного и того же родителя (и настройка зависимостей выполняется с помощью управления зависимостями),
вы можете использовать: mvn versions:set -DnewVersion=xx в агрегаторе pom.xml для обновления версий.

* Если управление версиями будет происходить довольно часто, можно использовать версии моментальных снимков.

Запуск тестирования ресурса осуществляется из консоли следующей командой:

mvn test -DsuiteXmlFile='src/test/resources/regression.xml'

Пример результата тестирования:

[INFO] Tests run: 15, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 79.842 s - in TestSuite
[INFO]
[INFO] Results:
[INFO]
[INFO] Tests run: 15, Fail[INFO] Tests run: 15, Failures: 0, Errors: 0, Skipped: 0
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  01:31 min
[INFO] Finished at: 2021-12-24T12:49:07+03:00

В ходе тестирования запущено 15 тестов, неудачных попыток 0, ошибок 0, пропущено 0, Время обработки 79.842 сек.
______________________________

Regression.xml

В проекте содержится regression.xml файл.
Regression.xml файл служит для конфигурирования процесса тестирования настоящего проекта и содержит в себе параметры проведения тестирования такие как:

- версию файла;
- стандарт кодирования символов;
- количество, наименование и способ потоков тестирования
- имя теста (при необходимости номер)
- параметр указывающий используемый браузер
- классы содержащие тесты

   при необходимости проведения тестирования с использованием нескольких браузеров, параметры -

- имя теста (при необходимости номер)
- параметр указывающий используемый браузер
- классы содержащие тесты
  указываются необходимое количество раз.
  Regression.xml файл расположен по следующему пути:
  SauseDemo/scr/test/regression.xml
______________________________


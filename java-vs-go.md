# Go history

- https://www.zhubert.com/blog/2014/01/12/introduction-to-go-golang-part-1/

# Why Go

- Жуткое количество файлов
- Go сразу в корне


https://habrahabr.ru/post/261339/

- Немалую роль тут сыграл колоссальный практический опыт авторов Go — Пайка, Томпсона и компании — людей, стоявших у истоков Unix, языка C и UTF-8, а сейчас работающих над ключевыми продуктами Google. Так или иначе, но Go явился в некоторой степени радикальным языком, который качнул маятник сложности в другую сторону, пытаясь выровнять существующий ландшафт мира разработки ПО.
- И это именно то, что подразумевается под термином “простота” в контексте Go. Уменьшение сложности. Уменьшение времени необходимое среднестатическому программисту для понимания среднестатического проекта, написанного другими людьми. Уменьшение рисков ошибок. Уменьшение времени и затрат на «хорошие практики». Уменьшение шансов писать код плохо и некрасиво. Уменьшение времени на освоение языка. И так далее, и тому подобное.
- https://habrastorage.org/files/a3c/3fc/c6a/a3c3fcc6a7e448a79bbd341ae3be3a07.png

# https://habrahabr.ru/post/273535/

«Ухты, я прочёл код библиотеки один раз и я знал, что она делает. Я прочёл код Scala-версии библиотеки 4 раза и до сих пор не понимаю до конца, как она работает. Теперь я понимаю, почему вы так запали на Go». 

# Why not Go

- No code outline
- Name string `json:"name,omitempty" xml:"name"`

http://devs.cloudimmunity.com/gotchas-and-common-mistakes-in-go-golang/


https://habrahabr.ru/company/jugru/blog/352438/
Выводы
- Java становится все лучше, и способов выстрелить себе в ногу становится намного больше. Поэтому вот парочка советов:
- Не болейте стримозом

https://stackoverflow.com/questions/46356345/can-java-9-run-on-a-32-bit-os
Sorry, but we have no plans to ship 32-bit builds of JDK 9. We’re trying to focus more on the future than the past.
Yes, you can build your own 32-bit JDK 9 binaries.

Update 2: Apparently Oracle has decided to eliminate support for x86 Java forever.

## Habr

https://habrahabr.ru/company/piter/blog/304040/

1) Service discovery.
client side? server side? Как у Go с готовыми библиотеками под это дело? А такими которые уже опробованы в продакешене? А такими, которые опробованы в продакшене крупными компаниями аля нетфликс?
Понятное дело что можно использовать клиентов для Consul или Eureka.

2) Circuit breaker
Вот тот вот сервис подтупливает и отвечает по 1000 секунд вместо 5. Из-за этого все сервисы, которые на него завязаны тоже начинают тупить. Есть ли готовый продакшен фреймворк для go в этом случае? (Hystrix с страницей отчета)

3) Нужно сделать CRUD over REST, с пагинацией, с базовыми селектами.
Есть ли удобные и проверенные временем фреймворки для Go под это дело?

4) OAuth и сотоварищи. Насколько просто повесить на Go endpoint-ы авторизацию и аутентификацию?

5) Tracebility. Есть ли возможность *просто* отследить все сервисы через которые прошел запрос? Так, чтобы без руками пробрасывать UUID correlationID в заголовках или теле запроса?

6) Логирование. Stdout, конечно круто, а что насчет простой интеграции с ELK?



# Links
- Why we switched from Python to Go https://getstream.io/blog/switched-python-go/
- https://codeburst.io/passing-go-for-a-second-time-a346076f3bb7
- JavaScript https://medium.com/@johntucker_48673/really-appreciate-the-response-it-focused-my-attention-on-why-i-was-drawn-to-the-opinionatedness-86ac3fcbc5f6
- https://medium.freecodecamp.org/here-are-some-amazing-advantages-of-go-that-you-dont-hear-much-about-1af99de3b23a


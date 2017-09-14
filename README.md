# Тестовое задание для Frontend-разработчика

Ниже приведена иллюстрация к тому, что необходимо получить на выходе. Эскизы сделаны исходя из мобильной верстки.

![alt text](https://raw.githubusercontent.com/alexeyromanchuk/testtask/master/prototypes.png)

## Экран первый - наблюдение за курсами валют

1. Есть серверное API, точка https://testapi.copernicusgold.com/api/v1/rates?source=EUR&target=USD,
   которая для пары EUR/USD возвращает текущее значение курса.
2. Запрашиваем значение курса каждые 10 секунд.
3. В разделе History, в первой полоске пишем значение, которое было 1 минуту назад, во второй полоске - 2 минуты назад, в третьей, соответственно, 3 минуты назад.
4. Если курс в каком-либо их блоков History стал выше, чем текущий, то окрашиваем соответствующий блок в зеленый цвет, если стал ниже - в красный, если в точности равен текущему - в серый.
5. Переход на второй экран по стрелочке в правом верхнем углу



## Экран второй - регистрация задач при изменении курса

1. Создаем объект Задача, в котором заполняем поля "наименование" и "описание". Нужно проверять, чтобы введенные символы были только латинскими буквами, запятой, тире или звездочкой.
2. Выбираем режим - за каким курсом наблюдать из History (1, 2 или 3 минуты назад).
3. Указываем, когда считать Задачу выполненной: выбор из вариантов, когда текущий курс вырос, упал или совпал с соответствующим значением из History.
4. В правом верхнем углу - переход на третий экран, в левом - возврат на первый.



## Экран третий - список задач и их статусы

1. После регистрации задачи она попадает в список.
2. Происходит непрерывный мониторинг выполнения условия завершения задач при изменении курса - если для какой-либо задачи условия срабатывает, то её статус становится выполненным.
3. Выполненные задачи помещают в конец списка задач и выделяются серым цветом (как показано на рисунке)

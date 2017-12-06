# Tech-Terms-Advent-Calendar
## 1. **throttle & debounce**
> Паттерны для js (обертки), декораторы, они навешиваются на функции, чтобы снизить нагрузку на браузер и dom, чтобы притормозить частоту их выполнения.

**Throttle** - выполнять что-то не чаще одного раза в указанное n - время.

**Debounce** - запускает ф-цию не сразу, а через n - время.

## 2. **soft skills & hard skills**
> описывают способности 

**soft skills** («мягкие навыки» или «гибкие навыки») - умение убеждать, находить подход к людям, лидировать, межличностное общение, ведение переговорных процессов, работа в команде, личностное развитие, управление временем, эрудированность, креативность и т.п. Взаимодействие с людьми.

**hard skills** («твердые навыки») - делопроизводство, логистика, метод слепой печати, управление автомобилем, программирование и т.п. Профессиональные технические навыки.

## 3. **Continuous integration & Continuous deployment**
> непрерывное изменениям программного обеспечения, которые происходят в течении всего процесса разработки ПО.

**Continuous deployment** ("непрерывное развёртываение") - отвечает за то, чтобы весь новый функционал после тестирования сразу же попал в основную программу без ручного вмешательства инженеров DevOps. Пример Docker

**Continuous integration** - постоянное попадание кода в центральный репозиторий после успешного запуска тестов (unit – тесты). Agile Development

## 4. **Currying vs Partial application**
> языковые приемы, позволяют манипулировать количеством аргументов у функций или методов, трансформация ф-ции в другую ф-цию с меньшим к-вом аргументов.

**Currying** ф-ция в ф-ции

before
```
    function add(x, y) {
        return x + y;
    }
```
after
```
    function addC(x) {
        return function (y) {
            return x + y;
        }
    }
```

**Partial application** часть аргументов (хоть один, хоть все кроме одного) уже подставлены.

before
```
const job = 'programmer'
const salary1 = getAverageSalary(job, 'spain');
const salary2 = getAverageSalary(job, 'russia');
const salary3 = getAverageSalary(job, 'usa');
```
after
```
const getProgrammersSalaryByCountry =
  country => getAverageSalary('programmer', country);

const salary1 = getProgrammersSalaryByCountry('spain');
const salary2 = getProgrammersSalaryByCountry('russia');
const salary3 = getProgrammersSalaryByCountry('usa');
```

## 5. User story vs Epic
> относится к Agile - набор подходов по «гибкой» разработке программного обеспечения. Задачи, требования для проэкта.

**user story** - короткие пожелание (от заказчика или команды), что нужно реализовать, сделать, мини-задачи.

**epic** - основное, более общее пожелание, что включает очень много пользовательских историй.



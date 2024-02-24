
<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 3</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Знайомство з базовими командами  <br/>
CLI-режиму в Linux <br/></h2>



<div style="text-align: right;">
    <font size="4"><b>Виконали студенти <br/> групи РПЗ-13а <br/> Команда OSGURU: <br/> Войтенко В.С., <br/>  Селезень Є.С. <br/> Перевірив викладач <br/> Сушанова В.С. </b></font>
</div>

<br/>
<br/>
<br/>

<h2 align="center">Київ 2024</h2>

<hr>

**Мета роботи:**
1. Знайомство з базовими командами CLI-режиму в Linux.
2. Знайомство з базовими текстовими командами в термінальному режимі роботи в різних ОС.

**Матеріальне забезпечення занять**
1. ЕОМ типу IBM PC.
2. ОС сімейства Windows (Windows 7).
3. Віртуальна машина – Virtual Box (Oracle).
4. Операційна система GNU/Linux – CentOS.
5. Сайт мережевої академії Cisco netacad.com та його онлайн курси по Linux

**Завдання для попередньої підготовки.**<br/>
*Готував матеріал студент Войтенко В.*

1. Прочитайте короткі теоретичні відомості до лабораторної роботи та зробіть невеликий словник базових англійських термінів з питань призначення команд та їх параметрів.

<h2 align="center"><b>A BRIEF GLOSSARY OF BASIC ENGLISH TERMS RELATED <br/>
TO THE CLASSIFICATION OF VIRTUAL ENVIRONMENTS</b></h2>

|                       Термін англійською                   |                                    Термін українською                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Shell (the command line interpreter that translates commands entered by a user into actions to be performed by the operating system). | Оболонка (інтерпретатор командного рядка, який перекладає команди, введені користувачем, на дії, які повинна виконати операційна система.)|
| Command Line Interface (CLI) (a text-based interface for interacting with a computer through typed commands)| Інтерфейс командного рядка (CLI) (текстовий інтерфейс для взаємодії з комп'ютером за допомогою введених команд)|
| Bash Shell (The most commonly used shell for Linux distributions, which features  command line history, inline editing, scripting, aliases, and variables.) | Оболонка Bash (Найпоширеніша оболонка для дистрибутивів Linux, яка має такі функції: історія команд, вбудований редактор, скриптування, псевдоніми та змінні) |
| Prompt (Displays information about the user and the system in the command-line interface. Typically includes the username, system name, and current directory) | Віртуалізація (технологія, яка дозволяє створювати віртуальні версії апаратного забезпечення, операційних систем, сховищ даних та інших ресурсів) |
| Command (A software program that, when executed on the CLI, performs an action on the computer) | Команда (Програмне забезпечення, яке, коли виконується у CLI, виконує дію на комп'ютері.)|
| Arguments (the data passed to a specific command in the command line, indicate something for the command to act upon or which parameters it should use) | Аргументи (це дані, які передаються певній команді у командному рядку. Вони вказують на щось, на що має впливати команда або які параметри вона має використовувати)  |
| Options (used with commands to expand or modify the way a command behaves) | Опції (параметри) (використовуються з командами для розширення або модифікації способу поведінки команди) |
| Internal commands (built-in commands) | Вбудовані команди (внутрішні команди) |
| External commands (stored in files) | Зовнішні команди (зберігаються в файлах) |
| Aliases (map longer commands to shorter key sequences) | Псевдоніми (відображення довших команд на короткі послідовності клавіш) |
| Functions (built using existing commands to create new commands or override existing ones) | Функції (створюються за допомогою існуючих команд для створення нових команд або перевизначення вбудованих або команд, що зберігаються у файлах) |
| Quoting (the use of various types of quotation marks or quotes in programming and working with the command line to specify how text should be processed) | Укладення (цитування) (це використання різних видів лапок або кавичок у програмуванні та роботі з командним рядком для вказання, як текст має бути оброблений) |
| Double quotes (") Single quotes (') Back quotes (`) | Подвійні лапки (") Одинарні лапки (') Зворотні лапки (`) |
| Control statements (Allow the use of multiple commands at once or run additional commands) | Керуючі оператори (Дозволяють використовувати кілька команд одночасно або запускати додаткові команди) |
| Semicolon ( ; )  | Крапка з комою |
| Double ampersand (&&) | Подвійний амперсанд |
| Double pipe (\||) \| Подвійна вертикальна риска |

4. Дайте визначення наступним поняттям:

1\)	**Command Prompt:** This is software that executes commands provided by the user or other programs and interacts with the operating system to perform specific tasks. A command prompt takes commands from the user via the command line or other sources and executes them on the system.

2\)	**Shell:** This is the interface between the user and the operating system that accepts commands from the user and passes them to the operating system kernel for execution. The shell can provide access to functions such as running programs, managing files, and inputting/outputting data.

3\) **Command:** This is an instruction or direction that a user or program provides to an operating system to perform a specific action. A command can be entered on the command line or invoked from a program interface, and it tells the operating system what to do. Commands can perform a variety of actions, from managing files and processes to configuring the system and interacting with the user.

5. Дайте відповіді на наступні питання:

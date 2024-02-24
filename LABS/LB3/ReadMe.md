
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
| Double pipe (\|\|) | Подвійна вертикальна риска |
| Variables (is a feature that allows the user or the shell to store data temporarily in memory) | Змінні (можливість, яка дозволяє користувачеві або оболонці зберігати дані тимчасово в памяті) |
| Command Types | Типи команд |


4. Дайте визначення наступним поняттям:

1\)	**Command Prompt:** This is software that executes commands provided by the user or other programs and interacts with the operating system to perform specific tasks. A command prompt takes commands from the user via the command line or other sources and executes them on the system.

2\)	**Shell:** This is the interface between the user and the operating system that accepts commands from the user and passes them to the operating system kernel for execution. The shell can provide access to functions such as running programs, managing files, and inputting/outputting data.

3\) **Command:** This is an instruction or direction that a user or program provides to an operating system to perform a specific action. A command can be entered on the command line or invoked from a program interface, and it tells the operating system what to do. Commands can perform a variety of actions, from managing files and processes to configuring the system and interacting with the user.

5. Дайте відповіді на наступні питання:

*- Яку базову інформацію надає рядок запрошення prompt?*

The prompt line provides basic information about the current working environment and system status. It usually includes the user name, system or host name, and the path to the current working directory. 
<br/>
For example, a typical prompt string might look like this:
<br/>
**sysadmin@localhost:~$**

The prompt string contains the following information:
- User name (sysadmin)
- System name (localhost)
- Current directory (~)
- Current Directory (~) "$" is usually a character that indicates the end of the prompt line

*Для чого команді потрібні параметри та аргументи?*

Arguments indicate something that the command should act on or what parameters it should use.  Variables are used with commands to extend or modify the way the command behaves.

*- Яке призначення команд ls, які параметри та аргументи вона може мати? Наведіть 3 приклади.*

The main parameters and arguments of the ls command:

Option -l: Displays detailed information about files and directories, such as access permissions, owner, group, file size, date and time of modification.

Example: ls -l.

The -a option: Shows all files, including hidden files, that start with a dot.

Example: ls -a

The directory argument: Shows the contents of the specified directory instead of the current directory.

Example: ls /home/user/documents

*- Яким чином можна використати історію команд, які переваги це надає?*

Allows users to view and repeat previously entered commands in the terminal: 

а\) The user can simply view the command history by typing the history command in the terminal. This will show a list of recently entered commands and their numbers.

b\) Repeating the previous command: To repeat the last command entered, you can use the up arrow key or type !!.

c\) Repeating a command by its number: The user can repeat any command from the history using its number. For example, !23 will repeat the 23rd command in the history.

d\) Search for commands in the history: Using the Ctrl+R key, the user can search for previous commands by partial phrase or word.
Benefits: automation and error correction.

*- Яке призначення команди echo?*

echo is used to output text or variables to the screen or to a file 

*- Охарактеризуйте поняття змінної в оболонці Bash, які типи змінних вона підтримує?*

A variable in the Bash shell is a named container that is used to store a value.

**Types of variables:**

Local variables: available only within the current script or shell.
<br/>
Environment variables: available to all child processes running from the current shell.
<br/>
Export variables: available to all child processes as well as to other shells running from the current shell.

**Data types:**

String: text data.
<br/>
Integer: numeric data.
<br/>
Lists: ordered collections of data.
<br/>
Associative arrays: unordered collections of data where each element has a key and a value.

*- Яке призначення команд env, export та unset?*

**env:** displays a list of all environment variablesб сan be used to run commands with a modified environment.
<br/>
**export:** used to create environment variables or to extend the visibility of existing variables to all child processes.
<br/>
**unset:** used to remove variables from the shell.

**Хід роботи.**

1. Опрацюйте всі приклади команд, що представлені у лабораторній роботі курсу NDG Linux Essentials - Lab 5: Command Line Skills та Lab 6: Getting Help. Створіть таблицю для опису цих команд***

[//]: # (ВСТАВИТИ ТАБЛИЦЮ!!!)

2. Робота в в терміналі (закріплення практичних навичок) обов'язково представити свої скріншоти:
   
2.1. Робота зі змінними (Variables) та псевдонімами (Aliases) в терміналі:
- Створіть змінні, що будуть містити Ваші імена та прізвища $var_name1, $var_name2, $var_name3

![Export var_name](./images/export_var_name.jpg)

- За допомогою команди echo виведіть імена студентів вашої команди
  
![Echo var_name](./images/echo_var_name.jpg)

- Створіть псевдоніми mycal1, mycal2, mycal3 для команди cal для автоматичного виведення
календарю вашого року народження

![Alias](./images/alias.jpg)

![Alias_result](./images/result_alias.jpg)

2.2. Робота з функціями (Functions) в терміналі:
- Створіть функцію students_report, що порядково буде виводити спочатку імена студентів Вашої
команди, а потім роки їх народження.

![Function](./images/function.jpg)

![Reesult_function](./images/result_function.jpg)

2.3. Робота з лапками (Quoting) в терміналі. Виведіть в командному рядку наступні речення:
- “We create such variables as $var_name1, $var_name2, $var_name3, which stored our names Name1, Name2, Name3” (у реченні спочатку виводимо назви змінних, а потім їх вміст)

![2_3_a](./images/2_3_a.jpg)

- “We create such Aliases as mycal1, mycal2, mycal3, which can show our calendars: Calendar1, Calendar2, Calendar3” (у реченні спочатку виводимо назву команди-псевдонімів, потім вивід
цих команд).

![2_3_b](./images/2_3_b.jpg)

2.4. Робота з інструкціями керування (Control Statements) в терміналі:.
- Чи можна завдання 2.1 та 2.2 ходу роботи виконати через інструкції керування без написання
окремої функції, як це буде виглядати?

![2_4](./images/2_4.jpg)

2.5. Робота з командами довідки (Man Pages) в терміналі:.
- На прикладі команди uname продемонструйте як отримати довідку. На основі отриманої додаткової інформації наведіть 5 різних варіантів виводу результату інформації по даній команді з використанням 5 різних параметрів (Options)

![2_5_1](./images/2_5_1.jpg)

![2_5_2](./images/2_5_2.jpg)

![2_5_3](./images/2_5_3.jpg)

![2_5_4](./images/2_5_4.jpg)

![2_5_5](./images/2_5_5.jpg)

![2_5_6](./images/2_5_6.jpg)

![2_5_7](./images/2_5_7.jpg)


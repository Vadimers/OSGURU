<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 5</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Знайомство з командами навігації по файловій системі та керування файлами та каталогами” <br/></h2>



<div style="text-align: right;">
    <font size="4"><b>Виконали студенти <br/> групи РПЗ-13а <br/> Команда OSGURU: <br/> Войтенко В.С., <br/>  Селезень Є.С. <br/> Перевірив викладач <br/> Сушанова В.С. </b></font>
</div>

<br/>
<br/>
<br/>

<h2 align="center">Київ 2024</h2>

<hr>

**Мета роботи:**
<br/>
 Отримання практичних навиків роботи з командною оболонкою Bash.
<br/>
 Знайомство з базовими командами навігації по файловій системі.
<br/>
 Знайомство з базовими командами для керування файлами та каталогами.
<br/>

**Матеріальне забезпечення занять:**
1. ЕОМ типу IBM PC.
2. ОС сімейства Windows та віртуальна машина Virtual Box (Oracle).
3. ОС GNU/Linux (будь-який дистрибутив).
4. Сайт мережевої академії Cisco netacad.com та його онлайн курси по Linux

**Завдання для попередньої підготовки.**<br/>
*Готував матеріал студент Войтенко В.*

1. Прочитайте короткі теоретичні відомості до лабораторної роботи та зробіть невеликий словник базових англійських термінів з питань призначення команд та їх параметрів.

<h2 align="center"><b>A BRIEF GLOSSARY OF BASIC ENGLISH TERMS RELATED <br/>
TO THE CLASSIFICATION OF VIRTUAL ENVIRONMENTS</b></h2>

|                       Термін англійською                   |                                    Термін українською                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Hierarchical organization structure (a system of organizing elements into levels or ranks, where each level contains sub-elements related to the one above it) | Ієрархічна структура організації (система організації елементів на рівні або в рангах, де кожен рівень містить під-елементи, пов'язані з вищим)|
| The top level of the directory structure (the highest level in the hierarchy of directories within a filesystem)| Верхній рівень структури каталогів (найвищий рівень у ієрархії каталогів у файловій системі)|
| Filesystem (a method used by an operating system to organize and store data on a storage device) | Файлова система (метод, що використовується операційною системою для організації та зберігання даних на пристрої зберігання) |
| Unix ﬁle structure (the organization of files and directories in the Unix operating system) | Структура файлів Unix (організація файлів та каталогів у операційній системі Unix) |
| Linux ﬁlesystem (the organization of files and directories in the Linux operating system) | Структура файлів Linux (організація файлів та каталогів у операційній системі Linux)|
| Filesystem Hierarchy Standard (FHS) (a set of guidelines that define the structure of directories in Unix-like operating systems, including Linux) | Стандарт ієрархії файлової системи (набір рекомендацій, що визначають структуру каталогів у подібних до Unix операційних системах, включаючи Linux)  |
| Home directory (a unique directory assigned to your user account) | Домашній каталог (унікальна директорія, призначена вашому обліковому запису користувача) |
| GUI-based applications (applications that have a graphical user interface, allowing users to interact with them using visual elements such as windows, buttons, and icons) | Програми з графічним інтерфейсом користувача (програми, які мають графічний інтерфейс користувача, що дозволяє користувачам взаємодіяти з ними за допомогою візуальних елементів, таких як вікна, кнопки та піктограми) |
| Globbing (a mechanism in shell scripting that allows pattern matching against filenames) | Глобування (механізм у скриптінгу оболонки, який дозволяє порівнювати шаблони з іменами файлів) |
| Glob characters (special characters used in globbing to represent sets of filenames) | Символи глобування (спеціальні символи, які використовуються у глобуванні для представлення наборів імен файлів) |
| Filename length (the number of characters in a filename) | Довжина імені файлу (кількість символів у назві файлу) |
| Asterisk * character (used to represent zero or more of any character in a filename) | Символ зірочка * (використовується для позначення нуля або більше будь-яких символів у назві файлу) |
| Question mark ? character (represents any single character) | Знак питання ? символ (представляє будь-який окремий символ) |
| Bracket [] characters (used to match a single character by representing a range of characters that are possible match characters) | Символи дужки [] (використовуються для зіставлення одного символу шляхом представлення діапазону символів, які є можливими символами зіставлення) |
| Exclamation point ! character (used in conjunction with the square brackets to negate a range)  | Символ оклику ! (використовується разом з квадратними дужками для заперечення діапазону) |

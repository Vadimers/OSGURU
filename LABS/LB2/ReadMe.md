<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 2</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Знайомство з інтерфейсом <br/>
та можливостями OC Linux"</h2>



<div style="text-align: right;">
    <font size="4"><b>Виконали студенти <br/> групи РПЗ-13а <br/> Команда OSGURU: <br/> Войтенко В.С., <br/>  Селезень Є.С. <br/> Перевірив викладач <br/> Сушанова В.С. </b></font>
</div>

<br/>
<br/>
<br/>

<h2 align="center">Київ 2024</h2>

<hr>

**Мета роботи:**
1. Знайомство з інтерфейсами ОС Linux.
2. Отримання практичних навиків роботи в середовищах ОС Linux та мобільної ОС – їх графічною
оболонкою, входом і виходом з системи, ознайомлення зі структурою робочого столу, вивчення
основних дій та налаштувань при роботі в системі
   
**Матеріальне забезпечення занять**
1. ЕОМ типу IBM PC.
2. ОС сімейства Windows (Windows 7).
3. Віртуальна машина – Virtual Box (Oracle).
4. Операційна система GNU/Linux – CentOS.
5. Сайт мережевої академії Cisco netacad.com та його онлайн курси по Linux

**Завдання для попередньої підготовки.**<br/>
*Готував матеріал студент Войтенко В.*

1. Прочитайте короткі теоретичні відомості до лабораторної роботи та зробіть невеликий словник базових англійських термінів з питань класифікації віртуальних середовищ.

<h2 align="center"><b>A BRIEF GLOSSARY OF BASIC ENGLISH TERMS RELATED <br/>
TO THE CLASSIFICATION OF VIRTUAL ENVIRONMENTS</b></h2>

|                       Термін англійською                   |                                    Термін українською                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Command Line Interface (CLI) (a simple text input system for entering anything from single-word commands to complicated scripts) | Інтерфейс командного рядка (CLI) (це проста система введення тексту для введення як окремих команд так і складних сценаріїв)|
| GUI terminal (a program within the GUI environment that emulates a terminal window)| GUI-термінал (це програма в межах середовища GUI, яка емулює вікно терміналу)|
| Virtual Terminal (a terminal interface accessed independently of the graphical interface, typically requiring user login before executing commands) | Віртуальний термінал (інтерфейс терміналу, доступний незалежно від графічного інтерфейсу, який зазвичай вимагає входу користувача перед виконанням команд) |
| Kernel (the core component of an operating system responsible for managing system resources, handling tasks, and facilitating communication between hardware and software) | Ядро (основний компонент операційної системи, що відповідає за управління системними ресурсами, обробку завдань і полегшення комунікації між апаратним та програмним забезпеченням) |
| Application (software programs that perform specific tasks or functions on a computer system, interacting with the kernel to access resources) | Додаток (програмне забезпечення, що виконує конкретні завдання або функції на комп'ютерній системі, взаємодіючи з ядром для доступу до ресурсів)|
|  API (Application Programming Interface) (a set of protocols, tools, and definitions that allow different software applications to communicate with each other) | API (Інтерфейс програмування додатків) (набір протоколів, інструментів і визначень, що дозволяють різним програмним додаткам взаємодіяти один з одним) |
| Multitasking (the process by with the kernel handles the switching of applications) | Багатозадачність (це процес, при якому ядро керує перемиканням додатків) |
| Process (is one task that is loaded and tracked by the kernel) | Процес (це одне завдання, яке завантажується і відстежується ядром) |
| Server Applications (software designed to provide services or data to other computers or clients over a network) | Серверні додатки (програмне забезпечення, призначене для надання послуг або даних іншим комп'ютерам або клієнтам через мережу) |
| Desktop Applications (software programs used directly by users for tasks such as browsing the web, editing documents, or playing media) | Додатки для робочого столу (програмне забезпечення, яке використовується безпосередньо користувачами для таких завдань, як перегляд веб-сторінок, редагування документів або відтворення медіафайлів) |
| Tools (software utilities or programs aimed at aiding in the management, configuration, or development of computer systems) | Інструменти (утиліти або програмне забезпечення, спрямовані на допомогу у керуванні, налаштуванні або розробці комп'ютерних систем) |
| Distribution (a variant of the Linux operating system, typically consisting of the Linux kernel, GNU utilities, and additional software packages, tailored for specific use cases or user preferences) | Розподілення (варіант операційної системи Linux, який зазвичай складається з ядра Linux, утиліт GNU та додаткових пакунків програмного забезпечення, налаштованих для конкретних випадків використання або вимог користувачів) |
| Evaluating application software (the process of analyzing and assessing software to determine its suitability for a specific use case, is an important skill to be learned by the aspiring Linux administrator) | Оцінка програмного забезпечення (процес аналізу та оцінки програмного забезпечення з метою визначення його придатності для конкретного використання, це важлива навичка, яку повинен засвоїти майбутній Linux-адміністратор) |

<br/>

4. Дайте визначення наступним поняттям:

*Готував матеріал студент Войтенко В.(варіант - 3) та Селезень Є.(варіант - 16)*

<br/>

**CLI-режим - CLI mode (Command Line Interface mode)**, which allows the user to interact with the computer by entering commands via text input.

**Термінал на основі графічного інтерфейсу користувача - GUI terminal (Graphical User Interface terminal)** - software that emulates a terminal in a graphical user interface, allowing users to execute commands and interact with the operating system using a text-based interface.

**Віртуальний термінал - Virtual Terminal** - a terminal interface accessed independently of the graphical interface, typically requiring user login before executing commands.

**Відповіді на контрольні запитання**
<br/>

***Готував матеріал студент Войтенко В.***

1. Наведіть приклади серверних додатків Linux для сервера баз даних, серверів розсилки повідомлень та файлообмінників.

1) Database server:
   - MySQL or MariaDB: Popular open-source relational database management system (RDBMS).
   - PostgreSQL: Another powerful relational DBMS supporting advanced SQL extensions and ACID properties.
   - MongoDB: A NoSQL database storing data in JSON-like documents.

2) Mail servers:
   - Postfix: Popular Mail Transfer Agent (MTA) used for sending and receiving email.
   - Sendmail: Another MTA providing similar functionality to Postfix.
   - Exim: Another MTA with extensive customization and extension capabilities.

3) File exchanges:
   - vsftpd: Very Secure FTP Daemon, a fast and secure FTP server for file transfer.
   - ProFTPD: Another powerful FTP server with many features and customization options.
   - Samba: Allows file sharing between Linux systems and Windows computers using the SMB/CIFS protocol.


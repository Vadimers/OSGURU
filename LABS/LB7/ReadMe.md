<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 7</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Створення скриптових сценаріїв та визначення апаратної конфігурації системи” <br/></h2>



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
|  Shell script (a shell script is an executable file containing a series of commands stored in a text file. When executed, each command is run sequentially) | Сценарій оболонки (файл виконуваних команд, збережений у текстовому файлі. При запуску кожна команда виконується послідовно) |
| Binary search path ($PATH) (a list of directories where executable files are located) | Бінарний шлях пошуку ($PATH) (cписок каталогів, де знаходяться виконувані файли) |
| chmod (command for changing file access permissions) | chmod (зміна прав доступу)	(команда для зміни прав доступу до файлу) |
| GNU nano (a simple text editor suitable for editing small text files) | GNU nano (простий текстовий редактор, придатний для редагування невеликих текстових файлів) |
| Exit (Ctrl+X) (сommand to exit a program or interface) | Вихід (Ctrl+X) (команда для виходу з програми або інтерфейсу) |
| Save (Ctrl+O) (command to save changes made to a file)  | Зберегти (Ctrl+O) (команда для збереження внесених змін у файл)  |
| Paste (Ctrl+U) (command to insert the contents of the copy buffer at the current cursor position) | Вставити (Ctrl+U) (команда для вставлення вмісту буфера обміну у поточну позицію курсора) |

*Готували матеріал студенти Войтенко В. та Селезень Є.*

1. На базі розглянутого матеріалу дайте відповіді на наступні питання:

4.1 *Охарактеризуйте поняття скриптового сценарію у командній оболонці.

A shell script in a command line environment is a file containing a sequence of commands to perform specific tasks or operations. It is typically created to automate routine tasks or to execute a series of commands in a logical order. Scripts may include conditional constructs, loops, variables, and other elements to enable complex operations and data processing.

4.2 *Яким чином створюються та редагуються скрипти, що треба зробити щоб запустити скрипт?

Scripts can be created and edited using text editors such as nano, vi, or any other suitable editor. To create a new script, you use file creation commands like touch or nano. After creating the script file, you need to edit it by adding the necessary commands and logic.

To execute the script, you first need to give it execute permissions using the chmod +x script_name.sh command, where script_name.sh is the name of your script. Then you can run the script by specifying its name along with the file path, for example, ./script_name.sh.

4.3 **Які основні компоненти материнської плати ви знаєте?

Central Processing Unit (CPU): Performs calculations and manages the computer's operation.

Chipset: Manages data transmission between various computer components and interacts with other devices, such as the CPU, RAM, and peripheral devices.

CPU Socket: A socket into which the CPU is inserted.

Memory Slots (DIMM/RAM): Places for installing RAM, which is used for temporarily storing data that the CPU can quickly access.

Expansion Slots (PCI, PCIe): Allow connection of expansion cards, such as video cards, sound cards, etc.

Input/Output Ports (USB, HDMI, Ethernet, Audio): Allow connection of external devices, such as keyboard, mouse, monitor, speakers, etc.

BIOS/UEFI Chip: Provides initialization of hardware components when the computer starts up and initial configuration of the system.

CMOS Battery: Stores BIOS/UEFI settings and system time when the computer is turned off.

Power Supply System (Power Supply Unit, Capacitors): Provides power to all components of the motherboard and other computer devices.

4.4 **Коротко охарактеризуйте для яких пристроїв оперують поняттями MBR та GPT?

MBR (Master Boot Record) and GPT (GUID Partition Table) are two different disk partitioning schemes used to organize information on storage devices such as hard drives. MBR was a widely used standard for BIOS-based computers, while GPT is the modern standard, particularly for devices with UEFI (Unified Extensible Firmware Interface). Therefore, MBR is used on older BIOS-based computers, while GPT is used on modern UEFI-based computers.

4.5 **В чому суть операції монтування, для чого вона потрібна?

Mounting in computer systems involves temporarily connecting a file system located on an external device to the directory hierarchy of a computer. Connecting an external device to the system and mounting it allows the computer to access files and folders stored on that device.

Mounting serves several purposes, including:

**Accessing external devices:** For example, mounting enables access to files on USB drives, external hard drives, etc.

**Working with partitions on hard drives:** Connecting and mounting disk partitions allows reading and writing data to them.

**Exchanging information between systems:** Mounting can be used to exchange files between different operating systems, such as between Linux and Windows.

**Ensuring security and confidentiality:** Some systems require mounting to ensure data security and confidentiality, such as encrypting files on an external device.

In summary, mounting is an important operation for accessing external devices and exchanging information between different systems in computer environments.

*Готував матеріал студент Войтенко В.*

**Хід роботи:**

2. Опрацюйте всі приклади команд, що представлені у лабораторних роботах курсу NDG Linux Essentials - Lab 11: Basic Scripting та Lab 12: Understanding Computer Hardware. Створіть таблицю для опису цих команд

|                        Назва команди                       |                                Її призначення та функціональність                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| sh test.sh | Запуск скрипту |
| <p >ANIMAL="penguin" <p> echo "My favorite animal is a $ANIMAL <p/> | Використання змінної у скрипті |
| <p> #!/bin/bash CURRENT_DIRECTORY=`pwd` <p> echo "You are in $CURRENT_DIRECTORY" <p/> | Вивід іншої команди як вміст змінної, помістивши команду в символ лапки ` |
| <p> #!/bin/bash <p> echo -n "What is your name? " <p> read NAME <p> echo "Hello $NAME!" <p/> | Отримання вхідних даних від користувача скрипта і присвоєння їх змінній за допомогою команди read |
| ./test.sh Linux | Використання аргументу в скрипті |
| <p> grep -q root /etc/passwd <p> echo $? <p/> | Перевірка чи успішно завершилася попередня команда |
| <p> if somecommand; then <p> /# do this if somecommand has an exit <p> code of 0 <p> fi <p/> | Використання розгалудження. Якщо код виходу дорівнює 0, то буде виконано вміст до закриваючого fi |
| test –f /dev/ttyS0 | Перевірка чи існує файл |
| test –d /tmp | Перевірка чи існує каталог |
| free -m | Виведення рівня використання пам’яті |
| lspci | Виведення пристроїв підключених до шини PCI |
| lsusb | Виведення пристроїв підключених до портів USB |
| fdisk, cfdisk, fsdisk | Команди для модифікації розділів MBR |
| gdisk, cdisk, sdisk | Команди для перегляду та модифікації GPT-розділів |

Створіть скриптові сценарії з виводом текстових повідомлень для користувача (продемонструйте скріншоти):

сценарій має виводити привітання до поточного користувача вказуючи поточну дату та інформацію про поточну систему;

![1_1](./images/1_1.png)

<br/>

<br/>

![1_2](./images/1_2.png)

<br/>

<br/>

*сценарій має виводити інформацію про апаратну конфігурацію поточної системи (використовуйте команди розглянуті в Lab 12: Understanding Computer Hardware);

![2_1](./images/2_1.png)

<br/>

<br/>

![2_2](./images/2_2.png)

<br/>

<br/>

**наведіть свій приклад скриптового сценарію.

 ![3_1](./images/3_1.png)

<br/>

<br/>

 ![3_2](./images/3_2.png)

<br/>

<br/>

**Контрольні запитання:**

1. В чому відмінність між командами arch та lscpu?
   
The commands arch and lscpu are designed to display information about the processor architecture, but they show different aspects of this information:

arch: This command displays information about the system architecture it operates on. Typically, it only indicates the processor architecture, such as x86_64 (64-bit architecture Intel or AMD), i686 (32-bit architecture Intel or AMD), or others.

lscpu: This command provides more detailed information about the processor, including architecture, processor model, number of cores and threads, cache size, virtualization features, and other technical characteristics. Additionally, it can also output information about the system architecture and CPU operating modes, such as 32-bit or 64-bit.

2. Якою командою можна отримати інформацію про стан використання RAM поточною системою?
To obtain information about the usage of RAM by the current system, you can use the command free. This command will display the total amount of free and used RAM, as well as other related information such as buffered and cached memory.

3. *Яким чином у скриптах можна опрацьовувати змінні та створювати розгалужені та циклічні сценарії?

In scripts, variables can be processed, and branching and looping scenarios can be created using scripting languages such as Bash (for Unix-like systems) or PowerShell (for Windows).

Variable handling:

**Assigning values to variables:** For example, variable=value.
**Using variable values:** For example, echo $variable.<br/>

Branching:

**Conditional statements:** Used to execute different code blocks depending on a specified condition. In Bash, this can be the if-else construct.

Loops:

**for loop:** Used to iterate over a block of code for each item in a list
**while loop:** Executes as long as a specified condition is true. 

These constructs enable scripts to be more flexible and automated, handling variables, making branching decisions, and repeating actions in loops as per the program's requirements.

4. *Які команди для перегляду стану підключення периферійних пристроїв можна використати в терміналі? 

Linux/Unix: lsusb for USB devices, lspci for PCI devices, lsblk for block devices.<br/>
macOS: system_profiler SPUSBDataType.<br/>
Windows: Use "Device Manager" or the command wmic path Win32_PnPEntity get caption, status to view information about connected devices.<br/>

5. **Які можливості застунку gparted? 

GParted allows you to:

Create, delete, and modify disk partitions.<br/>
Resize partitions without data loss.<br/>
Move partitions on the disk.<br/>
Rename partitions.<br/>
Check and repair file systems.<br/>
Support various file system formats.<br/>
Edit using relative and absolute block devices.<br/>

Conclusion:
<br/>
In this lab, we learned basic commands for managing file and directory navigation and navigating the file system. We also gained some skills in working with the Bash shell and consolidated English terms for the purpose of commands and their parameters.
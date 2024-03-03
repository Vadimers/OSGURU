
<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 4</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Команди Linux  <br/>
 для управління процесами" <br/></h2>



<div style="text-align: right;">
    <font size="4"><b>Виконали студенти <br/> групи РПЗ-13а <br/> Команда OSGURU: <br/> Войтенко В.С., <br/>  Селезень Є.С. <br/> Перевірив викладач <br/> Сушанова В.С. </b></font>
</div>

<br/>
<br/>
<br/>

<h2 align="center">Київ 2024</h2>

<hr>

[//]: # (НАПИСАТИ ТАБЛИЦЮ!)

2. На базі розглянутого матеріалу дайте відповіді на наступні питання:

2.1. Які команди для моніторингу стану процесів ви знаєте. Як переглянути їх можливі параметри?

**top:** The top command displays a list of active processes in real time. It shows general system information such as CPU usage, memory, process information, and more.

![top](./images/top.png)

<h3 align="center"><b>top</b></h3>

<br/>

<br/>

**htop:** htop is an interactive alternative to the top command. It provides more functionality and a user-friendly interface for interacting with processes.

![htop](./images/htop.png)

<h3 align="center"><b>htop</b></h3>

<br/>

<br/>

**ps:** The ps command allows you to display a list of processes. You can use various flags to get more information about the processes, such as ps aux to list all processes.

![ps](./images/ps.png)

<h3 align="center"><b>ps</b></h3>

<br/>

<br/>

**pidstat:** This command provides real-time process statistics, including CPU usage, memory, and other parameters.

![pidstat](./images/pidstat.png)

<h3 align="center"><b>pidstat</b></h3>

<br/>

<br/>

**iotop:** This command allows you to monitor the input/output (I/O) on your system, that is, disk I/O activity.

![iotop](./images/iotop.png)

<h3 align="center"><b>iotop</b></h3>

<br/>

<br/>

**strace:** This tool tracks system calls and signals sent and received by processes.

![strace](./images/strace.png)

<h3 align="center"><b>strace</b></h3>

<br/>

<br/>

**lsof:** The lsof command displays a list of open files and ports on the system, including the processes that use them.

![lsof](./images/lsof.png)

<h3 align="center"><b>lsof</b></h3>

<br/>

<br/>

2.2. Чи може команда ps у реальному часі відслідковувати стан процесів?

No, the ps command cannot track the state of processes in real-time. It only provides a snapshot of the process state at the time it is invoked.
To monitor the state of processes in real-time in Linux, the top command is  used. It displays active processes in real-time and updates the information automatically.

2.3. За якими параметрами можливе сортування процесів в команді top? Як переключатись між ними?

The top command allows sorting processes, including by the following parameters:

**ViRT:** 

**RES:**

**SHR:**

**%CPU:** Percentage of CPU time used by the process. 

**%MEM:** Percentage of physical memory used by the process.

**PID:** Process ID.

**TIME+:** Total CPU time used by the process since its start.

**COMMAND:** Name of the command or program executed by the process.

2.4. Які команди для завершення роботи процесів ви знаєте?

Commands for terminating processes:

```kill```: allows you to send signals to processes based on their process IDs (PIDs);

```killall```: allows you to stop processes by their names instead of using PID numbers;

Хід роботи.


1. Початкова робота в CLI-режимі в Linux ОС сімейства Linux:

    1.3. Запустіть свою операційну систему сімейства Linux (якщо працюєте на власному ПК та її
    встановили) та запустіть термінал.

![Start Ubuntu](./images/start_ubuntu.png)

<h3 align="center"><b>Start Ubuntu</b></h3>

<br/>

<br/>

2. Дайте відповіді на наступні питання:

- Як вивести вміст директорії /proc? Де вона знаходиться та для чого призначена? Охарактеризуйте інформацію про її вміст?

To view the contents of the /proc directory, you can use the ls command in the terminal.

```ls/proc```

This command will display a list of files and folders contained in the /proc directory.

The /proc directory contains virtual files that provide information about the system's hardware, processes, and kernel runtime parameters. Each file in the /proc directory corresponds to a specific aspect of the system, and reading these files allows users and system utilities to gather detailed information about the system's configuration and current state.

Some common types of information available in the /proc directory include:

1.	Process Information: Files like /proc/[pid]/stat and /proc/[pid]/status provide detailed information about each running process, including its process ID (PID), parent process ID (PPID), memory usage, CPU usage, and more.

2.	System Information: Files like /proc/cpuinfo and /proc/meminfo provide information about the system's CPU, memory, and other hardware components.

3.	Kernel Information: Files like /proc/sys/kernel/version and /proc/sys/kernel/panic contain information about the running kernel, including its version and various configuration parameters.

4.	Network Information: Files like /proc/net/dev provide information about the system's network interfaces, including statistics on received and transmitted data.
Overall, the /proc directory serves as a convenient interface for accessing real-time system information in Linux.

- Як вивести інформацію про поточні сеанси користувачів. Якою командою це можна зробити?

You can view information about current user sessions using the who command. This command displays a list of users currently logged into the system, along with the times they logged in and other useful information about their sessions.

- Які дії можна зробити в терміналі за допомогою комбінацій Ctrl + C, Ctrl + D та Ctrl + Z?

1.	**Ctrl + C:** this combination interrupts the execution of the current command or program. It sends the INT (interrupt) signal to the process, typically resulting in its immediate termination;
2.	**Ctrl + D:**  this combination signals the end of file (EOF) in the terminal or exits you from the current shell if it is awaiting input;
3.	**Ctrl + Z:**  this combination suspends the execution of the current process and puts it into the background. It sends the STOP signal to the process, pausing its execution but not terminating it.

- Чим відрізняється фоновий процес від звичайного. Де вони використовуються?

**Foreground Process:**

a.	Executes in an active mode and displays its output on the screen.

b.	Blocks input of new commands until it completes its execution or is suspended.

c.	Often requires user interaction to terminate or continue its operation.

**Background Process:**

a.	Executes in the background mode and does not display its output on the screen.

b.	Does not block the terminal, allowing the user to enter commands while it runs.

c.	Typically used for tasks that require a long execution time or do not require active user participation.

- Опишіть наступні команди та поясніть що вони виконують – команда jobs, bg, fg.

1.	**Command jobs:**

*Description:* The jobs command displays a list of active tasks that have been launched in the current shell and are in the background mode.

*Usage:* jobs

2.	**Command bg:**

*Description:* The bg command is used to send stopped (suspended) background jobs into execution directly in the background mode.

*Usage:* bg [job_spec], where job_spec can be a job ID or % followed by its number.

3.	**Command fg:**

*Description:* The fg command is used to bring background jobs to the foreground and continue their execution in an actively interacting mode with the user.

*Usage:* fg [job_spec], where job_spec can be a job ID or % followed by its number.

- Якою командою можна переглянути інформацію про запущені в системи фонові процеси та задачі?

The command to view information about background processes and tasks running in the system is ```jobs```.

- Як призупинити фоновий процес, як його потім відновити та при необхідності перезапусти?

1) To suspend: Ctrl + Z;

2) To resume: ```fg [job number]```;

3) To restart: ```bg [job number]```.

3. Запустіть термінал, та в командному рядку виконайте наступні дії для ознайомлення з роботою з процесами:

- запустіть команду top, проаналізуйте отриманий в цій команді результат та охарактеризуйте найбільш активні процеси у системі;

![Command "top"](./images/top.png)

<h3 align="center"><b>Command "top"</b></h3>

<br/>

<br/>

**Shift + P:** sorting mode by the level of CPU resource consumption;

**Shift + M:** sorting by memory;

**Shift + T:** sorting by process execution time;

**Shift + N:** sorting processes by number;

- призупинити виконання команди top (треба використати комбінацію клавіш);

Use combination: **Ctrl + Z**

- вивести інформацію про процеси за допомогою команди ps;

![Command "ps"](./images/ps.png)

<h3 align="center"><b>Command "ps"</b></h3>

<br/>

<br/>

- наведіть 5 прикладів з використанням різних параметрів команди ps (наприклад, вивести тільки системні процеси, вивести процеси конкретного користувача, вивести дерево процесів тощо).
Опишіть, що саме роблять обрані Вами параметри

```pstree``` - displays the process tree

![Command "pstree"](./images/pstree2.png)

<h3 align="center"><b>Command "pstree"</b></h3>

<br/>

<br/>

```ps aux``` - displays information about all processes running on the system

![Command "ps aux"](./images/ps_aux.png)

<h3 align="center"><b>Command "ps aux"</b></h3>

<br/>

<br/>

``` ps r ``` - display processes to the "running" state

![Command "ps r"](./images/ps_r.png)

<h3 align="center"><b>Command "ps r"</b></h3>

<br/>

<br/>

```ps T``` - display information about processes that are in the "stopped" state

![Command "ps T"](./images/ps_t.png)

<h3 align="center"><b>Command "ps T"</b></h3>

<br/>

<br/>

```ps x``` - displays all processes, even those that are not associated with the terminal

![Command "ps x"](./images/ps_x.png)

<h3 align="center"><b>Command "ps x"</b></h3>

<br/>

<br/>

- передивіться чи є у Вас запущені фонові процеси, які саме?

```sleep 200 &```

:arrow_down:

```jobs```

![Command "jobs"](./images/sleep_jobs.png)

<h3 align="center"><b>Command "jobs"</b></h3>

<br/>

<br/>

***+*** it`s a backgroung procces

***&*** it`s a running into background procces

- відновити виконання призупиненого фонового процесу спочатку у позиції “на передньому плані” (foreground), потім ще раз його призупинити, а потім відновити його виконання у позиції “на задньому плані” (background)

![From background to foreground](./images/background_into_foreground.png)

<h3 align="center"><b>From background to foreground</b></h3>

<br/>

<br/>

- завершити роботу даного фонового процесу.

Use **Ctrl + C**

![Finish the procces](./images/kill_the_procces.png)

<h3 align="center"><b>Finish the procces</b></h3>

<br/>

<br/>

**Відповіді на контрольні запитання:**
1. What is the purpose of the /proc directory in Linux systems and what type of information does it store?

The /proc directory in Linux systems serves as an interface to kernel data structures and stores various system information such as process information, hardware configuration, and system settings.

2. How can you dynamically determine which among three processes is currently utilizing the most memory in Linux? Additionally, what percentage of memory does it consume from the total available memory?

To dynamically determine which process is using the most memory among three processes, you can use commands like 'top' or 'ps' to monitor memory usage. Calculate the memory usage of each process and compare them. The percentage of memory consumption can be calculated by dividing the memory usage of the process by the total available memory and then multiplying by 100.

3. How can you obtain the hierarchy of parent processes in Linux systems? Provide a description of its structure.

You can obtain the hierarchy of parent processes in Linux systems using the 'pstree' command. This command displays processes in a tree format, illustrating their parent-child relationships. The structure shows parent processes at the top with their child processes listed beneath them, forming a hierarchical tree.

4. What are the differences between the 'top' command and 'ps' command in Linux?

The 'top' command provides a dynamic real-time view of system processes, continuously updating information such as CPU and memory usage. On the other hand, the 'ps' command provides a snapshot of current processes running on the system at the moment the command is executed.

5. In comparison to 'top', what additional features does 'htop' offer?

'htop' offers additional features such as a more user-friendly interface, color-coded display, horizontal and vertical scrolling, and the ability to navigate and manipulate processes more efficiently, including the option to kill processes directly from the interface.

6. What components does your mobile OS include for monitoring running processes?

Components of my mobile OS for monitoring running processes may include a built-in task manager application, system monitor widgets, and settings options to view and manage processes.

7. Does your mobile OS support terminal management of processes? If so, how?

Yes, my mobile OS supports terminal management of processes. Users can utilize terminal applications to view processes, send signals, and manage them effectively using commands such as 'ps', 'kill', and 'top'.

8. Is it possible to install third-party applications on your Samsung mobile phone for organizing management and monitoring of processes? If yes, briefly describe them.

Yes, it is possible to install third-party applications on my Samsung mobile phone for managing and monitoring processes. These applications, such as Task Manager for Android or System Monitor, offer features like detailed process information, resource usage monitoring, and options to terminate or manage processes efficiently.

**Conclusion**: In the course of the laboratory work, we studied new commands, their functionality, and learned how to work with them in the Linux terminal.

<h2> The brief dictionary of basic English terms regarding the purpose of commands and their parameters. </h2>

**-A**    Shows all processes 

**-N**    Shows the opposite of the specified parameters 

**-a**    Shows all processes except session headers and processes without a terminal 

**-d**    Shows all processes except session headers 

**-e**    Shows all processes 

**-C cmdlist**     Shows processes contained in the list cmdlist 

**-G grplist**     Shows processes with a group ID listed in grplist 

**-U userlist**    Shows processes owned by a userid listed in userlist 

**-g grplist** Shows processes by session or by groupid contained in grplist 

**-p pidlist** Shows processes with PIDs in the list pidlist 

**-s sesslist** Shows processes with session ID in the list sesslist 

**-t ttylist** Shows processes with terminal ID in the list ttylist 

**-u userlist** Shows processes by effective userid in the list userlist

 **-F**         Uses extra full output 

**-O** format Displays specific columns in the list format, along with the default columns 

**-M** Displays security information about the process 

**-c** Shows additional scheduler information about the process 

**-f** Displays a full format listing Shows job information 

**-l** Displays a long listing

**-o** format Displays only specific columns listed in format 

**-y** Prevents display of process flags 

**-Z** Displays the security context information

**-H** Displays processes in a hierarchical format (showing parent processes) 

**-n namelist**   Defines the values to display in the WCHAN column 

**-w**   Uses wide output format, for unlimited width displays 

**-L**  Shows process threads 

**-V**  Displays the version of ps

**PProcess:** An executing unit of software within an operating system.

Процес: Виконавча одиниця програмного забезпечення в операційній системі.

**ps Command:** A command-line utility in Unix and Unix-like operating systems that provides information about active processes. Команда ps: Командна утиліта в операційних системах Unix та подібних Unix, яка надає інформацію про активні процеси.

**ps Command Parameters:**

Параметри команди ps:

**Unix-style parameters:** Parameters preceded by a dash.

Параметри у стилі Unix: Параметри, передбачені дефісом.

**BSD-style parameters:** Parameters not preceded by a dash.

Параметри у стилі BSD: Параметри, які не передуються дефісом.

GNU long parameters: Parameters preceded by a double dash.

Параметри у стилі GNU: Параметри, передбачені подвійним дефісом.

**Real-time Process Monitoring:** Displaying information about processes in an operating system in real-time.

Моніторинг процесів у реальному часі: Відображення інформації про процеси в операційній системі у реальному часі.

**top Command:** A command-line utility that displays information about processes in an operating system in real-time.

Команда top: Командна утиліта, що відображає інформацію про процеси в операційній системі у реальному часі.

**Linux Process Signals:** Predefined messages that processes recognize and may act upon, determining their behavior.

Сигнали процесів Linux: Передбачені повідомлення, які процеси розпізнають та можуть виконати дії, визначаючи їх поведінку.

**kill Command:** A command-line utility that allows sending signals to processes based on their process IDs (PID).

Команда kill: Командна утиліта, яка дозволяє надсилати сигнали процесам на основі їх ідентифікаторів процесу (PID)

**killall Command:** A command-line utility that allows stopping processes by their names instead of PIDs.

Команда killall: Командна утиліта, яка дозволяє припинити роботу процесів за їх назвами замість PID.

**The -e parameter** shows all the processes running on the system. Параметр -e показує всі процеси, які запущені в системі.

**The -f parameter** expands the output to include additional columns of information. 

Параметр -f розширює вивід, додавши додаткові стовпці інформації.

•	**UID**: The user responsible for launching the process. 

•	Користувач, відповідальний за запуск процесу.

•	**PID**: The process ID of the process. Ідентифікатор процесу (PID) процесу. 

•	**PPID** The PID of the parent process (if a process is started by another process). PID батьківського процесу (якщо процес запущений іншим процесом).

•	**C** Processor utilization over the lifetime of the process. Використання процесора протягом життєвого циклу процесу.

•	**STIME** The system time when the process started. Час системи, коли процес почав виконуватися.

•	**TTY** The terminal device from which the process was launched. Термінальний пристрій, з якого було запущено процес.

•	**TIME** The cumulative CPU time required to run the process. Кумулятивний час процесора, необхідний для виконання процесу.

•	**CMD** The name of the program that was started. Назва програми, яка була запущена.

 **-l parameter,** parameter which produces a long format output. створює вивід у довгому формат

•	**F**: System flags assigned to the process by the kernel. Прапорці системи, призначені для процесу ядром

•	**S** The state of the process (D = running on processor; S = sleeping; R = runnable, waiting to run; Z = zombie, process terminated but parent not available; T = process stopped). Стан процесу (O = запущено на процесорі; S = сплячий; R = готовий до запуску; Z = зомбі, процес завершився, але батьківський процес не відповідає; T = процес зупинено).
	
•	**PRI** The priority of the process (higher numbers mean lower priority). Пріоритет процесу (вищі числа означають менший пріоритет).
	
•	**NI** The nice value, which is used for determining priorities. Приємне значення, яке використовується для визначення пріоритетів

•	**ADDR** The memory address of the process. Адреса пам'яті процесу.

•	**SZ** Approximate amount of swap space required if the process was swapped out. Приблизна кількість простору обміну, необхідного, якщо процес був замінений.

•	**WCHAN** Address of the kernel function where the process is sleeping. Адреса функції ядра, де спить процес

**the top command** output provides a detailed list of the currently running processes, along with various information columns, which are similar to those in the ps command output/ надає докладний список поточних запущених процесів, разом з різними колонками інформації, що схожа на вивід команди ps

•	**PID** Process ID of the process. Ідентифікатор процесу

•	**USER** User name of the owner of the process. Ім'я користувача, власника процесу.

•	**PR** Priority of the process. Пріоритет процесу.

•	**NI** Nice value of the process. Значення "приємності" (nice value) процесу.

•	**VIRT** Total amount of virtual memory used by the process. Загальний обсяг віртуальної пам'яті, яку використовує процес.

•	**RES**: Amount of physical memory the process is using. Кількість фізичної пам'яті, яку використовує процес.

•	**SHR** Amount of memory the process is sharing with other processes. Кількість пам'яті, яку процес спільно використовує з іншими процесами.

•	**S** Process status (D = interruptible sleep, R = running, S = sleeping, T = traced or stopped, or Z = zombie). Статус процесу (D = переривний сон, R = виконується, S = спить, T = відстежується або зупинено, або Z = зомбі).

•	**%CPU** Share of CPU time that the process is using. Доля часу ЦП, який використовує процес.

•	**%MEM** Share of available physical memory the process is using. Доля доступної фізичної пам'яті, яку використовує процес.

•	**TIME+**: Total CPU time the process has used since starting. Загальний час ЦП, який процес використовував з моменту запуску.

•	**COMMAND** Command line name of the process (program started). Ім'я командного рядка процесу (програма, що була запущена)

**A process signal**  a predefined message that processes recognize and may choose to ignore or act on.
Заздалегідь визначене повідомлення, яке процеси впізнають і можуть вибрати, чи ігнорувати, чи діяти на нього.

1 HUP Hangs up Завершує роботу.

2 INT Interrupts Інтерферує.

3 QUIT Stops running Припиняє роботу.

9 KILL Unconditionally terminates Безумовно завершує роботу.

11 SEGV Produces segment violation Викликає порушення сегменту.

15 TERM Terminates if possible Завершує роботу, якщо можливо.

17 STOP Stops unconditionally, but doesn't terminate Безумовно припиняє роботу, але не завершує її.

18 TSTP Stops or pauses, but continues to run in background Призупиняє або паузить роботу, але продовжує виконання у фоновому режимі.

19 CONT Resumes execution after STOP or TSTP. Продовжує виконання після призупинки або паузи.
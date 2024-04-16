<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 8</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Збереження службових даних системи та її мережева конфігурація” <br/></h2>



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
|  Processes (instances of programs running on a computer, including programs currently running and waiting to execute)  | Процеси (екземпляри програм, які виконуються на комп'ютері, включаючи програми, які запущені в даний момент і чекають на виконання) |
| Memory (physical or virtual space used to store data or programs on a computer) | Пам'ять (фізичний або віртуальний простір, який використовується для зберігання даних або програм на комп'ютері) |
| Filesystem Hierarchy Standard (standard that defines the structure of directories and files in Unix-like operating systems) | Стандарт ієрархії файлової системи (стандарт, який визначає структуру каталогів та файлів в операційній системі Unix або подібних) |
| NAT (Network Address Translation) - network address translation (technology that allows using a single external IP address for all devices in a local network) | NAT (Network Address Translation) - переклад адрес мережі (технологія, яка дозволяє використовувати один зовнішній IP-адрес для всіх пристроїв у локальній мережі) |
| Porting (process of adapting software to work on different hardware or software platforms) | Портинг (процес адаптації програмного забезпечення для роботи на різних апаратних або програмних платформах) |
| ifconfig (command in Unix and Unix-like operating systems used to configure network interfaces) | ifconfig (команда в Unix і Unix-подібних операційних системах, яка використовується для налаштування мережевих інтерфейсів) |
| ip (command in Unix and Unix-like operating systems that provides information about network interfaces and network configuration) | ip (команда в Unix і Unix-подібних операційних системах, яка надає інформацію про мережеві інтерфейси та конфігурацію мережі) |
| route (command in Unix and Unix-like operating systems used to display and edit the network routing table) | route (команда в Unix і Unix-подібних операційних системах, яка використовується для відображення та редагування таблиці маршрутизації мережі) |
| ping (command in Unix and Unix-like operating systems used to check the availability and measure the response time of network devices) | ping (команда в Unix і Unix-подібних операційних системах, яка використовується для перевірки доступності і вимірювання часу відповіді від мережевих пристроїв) |
| netstat (command in Unix and Unix-like operating systems that provides information about network connections, routes, interfaces, etc.) | netstat (команда в Unix і Unix-подібних операційних системах, яка надає інформацію про мережеві з'єднання, маршрути, інтерфейси тощо) |
| ss (command in Unix and Unix-like operating systems that provides information about socket status and supports all major packet and socket types) | ss (команда в Unix і Unix-подібних операційних системах, яка надає інформацію про статус сокетів та підтримує всі основні типи пакетів і сокетів) |
| dig (command in Unix and Unix-like operating systems used to perform DNS queries and retrieve information about domain names) | dig (команда в Unix і Unix-подібних операційних системах, яка використовується для виконання DNS-запитів та отримання інформації про доменне ім'я) |
| host (command in Unix and Unix-like operating systems that associates domain names with IP addresses and vice versa) | host (command in Unix and Unix-like operating systems that associates domain names with IP addresses and vice versa) |
| ssh (command in Unix and Unix-like operating systems that allows connecting to another computer over the network, logging in, and performing tasks on the remote machine) | ssh (команда в Unix і Unix-подібних операційних системах, яка дозволяє підключатися до іншого комп'ютера по мережі, виконувати вхід і виконувати завдання на віддаленому комп'ютері) |

*Готували матеріал студенти Войтенко В. та Селезень Є.*

4. На базі розглянутого матеріалу дайте відповіді на наступні питання:

4.1 Розкрийте поняття “псевдо файлової системи”, для чого воно потрібно системі?



4.2 Чому користувачі не так часто звертаються на пряму до каталогу /proc, яким чином з нього можна отримати інформацію?



4.3 *Яке призначення файлів /proc/cmdline, /proc/meminfo та /proc/modules?



4.4 *Яке призначення команди free?



4.5 *Для чого потрібні лог-файли, наведіть приклади їх застосування?



4.6 **Яке призначення файлу /var/log/dmesg?



4.7 **Для чого розроблено FHS?



4.8 **Які основні команди є у Linux для перегляду та конфігурації мережі



*Готував матеріал студент Войтенко В.*

**Хід роботи:**

2. Опрацюйте всі приклади команд, що представлені у лабораторних роботах курсу NDG Linux Essentials - Lab 13: Where Data is Stored та Lab 14: Network Configuration. Створіть таблицю для опису цих команд

|                        Назва команди                       |                                Її призначення та функціональність                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| su | Змінюємо поточного користувача на root |
| ls /proc | Переглядаємо вміст системного каталогу /proc (для цього потрібні права доступу root) |
| ls /proc/cmdline | Перегляд інформації, що передається ядру під час завантаження |
| ls /proc/ meminfo | Перегляд інформації про використання пам'яті ядра |
| ls /proc/modules | Перегляд списку модулів, завантажених у ядро |
| pstree | Відображення процесів у вигляді “дерева” |
| ps | Показує лише запущенні процеси |
| top | Відображення динамічного екранного інтерфейсу, який регулярно оновлюватиме результати роботи запущених процесів |
| free | Перегляд знімку пам’яті |
| cat | Перегляд файлів журналів |
| journalctl | Перегляд файлів журналів |
| file | Перегляд двійкових файлів журналу |
| dmesg | Перегляд повідомлень ядра |
| dpkg -L packagename | Перегляд списку файлів програм (Debian) |
| rpm -ql packagename | Перегляд списку файлів програм (Red Hat) |
| host example.com | Перегляд IP-адреси на DNS-сервері |
| ifconfig | Відображення інформації про конфігурацію мережі |
| ip | Відображає розширену функціональність і набір опцій |
| route | Переглядає таблицю, яка описує, куди надсилаються мережеві пакунки |
| ping | Визначає чи є інша машина “доступною” |
| netstat -r | Відображення інформації про мережеві з'єднання, а також для відображення таблиці маршрутизації, подібно до команди route |
| netstat -tln | Показ відкритих портів |
| ss | Показує статистики сокетів і підтримує всі основні типи пакетів і сокетів. Використовується для перегляду з'єднань, встановлених на даний момент між локальною та віддаленими машинами, а також статистики цих з'єднань |
| dig | Виконує запити до DNS-сервера, щоб визначити, чи доступна на ньому необхідна інформація |
| host | Працює з DNS, щоб зв'язати ім'я хоста з IP-адресою |
| ssh | Дозволяє вам підключитися до іншого комп'ютера через мережу, увійти в систему і виконувати завдання на віддаленому комп'ютері |
| exit | Повернення на локальний комп'ютер |
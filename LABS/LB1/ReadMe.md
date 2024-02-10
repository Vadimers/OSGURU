<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">“ЗВІТ ПО ВИКОНАННЮ”<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 1</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">“Тема: “Знайомство з робочим середовищем ”<br/>
віртуальних машин та особливостями <br/>операційної системи Linux”</h2>



<div style="text-align: right;">
    <font size="4"><b>Виконали студенти <br/> групи РПЗ-13а <br/> Команда OSGURU: <br/> Войтенко В.С., <br/>  Селезень Є.С. <br/> Перевірив викладач <br/> Сушанова В.С. </b></font>
</div>

<br/>
<br/>
<br/>

<h2 align="center">Київ 2024</h2>

<hr>

**Мета роботи:**
1. Знайомство з гіпервізорами різного типу, віртуалізацією при роботі з операційними системами.
2. Знайомство з основними видами сучасних ОС, короткий огляд їх можливостей.
   
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
TO THE CLASSIFICATION OF VIRTUAL ENVIRONMENTS<b><h2/>

|                       Термін англійською                   |                                    Термін українською                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Operating System (software managing hardware and software) | Операційна система (програмне забезпечення для управління апаратними та програмними компонентами)|
| Host Operating System (the main OS that controls and manages virtual machines, allowing guest operating systems to run on them)| Головна операційна система (головна ОС, яка контролює та управляє віртуальними машинами, де можуть працювати гостьові операційні системи)|
| Guest Operating System (OS running on a virtual machine created and managed by the host operating system) | Гостьова операційна система (ОС, що працює на віртуальній машині, яка створена та управляється головною операційною системою) |
| Virtualization (a technology that allows creating virtual versions of hardware, operating systems, data storage, and other resources) | Віртуалізація (технологія, яка дозволяє створювати віртуальні версії апаратного забезпечення, операційних систем, сховищ даних та інших ресурсів) |
| Virtual Machine (VM) (a software-based emulation of a physical computer, capable of running an operating system and applications) | Віртуальна машина (програмне забезпечення, що емулює фізичний комп'ютер і може запускати операційну систему та програми)|
| Virtualization Host (the physical machine or server on which virtual machines are created and managed) | Хост для віртуалізації: (фізична машина або сервер, на якому створюються та керуються віртуальні машини) |
| Hypervisor (is software or hardware that enables the creation and management of virtual machines on a physical host, also known as a Virtual Machine Monitor (VMM)) | Гіпервізор: (це програмне або апаратне забезпечення, яке дозволяє створювати віртуальні машини та керувати ними на фізичному хості, також відомий як монітор віртуальної машини (VMM)) |
| Type 1 Hypervisor (a hypervisor that runs directly on the hardware, without the need for an underlying operating system. Also known as a bare-metal hypervisor) | Гіпервізор 1 типу (працює безпосередньо на апаратному забезпеченні, без необхідності в операційній системі на нижньому рівні. Також відомий як гіпервізор без операційної системи) |
| Type 2 Hypervisor (a hypervisor that runs on top of an existing operating system and relies on it for certain functions. Also known as a hosted hypervisor) | Гіпервізор 2 типу (працює на вже існуючій операційній системі та залежить від неї для деяких функцій. Також відомий як гіпервізор на основі операційної системи) |
| Shared Hosting | Спільний хостинг |
| Dedicated Hosting | Виділений хостинг |
| Kernel Module  (software component aiding virtualization tasks) | Ядро модуля (програмний компонент, доданий до ядра операційної системи для допомоги в завданнях віртуалізації) |
| Kernel-based Virtual Machine (KVM) | Віртуальна машина на основі ядра |
| Java Virtual Machine (JVM A virtual machine that executes Java bytecode, allowing Java programs to run on any device with a JVM | Віртуальна машина Java (JVM) (віртуальна машина, яка виконує байт-код Java, дозволяючи запускати Java-програми на будь-якому пристрої з JVM) |
| Open Source  (software for which the source code is freely available, allowing users to view, modify, and distribute it)  | Відкрите ПЗ (програмне забезпечення, для якого вільно доступний вихідний код, що дозволяє користувачам переглядати, змінювати та поширювати його) |
| Linux Kernel (core component of the Linux operating system responsible for managing hardware resources) | Ядро Linux (основна складова операційної системи Linux, відповідальна за управління апаратними ресурсами) |
| GNU/Linux  (the combination of the Linux kernel and the GNU software, forming a complete operating system) | GNU/Linux (комбінація ядра Linux та програмного забезпечення GNU, що утворює повну операційну систему) |
| Machine Simulator (a virtualization approach that involves translating and caching code blocks to enhance performance) | Машинний симулятор (підхід віртуалізації, який включає переклад та кешування коду для підвищення продуктивності) |
| Binary Translation (a technique used to improve the performance of virtual machines by translating blocks of code on-the-fly) | Бінарний переклад (техніка, що використовується для покращення продуктивності віртуальних машин за допомогою перекладу коду на льоту) |
| Distribution  (a packaged collection of the Linux kernel, GNU tools, and additional software, often tailored for specific purposes) | Дистрибутив (упакований набір для конкретних завдань) |
| Command Line Interface (CLI) (a text-based interface for interacting with a computer through typed commands) | Інтерфейс командного рядка (CLI) (текстовий інтерфейс для взаємодії з комп'ютером за допомогою введених команд) |
| Graphical User Interface (GUI) (an interface that uses graphical elements, like windows and icons, for user interaction) | Графічний інтерфейс користувача (GUI) (інтерфейс, що використовує графічні елементи, такі як вікна та піктограми, для взаємодії з користувачем) |
| Multi-tasking (The ability of an operating system to schedule and run multiple tasks simultaneously). | Мультизадачність (здатність операційної системи розкладати та виконувати одночасно кілька завдань) |
| Proprietary Code (software code that is owned and controlled by a specific entity, restricting access and modification) | Пропрієтарний код (код програмного забезпечення, який належить та контролюється конкретною компанією, обмежуючи доступ та зміни) |



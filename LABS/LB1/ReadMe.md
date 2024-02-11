<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 1</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Знайомство з робочим середовищем <br/>
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
TO THE CLASSIFICATION OF VIRTUAL ENVIRONMENTS</b></h2>

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

<br/>

2. Прочитавши матеріал з коротких теоретичних відомостей дайте відповіді на наступні питання:

*Готував матеріал студент Войтенко В.*

<br/>

2.1. Охарактеризуйте поняття «гіпервізор». Які бувають їх типи?

A **hypervisor** is software or hardware that allows multiple virtual machines to be created simultaneously and in parallel on a single physical computer. Each virtual machine has its own operating system. The hypervisor is responsible for distributing physical resources (such as CPU, memory, network) among these virtual machines and ensures mutual isolation between them.
There are two main types of hypervisors: 
<br/>
**Type 1 (bare-metal):** These hypervisors are installed directly on the physical hardware. They work directly at the hardware level and have direct access to the computer's resources. This provides better performance and efficiency compared to Type 2. Examples: VMware ESXi, Microsoft Hyper-V.
<br/>
**Type 2 (hosted):** These hypervisors are installed on an operating system that is already installed on the physical hardware. They work at the operating system level and use it to access hardware resources. This may reduce performance compared to Type 1, but provides more flexibility. Examples: VMware Workstation, Oracle VirtualBox.

2.2. Перерахуйте основні компоненти та можливості гіпервізорів відповідно до свого варіанту (порядковий номер по журналу)

**Xen** is an open-source hypervisor that enables the virtualization of various operating systems on hardware. 
<br/>
<u>The main components of the Xen hypervisor are:</u>

**1. Domain 0 (Dom0):** Dom0 is a special domain that boots first and has direct access to the hardware. Dom0 is responsible for managing the resources of the Xen hypervisor and other guest domains.<br/>
**2. Guest Domains (DomU):** DomU refers to guest domains that run on the Xen hypervisor and can be various operating systems. Each DomU is isolated from others and has its own memory areas and virtualized devices.

<u>The main capabilities of the Xen hypervisor are:</u>

**1. Paravirtualization:** Xen utilizes paravirtualization technology, allowing virtual machines to interact directly with the hypervisor and hardware.<br/>
**2. Support for different architectures:** Xen supports virtualization on different processor architectures such as x86, x86_64, ARM, and others.<br/>
**3. Live Migration:** Xen supports the ability to migrate guest domains from one physical server to another without service interruption for users.<br/>
**4. Resource Isolation:** Ensures that the resources of one virtual machine do not impact others, providing isolation and security.<br/>
**5. Support for hardware virtualization technologies:** Xen can utilize hardware extensions such as Intel VT-x and AMD-V to enhance virtualization performance.<br/>
**6. Hot Swap:** Support for hot swapping hardware components, enabling replacement without interrupting virtual machine operation.<br/>
**7. Fault-Tolerant Systems Support:** Capability to create highly available and fault-tolerant virtual machines using clusters and other mechanisms.<br/>
**8. Multilevel Mandatory Access Control (MAC):** Xen has an advanced access control system that allows setting access rights to system resources for each guest.<br/>
**9. Dynamic resource allocation:** Xen supports dynamic allocation of resources to guest domains, such as CPU time, memory size, and network resources.<br/>

Xen meets high security and reliability requirements, as evidenced by its usage by serious companies like Amazon, BitDefender, and others.

2. Після перегляду відео дайте відповіді на наступні питання.
   
2.1	Перерахуйте етапи для розгортання операційної системи на базі віртуальної машини VirtualBox.

- Download the ISO image or other image of the operating system you want to install.
- Create a new virtual machine
- Select the size of memory, the number of processors, and the virtual hard disk file
- Set up a network connection
- Connect the image of the virtual machine we need
- Start the system installation

2.2	Чи є якісь апаратні обмеження при встановленні 32- та 64-бітних ОС?

- The processor must support the appropriate architecture for 64-bit operating systems
- The processor must support virtualization
- Sufficient disk space
- Sufficient amount of RAM
- Some systems may require enabling virtualization in the BIOS or UEFI

2.3	Які основні етапи при встановленні CentOS в текстовому режимі?

2.4	Яким чином можна до установити графічні оболонки Gnome та KDE на CentOS, якщо вона вже встановлена в текстовому режимі (вкажіть необхідні команди та пакети)? 

2.5	Дайте коротку характеристику графічних інтерфейсів, що використовуються в різних дистрибутивах Linux  відповідно до свого варіанту (порядковий номер по журналу), табл.2.

The Xfce and Fvwm graphical interfaces used in various Linux distributions.
Xfce is a lightweight desktop environment for Unix-like operating systems. 
The advantage lies in its speed and low resource usage, while also being attractive and easy to use.
<br/>
Xfce embodies the traditional UNIX philosophy of modularity and reusability.
 It consists of a series of interrelated components that can be optionally used in other projects. Among these components are:
 <br/>
- Window manager
- Application launcher panel
- Display manager
- Session and power management manager
- File manager - Thunar
- Web browser - Midori
- Environment settings configuration system. They are packaged separately, and users can choose from available packages to create their own desktop environment.
<br/>
Another priority for Xfce is compliance with standards, especially those defined by freedesktop.org. Xfce can be installed on almost all UNIX platforms: Linux, NetBSD, FreeBSD, Solaris, Cygwin, MacOS X, x86, PowerPC, Sparc, and Alpha.

**Fvwm** (F Virtual Window Manager) is a lightweight, highly customizable graphical interface for various Linux distributions. Brief overview of Fvwm:

- Highly Customizable: Fvwm empowers users to customize their desktop environment extensively, including window decorations, placement policies, mouse and keyboard bindings, and more.
- Lightweight: Designed to be efficient, Fvwm consumes minimal system resources compared to other window managers, making it suitable for older hardware or systems with limited resources.
- Modular Architecture: Fvwm adheres to the Unix philosophy of modular design, consisting of independent modules that users can combine and configure to create a personalized desktop environment.
- Rich Feature Set: Despite its lightweight nature, Fvwm offers virtual desktops, support for multiple window managers, and extensive keyboard shortcuts.
- Highly Extensible: Fvwm supports extensions and customization through scripting languages like Perl and FvwmScript, enabling users to enhance the functionality of their desktop environment.
- Compatibility: Fvwm is compatible with various Unix-like operating systems, including Linux, FreeBSD, and OpenBSD.
In summary, Fvwm provides users with a highly customizable and lightweight window manager that offers extensive flexibility and functionality while conserving system resources.
<br/>
In summary, Fvwm provides users with a highly customizable and lightweight window manager that offers extensive flexibility and functionality while conserving system resources.

**Відповіді на контрольні запитання**
<br/>
***Готував матеріал студент***
1. Порівняйте гіпервізори типу 1 та типу 2, яка між ними відмінність та сфера їх застосування?
<br/>
Type 1 and Type 2 hypervisors to perform core virtualization functions,  with varying levels of performance and efficiency.

| **Type 1 Hypervisors (Bare-metal Hypervisors)** | **Type 2 Hypervisors (Hosted Hypervisors)** |
|---------------------------------------------|-----------------------------------------|
| run directly on the hardware of the physical server | run within the host operating system environment (e.g., Windows, Linux, or macOS) |
| have direct access to the hardware, which allows for better virtualization performance and efficiency | are installed as additional software on top of the host operating system and use its API to interact with the hardware |
| are typically used in server environments where high reliability, performance, and scalability are required | are commonly used in desktop or development environments for testing, development, and experimentation with virtualized environments |

Type 1 hypervisors are employed in enterprise settings to manage a large number of virtual machines and process significant resources. Type 2 hypervisors used to create isolated environments for different operating systems and software environments, primarily in smaller or development environments.

2. Розкрийте поняття «GNU GPL», яка його основна концепція?

**GNU GPL (General Public License)** is one of the most popular licenses for free software, created by Richard Stallman for the GNU project. The goal of the GNU GPL is to grant users the rights to copy, modify, and distribute the program, and ensure that users of all derived works will also receive these rights. The main principles of the GNU GPL:
- Freedom to Use: Users have the right to freely use the software for any purpose without restrictions.
- Freedom to Modify: Users can make changes to the software code, correct errors, and adapt the software to their needs.
- Freedom to Distribute: Users can distribute modified versions of the software, as well as develop and distribute their own extensions.
- License Terms Remain Unchanged: The licensing terms of the GNU GPL remain unchanged for all users who receive the software under this license.
- Preservation of Open Source Code: All modified versions of the software distributed under the GNU GPL license must also be available in an open-source format.

3. В чому суть програмного забезпечення з відкритим кодом?


4. Що таке дистрибутив?


5. Які задачі системного адміністрування можна реалізувати на базі ОС Linux?
- Manage users and groups
- Support for local area networks and web applications
- File system management
- Security management
- Virtualization
- Automation of tasks

6. Як пов'язані між собою ОС Android та Linux? 
-  The Android kernel uses the Linux kernel

7. Основні можливості та сфера використання Embedded Linux?


8. Яким чином можна змінити типу завантаження Linux: в текстовому режимі (3 рівень) або графічному (рівень 5)? Чим відрізняються режими CLI та GUI?

**Висновок**
<br/>
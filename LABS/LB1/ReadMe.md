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

*Готував матеріал студент Войтенко В. та Селезень Є.*

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


<u>The main components of the VirtualBox hypervisor are:</u>

**1. Hypervisor Core:** At the core of VirtualBox is the hypervisor itself, which directly interacts with the host hardware to manage virtualization. It is responsible for creating, running, and controlling virtual machines.<br/>
**2. Virtualization Engine:** This component implements the low-level functionality required for virtualization, including memory and CPU management, device emulation, and instruction execution.<br/>
**3. VM Monitor (VMM):** The VM Monitor is responsible for monitoring and controlling the execution of virtual machines. It intercepts privileged instructions from guest operating systems and manages their execution on the host hardware.<br/>
**4. Hardware Abstraction Layer (HAL):** The HAL abstracts the physical hardware resources of the host system, presenting them to guest operating systems as virtual hardware components. This allows multiple VMs to run simultaneously on the same physical machine without interference.<br/>
**5. Device Emulation:** VirtualBox includes device emulation components that emulate virtual hardware devices, such as virtual CPUs, memory, disk controllers, network interfaces, and graphics adapters. These virtual devices are presented to guest operating systems as if they were real hardware.<br/>
**6. Virtual Machine Manager (VMMgr):** This component provides a management interface for controlling virtual machines, managing their configuration, starting and stopping them, and monitoring their performance.<br/>
**7. Frontend Interface:** VirtualBox provides user-friendly frontend interfaces, including a graphical user interface (GUI) and a command-line interface (CLI), for configuring and managing virtual machines.<br/>
**8. Service Interfaces:** VirtualBox exposes service interfaces for interacting with the hypervisor and virtual machines programmatically. These interfaces enable automation and integration with other systems and tools.<br/>

<u>The main capabilities of the VirtualBox hypervisor are:</u>

**1. Virtual machines (VMs):** VirtualBox allows you to create and run virtual machines of different operating systems such as Windows, Linux, macOS and others. Each virtual machine runs as a separate virtual environment with its own processor, memory, disk, and network settings.<br/>
**2. Guest support:** VirtualBox provides support for a large number of guest operating systems, including various versions of Windows, Linux, macOS, FreeBSD, and more. This allows users to run a variety of OSes on their primary computer.<br/>
**3. Sharing resources:** VirtualBox allows you to configure file and folder sharing between the host system and the guest OS.<br/>
**4. System resources:** The user can configure the amount of available system resources (such as CPU, RAM, disk) for each virtual machine.<br/>
**5. Networking:** VirtualBox provides various networking options for virtual machines, such as NAT, bridge, internal network, etc. This allows you to customize communication between virtual machines and external networks.<br/>
**6. Snapshots:** VirtualBox allows you to create snapshots of virtual machines, which allows you to save the state of the system at a certain point in time and return to it when necessary.<br/>
**7. Virtualization of hardware devices:** VirtualBox supports the virtualization of hardware devices such as USB devices, network adapters, sound devices, etc., allowing them to be used in virtual machines.<br/>
**8. Compatibility and advanced features:** VirtualBox has a high level of compatibility with different versions of operating systems and software. There are also advanced features that allow for USB 2.0 and 3.0 support, GPU virtualization, and more.<br/>

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

Install VirtualBox, create a virtual machine, add carrier, install CentOS.

2.4	Яким чином можна до установити графічні оболонки Gnome та KDE на CentOS, якщо вона вже встановлена в текстовому режимі (вкажіть необхідні команди та пакети)? 

**1. Install the necessary graphical desktop packages.**

Package for GNOME: sudo yum groupinstall "GNOME Desktop"
Package for KDE: sudo yum groupinstall "KDE Plasma Workspaces"

**2. Install the login manager:**
After installing the graphical desktop, you need to install a login manager to handle the login process. For GNOME, GDM (GNOME Display Manager) is used, and for KDE, you can install SDDM (Simple Desktop Display Manager) or KDM (KDE Display Manager).<br/>
For GNOME:
sudo systemctl enable gdm
sudo systemctl set-default graphical.target

For KDE (SDDM):
sudo systemctl enable sddm
sudo systemctl set-default graphical.target

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

**KDE (K Desktop Environment):**
KDE is one of the most popular and feature-rich graphical interfaces for Linux. It boasts a wide range of features and tools, making it highly customizable and extensible. KDE has a modern and stylish design, providing a high level of convenience for users. Its components, such as the taskbar, window manager, and system settings, are tightly integrated and work well together. KDE is commonly used in Linux distributions such as Kubuntu, openSUSE KDE, Fedora KDE Spin, and others.

**Fluxbox:**
Fluxbox is a lightweight and fast graphical interface for Linux. It has a minimalist design and a simplified interface, making it ideal for older or resource-constrained systems. Fluxbox lacks many built-in features, but it can be extended using various modules and scripts. It allows users to fully customize their working environment by editing configuration files. Fluxbox is excellent for users seeking a simple and efficient graphical interface without unnecessary resource overhead. It is often used in lightweight Linux distributions such as CrunchBang, Bodhi Linux, or as an alternative option in more general-purpose distributions.

**Відповіді на контрольні запитання**
<br/>
***Готував матеріал студент Войтенко В.***
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

***Готував матеріал студент Селезень Є.***

3. В чому суть програмного забезпечення з відкритим кодом?

This is software whose source code is available for viewing, use, modification, and distribution. Open source fosters collaboration and innovation because anyone can contribute to the development and improvement of the program.

4. Що таке дистрибутив?

This is a version of the Linux operating system, which includes the Linux kernel, various programs, and tools, forming a comprehensive working environment for the user. Each distribution may have its own features, such as Ubuntu, Fedora, Debian, CentOS, and so on.

***Готував матеріал студент Войтенко В.***

5. Які задачі системного адміністрування можна реалізувати на базі ОС Linux?
- Manage users and groups
- Support for local area networks and web applications
- File system management
- Security management
- Virtualization
- Automation of tasks

6. Як пов'язані між собою ОС Android та Linux? 
-  The Android kernel uses the Linux kernel

***Готував матеріал студент Селезень Є.***

7. Основні можливості та сфера використання Embedded Linux?

Embedded Linux is used for embedded systems, such as mobile devices, medical devices, automotive electronics, and more. Key features include small size, low power consumption, and the ability to operate on various hardware platforms.

8. Яким чином можна змінити типу завантаження Linux: в текстовому режимі (3 рівень) або графічному (рівень 5)? Чим відрізняються режими CLI та GUI?

To change the boot type to either text mode (runlevel 3) or graphical mode (runlevel 5), you can edit the GRUB (Grand Unified Bootloader) configuration file /etc/default/grub and modify the value of GRUB_CMDLINE_LINUX_DEFAULT.

The Command Line Interface (CLI) mode differs from the Graphical User Interface (GUI) mode in that it operates in text mode and requires inputting commands from the keyboard, whereas the GUI mode provides a graphical interface for interacting with the user using both mouse and keyboard.

**Висновок**
<br/>
During the laboratory work, we got acquainted with different types of hypervisors, the main types of modern operating systems and virtualization when working with operating systems; gained theoretical and practical knowledge to work with Git and the GitHub website, and learned to work in the command line in more detail.

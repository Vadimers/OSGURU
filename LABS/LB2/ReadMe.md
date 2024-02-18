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

***Готував матеріал студент Войтенко В.***

<br/>

**CLI-режим - CLI mode (Command Line Interface mode)**, which allows the user to interact with the computer by entering commands via text input.

**Термінал на основі графічного інтерфейсу користувача - GUI terminal (Graphical User Interface terminal)** - software that emulates a terminal in a graphical user interface, allowing users to execute commands and interact with the operating system using a text-based interface.

**Віртуальний термінал - Virtual Terminal** - a terminal interface accessed independently of the graphical interface, typically requiring user login before executing commands.

**Відповіді на контрольні запитання**
<br/>

***Готував матеріал студент Войтенко В.***


**Хід роботи**

1. Робота в графічному режимі в ОС сімейства Linux (робота з інтернет-джерелами):

   1.1. Оберіть графічну оболонку для ОС сімейства Linux, яку ви хочете розглянути. Розгляньте
структуру робочого простору користувача, та опишіть основні його компоненти (***показано
основні компоненти оболонки Gnome):

![Application](./images/Application.jpg)

<h3 align="center"><b>Application</b></h3>

<br/>

<br/>

![Places](./images/Places.jpg)

<h3 align="center"><b>Places</b></h3>

<br/>

<br/>

![Activity overview](./images/Activity_overview.jpg)

<h3 align="center"><b>Activity overview</b></h3>

<br/>

<br/>

&nbsp; &nbsp; &nbsp; 1.2 Запуск програм. Дослідіть можливості запуску додатків різними способами (описати спосіб і по-
можливості показати скріншоти):

![Run via Favorites](./images/Run_via_Favorites.jpg)

<h3 align="center"><b>Run via Favorites</b></h3>

<br/>

<br/>

![Search in menu](./images/Search_in_menu.jpg)

<h3 align="center"><b>Search in menu</b></h3>

<br/>

<br/>

![Search in menu 2](./images/Search_in_menu_2.jpg)

<h3 align="center"><b>Next step to search in menu</b></h3>

<br/>

<br/>

![Run via file](./images/Run_via_file.jpg)

<h3 align="center"><b>Run via widget</b></h3>

<br/>

<br/>

![Run via global menu](./images/Run_via_global_menu.jpg)

<h3 align="center"><b>Run via global menu</b></h3>

<br/>

<br/>

![Run via terminal](./images/Run_via_terminal.jpg)

<h3 align="center"><b>Run via terminal</b></h3>

<br/>

<br/>

&nbsp; &nbsp; &nbsp; 1.3. Вихід з системи та завершення роботи в Linux. Як виконати в графічному інтерфейсі наступні дії
(наведіть скріни):

- Зміна користувача на root

![Change user](./images/Change_user.jpg)

<h3 align="center"><b>Change user</b></h3>

<br/>

<br/>

![Change user 2](./images/Change_user_2.jpg)

<h3 align="center"><b>Next step to change user</b></h3>

<br/>

<br/>

![Change user 3](./images/Change_user_3.jpg)

<h3 align="center"><b>Next step to change user</b></h3>

<br/>

<br/>

![Change user 4](./images/Change_user_4.jpg)

<h3 align="center"><b>Next step to change user</b></h3>

<br/>

<br/>

![Change user 5](./images/Change_user_5.jpg)

<h3 align="center"><b>Next step to change user</b></h3>

<br/>

<br/>

- Перезавантаження системи і вимкнення системи

![Restart and power off](./images/Restart_and_power_off.jpg)

<h3 align="center"><b>Restart and power off system</b></h3>

<br/>

<br/>

![Restart and power off 2](./images/Restart_and_power_off_2.jpg)

<h3 align="center"><b>Next step to restart and power off system</b></h3>

<br/>

<br/>

2. Робота в середовищі мобільної ОС.

   2.1. Опишіть головне меню вашої мобільної ОС, який графічний інтерфейс вона використовує?
Here are some of the key features of the Android main menu:

   **Icon grid:** The home screen is home to app icons that you can move, organize, and delete.
   <br/>
   **Quick access bar:** At the top of the screen is the quick access bar where you can find icons for Wi-Fi, Bluetooth, screen brightness, and other settings.
   <br/>
   **Widget:** You can add widgets to the Home screen to get quick access to information and features such as weather, calendar, news, and more.
   <br/>
   **Folder:** You can create folders to organize similar apps or widgets.
   <br/>
   **Search:** You can use the search bar to find apps, contacts, files, and other data on your device.
   <br/>
   **Android's graphical user interface**

   Android uses ***Material Design***, a design language developed by Google. Material Design focuses on simplicity, clarity, and intuitiveness. It uses smooth animations, shadows, and vibrant colors to make the user interface feel pleasant and comfortable.

&nbsp; &nbsp; &nbsp; 2.2. Опишіть меню налаштувань компонентів мобільного телефону.

   ![My phone setting](./images/Setting.jpg)

<h3 align="center"><b>My phone setting</b></h3>

&nbsp; &nbsp; &nbsp; 2.3. Використання комбінацій клавіш для виконання спеціальних дій.

   *Go to the Home screen:* Press the Home key.
   <br/>
   *Open your recent apps:* Press the View key.
   <br/>
   *Take a screenshot:* Press the Volume Down and Power keys simultaneously.
   <br/>
   *Turn Do Not Disturb mode on/off:* Press the Volume Down key for 3 seconds.
   <br/>
   *Turn off the phone:* Press the Power key for 10 seconds.
   <br/>
   *Restart the phone:* Hold down the Power and Volume Down keys for 7 seconds.
   
   Android has a gesture control feature.

   Gestures can be different: resetting, pressing, moving a finger along a certain trajectory, etc. Each smartphone manufacturer may have its own gestures and settings.

&nbsp; &nbsp; &nbsp; 2.4. Вхід у систему та завершення роботи пристрою. Особливості налаштувань живлення батареї.

Logging in to the system:

а)
<br/>
Power on: Hold down the Power key for a few seconds.
Unlock: Enter PIN, password, pattern key or use biometric authentication (fingerprint, face and eyes recognition)
<br/>
Turn off: Hold down the Power key for a few seconds.

b)
<br/>
Power saving mode: This mode helps extend battery life by limiting background activity and some functions.
Adaptive Battery: Android automatically learns your usage habits and optimizes your battery life by limiting battery usage to unused apps.
<br/>
Battery usage statistics: You can see which apps consume the most battery power.
Battery optimization: Android can help you optimize your battery usage by recommending settings and actions.

**Відповіді на контрольні запитання**

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

2. Порівняйте оболонки Bourne, C, Bourne Again (Bash), the tcsh, Korn shell (Ksh) та zsh.

1) Bourne Shell (sh):
   - One of the first Unix shells.
   - Has limited functionality compared to modern shells.
   - Used as the standard shell for many Unix systems.

2) C Shell (csh):
   - Has a syntax similar to the C programming language.
   - Supports a range of useful features, such as command history and pseudographic capabilities.

3) Bourne Again Shell (Bash):
   - Extension of the Bourne Shell with many enhancements and additional features.
   - Used by default in many modern Linux distributions.
   - Supports command history, job control, environment variables, and other useful features.

4) Tcsh:
   - Extension of the C Shell with additional features such as autocompletion and error correction.
   - Has a similar syntax to the C Shell but with more capabilities.

5) Korn Shell (Ksh):
   - Combines functionality from the Bourne Shell and C Shell.
   - Has many extensions and enhancements, including support for dynamic variables, branching, and loops.

6) Z Shell (Zsh):
   - Has many features that enhance user convenience and productivity.
   - Provides better autocompletion, directory management, and other advanced capabilities compared to other shells.
   - Often used as an alternative shell to Bash on Unix systems.

5. Чому використання віртуалізації зараз стало таким актуальним?
   
The use of virtualization has become relevant for several reasons:

**Efficient resource utilization:** Virtualization allows better utilization of computational resources by sharing physical servers to run multiple virtual machines.

**Cost savings:** Through virtualization, companies can reduce expenses on hardware, electricity, and space since fewer physical servers are needed to deploy applications.

**Greater flexibility and mobility:** Virtualization enables quick scaling and deployment of new virtual environments without significant delays and time costs.

**Enhanced security:** Virtualization enables the isolation of different applications and environments, reducing vulnerability risks and data leaks.

**Software testing and development:** Virtualization provides developers with a convenient way to test software in various environments without the need for physical devices.

**Enablement of heterogeneous environments:** Virtualization allows running different operating systems and applications on a single physical server, making it easier to manage and support diverse environments.

Overall, virtualization enables companies to optimize their computational resources, increase productivity, and reduce costs, making it highly relevant for modern organizations.

10. ***Чи можлива реєстрація в системі Linux декілька разів під одним і тим же системним ім’ям? Які переваги це може надати?

In Linux, it's possible to register multiple users under the same system username. This is achieved by creating different accounts with the same username (username), but with unique user identifiers (user ID or UID).
<br/>

Advantages:

Software testing:
<br/>
You can run multiple instances of an application under the same user to test different scenarios.
<br/>

Debugging problems:
<br/>
You can run two SSH sessions under the same user to debug issues with a remote server.
<br/>

Resource sharing:
<br/>
It is possible to allow multiple users to use the same account to access shared resources such as files and printers.


***Готував матеріал студент Селезень Є.***

3. Для чого потрібен менеджер пакетів. Які менеджери пакетів ви знаєте у Linux?

A package manager is a software tool used to automate the process of installing, upgrading, configuring, and removing software packages on a computer system. It simplifies the management of software dependencies and ensures that the software installed on a system is up-to-date and properly configured.

In Linux, there are several package managers, each commonly associated with a particular distribution:

**APT (Advanced Package Tool):** Used primarily in Debian-based distributions such as Debian, Ubuntu, Linux Mint, etc. The main commands are apt-get and apt.

**DPKG:** Although not technically a package manager itself, DPKG is the underlying package management system used by APT. It deals with the installation and removal of Debian packages (.deb files).

**RPM (RPM Package Manager):** Used in Red Hat-based distributions such as Red Hat Enterprise Linux (RHEL), Fedora, CentOS, openSUSE, etc. The main command is rpm.

**YUM (Yellowdog Updater, Modified):** A package management tool that relies on RPM packages, used primarily in Red Hat-based distributions. It has been largely replaced by DNF in newer versions of Fedora and CentOS.

**DNF (Dandified YUM):** The next-generation version of YUM, used in newer versions of Fedora, CentOS, and other RPM-based distributions. It's more feature-rich and performs better than YUM.

**ZYpp:** Used in openSUSE and SUSE Linux Enterprise distributions.

**Pacman:** Used in Arch Linux and its derivatives such as Manjaro. It's a simple and powerful package manager.

**Portage:** Used in Gentoo Linux. Portage is based on source code, and it compiles software locally based on the user's preferences and configurations.

These package managers, along with their associated tools, make it easy for Linux users to manage software installations, updates, and removals in a consistent and efficient manner.

4. Які засоби безпеки використовуються в Linux? 

Linux incorporates various security features at different levels to ensure the integrity, confidentiality, and availability of the system and its resources. Some of the key security features in Linux include:

**User and Group Permissions:** Linux uses a robust permission system where each file, directory, and device has associated permissions for the owner, group, and other users. This helps control access to resources.

**Firewall (iptables/firewalld):** Linux distributions typically include firewall software such as iptables or firewalld, which allow administrators to define rules for packet filtering and network address translation (NAT).

**SELinux (Security-Enhanced Linux):** Developed by the NSA, SELinux provides mandatory access controls (MAC) to restrict the actions that users and processes can perform on the system. It adds an extra layer of security beyond traditional Linux permissions.

**AppArmor:** Similar to SELinux, AppArmor is a Linux security module that confines individual programs to a set of rules that define what files, capabilities, and network access they can use.

**Kernel Hardening:** The Linux kernel includes various security features such as Address Space Layout Randomization (ASLR), which randomizes the memory addresses used by processes to make it harder for attackers to predict target locations.

**Secure Boot:** Secure Boot is a feature supported by many modern Linux distributions and UEFI firmware that ensures only trusted software can run during the boot process, thereby protecting against boot-time malware.

**Full Disk Encryption (e.g., LUKS):** Linux supports full disk encryption using tools like LUKS (Linux Unified Key Setup), which encrypts entire partitions or disks to protect data at rest.

**Package Signing:** Package managers in Linux distributions typically use digital signatures to verify the authenticity and integrity of software packages before installation, mitigating the risk of installing tampered or malicious software.

**Audit Framework:** Linux includes an audit subsystem that allows administrators to track and monitor system activities, helping to detect and investigate security breaches or policy violations.

**Secure Shell (SSH):** Linux distributions often come with SSH, which provides encrypted communication for securely accessing remote systems and transferring files.

6. Як ви розумієте поняття контейнеризації?

Containerization is a method of packaging, distributing, and running software applications and their dependencies in isolated environments called containers. Each container encapsulates the application, its runtime, libraries, and other dependencies, ensuring consistency and portability across different computing environments.

7. Які переваги/недоліки використання програмного забезпечення з відкритим кодом? 

Using open-source software offers several advantages and disadvantages:

Advantages:

**Cost-Effectiveness:** Open-source software is typically free to use, which can significantly reduce upfront costs for individuals, businesses, and organizations compared to proprietary alternatives. There are no licensing fees, and users can download, install, and modify the software without incurring additional expenses.

**Community Support:** Open-source projects often have vibrant communities of developers, users, and contributors who collaborate to improve the software, provide support, and share knowledge. This community-driven model fosters innovation, fosters collaboration, and ensures the longevity and sustainability of the software.

**Transparency and Customization:** Open-source software provides access to its source code, allowing users to inspect, modify, and customize the software to meet their specific needs and preferences. This transparency promotes trust, security, and flexibility, empowering users to tailor the software to their unique requirements without relying on proprietary vendors.

**Security and Reliability:** Open-source software benefits from peer review and scrutiny by a large community of developers, which can lead to faster identification and resolution of security vulnerabilities and bugs. Additionally, users have the freedom to audit the code, implement security enhancements, and contribute patches, thereby improving the overall security and reliability of the software.

**Interoperability and Compatibility:** Open-source software often adheres to open standards and protocols, promoting interoperability and compatibility with other software and systems. This compatibility reduces vendor lock-in, enables seamless integration with existing infrastructure, and facilitates data portability and interchangeability.

Disadvantages:

**Lack of Official Support:** While open-source software often benefits from community-driven support forums, documentation, and resources, it may lack the formalized support and service level agreements (SLAs) offered by proprietary vendors. This can pose challenges for organizations requiring dedicated technical assistance, maintenance, and troubleshooting.

**Complexity and Learning Curve:** Some open-source software solutions, particularly those with extensive customization options or advanced features, may have a steeper learning curve for users unfamiliar with the underlying technologies or programming languages. This complexity can require additional time, resources, and expertise to deploy, configure, and maintain effectively.

**Fragmentation and Compatibility Issues:** The decentralized nature of open-source development can lead to fragmentation, with multiple competing versions, distributions, and forks of the same software. This fragmentation may result in compatibility issues, interoperability challenges, and divergent ecosystems, making it difficult for users to navigate and choose the most suitable solution.

**Quality and Documentation Variability:** The quality and documentation of open-source software can vary widely depending on factors such as community size, project governance, and maintenance efforts. Some projects may lack comprehensive documentation, thorough testing, or regular updates, leading to inconsistencies, usability issues, and reliability concerns for users.

**Legal and Licensing Considerations:** While open-source licenses grant users certain freedoms and rights, they also impose obligations and restrictions that users must adhere to. Users must understand and comply with the terms of the applicable open-source licenses, which can vary in complexity and compatibility with proprietary software licenses. Failure to comply with license requirements can result in legal risks, compliance issues, and intellectual property disputes.

Overall, while open-source software offers numerous benefits such as cost savings, community support, and customization, it also presents challenges related to support, complexity, compatibility, quality, and legal considerations that users must carefully evaluate and address to maximize the value and effectiveness of open-source solutions.

8. Скільки активних віртуальних консолей (терміналів) може бути у процесі роботи Linux за замовчуванням? Як їх викликати та між ними перемикатися? Наведіть приклади?

In a default Linux system, typically, there are **six** virtual consoles (also known as virtual terminals) available for user interaction. These virtual consoles are numbered from 1 to 6, and they can be accessed using the keyboard shortcuts Ctrl + Alt + F1 through Ctrl + Alt + F6, respectively. Each virtual console provides a text-based interface for logging in, running commands, and interacting with the system.

To switch between virtual consoles, you can use the keyboard shortcuts mentioned above. For example, to switch to the first virtual console, you would press Ctrl + Alt + F1, and to switch to the second virtual console, you would press Ctrl + Alt + F2, and so on.

Here's a brief overview of how to access and switch between virtual consoles:

**Ctrl + Alt + F1:** Switch to the first virtual console.
**Ctrl + Alt + F2:** Switch to the second virtual console.
**Ctrl + Alt + F3:** Switch to the third virtual console.
**Ctrl + Alt + F4:** Switch to the fourth virtual console.
**Ctrl + Alt + F5:** Switch to the fifth virtual console.
**Ctrl + Alt + F6:** Switch to the sixth virtual console.
These virtual consoles provide independent login sessions, allowing multiple users to log in simultaneously and perform tasks separately. They are useful for troubleshooting, system maintenance, and running commands without the need for a graphical user interface.

Additionally, many Linux distributions also provide a seventh virtual console, accessible using Ctrl + Alt + F7, which typically runs the graphical user interface (GUI) session. This GUI session is where the desktop environment or window manager is displayed, allowing users to interact with the system using a graphical interface.

9. Яка віртуальна консоль (термінал) виконує функцію графічної оболонки?

In most Linux distributions, the virtual console (terminal) that serves as the graphical shell is typically accessed via Ctrl + Alt + F7. This virtual console hosts the graphical user interface (GUI) session, where the desktop environment or window manager is displayed.

When you boot into a Linux system with a graphical desktop environment installed (such as GNOME, KDE, Xfce, etc.), the system starts a display manager (such as GDM, LightDM, SDDM, etc.) on one of the virtual consoles (often on the seventh, accessed via Ctrl + Alt + F7). The display manager prompts the user to log in and then launches the desktop environment or window manager, which provides the graphical shell.

Users can interact with the graphical shell by using a mouse, keyboard, and graphical elements such as windows, icons, menus, etc., rather than the text-based interface provided by the other virtual consoles.

It's worth noting that the specific virtual console used for the graphical shell may vary depending on the Linux distribution and configuration. Some distributions may use a different virtual console for the graphical shell, but Ctrl + Alt + F7 is a common default.

10. Чи можлива реєстрація в системі Linux декілька разів під одним і тим же системним ім’ям? Які переваги це може надати?

Yes, in Linux, it is possible to have multiple login sessions under the same system username. This capability allows users to have concurrent sessions running simultaneously, each with its own environment and set of processes. There are several advantages to this:

**Concurrent Workflows:** Having multiple login sessions under the same username enables users to work on different tasks or projects simultaneously without interrupting each other. Each session maintains its own set of windows, applications, and workspaces, allowing for efficient multitasking.

**Remote Access:** Users can leverage multiple login sessions when accessing the system remotely via SSH or other remote access protocols. This enables users to have several terminal sessions open concurrently, each performing different tasks or monitoring various aspects of the system.

**Session Persistence:** If a user's session is interrupted or terminated unexpectedly (e.g., due to network issues or system reboots), having multiple login sessions allows the user to resume their work from another session without losing unsaved data or progress.

**Resource Management:** Users can distribute their computing tasks across multiple login sessions to better utilize system resources. For example, CPU-intensive tasks can be run in one session while leaving another session available for less resource-intensive activities.

**Multiuser Systems:** On multiuser systems where multiple users share the same machine, allowing multiple login sessions under the same username can help streamline user management and resource allocation. Users can log in from different locations or terminals and access their own personalized environments and files.

**Висновок**


During the laboratory work, our understanding of technology significantly broadened as we delved into both the Linux interface and the intricate structure of the mobile operating system (OS) present in our smartphones. This hands-on experience provided us with invaluable insights into the fundamental workings of these systems, empowering us with practical knowledge that is essential in today's digital landscape.

Exploring the Linux interface allowed us to comprehend the underlying principles of this powerful operating system, which serves as the backbone for a vast array of computing devices and systems worldwide. By navigating through its commands, file structures, and functionalities, we gained a deeper appreciation for its flexibility, efficiency, and robustness.

Additionally, dissecting the mobile OS architecture of our smartphones enabled us to grasp the intricacies of modern mobile computing. Understanding how various components such as the kernel, drivers, user interface, and applications interact within this ecosystem gave us a holistic view of the technology that has become integral to our daily lives.

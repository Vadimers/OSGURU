<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
Work-Case № 4</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Робота з менеджерами пакетів”</h2>



<div style="text-align: right;">
    <font size="4"><b>Виконали студенти <br/> групи РПЗ-13а <br/> Команда OSGURU: <br/> Войтенко В.С., <br/>  Селезень Є.С. <br/> Перевірив викладач <br/> Сушанова В.С. </b></font>
</div>

<br/>
<br/>
<br/>

<h2 align="center">Київ 2024</h2>

<hr>

1. В ході роботи досить часто виникає необхідність встановлювати нові програми та додатки. Для цього необхідно в терміналі вміти працювати з менеджерами пакетів:

● Дайте розгорнуте визначення таким поняттям як «пакет» та «репозиторій».
<br/>
A **package** is a collection of files that contains programs, libraries, configuration files, and other components that are necessary for the installation and proper operation of a software product or application. Each package usually has its own unique identifier, version, and dependencies that point to other packages that need to be installed or that it uses.

Packages make it easy to distribute, install, and update software on operating systems. They can be used to manage programs as well as to resolve dependencies between different software components.

A **repository** is a centralized storage of software for a particular operating system or distribution. A repository usually stores software packages, their metadata, and other information about them. Repositories provide users with access to software to install, update, and manage it.

Repositories are maintained by operating system developers or relevant communities that ensure that the packages are up-to-date and secure. Users can choose the repositories they want to use, as well as add their own repositories to access specialized software.

● Надайте короткий огляд існуючих менеджерів пакетів у Linux. Охарактеризуйте їх основні можливості.

**APT (Advanced Package Tool)**
<br/>
Використовується в Debian та на його основі заснованих дистрибутивах, таких як Ubuntu.
<br/>
Основна команда: apt-get.
<br/>
Можливості: встановлення, оновлення, видалення пакетів, пошук пакетів, керування залежностями, автоматичне вирішення конфліктів.

**DNF (Dandified Yum):**
<br/>
Використовується в Fedora, CentOS та інших дистрибутивах на основі Fedora.
<br/>
Основна команда: dnf.
<br/>
Можливості: встановлення, оновлення, видалення пакетів, пошук пакетів, керування залежностями, автоматичне вирішення конфліктів.

**Pacman:**
<br/>
Використовується в Arch Linux та його споріднених дистрибутивах.
<br/>
Основна команда: pacman.
<br/>
Можливості: оновлення, встановлення, пошук пакетів, видалення пакетів пакетів, керування залежностями, автоматичне вирішення конфліктів.

**ZYpp (ZYpper):**
<br/>
Використовується в openSUSE та SUSE Linux Enterprise.
<br/>
Основна команда: zypper.
<br/>
Можливості: встановлення, оновлення, видалення пакетів, пошук пакетів, автоматичне вирішення конфліктів, керування залежностями.

2. Визначте який менеджер пакетів використовує ваш дистрибутив Linux.
<br/>
Опишіть основні команди для роботи з ним:

● Пошук, скачування та установка необхідних пакетів, яких у Вашій системі немає (зі сховища по замовчуванню, з нового репозиторію тощо).
<br/>
yum search "package name" (search for packages by name or keywords)

yum install "package name" (installing the package)

yum update (update all installed packages to the latest versions)

yum groupintall "package name" (installing a group of packages)

● Перегляд інформації про встановлені та доступні пакети.
<br/>
yum list installed ( view installed packages)

yum list available (view the packages available for installation)

yum info "package name"( detailed information about the package)

● Видалення непотрібних або застарілих пакетів.
<br/>
yum remove "package name" (delete a package)

yum autoremove (remove packages that are no longer needed)

● Оновлення менеджера пакетів.
<br/>
yum upgrate (update the yum package manager itself to the latest version)

3. Встановіть у терміналі через менеджер пакетів на свою систему:

● Новий відео- чи аудіоплейер.

sudo yum install epel-release
<br/>
:arrow_down:
<br/>
https://download1.rpmfusion.org/free/el/rpmfusion-free-release-7.noarch.rpm
<br/>
:arrow_down:
<br/>
sudo yum install vlc

![vlc](./images/vlc.png)

<br/>

<br/>

● Середовище для мови програмування, що ви вивчаєте.

yum install geany

![geany](./images/geany.jpg)

<br/>

<br/>

1. Яким чином можна встановити нові програми через магазини додатків та менеджери пакетів у графічному середовищі. Наведіть свої приклади.

![Application installer](./images/application_installer.jpg)

<br/>

<br/>

Consulution:

In this task, we've learned the importance of package management in our Linux system. Understanding terms like "package" and "repository" is crucial. We explored various package managers like apt, yum, and pacman, each offering unique features for tasks such as searching, installing, and updating packages.

Identifying and mastering basic commands for our specific package manager ensures smooth system maintenance. We successfully installed new software, including a video or audio player and a programming language environment, directly from the terminal.

We also discussed installing software through graphical application stores, highlighting the versatility of package management systems.

Overall, mastering package management is essential for maintaining our system's integrity, ensuring access to software, and upholding stability and security.

<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 6</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Команди Linux для архівування та стиснення даних. Робота з текстом” <br/></h2>



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
|  Compression (the process of reducing the size of a file or directory) | Стиснення (процес зменшення розміру файлу або каталогу )|
| Archiving (the process of backing up and saving data to a secure location, often in a compressed format) | Архівування (процес резервного копіювання та збереження даних у безпечному місці, часто в стислому форматі ) |
| Gzip (a classic compression tool that uses the DEFLATE algorithm) | Gzip (класичний інструмент стиснення, що використовує алгоритм DEFLATE) |
| Bzip2 (a compression tool that implements the Burrows-Wheeler algorithm) | Bzip2 (інструмент стиснення, який реалізує алгоритм Барроуза-Вілера) |
| Xz (a compression tool that uses the LZMA2 algorithm) | Xz (інструмент стиснення, що використовує алгоритм LZMA2) |
| Tar (a command-line utility used to manipulate and create archives)  | Tar (командний інструмент, який використовується для маніпулювання та створення архівів)  |
| Flags/Options (additional parameters passed to commands to modify their behavior) | Прапорці/опції (додаткові параметри, передані командам для зміни їх поведінки) |
| -z (gzip) (flag used with tar to indicate gzip compression) | -z (gzip)(прапорець, використовуваний з tar для позначення стиснення gzip) |
| -j (bzip2) (flag used with tar to indicate bzip2 compression) | -j (bzip2) (прапорець, використовуваний з tar для позначення стиснення bzip2) |
| -J (xz) (flag used with tar to indicate xz compression) | -j (xz) (прапорець, використовуваний з tar для позначення стиснення xz) |
| -t (tar) (flag used with tar to list the contents of an archive) | -t (tar) (прапорець, використовуваний з tar для виведення списку вмісту архіву) |
| -c (tar) (flag used with tar to create an archive) | -c (tar) (прапорець, використовуваний з tar для створення архіву) |
| -v (tar) (flag used with tar to display verbose output) | -v (tar) (прапорець, використовуваний з tar для виведення розгорнутої інформації) |
| -f (tar) (flag used with tar to specify the filename of the archive) | -f (tar) (прапорець, використовуваний з tar для вказівки імені файлу архіву) |

4. На базі розглянутого матеріалу дайте відповіді на наступні питання:

4.1 *Яке призначення команд  tar, xz, zip, bzip, gzip? Зробіть короткий опис кожної команди та виділіть їх основні параметри. Яким чином їх можна встановити.
<br/>
**tar:**

Description: The tar command is used for creating, unpacking, and managing archives. It allows combining multiple files into one archive while preserving their directory structure, permissions, and other file attributes.
<br/>
Main Parameters:
<br/>
-c: Create an archive
<br/>
-x: Extract an archive
<br/>
-f filename: Specify the archive's name
<br/>
-v: Verbose mode (output information)
<br/>
-z: Compression using gzip
<br/>
-j: Compression using bzip2
<br/>
-J: Compression using xz
<br/>
Installation: Tar is typically installed along with the base installation of the Linux operating system. If it's not installed, you can install it using your OS package manager.

**xz:**

Description: The xz command is used for compressing and decompressing files using the LZMA2 compression algorithm. It's commonly used to compress files or archives to reduce their size.
<br/>
Main Parameters:
<br/>
-z: Compress a file
<br/>
-d: Decompress a file
<br/>
-c: Send compressed output to standard output
<br/>
Installation: xz can be installed using your OS package manager.

**zip:**

Description: The zip command is used for creating and unpacking ZIP archives. It allows combining multiple files and directories into one archive with compression.
Main Parameters:
<br/>
-r: Recursively add directories
<br/>
-9: Maximum compression level
<br/>
-d: Delete files after compression
<br/>
Installation: Zip is typically installed along with the base installation of the Linux operating system. If it's not installed, you can install it using your OS package manager.

**bzip:**

Description: The bzip command is used for compressing and decompressing files using the bzip2 compression algorithm. It provides more efficient compression compared to gzip but usually requires more time for compression.
Main Parameters:
<br/>
-z: Compress a file
<br/>
-d: Decompress a file
<br/>
-s: Reduce memory requirements
<br/>
Installation: bzip can be installed using your OS package manager.

**gzip:**

Description: The gzip command is used for compressing and decompressing files using the DEFLATE compression algorithm. It's a classic compression tool in the Linux environment.
Main Parameters:
<br/>
-c: Send compressed output to standard output
<br/>
-d: Decompress a file
<br/>
-1 to -9: Compression level (from fastest to most efficient)
<br/>
Installation: Gzip is typically installed along with the base installation of the Linux operating system. If it's not installed, you can install it using your OS package manager.

4.2 **Наведіть три приклади реалізації архівування та стискання даних різними командами. 
<br/>

4.3 *Яке призначення команд  cat, less, more, head and tail? Зробіть короткий опис кожної команди та виділіть їх основні параметри. Яким чином їх можна встановити
<br/>

4.4 **Поясніть принципи роботи командної оболонки з каналами, потоками та фільтрами
<br/>

4.5 *Яке призначення команди grep?
<br/>
The purpose of the **grep command** is to search for text within the output data using regular expressions. It is widely used for filtering and extracting lines of text that match a specific pattern or criteria. grep can be used as a standalone command or in conjunction with other commands through pipelines for complex search tasks. For example, using grep in combination with ls allows you to find files with specific names or extensions in a directory.

**Хід роботи:**

2. Опрацюйте всі приклади команд, що представлені у лабораторних роботах курсу NDG Linux Essentials - Lab 9: Archiving and Compression та Lab 10: Working With Text. Створіть таблицю для опису цих команд

|                        Назва команди                       |                                Її призначення та функціональність                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| gzip longfile.txt | Файл стискається викликом команди gzip із назвою файлу як аргументом|
| gzip -l longfile.txt.gz | Команда gzip надасть інформацію щодо стиснення за допомогою параметра –l |
| tar -cf alpha_files.tar alpha* | tar-файл створюється з кількох файлів назва яких починається на alpha* |
| tar -czf alpha_files.tar.gz alpha* | Архіви можна стиснути для легшого транспортування за допомогою параметра -z у команді tar |
| tar -tjf folders.tbz | Перерахувати файли в архіві, розпакувати за допомогою команди bzip2, оперувати над даним архівом |
| tar -xjf folders.tbz | Розпакування архіву за допомгою параметру –x після того, як його буде скопійовано в інший каталог |
| zip alpha_files.zip alpha* | Створення стисненого архіву під назвою alpha_files.zip |
| zip –r alpha_files.zip alpha* | Використання рекурсії, щоб повернутися до підкаталога |
| unzip -l School.zip | Параметр –l (list) команд unzip містить список файлів у архівах .zip |
| cat food.txt | Відображення файлу за допомогою команди cat |
| less words | Перегляд файлу за допомогою команди less |
| ls /etc | head | Вивід перших десяти рядків команди |
| echo “Line 1” | Стандартний вивід команд на екран |
| echo “Line 1” > example.txt | Перенаправлення стандартного виводу команд у файл |
| cat example.txt  | Перегляд вихідних даних файлу |
| echo "New line 1" > example.txt | Перезапис будь-якого вмісту існуючого файлу |
| echo "Another line" >> example.txt | Додавання до файлу нового рядка |
| ls /fake 2> error.txt | Надсилання всіх повідомлень про помилки у файл error.txt |
|s /fake /etc/ppp &> all.txt | Надсилання у файл одразу два потоки |
| ls /fake /etc/ppp > example.txt 2> error.txt | Перенаправлення потоків до різних файлів |
| sort mypasswd | Зміна рядків файлів або введення в словниковому або числовому порядку |
| sort -t: -n -k3 mypasswd | Числове сортування третього поля файлу mypasswd |
| wc /etc/passwd /etc/passwd | Надає кількість рядків, слів і байтів для файлу, а також загальну кількість рядків, якщо вказано більше одного файлу |
| cut -d: -f1,5-7 mypasswd | Відображення першого, п’ятого, сьомого поля файлу бази даних mypasswd |
| grep --color bash /etc/passwd | Фільтрація рядків у файлі або виводу іншої команди, яка відповідає вказаному шаблону |
| grep 'r..f' red.txt | Знаходження будь-якого рядка, який містить літеру r за якою слідують рівно два символи, а потім літеру f |
| grep '....' red.txt | Знаходження слів які містять чотири символи |
| grep '[0-9]' profile.txt | Знаходження символу із списку або діапазону можливих символів, що містяться в дужках |
| grep 're*d' red.txt | Знаходження нуля або більше повторень літери e |
| grep 'r[oe]*d' red.txt | Знаходження нуля або більше повторень літери o або e |
| grep '^root' passwd | Використання ^ для того, щоб на початку рядка з’явився шаблон |
| grep 'r$' alpha-first.txt | Використання $, щоб переконатися, що шаблон з’явився в кінці рядка |
| grep 're*' newhome.txt | Знаходження r, за яким йде нуль або більше букв e |
|grep 're\*' newhome.txt | Знаходження справжнього символу зірочки |
| grep -E 'colou?r' spelling.txt | Знаходження відповідності colo після якого йде нуль або один символ u , після якого йде символ r |
| grep -E 'e+' red.txt | Знаходження одного або більшої кількості символів e |
| grep -E 'gray|grey' spelling.txt | Знаходження слова gray або grey |

3. Ознайомтесь з командою tar та за її допомогою виконати у терміналі наступні дії:

-створити файл з розширенням .tar;



-створити файл з розширенням .tar, що складається з декількох файлів і каталогів  одночасно;



-перегляду вмісту файлу;



-витягти вміст файлу tar;



-створити архівний файл tar, стиснений за допомогою bzip;



-витягти вміст файлу tar bzip;



-створити архівний tar файл, стисненого за допомогою gzip;



-витягти вміст файлу tar gzip.




4. *Як буде відбуватись перенаправлення потоків виведення в bash для наступних дій з командами (позначено як cmd) та файлами (позначено як file):

|                        Команда                       |                                Що виконує команда?                                |
|------------------------------------------------------|-----------------------------------------------------------------------------------|
| cmd 1> file | Redirects standard output to a file |
| cmd > file | Redirects standard output to a file |
| cmd 2> file | Redirects standard error to a file |
| cmd >> file | Appends standard output to a file |
| cmd &> file | Redirects both standard output and standard error to a file |
| cmd > file 2>&1 | Redirects standard output to a file and standard error to the same location as standard output |
| cmd >> file 2>&1 | Appends standard output to a file and standard error to the same location as standard output |
| cmd 2>&1 > /dev/null | Redirects standard error to the same location as standard output and then redirects standard output to /dev/null, discarding it |
| cmd 2> /dev/null | Redirects standard error to /dev/null, discarding it |
| cmd1 | cmd2 | Відображення файлу за допомогою команди cat |
| cmd1 2>&1 | cmd2 | Перегляд файлу за допомогою команди less |
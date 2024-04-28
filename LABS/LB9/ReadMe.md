<h3 align="center">“Київський фаховий коледж зв’язку”<br/>
Циклова комісія Комп’ютерної інженерії</h3>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h1 align="center">ЗВІТ ПО ВИКОНАННЮ<br/>
ЛАБОРАТОРНОЇ РОБОТИ № 9</h1>

<br/>

<h3 align="center">з дисципліни: «Операційні системи»</h3>

<h2 align="center">Тема: “Захист системи та користувачів у Linux. Створення користувачів та груп” <br/></h2>



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



 Виконайте наступні практичні завдання у терміналі наступні дії (продемонструвати скріншоти):

- виведіть інформацію про поточного користувача різними способами (підказка використовуйте команди id та grep);

![id](./images/id_1_1.png)

<h3 align="center"><b>id</b></h3>

<br/>

<br/>

![id -Gn](./images/id_gn_1_2.png)

<h3 align="center"><b>id -Gn</b></h3>

<br/>

<br/>

![id -u](./images/id_u_1_3.png)

<h3 align="center"><b>id -u</b></h3>

<br/>

<br/>

![id | grep "groups"](./images/id_grep_groups_1_4.png)

<h3 align="center"><b>id | grep "groups"</b></h3>

<br/>

<br/>

- *попрактикуйте в терміналі команди last, w та who. Порівняйте результати виводу кожної команди, які деталі відсутні в кожній із команд порівняно з іншими?

![last](./images/last_2_1.png)

<h3 align="center"><b>Command "last"</b></h3>

<br/>

<br/>

![w](./images/w_2_2.png)

<h3 align="center"><b>Command "w"</b></h3>

<br/>

<br/>

![who](./images/who_2_3.png)

<h3 align="center"><b>Command "who"</b></h3>

<br/>

<br/>

- *створіть дві нові групи користувачів - super_admins, noob_users та good_students, визначте їх ідентифікатори;

```sudo groupadd super_admins```

```sudo groupadd noob_users```

```sudo groupadd good_students```

<h3 align="center"><b>Creating groups</b></h3>

![grep 'group name' /etc/group](./images/grep_3_1.png)

<h3 align="center"><b>Defining groups indeficators</b></h3>

<br/>

<br/>

- *для кожного члену Вашої команди за допомогою терміналу створіть нового користувача (якщо працюєте самі, то просто трьох довільних користувачів), не забудьте після створення нового користувача  одразу задати йому пароль;

![who](./images/useradd_passwd_4_1.png)

<h3 align="center"><b>Creating new users and providing them passwords</b></h3>

<br/>

<br/>

- **додайте нових користувачів у створені Вами нові групи таким чином, щоб у групах super_admins та noob_users було по 2 користувачі, один з яких є в обох групах, у групу good_students додайте - всіх трьох користувачів;

![Adding users to groups](./images/usermod_5_1.png)

<h3 align="center"><b>Adding users to groups</b></h3>

<br/>

<br/>

- **перегляньте інформацію про групи, та які користувачі до них входять, поясніть що ви бачите;

![cat /etc/group](./images/cat_6_1.png)

<h3 align="center"><b>Cheaking groups for users</b></h3>

<br/>

<br/>

- **видаліть першого створеного вами користувача, перегляньте чи залишиться інформація про нього в групах, де він перебував;

![userdel vadym](./images/userdel_vadym_7_1.png)

<h3 align="center"><b>Deleting user "vadym" and cheaking groups</b></h3>

<br/>

<br/>

- **видаліть другого користувача, перегляньте чи залишиться інформація про нього в групах, де він перебував; 

![userdel yevgeniy](./images/userdel_yevgeniy_8_1.png)

<h3 align="center"><b>Deleting user "yevgeniy" and cheaking groups</b></h3>

<br/>

<br/>

- **видаліть третього користувача, перегляньте чи залишиться інформація про нього в групах, де він перебував; 

![userdel petya](./images/userdel_petya_9_1.png)

<h3 align="center"><b>Deleting user "petya" and cheaking groups</b></h3>

<br/>

<br/>

- **перегляньте інформацію про існуючі групи користувачів;

![cat /etc/group](./images/userdel_petya_9_1.png)

<h3 align="center"><b>Cheaking groups</b></h3>

<br/>

<br/>

- **видаліть створені Вами групи користувачів;

![sduo groupdel "group name"](./images/groupdel_10_1.png)

<h3 align="center"><b>Deleting groups</b></h3>

<br/>

<br/>

- **перегляньте інформацію про існуючі групи користувачів.

![cat /etc/group](./images/cat_etc_group_11_1.png)

<h3 align="center"><b>Cheaking groups</b></h3>

<br/>

<br/>

*Готував матеріал студент Селезень Є.*

**Контрольні запитання:**

1. Чому в конфігураційних файлах паролі не зберігається в явному вигляді?



2. Чому не рекомендується виконувати повсякденні операції, використовуючи обліковий запис root?



3. *У чому відмінність механізмів отримання особливих привілеїв su і sudo?



4. *Чому домашній каталог користувача root не розміщено в каталозі /home?



5. *Для чого використовується команда getent?



6. *Як можна змінити пароль користувача?



7. **Яким чином можна видалити існуючі групи користувачів? Чи залишиться інформація про них десь у системі?



8. **Яке призначення команди chage?



9. **Які параметри команди usermod ви вважаєте найбільш використовуваними?



Conclusion:


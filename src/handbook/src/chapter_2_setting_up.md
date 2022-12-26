# Первичная настройка дистрибутива

После того, как система полностью загрузилась, вам необходимо выполнить
некоторые действия по её первичной настройки.

## Создание пользователей

Первым делом вам нужно создать обычного пользователя, из-под которого вы будете
работать по умолчанию. Для создания пользователей используется программа
`useradd`. Введите команду:

```
# useradd -m USERNAME -s /bin/bash
```

В том случае, если программа `useradd` завершилась без ошибок (а значит, нужный
пользователь создан), в терминал не будет ничего выведено. Если `useradd` вывела
в терминал какое-либо сообщение, то проанализируйте его и выполните те действия,
которые там, возможно, указаны.

После чего вам нужно дать ему пароль:

```
# passwd USERNAME
```

Программа выведет в терминал:

```
Изменение пароля для USERNAME
Введите новый пароль (минимальная длина 5 символов)
Используйте комбинацию из символов в верхнем и нижнем регистре и цифры
Новый пароль:
Повторите новый пароль:
passwd: пароль изменён.
```

В том случае, если по умолчанию у вас не русский язык, а английский, то вывод
будет таким:

```
Changing password for USERNAME
Enter the new password (minimum of 5 characters)
Please use a combination of upper and lower case letters and numbers.
New password:
Re-enter new password:
passwd: password changed.
```

<small>
<tt><code>USERNAME</code></tt> замените на имя пользователя. Например,
<tt><code>michail</code></tt>. Имя пользователя должно быть на английском и
содержать только буквы и, возможно, цифры. Все остальные символы использовать не
рекомендуется во избежание ошибок в работе системы и стороннего программного
обеспечения.</small>

### Объяснение команд

- `useradd` - программа для создания новых пользователей.
- `-m` в команде `useradd ...` - указывает программе `useradd` создавать
  домашнюю директорию пользователя в `/home/`.
- `-s /bin/bash` - закрепляет за создаваемым пользователем оболочку `/bin/bash`.
  Она будет использоваться для него по умолчанию. Других командных оболочек в
  Calmira GNU/Linux по умолчанию нет.
- `USERNAME` - вместо этих символов подставьте имя пользователя.
- `passwd` - устанавливает новый/изменяет пароль пользователя.

Для того, чтобы войти в систему от имени созданного пользователя, можно
использовать два способа:

**Способ 1:**

```
# su USERNAME
```

**Способ 2:**

```
# exit
```

После выполнения данной команды вас будет приветствовать приглашение к входу в
систему как на предыдущей странице. Введите имя созданного пользователя и его
пароль.

---

> ## Почему не рекомендуется работать от имени пользователя root?
>
> `root` - это системный привилегированный пользователь. Если вы работаете от
> его имени, то у вас есть широкие возможности для модификации и изменении
> операционной системы GNU/Linux-libre. Вы можете случайно удалить какой-либо
> системный файл, в результате чего работа системы будет либо некорректной, либо
> вообще невозможной. Кроме того, ваша система становится уязвимой для не самых
> хороших личностей, которые могут либо поломать её, либо украсть какие-либо
> данные, либо даже отправить в систему вирус или троян.
>
> Вопреки известному мнению о том, что "в GNU/Linux(-libre) нет вирусов" - это
> совсем не так. Вирусы, трояны и прочая гадость эксплуатирует уязвимости в
> программном обеспечении, в том числе и в ОС. А в любом ПО так или иначе есть
> баги, ошибки и уязвимости. Однако можно отметить тот факт, что для
> UNIX-подобных систем существует несколько меньше вирусов, чем для той же
> MS-Windows. Да и на компьютерах обычных пользователей вирусы - это редкое
> явление. Однако не следует пренебрегать своей безопасностью.
>
> Используйте учётную запись `root` исключительно в крайних случаях. В том
> случае, если вам нужно выполнить команду/программу с повышенными привилегиями,
> то используйте либо программу `su -c "команда"`, либо программу `sudo` (порт
> `general/sudo`. Информация об этой программе будет в главе 3. Установить её
> легко:
>
> ```
> # cport -i general/sudo
> ```
# Содержание

[Предисловие](./preface.md)

# Часть 1

- [Часть 1](./chapter_1.md)
  - [Введение](./chapter_1_intro.md)
  - [Установка дистрибутива версии >= 2.Х](./chapter_1_installation.md)

# Часть 2

- [Часть 2](./chapter_2.md)
  - [Авторизация в системе](./chapter_2_auth.md)
  - [Первичная настройка дистрибутива](./chapter_2_setting_up.md)
  - [Настройка GRUB](./chapter_2_grub.md)
  - [Редактирование файлов](./chapter_2_editors.md)
  - [Управление программным обеспечением](./chapter_2_software.md)
  - [Управление правами доступа](./chapter_2_permissions.md)
  - [Работа с системой инициализации](./chapter_2_init.md)

# Часть 3

- [Часть 3](./chapter_3.md)
  - [Ядро системы](./chapter_3_kernel.md)
  - [Оболочка системы](./chapter_3_env_intro.md)
    - [Основные программы](./chapter_3_env_soft.md)
    - [BASH](./chapter_3_env_bash.md)
    - [Перемещение по директориям](./chapter_3_env_dirs.md)
    - [Работа с файлами](./chapter_3_env_files.md)
    - [Переменные окружения](./chapter_3_env_vars.md)
    - [Пути до исполняемых файлов](./chapter_3_env_path.md)
    - [Получение интерактивной справки](./chapter_3_env_man.md)
    - [Ввод и вывод](./chapter_3_env_io.md)
    - [Основные ошибки](./chapter_3_env_errors.md)
  - [Управление процессами](./chapter_3_ps_intro.md)
    - [Компоненты процесса](./chapter_3_ps_process.md)
      - [PID и PPID](./chapter_3_ps_pid.md)
      - [UID и EUID](./chapter_3_ps_uid.md)
      - [GID и EGID](./chapter_3_ps_gid.md)
    - [Жизненный цикл процесса](./chapter_3_ps_lifetime.md)
    - [Сигналы](./chapter_3_ps_signals.md)
    - [Использование `kill`](./chapter_3_ps_kill.md)
    - [Использование `ps`](./chapter_3_ps_ps.md)
    - [Использование `top`](./chapter_3_ps_top.md)
    - [Изменение приоритета выполнения](./chapter_3_ps_nice.md)
    - [Файловая система `/proc`](./chapter_3_ps_proc.md)
  - [Управление пользователями](./chapter_3_users_intro.md)
    - [Учётная запись `root`](./chapter_3_users_root.md)
    - [Замена идентификатора пользователя: `su`](./chapter_3_users_su.md)
    - [Использование `sudo`](./chapter_3_users_sudo.md)
    - [Прочие системные учётные записи](./chapter_3_users_sysusers.md)
    - [Группы пользователей](./chapter_3_users_groups.md)
    - [Создание пользователей](./chapter_3_users_create.md)
  - [Управление правами доступа](./chapter_3_perm_intro.md)
    - [Стандартное управление доступом](./chapter_3_perm_chmod.md)
    - [Расширенное управление доступом](./chapter_3_perm_additional.md)
      - [Установка флагов `setuid` и `setgid`](./chapter_3_perm_setuid.md)
      - [ACL](./chapter_3_perm_acl.md)
  - [Управление программным обеспечением](./chapter_3_software.md)

# Часть 4

- [Часть 4](./chapter_4.md)
  - [Продвинутое использование Neovim](./chapter_4_nvim.md)
  - [Продвинутое использование sudo](./chapter_4_sudo.md)
  - [Продвинутое использование системы портов](./chapter_4_ports.md)
  - [Изменение параметров загрузки системы](./chapter_4_boot.md)

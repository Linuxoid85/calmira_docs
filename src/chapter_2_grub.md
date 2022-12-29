# Настройка GRUB

Первичный конфиг GRUB находится в файле `/boot/grub/grub.cfg`:

```
# Begin /boot/grub/grub.cfg
set default=0
set timeout=3

insmod ext2
set root=(hd0,2)

menuentry "Calmira v2.0 Core Edition" {
  linux /boot/vmlinuz-6.0-gnu root=/dev/sda2 ro quiet
}
```

Параметр `default` определяет выбранный по умолчанию пункт меню GRUB.

Параметр `timeout` определяет время (в секундах), по прошествии которого, в
случае бездействия пользователя, будет выбран стандартный пункт меню, указанный
в параметре `default`.

**TODO:** больше конкретики

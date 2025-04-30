# Домашнее задание к занятию  «Защита хоста»

### Задание 1

1. Установите **eCryptfs**.
2. Добавьте пользователя cryptouser.
3. Зашифруйте домашний каталог пользователя с помощью eCryptfs.

Создали второго пользователя и создали файлы в домашнем каталоге
![изображение](https://github.com/user-attachments/assets/5b65eab2-21ad-4585-86bf-e5f164abb4d9)

С помощью команды ecryptfs-migrate-home -u cryptouser зашифровываем домашний каталог пользователя cryptouser
![изображение](https://github.com/user-attachments/assets/5562eff7-ae2e-4374-9038-9a0c13d4ab06)

![изображение](https://github.com/user-attachments/assets/bfd90548-69cc-41e5-a3d8-b39a5c474e35)

### Задание 2

1. Установите поддержку **LUKS**.
2. Создайте небольшой раздел, например, 100 Мб.
3. Зашифруйте созданный раздел с помощью LUKS.

![изображение](https://github.com/user-attachments/assets/b2684ba4-25da-4e92-bacf-0ec18f43c59f)

![изображение](https://github.com/user-attachments/assets/e8a8bcc5-9e12-4b42-9739-3755113a564c)

![изображение](https://github.com/user-attachments/assets/2b24983a-2b0c-4ec5-86d8-bd95258a6ffc)

![изображение](https://github.com/user-attachments/assets/aa4823ff-fd7b-420c-94df-b5fb170c777e)

### Задание 3 *

1. Установите **apparmor**.
2. Повторите эксперимент, указанный в лекции.
3. Отключите (удалите) apparmor.


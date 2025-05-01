# Домашнее задание к занятию «Защита сети»

### Подготовка к выполнению заданий

1. Подготовка защищаемой системы:

- установите **Suricata**,
- установите **Fail2Ban**.

2. Подготовка системы злоумышленника: установите **nmap** и **thc-hydra** либо скачайте и установите **Kali linux**.

Обе системы должны находится в одной подсети.

------

### Задание 1

Проведите разведку системы и определите, какие сетевые службы запущены на защищаемой системе:

**sudo nmap -sA < ip-адрес >**  
![изображение](https://github.com/user-attachments/assets/f05eb030-2fa1-4f9a-a540-934c504d63d0)

Лог suricata не зафиксировал действия

**sudo nmap -sT < ip-адрес >**  
![изображение](https://github.com/user-attachments/assets/f52b9d65-64f0-447c-b15e-0f8e30ddf3a5)

![изображение](https://github.com/user-attachments/assets/38903214-8c1e-4148-9684-02b77d1aa44b)

**sudo nmap -sS < ip-адрес >**  
![изображение](https://github.com/user-attachments/assets/d1c8e36c-dc14-480b-8c5f-808e8ff4572c)

![изображение](https://github.com/user-attachments/assets/ae500564-e664-48c2-ad1c-f925aa4a4434)

**sudo nmap -sV < ip-адрес >**  
![изображение](https://github.com/user-attachments/assets/8dac8af1-8453-400e-b8fe-63eb6512383c)

![изображение](https://github.com/user-attachments/assets/fb39dea9-2e81-4090-9edb-4a3c50a74b14)

------

### Задание 2

Проведите атаку на подбор пароля для службы SSH:

**hydra -L users.txt -P pass.txt < ip-адрес > ssh**

1. Настройка **hydra**: 
 
 - создайте два файла: **users.txt** и **pass.txt**;
 - в каждой строчке первого файла должны быть имена пользователей, второго — пароли. В нашем случае это могут быть случайные строки, но ради эксперимента можете добавить имя и пароль существующего пользователя.

![изображение](https://github.com/user-attachments/assets/1fd80623-43e0-401b-822a-b3e01fba4261)

2. Включение защиты SSH для Fail2Ban:

-  открыть файл /etc/fail2ban/jail.conf,
-  найти секцию **ssh**,
-  установить **enabled**  в **true**.

![изображение](https://github.com/user-attachments/assets/9385b2e2-caca-4403-9af0-95ab4fe14ea1)

![изображение](https://github.com/user-attachments/assets/5656a7ea-2ca1-4d3b-8015-38a132aff6a4)

![изображение](https://github.com/user-attachments/assets/7e59273e-bec1-4d8e-919c-e460b97aae07)

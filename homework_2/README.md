# Подготовка к выполнению

В Yandex Cloud создайте новый инстанс (4CPU4RAM) на основе образа jetbrains/teamcity-server.
Дождитесь запуска teamcity, выполните первоначальную настройку.
Создайте ещё один инстанс (2CPU4RAM) на основе образа jetbrains/teamcity-agent. Пропишите к нему переменную окружения SERVER_URL: "http://<teamcity_url>:8111".
Авторизуйте агент.
Сделайте fork репозитория.
Создайте VM (2CPU4RAM) и запустите playbook.



### Создал 3 вм согласно инструкциям:

<img width="1852" height="244" alt="ci cd_homework1 2" src="https://github.com/user-attachments/assets/215b715c-eb0c-48a8-b55a-87868095ab8d" />


### Увидел что есть неавторизованнный агент, что говорит о корректности первоначальных настроек:

<img width="888" height="387" alt="ci cd_homework1" src="https://github.com/user-attachments/assets/5fafcdb9-8a61-41d3-9e3d-748414f90467" />


### Авторизуем:

<img width="1230" height="278" alt="ci cd_homework1 3" src="https://github.com/user-attachments/assets/029da037-cfe5-4bdf-9b52-6173efd6cad9" />

## На этом подготовка к выполнению задания завершена. Идем дальше.

# Основная часть.

1) Создайте новый проект в teamcity на основе fork.
2) Сделайте autodetect конфигурации.
3) Сохраните необходимые шаги, запустите первую сборку master.



### Сделал, произвел билд, все прошло успешно:

<img width="1520" height="721" alt="ci cd_homework1 4" src="https://github.com/user-attachments/assets/3013c83d-79ab-4de2-8a68-e82321cecbd7" />
<img width="1510" height="527" alt="ci cd_homework1 5" src="https://github.com/user-attachments/assets/f3da39be-3014-4c56-a58e-051fa0993a64" />

4) Поменяйте условия сборки: если сборка по ветке master, то должен происходит mvn clean deploy, иначе mvn clean test.

Создал еще один шаг, в котором указал условия:

<img width="1503" height="672" alt="ci cd_homework1 6" src="https://github.com/user-attachments/assets/74dbe717-3c59-4d0f-8cc3-0879c4a29812" />


5) Для deploy будет необходимо загрузить settings.xml в набор конфигураций maven у teamcity, предварительно записав туда креды для подключения к nexus.
6) В pom.xml необходимо поменять ссылки на репозиторий и nexus.
7) Запустите сборку по master, убедитесь, что всё прошло успешно и артефакт появился в nexus.


### Сборка

<img width="1510" height="900" alt="ci cd_homework1 7" src="https://github.com/user-attachments/assets/ce0d6768-810a-418b-8c0d-695c785d2c23" />

### Артефакт в Nexus

<img width="1906" height="384" alt="ci cd_homework1 8" src="https://github.com/user-attachments/assets/5854536e-a241-4bcf-9ae7-62e9c2c12e22" />

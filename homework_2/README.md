### Подготовка к выполнению

В Yandex Cloud создайте новый инстанс (4CPU4RAM) на основе образа jetbrains/teamcity-server.
Дождитесь запуска teamcity, выполните первоначальную настройку.
Создайте ещё один инстанс (2CPU4RAM) на основе образа jetbrains/teamcity-agent. Пропишите к нему переменную окружения SERVER_URL: "http://<teamcity_url>:8111".
Авторизуйте агент.
Сделайте fork репозитория.
Создайте VM (2CPU4RAM) и запустите playbook.



## Создал 3 вм согласно инструкциям:

<img width="1852" height="244" alt="ci cd_homework1 2" src="https://github.com/user-attachments/assets/215b715c-eb0c-48a8-b55a-87868095ab8d" />


Увидел что есть неавторизованнный агент, что говорит о корректности первоначальных настроек:

<img width="888" height="387" alt="ci cd_homework1" src="https://github.com/user-attachments/assets/5fafcdb9-8a61-41d3-9e3d-748414f90467" />


Авторизуем:

<img width="1230" height="278" alt="ci cd_homework1 3" src="https://github.com/user-attachments/assets/029da037-cfe5-4bdf-9b52-6173efd6cad9" />


Запускаем build и видим что все прошло успешно:


<img width="1520" height="721" alt="ci cd_homework1 4" src="https://github.com/user-attachments/assets/3013c83d-79ab-4de2-8a68-e82321cecbd7" />
<img width="1510" height="527" alt="ci cd_homework1 5" src="https://github.com/user-attachments/assets/f3da39be-3014-4c56-a58e-051fa0993a64" />

# 2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d

<b>University:</b> [ITMO University](https://itmo.ru/ru/) <br>
<b>Faculty:</b> [FTMI](https://ftmi.itmo.ru) <br>
<b>Course:</b> [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/) <br>
<b>Year:</b> 2024/2025 <br>
<b>Group:</b> U4125 <br>
<b>Author:</b> Buchnikova Ekaterina Dmitrievna  <br>
<b>Lab:</b> Lab1 <br>
<b>Date of create:</b> 21.04.2025 <br>
<b>Date of finished:</b> 25.04.2025<br>

1. Сначала заходим на клауд  раздел `IAM & Admin` 

![](https://github.com/katherinebutch/2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d/blob/main/lab1/Screenshot%20at%20Apr%2025%2011-01-12.png?raw=true)

2. Там выбираем вкладку service accounts и нажимаем + create service account - называем по инструкции. Выбираем роль `Storage Admin`. Сохраняем созданный аккаунт.

   ![Screenshot at Apr 25 11-02-42.png](https://github.com/katherinebutch/2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d/blob/main/lab1/Screenshot%20at%20Apr%2025%2011-02-42.png?raw=true)

3. Переходим в Compute engine - во вкладку VM instances - создаем инстанс. 

      ![Screenshot at Apr 25 11-04-58.png](https://github.com/katherinebutch/2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d/blob/main/lab1/Screenshot%20at%20Apr%2025%2011-04-58.png?raw=true)

4. Называем машину в соотвествии с инструкцией - задаем ей параметр  micro 

      ![Screenshot at Apr 25 11-07-07.png](https://github.com/katherinebutch/2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d/blob/main/lab1/Screenshot%20at%20Apr%2025%2011-07-07.png?raw=true)

5. Переходим во вкладку Security - подключаем наш service accout 

   ![Screenshot at Apr 25 11-07-57.png](https://github.com/katherinebutch/2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d/blob/main/lab1/Screenshot%20at%20Apr%2025%2011-07-57.png?raw=true)

6. Переходим во вкладку advanced - там меняем в provising model вместо standart => spot 

   ![Screenshot at Apr 25 11-08-35.png](https://github.com/katherinebutch/2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d/blob/main/lab1/Screenshot%20at%20Apr%2025%2011-08-35.png?raw=true)

7. Идем в VM инстансы - по ssh подключаемся - вводим комманды управлять данными. С помощью утилиты `gsutils` найдите бакет `lab1-bucket-itmo` и скопируйте 3 файла в локальную папку на VM. Используя команду `ls -lah` отобразите что эти файлы хранятся у вас на VM.

               mkdir ~/lab1-files

               gsutil cp gs://lab1-bucket-itmo/* ~/lab1-files/

   ![2025-04-25 11.10.00.jpg](https://github.com/katherinebutch/2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d/blob/main/lab1/2025-04-25%2011.10.00.jpg?raw=true)

8. Меняем права доступа для вашего service account с `Storage Admin` на `Compute Viewer` (у меня не получилось поменять, машина залипла, поэтому я создала новый сервис аккаунт с правами `Compute Viewer` )

9. Видим что нам выскакивает ошибка - потому что у нас нет доступа. 

      ![2025-04-25 11.10.38.jpg](https://github.com/katherinebutch/2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d/blob/main/lab1/2025-04-25%2011.10.38.jpg?raw=true)


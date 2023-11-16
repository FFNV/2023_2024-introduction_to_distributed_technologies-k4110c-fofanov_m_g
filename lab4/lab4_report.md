University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)
Year: 2023/2024
Group: K4110с
Author: Fofanov Maksim Gerbertovich
Lab: Lab4
Date of create: 04.11.2023
Date of finished: 05.11.2023

Запускаем кластер Minikube, указав сетевой плагин как Calico и два узла:

![img_31.png](img_31.png)

Проверяем статус узлов и подов Calico в кластере:

![img_25.png](img_25.png)

![img_24.png](img_24.png)

Присваиваем метки узлам, чтобы указать их соответствующим стойкам:

![img_28.png](img_28.png)

Проверяем метки узлов:

![img_29.png](img_29.png)

Проверяем версию Calico:

![img_30.png](img_30.png)

Создадаем манифест для выдачи диапазонов в соответствии с распределением нод по стойкам:

![img_35.png](img_35.png)

Проверяем что calico выдал диапазон по умолчанию. Удаляем его. Применяем манифест:

![img_26.png](img_26.png)

Сверяем новые диапазоны:

![img_27.png](img_27.png)

Создаем и запускаем configMap и deployment:

![img_36.png](img_36.png)

![img_37.png](img_37.png)

![img_23.png](img_23.png)

Создадем сервис для deployment:

![img_39.png](img_39.png)

Пробрасываем порт:

![img_21.png](img_21.png)

Переходим по http://127.0.0.1:3000/:

![img_15.png](img_15.png)

Получаем информацию о подах, и используем 'grep' для поиска IP-адресов подов:

![img_20.png](img_20.png)

Пингуем поды, с помощью FQDN нашего сервиса:

![img_19.png](img_19.png)

![img_18.png](img_18.png)

Второй способ:

![img_17.png](img_17.png)

Схема:

![img_41.png](img_41.png)


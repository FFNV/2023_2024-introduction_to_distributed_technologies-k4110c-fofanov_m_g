University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)
Year: 2023/2024
Group: K4110с
Author: Fofanov Maksim Gerbertovich
Lab: Lab3
Date of create: 01.11.2023
Date of finished: 02.11.2023

Запускаем minikube cluster:

![img_3.png](img_3.png)

Опишем ConfigMap, через который мы будем передавать нужные переменные:

![img_16.png](img_16.png)

Опишем Deployment, который мы будем использовать вместо ReplicaSet:

![img_17.png](img_17.png)

Опишем Service, через который будем получать доступ к подам:

![img_10.png](img_10.png)

Опишем Ingress, через сущность будем обрабатывать внешние запросы к кластеру:

![img_11.png](img_11.png)

Включим minikube addons enable ingress:

![img_12.png](img_12.png)

Применим конфигурацию:

![img_4.png](img_4.png)

Сгенерируем TLS сертификат и импортируем сертификат в minikube:

![img_5.png](img_5.png)

![img_6.png](img_6.png)

![img_7.png](img_7.png)

Добавим запись хоста в /etc/hosts:

![img_13.png](img_13.png)

Используем команду minikube tunnel:

![img_8.png](img_8.png)

Переходим в браузер по fofanov-lab3.com:

![img_1.png](img_1.png)

Проверяем сертификат: 

![img_14.png](img_14.png)

Диаграмма:

![img_18.png](img_18.png)

Останавливаем minikube cluster:

![img_19.png](img_19.png)
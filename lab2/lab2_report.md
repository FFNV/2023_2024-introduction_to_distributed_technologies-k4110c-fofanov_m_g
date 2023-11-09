University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)
Year: 2023/2024
Group: K4110с
Author: Fofanov Maksim Gerbertovich
Lab: Lab2
Date of create: 28.10.2023
Date of finished: 31.10.2023


Разворачиваем minikube cluster:

![img_2.png](img_2.png)

Манифест, где Deployment с двумя репликами приложения и Service, 
который позволяет обращаться к этим репликам через NodePort на порту 3000 внутри кластера:

![img_9.png](img_9.png)

Запустим службу и деплоймент при помощи команды:

![img_4.png](img_4.png)

Проверяем состояние развернутых объектов Kubernetes. 
Видим, что деплоймент под названием my-app имеет 2 реплики, 
которые успешно работают, и сервис my-app типа NodePort.

![img_5.png](img_5.png)

Пробрасываем порт:

![img_6.png](img_6.png)

Открываем сервис my-app в браузере:

![img_3.png](img_3.png)

![img_1.png](img_1.png)

![img.png](img.png)

Останавливаем minikube cluster:

![img_7.png](img_7.png)

Схема организации контейеров и сервисов:
![img_10.png](img_10.png)

Вывод:

С помощью манифестов в данной работе была создана инфраструктура, включающая развертывание (Deployment) приложения с двумя репликами. При этом в переменные окружения контейнеров были переданы следующие значения:

REACT_APP_USERNAME было установлено равным "maxim_fofanov".

REACT_APP_COMPANY_NAME было установлено равным "ITMO".

Дополнительно, была создана служба (Service) типа NodePort, 
которая позволила перенаправлять входящий трафик в поды приложения. 
Это позволило нам доступать к приложению извне кластера.

Благодаря этой конфигурации смогли успешно развернуть приложение в Kubernetes, 
управлять им с двумя репликами и увидеть, как переданные переменные окружения ("maxim_fofanov" и "ITMO") доступны в разных контейнерах приложения.
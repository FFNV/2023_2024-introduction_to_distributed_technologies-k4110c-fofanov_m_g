University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)
Year: 2023/2024
Group: K4110с
Author: Fofanov Maksim Gerbertovich
Lab: Lab1
Date of create: 28.09.2023
Date of finished: 31.09.2023


Разворачиваем minikube cluster:

![img_1.png](img_1.png)

Манифест для развертывания пода HashiCorp Vault:

![img_8.png](img_8.png)

Разворачиваем объект Deployment в кластере:

![img_2.png](img_2.png)

Загружаем Docker-образ "vault:1.13.3:

![img_3.png](img_3.png)

Создаем один временный Pod с именем "vault":

![img_4.png](img_4.png)

Создаем сервис для доступа к Pod с именем "vault":

![img_5.png](img_5.png)

Копируем root token из логов:

![img_7.png](img_7.png)

![img_12.png](img_12.png)

Настраиваем пересылку портов, что позволит обращаться к сервису Vault, работающему в кластере, через локальный порт 8200:

![img_6.png](img_6.png)

Заходим в vault по ссылке http://localhost:8200:

![img_9.png](img_9.png)

Авторизируемся в vault, с помощью root token:

![img.png](img.png)

Схема организации контейеров и сервисов:

![img_10.png](img_10.png)

Останавливаем minikube cluster:

![img_11.png](img_11.png)

Вывод:

1. Запустили локальный Kubernetes-кластер с помощью Minikube, используя Docker.

2. Развернули объект Deployment с именем "vault-deployment".

3. Загрузили Docker-образ "vault:1.13.3" из Docker Hub.

4. Создали временный Pod с именем "vault".

5. Создали сервис, который предоставляет доступ к Pod с именем "vault".

6. Настроили пересылку портов, что позволяет обращаться к сервису Vault через локальный порт 8200.

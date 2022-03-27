# Выполнено ДЗ №

 - [ ] Основное ДЗ
 - [ ] Задание со *

## В процессе сделано:
 - Причина перезапуска контейнеров restartPolicy
 - Деплой собственного веб-приложения web-app. Создание страницы, манифеста, пода, проброса порта.
 - Билд докер образа, загрузку в регистри, деплой в кластер кубернетиса с исправлением пробле запуска контейнера.
 - Знакомство с вспомагательными приложениями (проброс портов).

## Как запустить проект:
 - Запуск web-app проекта kubectl apply -f web-pod.yaml && kubectl port-forward --address 0.0.0.0 pod/web-app 8000:80
 - Запуск forntend-pod-healthy kubectl appl -f frontend-pod-healthy.yaml + проброс порта в Kube Forwarder 8080:8080 или проверить kubectl get pod frontend-pod-healty 

## Как проверить работоспособность:
 - Например, перейти по ссылке http://localhost:8000/homework.html
 - Проверить работоспособность frontend-pod-healthy http://localhost:8080/

## PR checklist:
 - [ ] Выставлен label с темой домашнего задания
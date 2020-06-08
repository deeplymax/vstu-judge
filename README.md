# vstu-judge
Проект для тестирования кода на Си

# Запуск
Необходимо собрать контейнер для сборки и тестирования
```sh
cd /vstu-judge-images
docker-compose build
```
Затем собираем проект
```sh
cd ../
docker-compose up
```
Тестирование в postman можно выполнить из заранее сформированных файлов
```sh
vstu_judge_submission_status_check.postman_collection.json
vstu_judge_submit.postman_collection.json
```

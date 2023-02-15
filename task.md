Topic: CI/CD

Дата видачі: 11.01.2023

Дата здачі: 18.01.2023

Максимальна оцінка: 100 балів

Індивідуальне виконання

Результатом домашнього завдання стане Docker image, що автоматично збирається, для Airflow PM Academy Gitlab CI/CD practice.

Tasks:
Create new gitlab repository
This repository must contain all needed things to create docker image for apache airflow job, it must include:
python3 any version
airflow library for python
Customizable LABEL
Create pipeline, which must meet follow requirements:
If commit was done to any branch, which name starts with “feature/” - build image, tag it with short hash of commit and latest tags, and push these images to gitlab container registry of this repository
if commit was done to master branch through merge request - build image, tag it with pipeline id and push image to gitlab container registry
if someone tag master branch - build image and tag it with branch’s tag and push it to gitlab container registry
Regardless of trigger, resulted docker image must contain LABEL, key “maintainer” and value - name of person who triggered build

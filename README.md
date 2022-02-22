## Практическая работа Git Bash №1
1.	Создать папку
```
mkdir CV
```
2.	Зайти в папку
```
cd CV
```
3.	Создать 3 папки
```
mkdir folder1 folder2 folder3
```
4.	Зайти в любую папку
```
cd folder1
```
5.	Создать 3 txt файла
```
touch txt_1.txt txt_2.txt txt_3.txt json_1.json json_2.json
```
6.	Создать 2 json файла, несколькими командами последовательно
```
touch json_1.json && touch json_2.json
```
7.	Создать 3 папки
```
mkdir folder1_1 folder1_2 folder1_3
```
8.	Вывести список содержимого папки
```
ls -la
```
9.	Открыть любой txt файл
```
vim txt_3.txt
```
10.	Написать туда что-нибудь, любой текст
```
"i" welcome to my world
```
11.	Сохранить и выйти
```
"esc" :wq
```
12.	Выйти из папки на уровень выше
```
cd ..
```
13.	Переместить любой файл, который создали, в любую другую папку
```
mv txt_2.txt folder1_3
```
14.	Скопировать любой файл, который создали, в любую другую папку
```
cp json_1.json folder1_1
```
15.	Найти файл по имени
```
find ./ -type f -name "txt_3.txt"
```
16.	Просмотреть содержимое в реальном времени
```
tail -f folder1/txt_3.txt | grep -i insert folder1/txt_3.txt
```
17.	Вывести несколько первых строк из текстового файла
```
cat txt_3.txt | sed -n 1,2p
```
18.	Вывести несколько последних строк из текстового файла
```
cat txt_3.txt | sed -n 6,7p
```
19.	Просмотреть содержимое длинного файла
```
less txt_3.txt
```
20.	Вывести дату и время;
```
date
```
21.	Отправить http запрос на сервер;
```
curl -p 'https://reqres.in/api/users&page=1'
```
22.	Написать скрипт, который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13, 14;
```
touch script.sh
vim script.sh

#!/bin/bash
cd file_script
mkdir folder1 folder2 folder3
cd folder1
touch txt_1.txt txt_2.txt txt_3.txt
touch json_1.json && touch json_2.json
mkdir folder1_1 folder1_2 folder1_3
ls -la
mv txt_2.txt folder1_3
cp json_1.json folder1_1

chmod +x ./script.sh
./script.sh
```

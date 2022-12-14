# Инструкция по работе с Git

Git  - это программа, подготовленная для контроля версий с целью упростить управление проектом.

![Эмблема Гита](git.jpg)

## Создание нового репозитория

Чтобы создать новый репозиторий (инерциализировать) нужно ввести команду:

    git init

## Проверка актуального состояния репозитория.

  Для того, чтобы проверить в каком состоянии находится репозиторий нужно ввести команду:

    git status

## Создание записи в репозиторий

Для того чтобы перенести ожидающие изменения из рабочего каталога в раздел проиндексированных файлов, нужно ввести команду:

    git add

Для того чтобы сохранить изменеия в определенное место необхожимоо прописать после add имя файла:

    git add <имя файла>

## Сохранение записи.

Для того чтобы сохранить шаг изменений существует команда:

    git commid

* а следующая команда выполнит коммит и выведет на экран дополнительную информацию по созданному коммиту:

        git commit -m "message"

* а данная команда сохраняет ожмдающие изменения с выводом информации по созданному коммиту:

        git commit -аm "message"

## Отслеживание разницы.

Для того чтобы увидеть разницу между коммитами необходимо ввести следующую команду:

    git diff

Команда:

    git diff <hash1> <hash2>

позволяет отследить изменения между определенными коммитами

## Переключение между версиями коммита.

Для того чтобы переключиться на определенную версию коммита необходимо ввести команду:

    git checkout <hash>

для водвращения в действующую версию необходимо ввести:

    git checkout master

## История коммитов в данном репозитарии.

Для того чтобы посмотреть историю созданных в обратном хронологическом порядке коммитов в данном репозитарии необходимо ввести:

    git log

Варианты:

* git log --oneline
* git log --all
* git log --oneline --all

позволяют увидеть различные варианты истории сохранненых коммитов.

## Ветвление

Ветвление в Гит нужны для внесения изменений/добработки и правки информации, которую через какое-то время мы вольем в основную ветку master.

### Отображение всех имеющихся веток
Для показа всех веток используется комманда:

    git branch


### Создание новой ветки

Для того чтобы создать новую ветку необходимо ввести следующую комманду:

    git branch <branch_name>

### Удаление ветки

Для того чтобы после сляния веток удалить ненужную ветку необходимо ввести команду:

    git branch -d <branch_name>

### Переключение между ветками

Чтобы переключится на другую ветку необходимо ввести команду:

    git checkout <branch_name>

### Графическое отображение ветки

Для того чтобы увидеть в терминале графическое отображение ветвки небходимо ввести команду:

    git log --graph

Для того чтобы увидеть все ветвления в графическом отображении нужно ввести команду:

    git log --all --oneline --graph

### Слияние веток
Для того чтобы слить ветку в мастер необходимо выполнить следующую комманду:

    git merge <branch_name>

## Конфликт слияния и его разрешение.

Если при слиянии веток образовался конфликт данных который автоматически VSC не урегулировал, то необходимо вручную устранить конфликт с использованием 4-х вкладок.

* Первая из них примет существущую в ветке мастер информацию;
* Вторая заменить информацию на ту которая находится во вливаемолй ветке;
* Третья оставит все как есть;
* Четвертая скажет поработать руками и головой. 

## Удаленный репозиторий

Удаленные репозитории нужны для ...

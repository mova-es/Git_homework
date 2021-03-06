# Step-by-step guide to git / Инструкция по утилите git

*After installation of git please enter two commands in order to "introduce yourself"*

    git config --global user.name «Ваше имя англ буквами»

    git config --global user.email ваша_почта@example.com

*Create a Local Git Repository by running the __git init__ command:*

If you want Git to start tracking a file, run the following command:
 
    git add *filename*

Для экономии времени можно ввести первые два символа названия файла и нажать tab.

Также команду git add необходимо вводить каждый раз перед добавлением коммита.

Для создания коммита используется следующая команда:

    git commit -m "ваш комментарий"

Для просмотра всех коммитов введите команду: 

    git log
    
Для просмотра истории коммитов в виде графа используйте команду

    git log --graph

Для просмотра состояния текста в определенном коммите введите:

    git checkout xxxx,
    где xxxx - это первые четыре символа хэша коммита

Также git checkout используется для перехода на нужную ветку или в текущее состояние, например:

    git checkout master

Основная ветка по умолчанию называется "master".

Команда для вывода версии git:

    git --version

Для определения, какие файлы в каком состоянии находятся, используется команда:

    git status

Для просмотра разницы между текущим и сохраненным файлом используется команда:

    git diff

## Работа с ветками

Для отображения веток используется команда *git branch*, при этом знак (*) показывает активную ветку в списке.

Для создания новой ветки введите команду 

    git branch new_branch_name

Чтобы удалить ветку, воспользуйтесь следующей командой:

    git branch -d branch_to_delete
    
Для принудительного удаления ветки используется следующая команда:

    git branch -D branch_to_delete

Для перехода от ветки к ветке введите: 

    git checkout branch_name

Чтобы объединить branch_name с текущей веткой, воспользуйтесь следующей командой:

    git merge branch_name

## Игнорирование файлов

Для того, чтобы git игнорировал некоторые файлы, например, картинки, необходимо выполнить следующие шаги:
1. Создать файл .gitignore
2. В этом файле записать имя игнорируемого файла (адрес)
3. Добавить файл в репозиторий git add .gitignore
4. Создать коммит git commit -m "your_comment"
5. Готово!

## Работа с сервисом GitHub

Чтобы отправить кому-то репозиторий, можно воспользоваться сервисом GitHub.

Чтобы скопировать репозиторий с сайта, нужно скопировать ссылку и ввести в терминале команду *git clone (ссылка)*.
После этого необходимо поменять директорию с помощью команды *cd (название папки)*.

Чтобы загрузить свой репозиторий на сайт, можно воспользоваться тремя способами:
1. создать новый репозиторий 
2. вставить существующий
3. импортировать из другого репозитория

**Описание второго способа:**
ввести команды: 

git remote add origin (ссылка)
git branch -M main
git push -u origin main

Чтобы загрузить актуальную версию репозитория с гитхаб, используйте команду *git pull*.
Также эта команда после загрузки репозитория выполняет слияние веток.

**Краткая инструкция:**
1. Создать аккаунт на гитхаб
2. Создать локальный репозиторий
3. "Подружить" локальный и удаленный репозитории
4. Отправить (push) локальный репозиторий в удаленный, при этом необходимо авторизоваться на гитхаб
5. Внести изменения из другого места
6. Скачать (pull) актуальное состояние из удаленного репозитория

**Instruction:**
1. Create an accounton GitHub website
2. Create a local repository
3. Connect the local and the remote repositories
4. Upload (push) the local repository to the remote, at this time please sign in to your account on GitHub website
5. Modify necessary files from other PC
6. Download (pull) the updated version from remote repository

Порядок действий для выполнения pull request:
fork -> clone -> new branch -> commit -> push -> pull request 

Команда *pull request* используется для внесения изменений в репозиторий без доступа к нему, т.е. предлагаем внести изменения автору репозитория.

**Инструкция:**
1. Сделать копию репозитория на своем аккаунте с помощью команды fork.
2. Со своего аккаунта загрузить репозиторий в локальную папку.
3. Переключиться с локальной папки в клонированную.
4. Создать новую ветку.
5. В новой ветке создать новый файл, совершить необходимые действия.
6. Закоммитить изменения
7. Отправить изменения в свой аккаунт: git push --set-upstream origin (название ветки)
8. Предложить изменения хозяину репозитория -> compare and pull request.

Сейчас будет инструкция на английском языке и небольшой конфликт в ветках

**Instruction**
1. Create a repository copy in your account by running fork command
2. Clone the repository to the local folder
3. Change directory to the cloned folder
4. Create a new branch
5. Create a new file in the new branch and do necessary actions
6. Commit the changings
7. Push it to the account on github
8. Compare and pull request

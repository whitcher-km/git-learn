#git #learn 

#### Конфигурация
```sh
git config --global user.name "Andrey К"
git config --global user.email "1@1.com"
```

#### Инициализация проекта
```sh
git init .
```

#### Статус
```sh
git status
```

#### Добавить файлы к отслеживанию
```sh
git add file1.txt
git add *
git add .
```

#### Применить новые изменения (создать снимок)
```sh
git commit -m "First commit, Version 1"
```

#### История комитов
```sh
git log
#last commit
git log -1
# full info
git log -1 -p
```

#### Разница после **add** но перед коммитом
```sh
git diff --staged
```

#### Игнорирование
```sh
cat .gitignore
*.log
logs/
```

#### Загрузка на GitHub
создаём токен тут - https://github.com/settings/tokens
Используем токен при **git push**

```sh
git remote add origin https://github.com/whitcher-km/git-learn.git
git branch -M main
git push -u origin main
```
##### сохраняем токен
```sh
git config --global credential.helper store
```

##### посмотреть с чем связан репозиторий 
```sh
git remote -v
```
##### поменять привязку 
```sh
git remote set-url origin …
```

#### Ветвление
```sh
# Показать какие ветки есть
git branch
# Создание бренча
git branch имя_рек
# перейти на ветку
git checkout имя_рек
#создаnь и перейти 
git checkout -b имя_рек
# удалить ветку
git branch -d имя_рек
# слияние веток
git checkout main
git merge dev
```

#### Возврат на предыдущую версию
```sh
git chekout 11ace8bf0502543819bb7e005b3d4ac96f6bef6f
# вернуться на актуальную
git checkout main
# изменить прошлый комит
git commit --amend
# Жостко отменить все изменения последних 2-х коммитов
git reset --hard HEAD~2
# Стереть информацию о 3-х последнихкоммитах в логе физически оставив содержимое файлов
git reset --soft HEAD~3
```

#### Работа з GitHub
```sh
# клонирование репозитория
git clone https://github.com/whitcher-km/git-learn.git
# создаём новую ветку для локальных изменений

```

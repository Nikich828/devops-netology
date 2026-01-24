# Домашнее задание к занятию "`Системы контроля версий`" - `Лычагин Н.В.`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1
Создать и настроить репозиторий для дальнейшей работы на курсе
В рамках курса вы будете писать скрипты и создавать конфигурации для различных систем, которые необходимо сохранять для будущего использования. Сначала надо создать и настроить локальный репозиторий, после чего добавить удалённый репозиторий на GitHub.

Ответ:

1. Зарегистрируйте аккаунт на https://github.com/. Если предпочитаете другое хранилище для репозитория, можно использовать его.

```bash
    У меня уже был зарегестрирован аккаунт.
```
2. Создайте публичный репозиторий, который будете использовать дальше на протяжении всего курса, желательное с названием devops-netology. Обязательно поставьте галочку Initialize this repository with a README

![alt text](https://github.com/Nikich828/devops-netology/blob/main/1.jpeg)

3. Создайте авторизационный токен для клонирования репозитория.

```bash
    Уже был создан.
```
4. Склонируйте репозиторий, используя протокол HTTPS (git clone ...).
5. Перейдите в каталог с клоном репозитория (cd devops-netology).
![alt text](https://github.com/Nikich828/devops-netology/blob/main/2.jpeg)

6. Произведите первоначальную настройку Git, указав своё настоящее имя, чтобы нам было проще общаться, и email (git config --global user.name и git config --global user.email johndoe@example.com).
```bash
    Как только я сделал задание целиком, я заметил что пропустил этот пункт >_< ...
```
![alt text](https://github.com/Nikich828/devops-netology/blob/main/20.png)

7. Выполните команду git status и запомните результат.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/3.jpeg)

8. Отредактируйте файл README.md любым удобным способом, тем самым переведя файл в состояние Modified.
9. Ещё раз выполните git status и продолжайте проверять вывод этой команды после каждого следующего шага.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/4.jpeg)
```bash
    Файл README.md в состоянии (modified) и изменения не подготовлены для коммита (not staged).
```
10. Теперь посмотрите изменения в файле README.md, выполнив команды git diff и git diff --staged.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/5.jpeg)
```bash
    git diff показывает что удалена строка # devops-netology и добавлена # devops-netology123, а git diff --staged ничего не показывает т.к. изменения не добавлены в staged.
```
11. Переведите файл в состояние staged (или, как говорят, просто добавьте файл в коммит) командой git add README.md.
12. И ещё раз выполните команды git diff и git diff --staged. Поиграйте с изменениями и этими командами, чтобы чётко понять, что и когда они отображают.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/6.jpeg)
```bash
    Теперь git status показывает что файл готов к коммиту, git diff ничего не показывает т.к. изменения уже в индексе, git diff --staged показывает те же изменения, что ранее показывал git diff.

    Таким образом, подводя краткий итог:
    git diff - показывает изменения между рабочим каталогом и индексом
    git diff --staged - показывает изменения между индексом и последним коммитом
```
13. Теперь можно сделать коммит git commit -m 'First commit'.
14. И ещё раз посмотреть выводы команд git status, git diff и git diff --staged.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/7.jpeg)
```bash
    После коммита выводит данное сообщение: Your branch is ahead of 'origin/main' by 1 commit, это означает -  в локальном репозитории на 1 коммит больше, чем в удаленном (origin/main). Поэтому предлагает запушить, но это бдует дальше в задании.
```
### Создание файлов .gitignore и второго коммита

1. Создайте файл .gitignore (обратите внимание на точку в начале файла), проверьте его статус сразу после создания.
2. Добавьте файл .gitignore в следующий коммит (git add...).

![alt text](https://github.com/Nikich828/devops-netology/blob/main/8.jpeg)
```bash
    Вывод показывает, что мы добавили новый файл или перевели в состояние  staged.
```
3. На одном из следующих блоков вы будете изучать Terraform, давайте сразу создадим соотвествующий каталог terraform и внутри этого каталога — файл .gitignore по примеру: https://github.com/github/gitignore/blob/master/Terraform.gitignore.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/9.jpeg)
```bash
    Видим следующую ситуацию:

    .gitignore в staged, а terraform untracked files т.к мы не добавили каталог add .
```
4. В файле README.md опишите своими словами, какие файлы будут проигнорированы в будущем благодаря добавленному .gitignore

![alt text](https://github.com/Nikich828/devops-netology/blob/main/21.jpeg)

5. Закоммитьте все новые и изменённые файлы. Комментарий к коммиту должен быть Added gitignore.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/11.jpeg)


### Эксперимент с удалением и перемещением файлов (третий и четвёртый коммит)

1. Создайте файлы will_be_deleted.txt (с текстом will_be_deleted) и will_be_moved.txt (с текстом will_be_moved) и закоммите их с комментарием Prepare to delete and move.
2. В случае необходимости обратитесь к официальной документации — здесь подробно описано, как выполнить следующие шаги.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/12.jpeg)

![alt text](https://github.com/Nikich828/devops-netology/blob/main/13.jpeg)

3. Удалите файл will_be_deleted.txt с диска и из репозитория.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/14.jpeg)
```bash
    Вывод git status показывает, что файл удален.
```
4. Переименуйте (переместите) файл will_be_moved.txt на диске и в репозитории, чтобы он стал называться has_been_moved.txt.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/15.jpeg)
```bash
    В выводе добавилось, что файл переименован.
```
5. Закоммитьте результат работы с комментарием Moved and deleted.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/16.jpeg)

### Проверка изменения

1. В результате предыдущих шагов в репозитории должно быть как минимум пять коммитов (если вы сделали ещё промежуточные — нет проблем):
Initial Commit — созданный GitHub при инициализации репозитория.
First commit — созданный после изменения файла README.md.
Added gitignore — после добавления .gitignore.
Prepare to delete and move — после добавления двух временных файлов.
Moved and deleted — после удаления и перемещения временных файлов.
2. Проверьте это, используя комманду git log. Подробно о формате вывода этой команды мы поговорим на следующем занятии, но посмотреть, что она отображает, можно уже сейчас.
```bash
    Полный вывод
```
![alt text](https://github.com/Nikich828/devops-netology/blob/main/17.jpeg)
```bash
    Укороченный вывод
```
![alt text](https://github.com/Nikich828/devops-netology/blob/main/18.jpeg)

### Отправка изменений в репозиторий

Выполните команду git push, если Git запросит логин и пароль — введите ваши логин и пароль от GitHub.

В качестве результата отправьте ссылку на репозиторий.

![alt text](https://github.com/Nikich828/devops-netology/blob/main/19.jpeg)





### Приложение
# devops-netology123

## Игнорируемые файлы

Будут игнорироваться следующие файлы:

*.tfstate - все файлы, c раширением .tfstate будут проигнорированы (Пример - terraform.tfstate)
*.tfstate.* - все файлы, которые содержат в названии .tfstate. в названии (Пример - terraform.fstate.backup)
crash.log - файл с таким названием
crash.*.log - файл, где crash.любое название.log
*.tfvars - все файлы, c раширением .tfvars будут проигнорированы (Пример - variables.tfvars)
*.tfvars.json - все файлы с таким расширением
override.tf - файл с таким названием
override.tf.json - файл с таким названием
*_override.tf - файлы, которые заканчиваются на _override.tf (Пример - prod_override.tf)
*_override.tf.json - файлы, которые заканчиваются на _override.tf.json
.terraform.tfstate.lock.info - файл с таким названием
.terraformrc - файл с таким названием
terraform.rc - файл с таким названием

### Легенда

*- означает любые символы
*.расширение - означает все файлы с таким расширением
файл.* - означает все файлы, которые начинаются с этого имени
*_текст - означает все файлы, которые заканчиваются на этот текст
#- комментирование строки
!- означает исключени из правил, т.е файл наоборот не игнорируется
/ - в конце означает, что данное правило относится только к каталогам
### GIT
```
1. Создания депозитория git
git init

2. подготовленное (staged) 
git add <file>
git add <directory>
 
3. зафиксированное (committed)
git commit -m "added CommitTest.txt to the repo"

4. Просмотр состояния GIT
git status

5. Просмотр логов 
git log

6. Работа с деревьями  
git branch                     # list all branches
git branch <branch>            # create new one
git branch -d <branch>         # delete one
git checkout branch            # checkout to existing branch
git checkout -b <new-branch>   # create and checkout 

7. git merge <branch name>       # команда выполняется ИЗ ПРИНИМАЮЩЕЙ ветки, <branch name> - отдающая ветка
8. Итак, начнем с поиска правильной фиксации. Вы можете увидеть коммиты, которые внесли изменения в данный файл очень легко:

git log path/to/file

Если ваши сообщения о фиксации недостаточно хороши, и вам нужно посмотреть, что было сделано с файлом в каждой фиксации, используйте параметр -p/--patch:

git log -p path/to/file

Или, если вы предпочитаете графический просмотр gitk

gitk path/to/file

Вы также можете сделать это, как только вы запустили gitk через меню просмотра; одним из вариантов представления является список путей для включения.

В любом случае вы сможете найти SHA1 (хэш) коммита с версией нужного файла. Теперь все, что вам нужно сделать, это следующее:

# get the version of the file from the given commit
git checkout <commit> path/to/file
# and commit this modification
git commit

(Команда checkout сначала считывает файл в индекс, а затем копирует его в дерево работы, поэтому нет необходимости использовать git add, чтобы добавить его в индекс при подготовке к фиксации.)

Если ваш файл может не иметь простой истории (например, переименования и копии), см. замечание VonC. git может быть направлена ​​на поиск более тщательно для таких вещей, за счет скорости. Если вы уверены, что история простая, вам не нужно беспокоиться.

````

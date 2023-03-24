# report-02
Перед лабораторной рекомендуется выполнить:  
$ sudo apt install git  
$ sudo snap install sublim-text  
$ sudo apt install clang-format 

**task-1**  
1.Создать пустой репозиторий на git  
2.Создать локальный репозиторий mkdir ...  
 Выполнить команды со страницы на гите  
 echo "# test" >> README.md  
 git init  
 git add README.md  
 git commit -m "first commit"  
 git branch -M main  
 git remote add origin https://github.com/Fedorusita/test.git  
 git push -u origin main  
3. Создать cpp  
   touch hello_world.cpp  
   alias edit=subl  
   edit "hello_world.cpp"   
4. Добавим этот файл в лок. копию репозитория  
   git add "..."  
5. git commit -m "...."  
6. edit "hello_world.cpp"   
   изменить код  
8. git commit -a -m ".."  
9. git push -u origin main  


**task-2**
1. Локально создаём новую ветку   
    git checkout -b patch1  
2. edit "hello_world.cpp"  
   Вносим изменения     
3.  git commit -a -m "Fixed cpp file"  
    git push -u origin patch1  
4-5 Проверяем и делаем pr  
6. edit 'hello_world.cpp"  
   Вносим правки  
7.  git commit -a -m "Code with comments"     
    git push -u origin patch1   
8. Мержим и удаляем в удаленном репозитории  
9. git pull origin  
10. git log main   
11. git branch -d patch1  


**task-3**  
1. git checkout -b patch2   
2. clang-format -i -style=Mozilla "hello_world.cpp"  
3. git commit -a -m "Changed code style in cpp file"  
   git push -u origin patch2  
4. git checkout main    
   edit "Hello world.cpp" 
   git commit -a -m "Fixed cpp file"
   git push -u origin patch2  
5. git pull origin master  
   git rebase master  
   edit "hello_world.cpp"  
   git commit -a -m "Update code"  
6. git pull origin master  
   git rebase master  
   edit "Hello world.cpp"  
   git commit -a -m "Update Hello world.cpp"  
   git rebase --continue  
 7.Конфликты пропали.    




# Лабораторная работа №2 ТиМп
Выполнил Ерохин Павел ИУ8-23
#### Part 1.
    # создаем локальный репозиторий
    mkdir Lab_02
    cd Lab_02
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/FloydP1nk/Lab-02.git
    git push -u origin main
#
    touch hw.cpp
    //change hw.cpp
    git add -A
    git commit -m "add hw.cpp"
    //change hw.cpp
    git add -A
    git commit -m "add user name"
    git push origin main
    
#### Part 2.    
    git checkout -b patch1
    // change hw.cpp
    git add -A
    git commit -m "improve code style"
    git push origin patch1
##### *создаем pull-request*
    git add hw.cpp
    git commit -m "add comments"
    git push origin patch1
##### *Выполняем merge, удаляем ветку patch1 в удаленном репозитории*
    git checkout main
    git pull
    git branch -D patch1
    
#### Part 3.    
    git checkout -b patch2
    clang-format -style=Mozilla hw.cpp
    git add hw.cpp
    git commit -m "formated"
    git push origin patch2
##### *создаем pull-request*
##### *в ветке main изменем комментарий*
##### * в pull-request появились конфликты*
    git pull --rebase origin main
    git add -A
    git rebase --continue

![Снимок экрана 2023-03-09 в 03 31 27](https://user-images.githubusercontent.com/113801739/223884225-ead36940-b712-4234-9651-c24e0a875811.png)

    git push --force push origin patch2
    
![Снимок экрана 2023-03-09 в 03 32 50](https://user-images.githubusercontent.com/113801739/223884400-d15f22b7-dd45-4758-827a-68e4de938765.png)
    
    
    


# Инструкция по работе с Git
## Git - система управления версиями, с активной поддержкой и открытым кодом. Её создателем является [Линус Торвальдс](https://yandex.by/images/search?text=%D0%BB%D0%B8%D0%BD%D1%83%D1%81%20%D1%82%D0%BE%D1%80%D0%B2%D0%B0%D0%BB%D1%8C%D0%B4%D1%81%20%D1%84%D0%BE%D1%82%D0%BE&from=tabbar&p=1&pos=56&rpt=simage&img_url=https%3A%2F%2Fi2.wp.com%2Fwww.tfir.io%2Fwp-content%2Fuploads%2F2019%2F06%2Flinus-laugh.jpg%3Ffit%3D1920%252C1080%26ssl%3D1&lr=158)
![Logo](picture.png)
## Настройка программы: для начала работы, после установки программы мы вводим команды:
    git config --global user.name "Name"
    git config --global user.email "Usermail"

## Игнорирование файлов
В git вы сами решаете какие файлы и в какой коммит попадут, но возможно вы бы хотели, что бы определённые файлы никогда не попали в индекс и в коммит, да и вообще не отображались в списке не отлеживаемых. Для этого вы можете создать специальный файл (.gitignore) в вашем репозитории и записать туда шаблон игнорируемых файлов. как мы и сделали с картинкой выше.

## Создание репозитория

    git init — Создаёт git репозитории 
    git clone  <репозиторий> [<каталог>]  — Клонирует репозитории.

## Основные команды по работе с git 
    git status - получить информацию о его текущем состоянии
    git add - добавить файл к следующему коммиту
    git commit -m "message" - создание коммита
    git log - вывод на экран истории всех коммитов с их хэш-кодами
    git branch - посмотреть список веток
    git branch name - создать новую ветку
    git checkout name - переход к другой ветке
    git merge name - влить ветку
    git branch -d name - удалить ветку

## Ветвление в Git
Ветка в Git — это простой перемещаемый указатель на один из таких коммитов. По умолчанию, имя основной ветки в Git — master. Как только вы начнёте создавать коммиты, ветка master будет всегда указывать на последний коммит. Каждый раз при создании коммита указатель ветки master будет передвигаться на следующий коммит автоматически. Ветка «master» в Git — это не какая-то особенная ветка. Она точно такая же, как и все остальные ветки. Она существует почти во всех репозиториях только лишь потому, что её создаёт команда git init, а большинство людей не меняют её название.
    
**git log** не показывает все ветки по умолчанию
Если выполнить команду **git log** прямо сейчас, то в её выводе только что созданная ветка «testing» фигурировать не будет.

Ветка никуда не исчезла; просто Git не знает, что именно она вас интересует, и выводит наиболее полезную по его мнению информацию. Другими словами, по умолчанию **git log** отобразит историю коммитов только для текущей ветки.

Для просмотра истории коммитов другой ветки необходимо явно указать её имя: **git log testing** Чтобы посмотреть историю по всем веткам — выполните команду с дополнительным флагом: **git log --all.**

## Вспомогательные команды
    q - возврат в исходное окно терминала 
    clear - очистка окна терминала 
    
   ## Работа с удаленными репозиториями

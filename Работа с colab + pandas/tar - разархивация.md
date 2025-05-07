чтобы создать архив:
tar -cvf archive.tar /path/to/directory

-c - новый архив
-v - подробный режим (выводит список файлов во время архивирования)
-f указывает имя архива
Пример:
 tar -cvf archive.tar.(gz) /home/user/documents
* gz, xz, bz2

Извлечение:
* tar -xvf archive.tar
* tar -xvf archive.tar /path/to/desctiation


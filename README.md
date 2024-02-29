### ADB Homework

1. Отобразить подключенный девайс в консоли.  
```
./adb devices
```
2. Установить .apk файл приложения todolist на телефон с компьютера через  ADB
```
./adb install /e/platform-tools/apk/todolist/todolist.apk
```
3. Вывести адрес приложения todolist в системе Android  
```
./adb shell pm list packages | grep todolist
```
4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.
```
./adb exec-out screencap -p > /e/platform-tools/apk/todolist/screenshots/test.png
```
5. Вывести в консоль логи приложения todolist
```
./adb logcat | grep com.android.todolist
```
Выход: `Ctrl + C`  

6. Скопировать логи приложения todolist на компьютер.
```
./adb logcat | grep com.android.todolist > /e/platform-tools/apk/todolist/logs/logs.txt
```
Выход: `Ctrl + C`  

7. Удалить приложение todolist с телефона через ADB
```
./adb uninstall com.android.todolist
```


## ADB HW_1

 ##### 1. Отобразить подключенный девайс в консоли.
	
    adb devices
 
 ##### 2. Вывести адрес приложения todolist в системе Android

	adb shell pm list packages | grep todolist
 
 ##### 3. Установить .apk файл приложения todolist на телефон с компьютера через  ADB

	adb install /Users/yaroslav/Desktop/Todolist.apk

##### 4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.
	
    adb shell screencap /storage/emulated/0/DCIM/Screenshots/todo.png | adb pull /storage/emulated/0/DCIM/Screenshots/todo.png Desktop
 
 ##### 5. Вывести в консоль логи приложения todolist
	
    adb logcat | grep todolist
##### 6. Скопировать логи приложения todolist на компьютер
	
    adb logcat | grep todolist > Desktop/todolist.log
 ##### 7. Удалить приложение todolist с телефона через ADB
 
	adb uninstall com.android.todolist


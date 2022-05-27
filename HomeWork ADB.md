# HomeWork ADB (Android Debug Bridge)

## 1. Отобразить подключённый девайс в консоли.
	adb devices
    ------------------------------------
	List of devices attached
	emulator-5554   device

 ## 2. Вывести адрес приложения reminder в системе Android
    adb shell pm list packages "reminder" 
    ------------------------------------
    package:com.qrolic.reminderapp 

 ## 3. Установить .apk файл приложениия reminder на телефон с компьютера через  ADB
	adb install C:\Users\Evgeniy\Downloads\android_reminder-main\android_reminder-main\app\build\outputs\apk\debug\app-debug.apk
    ------------------------------------
	Performing Streamed Install
	Success

 ## 4. Сделать скриншот запущенного приложения reminder и сразу скопировать на компьютер в одной команде.
	adb shell screencap /sdcard/screenshot.png & adb pull /sdcard/screenshot.png C:/Users/ 
    ------------------------------------
	/sdcard/screenshot.png: 1 file pulled, 0 skipped. 25.9 MB/s (63768 bytes in 0.002s)

 ## 5. Вывести в консоль логи приложения reminder
	adb logcat "com.qrolic.reminderapp"
	
 ## 6. Скопировать логи приложения reminder на компьютер.
	adb logcat "com.qrolic.reminderapp" > C:/Users/reminder.log

 ## 7. Удалить приложение todolist с телефона через ADB
	adb shell pm uninstall "com.qrolic.reminderapp"
    ------------------------------------
	Success
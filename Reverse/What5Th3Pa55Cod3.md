# What5Th3Pa55Cod3?

1. Download the mysecret.apk
2. Download the `jadx` zip file [java decompiler](https://github.com/skylot/jadx/releases/tag/v1.2.0)
3. convert .apk > .rar/.zip
4. open the .dex file using `jadx` offline decompiler. 
![image](https://user-images.githubusercontent.com/59368650/138647691-875069eb-e98e-4e51-b604-96773164dc89.png)

5. Read the `Mainactivity` and `Main2activity` funtion. you can see there are two if() statement that are comparing the string. So, the 1st passCode is `6666`, 2nd birthdayCode is `19971025` 
![image](https://user-images.githubusercontent.com/59368650/138647839-f98b6f37-0529-4238-b190-b9033cf93150.png)

6. run the apk file using [online tools](https://appetize.io/upload)
7. enter the passcode and the birthday, we got flag!









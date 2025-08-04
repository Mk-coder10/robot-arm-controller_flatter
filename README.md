#  Robot Arm Controller

A Flutter + PHP web backend project to control a robotic arm using servo motor values.

---

##  Project Structure

robot_arm_project/
├── flutter_app/ # Flutter UI for controlling arm
├── backend_php/ # PHP scripts + database logic


---

## 💻 Setup Instructions

### 🔹 PHP Backend

1. Install [XAMPP](https://www.apachefriends.org/index.html)
2. Copy contents of `backend_php/` to:
C:\xampp\htdocs\robot_arm\

3. Start **Apache** from XAMPP Control Panel.

4. Create MySQL database with:

```sql
CREATE DATABASE robot_arm;
USE robot_arm;

CREATE TABLE poses (
  id INT AUTO_INCREMENT PRIMARY KEY,
  motor1 INT,
  motor2 INT,
  motor3 INT,
  motor4 INT
);

```

 Flutter App
1.Open the flutter_app/ folder in VS Code or Android Studio

2.Make sure pubspec.yaml includes the http package:
```
dependencies:
  flutter:
    sdk: flutter
  http: ^0.13.6
  ```
3.Add this permission to AndroidManifest.xml:

```
<uses-permission android:name="android.permission.INTERNET"/>
```
4.Run the app:
```
flutter pub get
flutter run
```
Make sure your emulator is running and your local server is accessible via http://10.0.2.2/.

<uses-permission android:name="android.permission.INTERNET"/>

### 📱 App Screenshot
<img src="https://github.com/user-attachments/assets/91a62126-0271-4aab-ae49-579e345c1366" width="250" alt="Robot Arm App UI" />



 Built With
 ```
Flutter (frontend)
PHP (backend)
MySQL (database)
XAMPP (local server)
```

TravelPass -- Traveller Login & Profile
Project Overview
TravelPass is an Android application developed using Kotlin and
XML layouts. It allows travellers to log in, manage a personal
profile, choose travel preferences, and save those preferences locally
using SharedPreferences.
Features
- Login: Username and password fields with input validation.
- Remember Me: Saves the username and restores it when the app is
  reopened.
- Traveller Profile: Enter a full name and select a preferred
  distance unit.
- Travel Alerts: Enable or disable travel alert preferences.
- Welcome Screen: Displays a personalized greeting and saved
  preferences.
- Options Menu: Provides Edit Profile, Settings, and Logout
  actions.
- Settings: Update distance units and travel alert preferences.
- Logout: Confirms the action, clears saved login information, and
  returns to the login screen.
Technologies and Android Components
  Technology / Component     Purpose
  Android Studio             Development environment
Kotlin                     Application programming language
XML Layouts                User interface design
SharedPreferences          Local key-value data storage
Explicit Intents           Navigation between activities
EditText                   Username, password, and name input
CheckBox                   Remember Me and Travel Alerts
RadioGroup / RadioButton   Distance unit selection
Options Menu               Edit Profile, Settings, and Logout
AlertDialog                Logout confirmation
Toast                      Short status and validation messages
Application Screens
1. MainActivity -- Login: Accepts username and password and
   provides the Remember Me option.
2. ProfileActivity -- Traveller Profile: Collects the traveller's
   name, distance unit, and travel alert preference.
3. WelcomeActivity -- Welcome: Shows the saved traveller name and
   preferences.
4. SettingsActivity -- Settings: Allows the user to update distance
   unit and travel alert preferences.
Application Navigation
MainActivity (Login)
        |
        v
ProfileActivity
        |
        v
WelcomeActivity
   /      |       \
  v       v        v
Edit    Settings  Logout
Profile    |        |
  |        v        v
  +----> Welcome  MainActivity
Local Data Storage
The application uses the SharedPreferences file TravelPassPrefs.

  Preference key     Data type   Description
  remember_me      Boolean     Whether Remember Me is selected
saved_username   String      Saved login username
profile_name     String      Traveller's full name
unit_distance    String      Selected distance unit (km or mi)
receive_alerts   Boolean     Whether travel alerts are enabled

The same preference file and keys should be used consistently wherever
the application reads or updates these values.
Project Structure
TravelPass/
├── app/
│   └── src/
│       └── main/
│           ├── java/com/example/travelpass/
│           │   ├── MainActivity.kt
│           │   ├── ProfileActivity.kt
│           │   ├── WelcomeActivity.kt
│           │   └── SettingsActivity.kt
│           ├── res/
│           │   ├── layout/
│           │   │   ├── activity_main.xml
│           │   │   ├── activity_profile.xml
│           │   │   ├── activity_welcome.xml
│           │   │   └── activity_settings.xml
│           │   ├── menu/
│           │   │   └── main_menu.xml
│           │   ├── drawable/
│           │   └── values/
│           └── AndroidManifest.xml
└── README.md
The package path and resource files shown above should match the actual
project structure.
Setup and Run
1. Install Android Studio.
2. Clone or download this repository.
3. Open the TravelPass project in Android Studio.
4. Allow Gradle to sync.
5. Start an Android emulator or connect an Android device with USB
   debugging enabled.
6. Select the app configuration and click Run.
Build Verification
To build the debug APK from the project root, run:
./gradlew app:assembleDebug
On Windows Command Prompt or PowerShell:
gradlew.bat app:assembleDebug
The project build was reported as successful with 0 compilation
errors. Runtime behavior should also be tested on an emulator or
physical device.
Test Checklist
- [ ] Empty username and password validation
- [ ] Remember Me saves and restores the username
- [ ] Profile details are saved
- [ ] Welcome screen displays saved details
- [ ] Edit Profile opens the profile screen
- [ ] Settings updates are reflected on the welcome screen
- [ ] Logout confirmation works
- [ ] Logout clears saved login information
- [ ] Back navigation does not reopen the logged-out welcome screen
Future Enhancements
- Google Maps integration
- Destination recommendations
- Weather information
- Hotel and restaurant recommendations
- Online authentication and cloud synchronization
  
Developer
Name: Gayathri R
Course: Master of Computer Applications (MCA)
University: Jain University

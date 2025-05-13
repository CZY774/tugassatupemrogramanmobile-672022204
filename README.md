# Android Login Form - Mobile Programming Assignment

![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-0095D5?&style=for-the-badge&logo=kotlin&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white)

## 📱 Project Overview

A modern Android login form built with Jetpack Compose for a university mobile programming assignment. The application features a clean, user-friendly interface with form validation and appropriate user feedback.

## ✨ Features

- **Modern UI with Jetpack Compose**
  - Material 3 design components
  - Responsive layout
  - Light/Dark theme support

- **Complete Form Fields**
  - Full Name input
  - Username input
  - Password input with visibility toggle
  - Confirm Password with visibility toggle
  - Register button

- **Form Validation**
  - Required field validation
  - Password length validation (minimum 6 characters)
  - Password matching validation
  - Real-time error clearing as user types

- **User Feedback**
  - Success toast messages
  - Error toast messages with specific feedback
  - Visual error indicators
  - Fields automatically clear after successful submission

## 🖼️ Screenshots

<table>
  <tr>
    <td>Empty Form</td>
    <td>Validation Errors</td>
    <td>Success State</td>
  </tr>
  <tr>
    <td><img src="/api/placeholder/200/400" alt="Empty Form" /></td>
    <td><img src="/api/placeholder/200/400" alt="Validation Errors" /></td>
    <td><img src="/api/placeholder/200/400" alt="Success State" /></td>
  </tr>
</table>

## 🔧 Technical Details

- **Language**: Kotlin
- **UI Framework**: Jetpack Compose
- **Minimum SDK**: 24
- **Target SDK**: 35
- **Architecture**: MVVM (Model-View-ViewModel)
- **Build System**: Gradle with Kotlin DSL

## 📁 Project Structure

```
app/
├── src/
│   ├── main/
│   │   ├── java/com/czy/tugassatupemrogramanmobile/
│   │   │   ├── MainActivity.kt              # Main activity with login screen
│   │   │   └── ui/theme/                    # Theming components
│   │   │       ├── Theme.kt                 # Color schemes and theme data
│   │   │       └── Typography.kt            # Text styles
│   │   └── res/                             # Resources
│   └── androidTest/                         # Instrumentation tests
└── build.gradle.kts                         # App module build configuration
```

## 🚀 Getting Started

### Prerequisites

- Android Studio Hedgehog (2023.1.1) or newer
- JDK 11 or higher
- Android SDK 35

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/android-login-form.git
   ```

2. Open the project in Android Studio.

3. Sync Gradle files.

4. Run the app on an emulator or physical device.

## 💡 Implementation Details

### Form Validation Logic

```kotlin
// Validate fields
var isValid = true

if (fullName.isEmpty()) {
    fullNameError = "Full name is required"
    isValid = false
}

if (username.isEmpty()) {
    usernameError = "Username is required"
    isValid = false
}

if (password.isEmpty()) {
    passwordError = "Password is required"
    isValid = false
} else if (password.length < 6) {
    passwordError = "Password must be at least 6 characters"
    isValid = false
}

if (confirmPassword.isEmpty()) {
    confirmPasswordError = "Please confirm your password"
    isValid = false
} else if (confirmPassword != password) {
    confirmPasswordError = "Passwords do not match"
    isValid = false
}
```

### Jetpack Compose UI Components

The project utilizes various Jetpack Compose components:
- `OutlinedTextField` for input fields with error states
- Material Icons for field decoration
- `Button` for form submission
- Toast messages for user feedback

## 🔍 Future Enhancements

- Implement database integration with Room
- Add fingerprint authentication
- Create a "Remember Me" feature
- Implement network-based authentication
- Add animations for smoother UX

## 📝 Assignment Requirements

This project was created to meet the following requirements:
- Create a login form with required fields
- Implement proper validation
- Provide user feedback for success/failure
- Clear fields after successful submission
- Use Jetpack Compose for a modern UI

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

- Your Name - [GitHub Profile](https://github.com/yourusername)

---

*This project was created as part of a university mobile programming course using Kotlin.*

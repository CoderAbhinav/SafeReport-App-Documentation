## Implementation Details

## Project Dependencies

```
Flutter version: x.x.x
GetX package version: x.x.x
Firebase Authentication package version: x.x.x
Firebase Cloud Firestore package version: x.x.x
```

## Project Architecture

This project follows the GetX architecture pattern which consists of Models, Views, Controllers, and Services.

## Folder Structure

```
lib/
  |- controllers/
      |- auth_controller.dart
      |- report_controller.dart
  |- models/
      |- user.dart
      |- report.dart
  |- services/
      |- firebase_service.dart
  |- views/
      |- login_view.dart
      |- report_view.dart
      |- home_view.dart
  |- main.dart

```

## Models
1. User: Represents the user with properties such as name, email, and role.
2. Report: Represents a report with properties such as title, description, and timestamp.


## Controllers
1. AuthController: Handles the authentication logic for the app using Firebase Authentication.
2. ReportController: Handles the reporting logic for the app using Firebase Cloud Firestore.

## Services
1. FirebaseService: Handles the communication with Firebase Authentication and Cloud Firestore.

## Views
1. LoginView: Allows the user to login to the app using their phone number.
2. ReportView: Allows the user to create a report about sexual harassment or discrimination.
3. HomeView: Displays the list of reports for the organization and allows the user to resolve them.
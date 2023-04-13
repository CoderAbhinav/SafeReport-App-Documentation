## Implementation Details

## Project Dependencies

```
dependencies:
  flutter:
    sdk: flutter

  cupertino_icons: ^1.0.2
  firebase_core: ^2.8.0
  firebase_auth: ^4.3.0
  firebase_database: ^10.0.16
  cloud_firestore: ^4.4.5
  google_fonts: ^4.0.3

```

## Project Architecture

This project follows the GetX architecture pattern which consists of Models, Views, Controllers, and Services.

## Folder Structure

```
lib/
  |- controllers/
      |- auth_controller.dart
      |- search_view_controller.dart
      |- employee_view_controller.dart
      |- organisation_view_controller.dart
  |- models/
      |- report.dart
      |- organisation.dart
  |- services/
      |- firebase_auth_service.dart
      |- firebase_database_service.dart
  |- views/
      |- components/
            |- buttons.dart
            |- headers.dart
      |- authentication_views/
            |- input_mobile_no.dart
            |- input_otp.dart
      |- common_views/
            |- search.dart
            |- report_detail.dart
            |- organisation_detail.dart
      |- employee_views/
            |- feed.dart
            |- file_report.dart
            |- my_reports.dart
            |- profile.dart
      |- organisation_views/
            |- feed.dart
            |- reports.dart
            |- profile.dart
      |- landing_view.dart
  |- utils/
      |- size_util.dart
      |- formatters.dart
      |- validators.dart
      |- theme.dart
  |- main.dart

```

## Models

### Organisation User Model
```
Organisation {
    uid: str, // uid from firebase user
    organisation_name: str,
    organisation_desc: str,
    website: str,
    counts: {
        registerd_sexual_harassment: int,
        resolved_sexual_harassment : int,
        ...
    },
    scores: {
        overall_score: int,
        sexual_harassment_score: int,
        ...
    }
}
```

### Report Model
```
Report{
    victim_uid: str, // will be uid of firebase user
    subject : str,
    catagory: str,
    description: str,
    filing_timestamp : DateTime,
    action_log : [
        {
            "action_type" : str [received | resolving| waiting_for_confirmation | resolved]
        }
    ],
    visibility : str [public | private],
    case_status : {
        closed : bool,
        closing_time_stamp : DateTime,
    },
}
```


## Controllers
1. AuthController: Handles the authentication logic for the app using Firebase Authentication.
2. EmployeeViewController: Handles the employee related operations such as showing custom feed, filing report, resolution confirmation etc.
3. OrganisationController: Handles the organisation related operations such as changing name, adding website, view & resolve issues, make cases public etc.

## Services
1. FirebaseService: Handles the communication with Firebase Authentication and Cloud Firestore.

## Views


## Overall Flow
![overall_flow](/assets/SafeReportFlow.png)
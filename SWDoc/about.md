# SafeReport

SafeReport is an app that allows users to anonymously report incidents of sexual harassment, discrimination, and other related issues to their organization. The app uses Flutter and Firebase for data storage and communication with the hardware device built in-house.

## Features

1. User registration with phone number
2. Option to register as an organization or an employee
3. Organizations can view reports from their employees
4. Employee identities are hidden to ensure anonymity
5. Organizations can add the phone numbers of their employees to the app
6. Reports deduct points from the organization
7. Daily panelty is deducted based on how many days it takes to resolve the issue
8. Rewards or increment in the organization score is given once the issue is solved
9. Scoring policy is based on response time, resolution time, frequency of issues, and employee feedback

## Installation

```
Clone the repository
Run flutter packages get to install the required packages
Set up Firebase in the app
Run the app on a physical device or emulator
```


## Usage

1. Register with your phone number
2. Select whether you want to register as an organization or an employee
3. If registering as an organization, fill out the basic information
4. If registering as an employee, wait for the organization to add your phone number
5. Create a report if you experience sexual harassment or discrimination
6. The report is shared with the organization anonymously
7. Organizations can view reports and take action to resolve them
8. The organization's score is determined based on response time, resolution time, frequency of issues, and employee feedback

## Future Enhancements

1. Integration with other messaging platforms such as WhatsApp or Slack to make it easier for employees to report issues
2. Integration with HR management systems to track the progress of reported issues
3. Integration with law enforcement agencies to allow employees to report incidents directly to them
4. Option to provide feedback on how the organization handled the issue

## [Implementation Details](/SWDoc/implementation.md)
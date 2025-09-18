# Discovery Meeting on 9/18/2025
## Meeting Start Time
**2025/09/18/03:30PM**

## Meeting End Time

**2025/09/18/04:10PM**

## Location/Medium

Zoom

## Present

 - James Ramsey
 - Jason Yoder
 - Josh Miller
 - Nolan Meyer
 - Kareline Jones
 - Jake King

## Minute Recorder

Jason Yoder

## Topics Discussed

- Introductions
- Jake (client) wants to communicate via Discord
- Teck stack
    - Flutter/Dart because the long term goal is to deploy to iOS and Android as well as host it as a web app. Flutter/Dart is a framework that helps with cross-platform development
    - Supabase backend (will be set up by Jake and access will be given to team when we get there)
- Jake wants access to all the code so he can give us pointers and help out if our team needs it.
- Heavy enphasis on abstraction and encapsulation for working with components
    - Each component should have it's own file and be called upon
- Jake wants very clean code and comments/docs to be able to navigate codebase easily
- Suggested we watch a Flutter/Dart tutorial to get a feel for setting up a project and the syntax
- IDE should be Android Studio or IntelliJ
- When using the app it should look like:
    - Go to an empty machine, put in dirty clothes
    - From app you can pay for the machine
    - App will use Nayax API for loyalty card that can have funds loaded to it
    - Machine will receive the payment
    - User can start the machine
    - User will get notified when the machine is finished
- Similar app is CSC Go (only other market competitor)
- Talked about how to test this app without physical machines
    - Probably buy some NFC cards to test that features
- Discussed logos and color assets to use, client will send those after meeting
- Coca Cola app uses Nayax API (if we want to investigate how it's workflow is)

## Things Clarified
 - Payment is not a tap to pay, rather a QR code or a API call in app
 - Loyalty card is for payment funds (loadded from Google/Apple pay) and rewards for every x amount of washes
 - General pay for machine functionality is higher priority than map functionality for now (only 1 location open)

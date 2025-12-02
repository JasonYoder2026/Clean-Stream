# Development Environment Manual

## How does the System work?

We are using multiple different technologies to make this happen. We are using [Supabase](https://supabase.com/docs/reference/dart/introduction) as our back end to handle user authentication. We will be using [Nayax](https://developerhub.nayax.com) to handle our payment processing as well as communicating with the laundry machines on the device. The language that this will be written in is [Dart](https://dart.dev/docs) utalizing the [Flutter](https://flutter.dev/?utm_source=google&utm_medium=cpc&utm_campaign=brand_sem&utm_content=na_us&gclsrc=aw.ds&gad_source=1&gad_campaignid=12961050228&gbraid=0AAAAAC-INI98espIDFsODzFO_aWp0EhpI&gclid=CjwKCAjw3tzHBhBREiwAlMJoUt8vkUU3NjmCHJG-pewF5kNrfZzxmrRCREMAxcXoAR-l6n7s3j0dGRoCmG0QAvD_BwE) framework. 

## Install Prerequisites

* We recommended installing [Android Studio](https://developer.android.com/studio?gclsrc=aw.ds&gad_source=1&gad_campaignid=21831783525&gbraid=0AAAAAC-IOZkwrUYtBbUxwVwTQTcwtHKqh&gclid=CjwKCAjw3tzHBhBREiwAlMJoUlUqWZvUnSc3QmXnzmvaXCqed31h13VPWRSIrh4R3v5epIR4NE2qcxoCW-8QAvD_BwE) for development of this project, as it is easy to use phone emulators with. You can also use [IntelliJ IDEA](https://www.jetbrains.com/idea/download/) as Android Studio is a fork of it, but are limited to browser testing.
  * In either Android Studio or IntelliJ IDEA, whichever you choose:
    * Navigate to File -> Settings
    * Go to the Plugins tab
    * Search for and install these plugins
      * Flutter
      * Dart
    * Restart your IDE for these to take affect
* We also recommend downloading [GitHub Desktop](https://desktop.github.com/download/).

## Clone Project
First step is going to be to go to the [repository](https://github.com/jamaki604/CleanStreamLaundryApp/tree/AutoLogIn) on GitHub. Once you get there you'll click on code then open with GitHub desktop.

<img width="1501" height="801" alt="Screenshot 2025-10-21 at 2 30 35 PM" src="https://github.com/user-attachments/assets/f2e2c7a0-e443-4cf0-b3a1-206b6ce4870b" />

Once you get into GitHub desktop you will click clone repository to clone it.


## Flutter Installation

### Mac
To install Flutter on Mac you will need to use Homebrew. To install Homebrew place this into your terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

After that is complete you'll want to run this in your terminal then you're good to go! 
```
brew install --cask flutter
```

### Windows
To install Flutter on Windows:
- Download the zip file [here](https://docs.flutter.dev/install/manual)
- Unzip the folder
- Move it to a directory that doesn't require administrative privlege to access (C:\Flutter works great), remember this directory!
- Add Flutter to your System PATH variable
  - Press the Windows key
  - Search "env"
  - Click "Edit the system envionment variables"
  - Click Environment Variables
  - <img width="557" height="581" alt="image" src="https://github.com/user-attachments/assets/322cd929-0207-4a6e-a403-49e321575c55" />
  - Click Path in the System variables screen
  - Click Edit...
  - <img width="708" height="780" alt="image" src="https://github.com/user-attachments/assets/fdfb621a-1ceb-4694-bbbb-f6f99473634b" />
  - Click New
  - Paste the path that leads to your Flutter file (C:\YOUR_LOCATION\Flutter\bin)
  - Verify the path is updated
  - <img width="590" height="657" alt="image" src="https://github.com/user-attachments/assets/d571ab7c-e2be-4e03-a6fe-06dfe432dfae" />
  - Click Ok three (3) times
  - Restart your computer to make sure the PATH variable gets updated

### Get Dependencies 
The first step will be to open this project in Andriod Studio, This project uses multiple different dart/flutter packages. Flutter has a very easy package manager system. In the terminal of Andriod studio run the command: 

```
flutter pub get 
```
This will install all of the dependencies. 

### Test
Once you have completed these steps you can run the command:
```
flutter test
```
You should see a result that looks something like this: 
<img width="632" height="240" alt="Screenshot 2025-10-21 at 2 29 12 PM" src="https://github.com/user-attachments/assets/ad2cadf7-5998-4a91-a628-d701c2d01ae2" />

## Important Files

### Environment file
Inside of the root of the project structure you will need to create a .env file. This is where you will store the API keys that are needed by the program to run. It should look something like this: 

```
SUPABASE_URL= "Supabase URL goes here"
ANON_KEY="ANON Key goes here"
STRIPE_PUBLISHABLE_KEY="Stripe public key goes here"
```
Contact Jake King for the URL, ANON KEY and Stripe publishable key - motokingjr@sbcglobal.net
## Folder structure
Our current folder structure looks like this:


<img width="455" height="688" alt="image" src="https://github.com/user-attachments/assets/632417ac-dece-4151-a7d5-bce5c2a6be73" />


All of our src code will go inside of the lib folder.

### Widgets
This is where all of our UI reusable widgets are housed

### Logic 
This is where all of our back end logic resides. Each subfolder is a specific feature that has been developed.

* Authentication: All authentication logic
* QrScanner: All the logic for our qr scanner.

### Middleware
This is where all of the controllers that UI uses to communicate with our backend reside. 

### Pages
This is where all of our UI pages reside.

### Testing
This folder will have the exact same structure as inside of our lib folder. Only difference is that this directory will be where all of our tests reside. 

## Running the Project

- You can use either a browser or phone emulator to run and test the code
- To use a browser:
  - Click the three lines next to the debug button
  - <img width="915" height="467" alt="image" src="https://github.com/user-attachments/assets/79441b25-7d87-4e39-987b-5075ab490dcc" />
  - Click "Edit"
  - In the "Additional run args:" field enter "--web-port=8080"
  - <img width="867" height="508" alt="image" src="https://github.com/user-attachments/assets/1a030f16-d86b-4987-90dc-b577246e0b8c" />
  - Click "Ok"
  - Select a web browser from the dropdown to run the code on
  - Run main.dart<br>
  <img width="827" height="303" alt="image" src="https://github.com/user-attachments/assets/e7f9784a-6c36-4a9c-a164-1b984d02462f" /><br>
- To use a phone emulator you need to use Android Studio
  - On the right open Device Manager
  - <img width="783" height="673" alt="image" src="https://github.com/user-attachments/assets/a9558d6b-d2aa-469c-b4c0-916b5b4f18d1" />
  - Click Add a new Device
  - <img width="447" height="837" alt="image" src="https://github.com/user-attachments/assets/6218ee11-f325-456e-a88b-f6e63b0df935" />
  - Select Create Virtual Device
  - Choose a device, Pixel 6 Pro is an average size screen so it's great for testing
  - Click Next
  - Name the device if you want
  - Choose a System Image (you'll probably have to download it)
    - Recommended to pick a version of Android 12 to make sure the app is compatible with some older versions
  - Once it is downloaded click Finish
  - Select the new device in the Device Manager and click Start
  - Once it is booted you will see it as an option for the run source at the top of the screen
  - Select the device from the dropdown and run main.dart

# Replicating via Docker

## Install prerequisites
- Download and install Docker Desktop
  - https://www.docker.com/products/docker-desktop/
  - Instructions for specific OSs are below
    - Windows: https://docs.docker.com/desktop/setup/install/windows-install/
    - MacOS: https://docs.docker.com/desktop/setup/install/mac-install/
    - Linux: https://docs.docker.com/desktop/setup/install/linux/
- After running the executable and installing, start Docker
## Clone the repository
- Clone the Clean Stream Laundry repository
  - ``` git clone https://github.com/jamaki604/CleanStreamLaundryApp.git ```

## Run
- From the root of the repository run:
  - ``` docker compose up --build ```
- Note: the initial build can take some time
- If you get prompted for networks accessing the app, allow it
- Navigate to localhost:8080 in a browser, there you will see the webapp
- Note: Only the webapp can be ran using Docker, as emulators require virtualization to run






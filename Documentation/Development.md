# Development Environment Manual

## How does the System work?

We are using multiple different technologies to make this happen. We are using [Supabase](https://supabase.com/docs/reference/dart/introduction) as our back end to handle user authentication. We will be using [Nayax](https://developerhub.nayax.com) to handle our payment processing as well as communicating with the laundry machines on the device. The language that this will be written in is [Dart](https://dart.dev/docs) utalizing the [Flutter](https://flutter.dev/?utm_source=google&utm_medium=cpc&utm_campaign=brand_sem&utm_content=na_us&gclsrc=aw.ds&gad_source=1&gad_campaignid=12961050228&gbraid=0AAAAAC-INI98espIDFsODzFO_aWp0EhpI&gclid=CjwKCAjw3tzHBhBREiwAlMJoUt8vkUU3NjmCHJG-pewF5kNrfZzxmrRCREMAxcXoAR-l6n7s3j0dGRoCmG0QAvD_BwE) framework. 

## Install Prerequisites

* We recommended installing [Android Studio](https://developer.android.com/studio?gclsrc=aw.ds&gad_source=1&gad_campaignid=21831783525&gbraid=0AAAAAC-IOZkwrUYtBbUxwVwTQTcwtHKqh&gclid=CjwKCAjw3tzHBhBREiwAlMJoUlUqWZvUnSc3QmXnzmvaXCqed31h13VPWRSIrh4R3v5epIR4NE2qcxoCW-8QAvD_BwE) for development of this project.
* We also recommend downloading [GitHub Desktop](https://desktop.github.com/download/).

## Clone Project
First step is going to be to go to the [repository](https://github.com/jamaki604/CleanStreamLaundryApp/tree/AutoLogIn) on GitHub. Once you get there you'll click on code then open with GitHub desktop.

<img width="1501" height="801" alt="Screenshot 2025-10-21 at 2 30 35 PM" src="https://github.com/user-attachments/assets/f2e2c7a0-e443-4cf0-b3a1-206b6ce4870b" />

Once you get into GitHub desktop you will click clone repository to clone it.


## Flutter Installation

### Mac
To install flutter on Mac you will need to use Homebrew. To install Homebrew place this into your terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

After that is complete you'll want to run this in your terminal then you're good to go! 
```
brew install --cask flutter
```

### Windows


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
```

## Folder structure
Our current folder structure looks like this:


<img width="911" height="711" alt="Screenshot 2025-10-21 at 2 41 57 PM" src="https://github.com/user-attachments/assets/73deec8e-1a55-4432-b2c6-3be93949ef3c" />

All of our src code will go inside of the lib folder.

### Components
This is where all of our UI componets are housed

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













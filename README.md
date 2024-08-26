## VitalTrack

## Overview
VitalTrack is an Android application designed to help users monitor their health metrics, such as steps, heart rate, and calories burned. Built with Kotlin, this app integrates Firebase for real-time data synchronization and Jetpack Compose for a modern, responsive user interface.

## Architecture
The app follows the MVVM (Model-View-ViewModel) architecture pattern, which promotes a clean separation of concerns and enables easy testing. The architecture is structured as follows:

**Model**: Contains the data models for health metrics. This layer also interacts with Firebase to store and retrieve data.
**View**: Composed of Jetpack Compose UI components, the View layer is responsible for displaying data to the user. It observes the ViewModel for any changes and updates the UI accordingly.
**ViewModel**: Acts as a bridge between the Model and View layers. It retrieves data from the Model and prepares it for display in the View. The ViewModel also handles user input and updates the Model as necessary.
Major Implementations
J**etpack Compose**: The UI is built using Jetpack Compose, which allows for a declarative approach to UI development. Components like LazyColumn are used for displaying lists of health metrics, and State is leveraged for managing UI states.
**Firebase Integration**: Firebase is used for both authentication and real-time data storage. User health metrics are stored in Firestore, and changes to the data are immediately reflected in the app thanks to Firebase's real-time capabilities. Firebase Authentication handles user sign-in, ensuring secure access to personal data.
**Health Data API**: The app uses Android's Health Data API to retrieve metrics like steps and heart rate directly from the user's device. This data is then processed and displayed in the UI.

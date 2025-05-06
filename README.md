# 📱 Image Loader Project

**By:** Nguyễn Quang Sáng
**Student ID:** 22110067

---

## 📌 Overview

This Android application demonstrates how to load and display an image from a user-provided URL using `AsyncTaskLoader` for efficient background processing. It also handles internet connectivity changes, shows appropriate UI feedback, and provides a smooth user experience.

---

## 🚀 Features

1. **Image Loading with AsyncTaskLoader**

   * Loads images from a URL asynchronously using `AsyncTaskLoader`.
   * Uses `LoaderManager` to manage lifecycle events and configuration changes.
   * Automatically retains and reloads image data after screen rotation.
   * Displays a loading spinner during image fetching.
   * Handles loading errors with user-friendly messages.

2. **Internet Connection Monitoring**

   * Implements a `BroadcastReceiver` to detect internet connectivity via `CONNECTIVITY_ACTION`.
   * Disables the "Load Image" button when no internet is available.
   * Updates the connection status text in real-time.
   * Ensures image loading is only allowed when connected to the internet.

3. **User Interface (Jetpack Compose)**

   * Built entirely using Jetpack Compose for modern UI development.
   * Components include:

     * `TextField`: for user to enter an image URL.
     * `Button`: to trigger image loading.
     * `Image`: to display the downloaded image.
     * `CircularProgressIndicator` and `Text`: to show loading and status messages.
   * Responsive layout with proper loading/error state management.

---

## 🛠️ Setup Instructions

### Prerequisites

* Android Studio Hedgehog or newer
* Kotlin 1.9+
* Android SDK (API level 21+)
* Internet connection for image loading and testing

### How to Run

1. Clone or download the project repository.
2. Open it in Android Studio.
3. Sync Gradle and let dependencies install.
4. Run the app on an emulator or physical device.

---

## 📄 File Breakdown

| File / Folder             | Purpose                                                              |
| ------------------------- | -------------------------------------------------------------------- |
| `MainActivity.kt`         | Hosts the Compose UI and initializes the loader.                     |
| `ImageAsyncTaskLoader.kt` | Custom `AsyncTaskLoader` implementation to download the image.       |
| `ConnectivityReceiver.kt` | Listens to internet connectivity changes and broadcasts status.      |
| `ui/ImageLoaderApp.kt`    | Composable UI for loading and displaying images with state handling. |
| `AndroidManifest.xml`     | Declares required permissions and registers components.              |

---

## 🧠 Key Concepts

### 🔁 AsyncTaskLoader

Replaces deprecated `AsyncTask` by providing better lifecycle integration and automatic result delivery after configuration changes like screen rotations.

### 📡 BroadcastReceiver

Monitors connectivity changes and communicates with the activity to update the user interface accordingly.

### 🧩 Jetpack Compose

Modern UI toolkit that simplifies building reactive user interfaces. This app uses Compose for all UI rendering.

---

## 💬 Comments in Code

* Code is clean and well-commented.
* Key logic for image loading and connectivity checks is clearly explained.
* UI behavior and state transitions are documented inline using comments.

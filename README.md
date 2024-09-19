TrackMyJourney

TrackMyJourney is an Android application that provides continuous location tracking services. The app tracks the user's location in the background, updates it regularly, and sends the data to a server for monitoring or analysis. The service operates in the foreground to ensure uninterrupted tracking, even when the app is not actively used.

## Features

- **Location Tracking**: Uses `FusedLocationProviderClient` to get accurate, real-time location updates.
- **Background Service**: Tracks location in the background, ensuring continuous monitoring.
- **Server Communication**: (Optional) Send location data to a remote server for further analysis.
- **Foreground Notification**: Displays a notification to inform the user about ongoing location tracking.
- **Edge-to-Edge UI Support**: Provides a modern look by utilizing edge-to-edge screen layout.

## Project Status

This is a **beginning-level project**, and I am actively working on it. In the future, I plan to introduce several new features to enhance its functionality, such as:
- Improved UI/UX design.
- Advanced location filtering and accuracy options.
- Integration with real-time mapping APIs.
- Enhanced server communication and data visualization.

Stay tuned for future updates!

## Installation

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/PraveenInTech/TrackMyJourney.git
   ```

2. Open the project in Android Studio.

3. Sync the project with Gradle files.

4. Build and run the project on an Android device or emulator (preferably with location permissions enabled).

## Permissions

The app requires the following permissions:
- `ACCESS_FINE_LOCATION`: For accessing precise location data.
- `ACCESS_COARSE_LOCATION`: For accessing approximate location data.
- `INTERNET`: (Optional) If sending location data to a server.

Make sure to enable these permissions in your AndroidManifest.xml and handle runtime permissions in the app.

## Usage

- When the app is launched, it requests location permissions from the user.
- Once permissions are granted, the app starts tracking the user’s location.
- A foreground notification will appear to inform the user that location tracking is active.
- The location updates will occur every 6 seconds and can optionally be sent to a server.

## Code Overview

### `MainActivity.java`
- Handles permission requests.
- Starts the `LocationService` once permissions are granted.

### `LocationService.java`
- Manages location tracking using `FusedLocationProviderClient`.
- Handles background tracking and server communication.
- Uses a foreground notification to ensure continuous service.

## How to Modify

### Change Update Frequency
- You can adjust the location update interval in `LocationService.java` by modifying the `setInterval` and `setFastestInterval` methods in the `LocationRequest`.

### Send Data to Your Server
- Implement the logic in `sendLocationToServer()` in `LocationService.java` to send location data to your server or API.

## Contributions

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/PraveenInTech/TrackMyJourney/issues) for any open issues.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any queries, reach out to me via:
- **Email**: praveenalagar@protonmail.com
- **GitHub**: [@PraveenInTech](https://github.com/PraveenInTech)

```

### Key Addition:
Under **Project Status**, the note has been added to mention that it's a beginning-level project with plans for future features and updates.

Let me know if you'd like to adjust anything further!

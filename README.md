# QR Scanner App

A simple Android application for scanning QR codes and displaying the scanned information.

## Features

- **QR Code Scanning**: Uses the camera to scan QR codes.
- **Display URL**: If a QR code contains a URL, the app shows a dialog with the URL and an option to visit the link.
- **WiFi Information**: If a QR code contains WiFi credentials, the app displays the SSID, password, and encryption type.

## Getting Started

### Prerequisites

- Android Studio
- Android device or emulator

### Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/qrscanner.git
    cd qrscanner
    ```

2. **Open the project in Android Studio**:
    - Open Android Studio
    - Click on `File > Open` and select the `qrscanner` directory

3. **Run the app**:
    - Connect your Android device or start an emulator
    - Click on the `Run` button in Android Studio

## Usage

1. **Open the app**: Launch the app on your Android device.
2. **Scan a QR code**: Point the camera at a QR code.
3. **View the result**: The app will display the contents of the QR code. If it's a URL, you can click the button to visit the link.

## Code Overview

### MainActivity

- Initializes the camera and sets up the `PreviewView` for displaying the camera feed.
- Requests camera permissions if not already granted.
- Binds the camera provider to the lifecycle of the activity and sets up the `ImageAnalyzer` for processing camera frames.

### MyImageAnalyzer

- Analyzes each frame from the camera.
- Uses ML Kit's barcode scanner to process the image and detect barcodes.
- Displays a dialog with the scanned information if a barcode is detected.

### BottomDialog

- A `BottomSheetDialogFragment` that displays the scanned URL and provides a button to visit the link.

## Dependencies

- **CameraX**: For accessing the camera and analyzing frames.
- **ML Kit**: For barcode scanning.
- **Material Components**: For UI components like `BottomSheetDialogFragment`.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions or suggestions, feel free to reach out to me at [your.email@example.com](mailto:your.email@example.com).

---

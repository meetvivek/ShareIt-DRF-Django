# ShareIt - File Sharing App

ShareIt is a basic file-sharing application built with Django and Django Rest Framework (DRF). This application allows users to upload multiple files, which are then zipped and made available for download via a unique link.

## Features

- **File Upload**: Users can upload multiple files at once.
- **File Zipping**: Uploaded files are automatically zipped into a single archive.
- **Unique Download Links**: Each upload generates a unique download link for easy sharing.
- **Simple User Interface**: Clean and intuitive UI for seamless file sharing.

## Overview

The application consists of several components, including views, serializers, and models, which work together to facilitate file uploads and downloads.

### File Upload Process

1. Users can select multiple files to upload.
2. Upon submission, files are validated and stored in a temporary folder.
3. The files are then zipped into a single archive.
4. A unique identifier (UID) is generated for each upload, which can be used to download the files later.

## API Endpoints

- **POST /handle/**: Endpoint for handling file uploads. Accepts a list of files and returns a unique identifier for the uploaded files.
- **GET /download/<uid>/**: Endpoint to download the zipped files using the generated UID.

## Code Structure

- **views.py**: Contains the view functions and classes for handling requests and responses.
- **serializers.py**: Defines the serializers for file and folder models.
- **models.py**: Contains the database models for storing file and folder information.
- **urls.py**: Configures the URL routing for the application.

## Technologies Used

- **Django**: The web framework used for building the application.
- **Django Rest Framework**: For building the API.
- **Bootstrap**: For styling the user interface.

## Usage Instructions

1. Go to the home page.
2. Select multiple files to upload using the file input.
3. Click on the upload button to upload the files.
4. After successful upload, you will receive a unique download link.
5. Use the link to download the zipped files.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please fork the repository and submit a pull request.

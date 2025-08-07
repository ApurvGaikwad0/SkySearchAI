# Sky Search AI

Sky Search AI is an Android application for seamless, interactive AI experiences. Users can chat with a GPT-based language model and generate images via DALL·E, with secure authentication and cloud storage.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)

## Overview

Sky Search AI empowers users to:

- Engage in natural language conversations with an AI chat interface.
- Generate custom images from text prompts.
- Save and retrieve generated content securely via cloud services.

Built as a learning-focused project, it demonstrates mobile app development best practices, cloud integration, and AI API usage.

## Features

- **User Authentication**: Secure signup, login, and logout flows powered by Firebase Auth.
- **AI Chat Interface**: Real-time chat with GPT models using OpenAI's Chat Completion API.
- **Image Generation**: Create DALL·E images from user prompts.
- **Text-to-Speech**: Optional voice responses through Android’s TextToSpeech engine.
- **Cloud Storage**: Store and fetch images from an AWS S3 bucket.
- **Modern UI**: Clean layouts using AndroidX, ConstraintLayout, Flexbox, and ChatKit.

## Architecture

- **Pattern**: MVVM ensures separation of concerns and easy testing.
- **Networking**: Volley handles API requests with minimal boilerplate.
- **UI**: ChatKit for chat bubbles and Picasso for image loading.
- **Cloud**: Firebase Auth & In-App Messaging; AWS S3 SDK for storage.
- **AI**: OpenAI Chat and Image Generation APIs.

## Tech Stack

- **Language**: Java
- **Android SDK**: API 28+ (Android Pie and above)
- **Libraries**:
  - AndroidX Core, AppCompat
  - ConstraintLayout, FlexboxLayout
  - ChatKit, Picasso, Volley
  - Firebase Auth, Firebase In-App Messaging
  - AWS Android SDK (S3)
- **Build**: Gradle with Version Catalogs (libs.versions.toml)

## Getting Started

### Prerequisites

- Android Studio (Flamingo or later)
- Android device/emulator (API level 28+)
- OpenAI API key
- Firebase project configured with Auth
- AWS S3 bucket with access credentials

### Installation

1. Clone the repo:
   ```bash
   git clone https://github.com/<username>/SkySearchAI.git
   cd SkySearchAI
   ```
2. Open in Android Studio.
3. Copy `local.properties.example` to `local.properties` and add:

   ```properties
   OPENAI_API_KEY=your_openai_api_key
   AWS_ACCESS_KEY_ID=your_aws_key
   AWS_SECRET_ACCESS_KEY=your_aws_secret
   ```
4. Add `google-services.json` to `app/` for Firebase.
5. Build and run on your device or emulator.

## Usage

1. Launch the app and authenticate.
2. Start chatting to receive AI text responses.
3. Tap the image icon to generate AI images.
4. Access saved images from the gallery, backed by AWS S3.

## Contributing

Contributions are welcome! Please:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/...`).
3. Commit your changes with clear messages.
4. Open a Pull Request for review.

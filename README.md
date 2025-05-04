# Flutter Supabase Boilerplate

A Flutter boilerplate project with core functionality and Supabase integration, optimized for iOS development. This project serves as a foundation for building Flutter applications with a clean architecture and essential features.

## 🚀 Features

- **Core Module**: Essential functionality for any Flutter app
  - Supabase integration with secure credential management
  - Environment variable configuration
  - Clean architecture foundation

## 🛠️ Prerequisites

- Flutter SDK (version 3.7.2 or higher)
- iOS development environment (Xcode)
- Supabase account and project

## 📦 Installation

1. Clone the repository:
```bash
git clone [your-repo-url]
cd [project-name]
```

2. Install dependencies:
```bash
flutter pub get
```

3. Create environment file:
```bash
cp .env.example .env
```

4. Update `.env` with your Supabase credentials:
```env
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key
```

## 🏗️ Project Structure

```
lib/
├── core/
│   ├── constants/
│   │   └── api_constants.dart    # API configuration
│   └── services/
│       └── supabase/
│           └── supabase_service.dart  # Supabase client
└── main.dart                     # Application entry point
```

## 🔧 Configuration

### Supabase Setup

1. Create a new project in Supabase
2. Get your project URL and anon key from the project settings
3. Add them to your `.env` file

### iOS Configuration

The project is configured for iOS development. Android and web configurations are minimal and can be added later.

## 🚀 Getting Started

1. Run the app:
```bash
flutter run
```

2. For iOS specifically:
```bash
flutter run -d ios
```

## 🔐 Security

- Environment variables are used for sensitive data
- `.env` file is git-ignored
- Supabase credentials are loaded at runtime

## 📝 Usage

### Accessing Supabase Client

```dart
final supabase = SupabaseService().client;

// Example: Query data
final data = await supabase
    .from('your_table')
    .select()
    .execute();
```

## 🛠️ Extending the Project

This boilerplate is designed to be extended with:

1. Feature modules following clean architecture
2. Additional core services (authentication, storage, etc.)
3. UI components and theme configuration
4. State management solutions

## 📚 Resources

- [Flutter Documentation](https://flutter.dev/docs)
- [Supabase Documentation](https://supabase.com/docs)
- [Clean Architecture in Flutter](https://resocoder.com/2019/08/27/flutter-tdd-clean-architecture-course-1-explanation-project-structure/)

## 🤝 Contributing

Feel free to submit issues and enhancement requests.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

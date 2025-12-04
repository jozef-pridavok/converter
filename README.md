# Currency Converter Calculator

A modern Flutter application for currency conversion with built-in calculator functionality. Supports both fiat currencies and cryptocurrencies with real-time exchange rates.

## Features

- 🧮 **Built-in Calculator** - Perform calculations and instantly convert results
- 💱 **Multi-Currency Support** - 150+ fiat currencies and 100+ cryptocurrencies
- 🔄 **Real-time Exchange Rates** - Automatic updates from exchangerate-api.com and CoinGecko
- 💾 **Offline Mode** - Cached exchange rates work without internet
- 🎨 **Modern UI** - Clean Material Design 3 interface with dark mode support
- 🖥️ **Cross-Platform** - Runs on Linux, macOS, Windows, Android, iOS, and Web

## Tech Stack

- **Flutter** - Cross-platform UI framework
- **Riverpod** - State management
- **Hive** - Local NoSQL database for caching
- **HTTP** - API communication

## Quick Start

### Prerequisites

- Flutter SDK (3.9.2 or higher)
- Dart SDK

### Installation

```bash
# Clone the repository
git clone https://github.com/jozef-pridavok/converter.git
cd converter

# Install dependencies
flutter pub get

# Run the app
flutter run
```

### Platform-Specific Builds

```bash
# Desktop
flutter run -d linux
flutter run -d macos
flutter run -d windows

# Mobile
flutter run -d android
flutter run -d ios

# Web
flutter run -d chrome
```

## Usage

1. **Select Currencies** - Tap currency icons to choose from 40+ fiat and 15+ crypto currencies
2. **Enter Amount** - Use the built-in calculator keypad to input values
3. **Auto-Convert** - All conversions happen instantly across all selected currencies
4. **Refresh Rates** - Tap the refresh button to update exchange rates

## Configuration

API endpoints and settings can be configured in `lib/services/api_exchange_rate_service.dart`:

```dart
class _Config {
  static const String fiatApiUrl = 'https://api.exchangerate-api.com/v4/latest/USD';
  static const String cryptoApiUrl = 'https://api.coingecko.com/api/v3/coins/markets';
  static const String baseCurrency = 'USD';
  static const int requestTimeoutSeconds = 10;
}
```

## Architecture

```
lib/
├── config/          # Configuration constants
├── models/          # Data models (Currency, ExchangeRate)
├── services/        # Business logic (API, Database)
├── providers/       # Riverpod state management
├── ui/
│   ├── screens/     # Main application screens
│   └── widgets/     # Reusable UI components
└── utils/           # Utility functions (NumberFormatter)
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Exchange rates provided by [exchangerate-api.com](https://exchangerate-api.com)
- Cryptocurrency data from [CoinGecko API](https://coingecko.com)

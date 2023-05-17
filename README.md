# Flutter Country Picker

A flutter package to select a country from a list of countries.

## Getting Started

Add the package to your pubspec.yaml:

   ```
   country_picker: ^2.0.20
   ```

In your dart file, import the library:

   ```
   import 'package:country_picker/country_picker.dart';
   ```

Show country picker using showCountryPicker:

   ```
   showCountryPicker(
  context: context,
  showPhoneCode: true, // optional. Shows phone code before the country name.
  onSelect: (Country country) {
    print('Select country: ${country.displayName}');
  },
);
   ```

## For localization

Add the CountryLocalizations.delegate in the list of your app delegates.

   ```
   MaterialApp(
      supportedLocales: [
        const Locale('en'),
        const Locale('el'),
        const Locale.fromSubtags(languageCode: 'zh', scriptCode: 'Hans'), // Generic Simplified Chinese 'zh_Hans'
        const Locale.fromSubtags(languageCode: 'zh', scriptCode: 'Hant'), // Generic traditional Chinese 'zh_Hant'
      ],
      localizationsDelegates: [
        CountryLocalizations.delegate,
        GlobalMaterialLocalizations.delegate,
        GlobalWidgetsLocalizations.delegate,
        GlobalCupertinoLocalizations.delegate,
      ],
      home: HomePage(),
 );
   ```



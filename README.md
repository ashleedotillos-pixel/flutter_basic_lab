# Flutter Basics Lab — IT 120 Integrative Programming and Technologies 2

**Student:** Ashlee R. Dotillos 
**Section:** ILGX3_DOTILLOS_ASHLEE
**Course:** IT 120 Integrative Programming and Technologies 2 (Weeks 10–11)  
**Lab:** Flutter Architecture, Widgets and Basic UI

## Project Structure

```
flutter_basics_lab/
├── lib/
│   ├── main.dart                  # Switches between activities
│   ├── student.dart               # Student name, ID, and theme color
│   ├── activity1_profile_card.dart   # Profile Card (StatelessWidget)
│   ├── activity2_water_tracker.dart  # Water Tracker (StatefulWidget + setState)
│   ├── activity3_weather_layout.dart # Weather Dashboard (Container, Row, Column, Expanded)
│   ├── activity4_cafe_menu.dart      # Campus Café Menu (Stack, ListView, GridView)
│   └── activity5_theme_components.dart # Settings Page (ThemeData, dark mode, components)
├── pubspec.yaml
├── screenshots/                   # 7 required PNG screenshots
├── ANSWERS.md                     # Review questions and observations
└── README.md
```

## Activities Completed

| # | App | Main Idea | Widgets Used |
|---|-----|-----------|--------------|
| 1 | Profile Card | StatelessWidget, widget tree | Card, Column, CircleAvatar, Row, Icon, Text |
| 2 | Water Tracker | StatefulWidget + setState() | IconButton, TextButton, LinearProgressIndicator |
| 3 | Weather Dashboard | Container, Row, Column, Expanded | Container, Expanded, StatBox, HourForecast |
| 4 | Campus Café Menu | Stack, ListView, GridView | Stack, Positioned, ListView, GridView, Chip, Card |
| 5 | Settings Page | ThemeData, dark mode, UI components | ThemeData, SwitchListTile, Wrap, Chip, SnackBar, buttons |

## How to Run

1. Open the project in VS Code: `code .`
2. Open `lib/main.dart` and change the import to the activity you want to run:
   ```dart
   import 'activity1_profile_card.dart' as activity;
   ```
3. Save (`Ctrl + S`) and press **F5** to run.
4. For hot restart after editing `student.dart`: press `Ctrl + Shift + F5`.

## How to Switch Activities

Edit `lib/main.dart` line 3:

```dart
// Activity 1
import 'activity1_profile_card.dart' as activity;

// Activity 2
import 'activity2_water_tracker.dart' as activity;

// Activity 3
import 'activity3_weather_layout.dart' as activity;

// Activity 4
import 'activity4_cafe_menu.dart' as activity;

// Activity 5
import 'activity5_theme_components.dart' as activity;
```

## Submission Requirements

1. **ZIP file:** `SECTION_LASTNAME_FIRSTNAME.zip` (e.g., `ILGX3_DOTILLOS_ASHLEE.zip`)
2. **Contents:** `lib/`, `pubspec.yaml`, `screenshots/` (7 PNGs), `ANSWERS.md`
3. **GitHub:** Push to a repository named `flutter_basics_lab`
4. **Do NOT include:** `build/` folder

## Grading Breakdown

- All five activities run (7 screenshots with name): 40 points
- Tasks completed in each activity: 20 points
- student.dart filled in and files organized: 10 points
- ANSWERS.md complete: 20 points
- GitHub link and correct file name: 10 points
- **Total: 100 points**

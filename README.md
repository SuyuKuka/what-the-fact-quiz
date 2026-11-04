# What the Fact Quiz

## About

**What the Fact Quiz** is a mobile application developed as a first-year Master's (M1 IMPAIRS) project at Université Paris Cité. Built entirely from scratch, this project demonstrates the implementation of a modern mobile architecture featuring local database persistence, dynamic question management, and an interactive user interface.

The application leverages a robust local database via Room to manage multiple question types, subjects, and difficulty levels, offering users a dynamic and progressive general knowledge challenge across various difficulties and subjects. It features a rich dataset of **666 questions** structured and parsed via JSON.

*Note: As this was developed as an academic project, the codebase emphasizes clean architectural patterns (MVVM), offline data handling, and structured data parsing. The source code and comments might contain some French. The user interface is fully in French.*

## Tech Stack

- **Language:** Kotlin (Android)
- **Database:** Room Database
- **UI Toolkit:** Jetpack Compose & Material 3
- **Background Tasks:** WorkManager for notifications and cooldown management
- **Data Formats:** JSON for data parsing
- **Architecture:** MVVM (Model-View-ViewModel)

## Key Features

- **Extensive Dataset:** Over 600 questions in total (precisely **666 questions** meticulously formatted and integrated via JSON files).
- **Diverse Question Types:** Support for 5 different question formats to thoroughly test general knowledge, including multiple-choice questions (MCQ), precision questions, insertion, sorting, and dynamic sorting.
- **Subjects & Difficulties:** Features 6 distinct subjects, each structured across 3 progressive difficulty levels.
- **Shop & Energy System:** Built-in store allowing users to purchase a monthly or annual subscription for unlimited energy/play time, alongside a free mode limited by cooldowns with automated notifications.
- **Background Notifications (WorkManager):** Automated background workers that send daily reminders to play, alongside real-time alerts when energy is fully restored or when a new energy point is acquired.
- **Leaderboard & Scoring:** Comprehensive scoring system (awarding up to 1000 points for correct answers, with partial points for approximate or specific question types) combined with a speed-based ranking system where faster completion secures a higher position.
- **User Profile:** Dedicated profile management allowing users to update their display pseudo.
- **Advanced Settings:** Customization options allowing users to modify the background wallpaper, font styling, and preferences.
- **Local Persistence & Sourcing:** Robust offline data management leveraging Room Database, combining OpenQuizzDB for MCQs and AI-assisted datasets (Gemini/ChatGPT) for other question types.

## Data Information

* **MCQ Questions Source:** [OpenQuizzDB](https://www.openquizzdb.org/listing/listing.php)
* **Other Question Types Sources:** [Gemini](https://gemini.google.com/app) and [ChatGPT](https://chatgpt.com)
* **Dataset Volume:** 
  * **MCQ Questions:** ~90 questions per subject and 30 per difficulty level
  * **Other Types:** ~72 questions per subject and 12 per difficulty level
* **Acquisition Technique:** JSON format
* **Database Integration Technique:** Room Database

## Project Structure

```text
📁 what-the-fact-quiz
│
├── 📁 app/src/main/
│   ├── 📁 java/fr/uparis/chenliu/projet
│   │   ├── 📁 data/                  # Data layer (database, entities, DAOs, and models)
│   │   │   ├── 📁 dao/               # Data Access Objects for Room
│   │   │   ├── 📁 database/          # Room database configuration
│   │   │   ├── 📁 entity/            # Database entities / tables
│   │   │   ├── 📁 model/             # Data models
│   │   │   └── 📁 data/              # Data sources and repositories
│   │   ├── 📁 navigation/            # App navigation and routing logic
│   │   └── 📁 ui/                    # User interface components
│   │       ├── 📁 menu/              # Menu screens and components
│   │       ├── 📁 quizz/             # Quiz game screens and logic
│   │       ├── 📁 theme/             # UI themes, colors, and typography
│   │       ├── 📁 viewmodel/         # ViewModels for UI state management
│   │       ├── 📁 worker/            # Background workers (WorkManager)
│   │       └── MainActivity.kt       # Main entry point activity
│   │
│   └── 📁 res/                       # Android resources (layouts, drawables, strings, etc.)
│       ├── 📁 anim                   # Animation XML files
│       ├── 📁 drawable               # Images, shapes, and vectors
│       ├── 📁 font                   # Custom font files
│       ├── 📁 mipmap                 # App launcher icons
│       ├── 📁 raw                    # Raw assets (e.g., JSON files)
│       ├── 📁 values                 # Strings, colors, and styles XML files
│       └── 📁 xml                    # XML configuration files
│
├── 📄 build.gradle                   # Build configuration
└── 📄 README.md                      # Project documentation
```

## Getting Started

### Prerequisites
- **Android Studio:** Narwhal 3 Feature Drop | 2025.1.3 (or higher)
- **Android SDK:** Compatible with your project's min/target SDK requirements
- **Environment:** Java / Kotlin development environment

### Installation

You can install and open the project using one of the two methods below:

#### Method 1: Directly via Android Studio

1. **Open Android Studio**.

2. **Select Clone repository (or *File > New > Project from Version Control...*).**

3. **Paste the repository URL:**
```text
https://github.com/SuyuKuka/what-the-fact-quiz.git
```

4. **Click Clone.**

#### Method 2: Via Terminal & Git

1. **Clone the repository:**
```bash
git clone https://github.com/SuyuKuka/what-the-fact-quiz.git
```

2. **Open in Android Studio:**
    * Open Android Studio, select Open (or Open an Existing Project), and choose the cloned what-the-fact-quiz directory.

#### Build and Run
* Let Gradle sync the project dependencies automatically.
* Run the app on an emulator or a physical Android device.

## Team

This project was developed collaboratively as a 2-person team:

- **CHEN Michel** - Mobile Development & Architecture
  [![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?logo=github)](https://github.com/SuyuKuka)
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-0A66C2?logo=linkedin)](https://linkedin.com/in/chen-michel)

- **LIU Kai-Xiang** - Mobile Development & Architecture
  [![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?logo=github)](https://github.com/Peak4s)

## License

This project was developed for academic purposes at **Université Paris Cité** and is provided for portfolio demonstration purposes. 

**Code:** The source code of this project is open-source and available under the GPL 3.0 License — see [LICENSE](LICENSE) for details.

**Assets:** Images assets (such as background, icons, fonts, etc) belong to their respective copyright owners. They are included here strictly for educational and portfolio demonstration purposes and are not distributed under an open-source license.
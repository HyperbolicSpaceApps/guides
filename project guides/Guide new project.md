Tell LLM your project etc 
Ask: 
- good repo name/description
- readme with outline like below. 
1-shot with the following example of output:

What it is (2-3 sentences, your honest MVP description)
Vision (bullet list of where it's going — agent-centric, voice, org frameworks etc.)
Stack (dart/flutter, Groq API, whatever you land on)
Getting started (clone, add your Groq API key, run)
Current state (e.g. "skeleton: text chat only, no persistence yet")
Roadmap (rough, just bullet points)
License

- Which license to use? Depending on use case. 
- Build a first MVP for lib folder (incl main.dart)

gh repo create
cd PROJECT_NAME
flutter create PROJECT_NAME_APP

Clean up the pubspec file and save

flutter pub get
Open the files with errors:
- missing package -> install with flutter pub add package_name
- part xx.g.dart -> flutter pub add build_runner, flutter pub add riverpod_annotation OR hive_generator, then dart run build_runner build. 

flutter add dependency_validator
dart run dependency_validator

Debug and flutter run

commiting to git :)

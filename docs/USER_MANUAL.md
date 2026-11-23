---
last_updated: 2026-11-23
version: 6.0.0
product_versions:
  ios: "1.1.0"
  android: "1.1.0"
generated_from: "dev-docs/specs/USER_MANUAL_SPEC.instructions.md"
---

# User Manual

## Overview

PowerShell Practice is an app for learning common PowerShell commands
(cmdlets) and testing yourself on them. It is for people who are new to
PowerShell or want to refresh their memory of everyday cmdlets, their aliases,
and their syntax.

The app includes a built-in library of 38 cmdlets in seven categories. You can
read about each cmdlet, mark it as learned, take quizzes, practice pipelines,
and type examples into an emulator to see their recorded output.

| Item | Details |
| --- | --- |
| Platform | Android, on phones and tablets; iOS, on iPhone and iPad |
| Interface | Touch interface with four tabs: **Home**, **Practice**, **Emulator**, and **Docs**. This layout is in development and arrives with the next version of each platform. Version 1.1.0 has the tabs **Learn**, **Practice**, **Progress**, and **Docs** |
| Version | Android 1.1.0, iOS 1.1.0. The App Store has iOS 1.0.0; 1.1.0 is waiting for App Review |

<!-- Verified from: platform/ios/powershell-practice.xcodeproj/project.pbxproj [MARKETING_VERSION, TARGETED_DEVICE_FAMILY, INFOPLIST_KEY_CFBundleDisplayName] -->
<!-- Verified from: platform/ios/powershell-practice/ContentView.swift [ContentView, AppTab] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/root/RootTab.kt [RootTab] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandLibrary.swift [CommandLibrary.all] -->
<!-- Verified from: platform/ios/powershell-practice/Models/Command.swift [CommandCategory] -->

This manual describes the layout that is in development. If your installed
version shows a **Learn** tab, see
[Find Your Way in Version 1.1.0 and Earlier](#find-your-way-in-version-110-and-earlier).

PowerShell Practice does not run PowerShell commands or connect to a
PowerShell server. It checks your quiz answers on the device.

<!-- Verified from: docs/PRIVACY.md [On your device] -->

## Installation and Setup

### Check the System Requirements

| Requirement | Details |
| --- | --- |
| Device | Android phone or tablet, or iPhone or iPad |
| Operating system | Android 8.0 or later, or iOS 26.5 or later |
| Account or sign-in | None required |
| Internet connection | Not required to learn or practice |

<!-- Verified from: platform/android/app/build.gradle.kts [minSdk = 26] -->
<!-- Verified from: platform/ios/powershell-practice.xcodeproj/project.pbxproj [IPHONEOS_DEPLOYMENT_TARGET, TARGETED_DEVICE_FAMILY] -->
<!-- Verified from: docs/PRIVACY.md [On your device, Developer services] -->

### Install on Android

Install PowerShell Practice from
[Google Play](https://play.google.com/store/apps/details?id=com.plaintxtoffice.powershellpractice).
It needs no account.

<!-- Verified from: platform/android/app/build.gradle.kts [applicationId] -->

### Install on iOS

Install PowerShell Practice on your iPhone or iPad from the
[App Store](https://apps.apple.com/app/id6837567736). It needs no account.
The App Store has version 1.0.0; version 1.1.0 is waiting for App Review.

<!-- Verified from: platform/ios/powershell-practice.xcodeproj/project.pbxproj [PRODUCT_BUNDLE_IDENTIFIER, MARKETING_VERSION] -->

### Set Up the App

No setup is needed. The command library is included with the app, and your
progress starts empty the first time you open it.

<!-- Verified from: docs/PRIVACY.md [On your device] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [CommandProgress] -->

## Starting the Program

### Open PowerShell Practice

1. Tap **PowerShell Practice** on your Home Screen, in the App Library on
   iPhone and iPad, or in the app list on Android.
1. The app opens on the **Home** tab, which shows the app's name, a card for
   each of the other tabs, and **Send Feedback**.

<!-- Verified from: platform/ios/powershell-practice.xcodeproj/project.pbxproj [INFOPLIST_KEY_CFBundleDisplayName] -->
<!-- Verified from: platform/ios/powershell-practice/ContentView.swift [ContentView selection] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/root/RootTab.kt [RootTab.Start] -->

If the app cannot open your saved progress, it shows **Your data couldn't be
opened** instead. See [Troubleshooting](#troubleshooting).

<!-- Verified from: platform/ios/powershell-practice/StorageRecovery.swift [StorageRecoveryGate] -->

### Close PowerShell Practice

The app has no quit command. Leave it the way you leave any other app, such as
by returning to the Home Screen. Learned commands and quiz answers are saved
as you go.

<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [learnedButton] -->
<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [submit] -->

## Getting Around

The app has four tabs in a tab bar. On Android, the tab bar floats at the
bottom of the screen, and windows at least 600 dp wide show the tabs along the
side instead.

Each tab keeps the screens you open in it, such as a cmdlet page or a guide,
while you use another tab, and the tab bar stays visible on those screens. On
Android, it also stays visible during quizzes and pipeline rounds, and tapping
the tab you are on returns it to its first screen. On iPhone and iPad, quizzes
and pipeline rounds open full screen.

| Tab | What you find there |
| --- | --- |
| **Home** | The app's name and icon, a card for each of **Practice**, **Emulator**, and **Docs**, and **Send Feedback** |
| **Practice** | Quiz options and **Start Quiz**, then pipeline options and **Start Pipeline Quiz** |
| **Emulator** | A prompt where you type examples and see their recorded output, with **Try an Example** and **Clear Screen** |
| **Docs** | Two parts, switched with the control at the top: **Commands**, the cmdlet library grouped by category with a search field, and **Guides**, the guides to PowerShell conventions followed by an **About** section with **Privacy**, **Send Feedback**, **Reset All Progress**, and the app version |

<!-- Verified from: platform/ios/powershell-practice/ContentView.swift [ContentView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/HomeView.swift [HomeView, HomeDestination] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [PracticeView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/EmulatorView.swift [EmulatorView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [DocsView, DocsSegment, GuideSections] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/root/RootScreen.kt [RootLayout, RootTabBar, RootRail, RailMinWidth] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/Navigation.kt [MainNavigation, tabEntryProvider] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [fullScreenCover] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/home/HomeScreen.kt [HomeScreen] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/docs/DocsScreen.kt [DocsScreen] -->

On **Home**, tap a card to switch to that tab; it is the same as tapping the
tab. The cards read:

| Card | Description shown |
| --- | --- |
| **Practice** | Test what you know with quizzes and pipeline exercises. |
| **Emulator** | Type PowerShell examples and see their simulated output. |
| **Docs** | Look up cmdlets, aliases, and guides. |

<!-- Verified from: platform/ios/powershell-practice/Views/HomeView.swift [HomeDestination.detail] -->
<!-- Verified from: platform/android/app/src/main/res/values/strings.xml [home_practice_description, home_emulator_description, home_docs_description] -->

The library uses these categories:

| Category | What it covers |
| --- | --- |
| Getting Help | Discover commands and read their documentation. |
| File System | Navigate folders and manage files. |
| Pipeline & Objects | Filter, sort, and reshape objects in the pipeline. |
| Processes & Services | Inspect and control running programs and services. |
| Output & Formatting | Control how results are displayed and exported. |
| Variables & Content | Read, write, and store data. |
| Networking | Test connections and talk to web services. |

<!-- Verified from: platform/ios/powershell-practice/Models/Command.swift [CommandCategory.blurb] -->

In **Docs**, tap a cmdlet or a guide to open it. Use the back button at the
top left to return to the list. On Android, the system Back gesture closes the
screen you opened; on the first screen of **Practice**, **Emulator**, or
**Docs**, it returns to **Home**.

<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [navigationDestination] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/root/RootTab.kt [backTarget, visibleTabs] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/ui/Components.kt [BackNavRow] -->

### Find Your Way in Version 1.1.0 and Earlier

Version 1.1.0 has the tabs **Learn**, **Practice**, **Progress**, and
**Docs**. Its cmdlets, quizzes, pipelines, and guides work as this manual
describes, but some are in different places. iOS version 1.0.0 has no guides
and no practice terminal.

| To do this | In version 1.1.0 and earlier |
| --- | --- |
| Browse and search cmdlets | Tap the **Learn** tab. |
| Practice pipelines | In the **Pipelines** section of the **Practice** tab, tap **Pick the Pipeline** or **Build the Pipeline**. Each round has 10 questions. |
| Type examples and see their output | In version 1.1.0, tap the **Practice** tab, then **Practice Terminal**. |
| Read the guides | In version 1.1.0, tap the **Docs** tab. |
| Open **Privacy** or send feedback | In version 1.1.0, use the **About** section of the **Docs** tab. In iOS version 1.0.0, **Send Feedback** is on the **Learn** tab's toolbar. On Android, **More options** (three dots) on any tab also has **Send feedback**. |
| See learned counts and quiz accuracy | Tap the **Progress** tab. It shows your learned count, quiz accuracy, progress by category, and a **Needs Review** list. |
| Clear learned cmdlets and quiz history | Tap the **Progress** tab, then **Reset All Progress**, then **Reset**. This cannot be undone. |

The layout that is in development has no **Progress** tab. Your learned marks
and each cmdlet's quiz record carry over to it, and **Reset All Progress** is
in the **About** section under **Docs**, **Guides**. See
[Reset All Progress](#reset-all-progress).

<!-- Verified from: docs/USER_MANUAL.md as generated on 2026-11-22 for version 1.1.0, commit 2663eec [Getting Around, Practice Pipelines, Check Your Progress, Reset All Progress, Feedback] -->
<!-- Verified from: README.md [Download] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [CommandProgress] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/di/AppModule.kt [Room.databaseBuilder "progress.db"] -->

## Everyday Tasks

### Browse and Search the Cmdlet Library

1. Tap the **Docs** tab. **Commands** is shown first; if **Guides** is
   showing, tap **Commands**.
1. Scroll through the categories, or tap the search field, which shows
   **Cmdlet, alias, or task**.
1. Type part of a cmdlet name, an alias, or words from its description. The
   list shows only matching cmdlets.
1. Tap a cmdlet to open it.

A check mark next to a cmdlet means you marked it as learned. If nothing
matches your search, the app shows a no-results message. To clear the search,
tap **Clear search** (the X) in the field.

<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [CommandSearchField, CommandSections.results(in:), CommandRow] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/docs/DocsScreen.kt [SearchField, CommandListItem, NoResults] -->

### Study a Cmdlet

The detail screen for a cmdlet shows:

- Its category, name, and its **Verb** and **Noun** parts.
- A short summary of what it does.
- **Syntax**, showing its common parameters.
- **Aliases**, when the cmdlet has any.
- **Examples**, each with an explanation and its **Output**: what
  PowerShell prints when you run it, or a note that it prints nothing. The
  output is a recorded sample; the app never runs commands.
- A tip, for some cmdlets.
- **Quiz record: X of Y correct**, after you have answered quiz questions
  about it.

<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [CommandDetailView.body, header, ExampleView, ExampleOutput] -->

### Copy a Command

1. Open a cmdlet's detail screen.
1. Next to the syntax or an example, tap the **Copy** button (two overlapping
   pages).
1. The text is placed on the clipboard so you can paste it into another app.

You can also select text in the syntax and examples. Other apps can read text
you paste into them.

<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [CodeBlock] -->
<!-- Verified from: docs/PRIVACY.md [Copying commands] -->

### Mark a Cmdlet as Learned

1. Open a cmdlet's detail screen.
1. Tap **Mark as Learned** at the bottom of the screen. The button changes to
   **Learned**.
1. To undo it, tap **Learned** again.

Learned cmdlets show a check mark in the **Commands** list, and the **Not Yet
Learned** quiz selection leaves them out. If the change cannot be saved, the
app shows **Couldn't update progress** and leaves your progress unchanged.

<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [learnedButton] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [pool(for:)] -->

### Take a Quiz

1. Tap the **Practice** tab.
1. Under **Quiz Type**, choose a quiz type:
   - **Multiple Choice**: pick the right cmdlet from four choices.
   - **Type the Command**: read the description and type the cmdlet. Aliases
     count as correct answers.
1. Under **Commands**, use **Practice** to choose which cmdlets to include.
1. Next to **Questions**, tap **Fewer questions** (minus) or **More
   questions** (plus) to choose how many questions to ask.
1. Tap **Start Quiz**.

<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [quizTypeSection, commandsSection, startQuizSection] -->
<!-- Verified from: platform/ios/powershell-practice/Theme.swift [QuestionStepper] -->
<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizMode] -->

| Option | Default | Accepted values |
| --- | --- | --- |
| Quiz Type | **Multiple Choice** | **Multiple Choice** or **Type the Command** |
| Practice | **All Commands** | **All Commands**, **Not Yet Learned**, **Needs Review**, or one category |
| Questions | 10 | 5 to 30, in steps of 5 |

<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [mode, scope, questionCount, PracticeScope] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/practice/PracticeViewModel.kt [PracticeUiState, MIN_QUESTIONS, MAX_QUESTIONS, QUESTION_STEP] -->

Each question in a quiz is about a different cmdlet. If your selection has
fewer cmdlets than the number of questions, the quiz asks one question per
cmdlet. The **Practice** list shows how many cmdlets each choice contains; on
Android, only the first three choices show a count. **Needs Review** holds the
cmdlets you have missed at least once and answer correctly less than 70% of
the time. **Start Quiz** is unavailable when the selection is empty. For
**Needs Review**, the app explains that commands you miss in quizzes will show
up there.

<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizBuilder.makeQuestions] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [needsReview] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [PracticeScope.menuLabel, startQuizSection footer] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/practice/PracticeScreen.kt [scopeTitle] -->

These choices apply only to the quiz you start. The app does not keep them
after it closes.

<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [@State mode, scope, questionCount] -->

### Answer Quiz Questions

The quiz shows the question number, such as **1 of 10**, and a progress bar.
On iPhone and iPad, it opens full screen; on Android, the tab bar stays below
it.

<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [toolbar, questionView] -->

In a **Multiple Choice** quiz, each question is one of two kinds:

- **Command** shows a cmdlet's description.
- **Alias** asks **Which cmdlet does the alias ... run?** For this kind, only
  the full cmdlet name is correct.

Tap one of the four choices. The correct choice is marked with a check mark,
and a wrong choice you picked is marked with an X.

<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizQuestion.prompt, isCorrect, makeChoices] -->
<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [questionKind, choices] -->

In a **Type the Command** quiz:

1. Read the description.
1. Type the cmdlet name after **PS>** in the **Verb-Noun** field.
1. Tap **Check**, or tap the **Done** key on the keyboard.

Typed answers ignore capitalization and leading or trailing spaces. The full
cmdlet name or any of its aliases is accepted.

<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [typedInput, submitTyped] -->
<!-- Verified from: platform/ios/powershell-practice/Models/Command.swift [Command.matches] -->

After you answer, the app shows **Correct!** or **Not quite. The answer is
...**, followed by an example of the cmdlet. For an alias question it also
shows the cmdlet's summary. Tap **Next Question** to continue, or **See
Results** after the last question.

<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [feedback, safeAreaInset] -->

Each answer is saved as soon as you give it. If it cannot be saved, the app
shows **Couldn't save your answer**. To leave a quiz early, tap **Close** (the
X) at the top left; answers you already gave stay saved.

<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [submit, toolbar, alert] -->

### Review Your Quiz Results

At the end of a quiz, the **Results** screen shows your score, such as **8 /
10**, with a short message. **Review These** lists each cmdlet you missed with
its summary. Tap **Done** to return to the **Practice** tab.

<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [QuizResultsView] -->

### Practice Pipelines

A pipeline joins cmdlets with `|` so that each one works on the objects the
one before it sends. The **Pipelines** section at the bottom of the
**Practice** tab asks questions about everyday tasks, such as listing the
services that are running.

1. Tap the **Practice** tab and scroll to **Pipelines**.
1. Choose how to answer:
   - **Pick the Pipeline**: choose the pipeline that does the task from four.
     Each wrong choice has one cmdlet swapped for a likely mistake.
   - **Build the Pipeline**: tap the commands into order. One command is a
     decoy that the pipeline does not need. Tap a command you placed to take
     it back out.
1. Next to **Questions**, tap **Fewer questions** (minus) or **More
   questions** (plus). A round has 1 to 14 questions, one for each pipeline
   in the app at most. It starts at 10, and the app remembers the number you
   choose, even after it closes.
1. Tap **Start Pipeline Quiz**.
1. For each question, make your choice or put every stage in place, then tap
   **Check Answer**.
1. Tap **Next Question** to continue, or **See Results** after the last
   question.

After each answer, the app shows the right pipeline and explains how it
works. At the end, **Pipeline Results** shows your score and lists the
pipelines you missed under **Pipelines to Review**; tap **Done** to return to
the **Practice** tab. Pipeline answers are not added to a cmdlet's quiz record
or to **Needs Review**. To leave early, tap **End Practice**. The app asks
**End this practice?**; tap **End Practice** again to confirm. On Android, the
system Back gesture during a round asks the same question.

<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/domain/Pipeline.kt [PipelineQuizBuilder, PipelineLibrary] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/practice/PracticeScreen.kt [PracticeScreen] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/pipeline/PipelineViewModel.kt [MIN_PIPELINE_QUESTIONS, MAX_PIPELINE_QUESTIONS, DEFAULT_PIPELINE_QUESTIONS, resolvedPipelineQuestionCount] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/practice/PipelineQuestionCountSetting.kt [PipelineQuestionCountSetting] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/pipeline/PipelineScreen.kt [PipelineRoute, EndPracticeDialog, PipelineScreen, PipelineBuilder, PipelineFeedback, PipelineResults] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [pipelineModeSection, savedPipelineQuestionCount, startPipelines] -->
<!-- Verified from: platform/ios/powershell-practice/Models/Pipeline.swift [PipelineSession.questionCountRange, defaultQuestionCount, questionCount(saved:)] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PipelineView.swift [builder, feedback, confirmationDialog, PipelineSummary] -->

### Use the Emulator

The emulator lets you type commands as you would at a PowerShell prompt and
see what they print. It knows the examples from the cmdlet pages and the
guides, and it never runs anything.

1. Tap the **Emulator** tab.
1. Tap the **Type a command** field after **PS>**, type an example, such as
   `Get-Location`, and tap **Run** or use the keyboard submit key.
1. Read the output under your command. Like PowerShell, the emulator ignores
   capitalization and extra spaces.

If you type a cmdlet or alias the emulator knows but an example it doesn't, it
lists that cmdlet's examples; tap one to fill it in. At the top of the screen,
**Try an Example** (the dice) fills in a random example and **Clear Screen**
(the eraser) clears what you have typed so far. Typing `cls`, `clear`, or
`Clear-Host` also clears it. You can paste a command with its prompt, such as
`PS C:\Users\alex> Get-Location`. The emulator keeps what you typed while you
use other tabs, until the app closes.

<!-- Verified from: platform/ios/powershell-practice/Views/EmulatorView.swift [EmulatorView, EntryView] -->
<!-- Verified from: platform/ios/powershell-practice/Models/PracticeTerminal.swift [PracticeTerminal.reply] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/terminal/EmulatorScreen.kt [EmulatorScreen, EmulatorTools, InputRow] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/domain/PracticeTerminal.kt [PracticeTerminal.reply] -->

### Read the Guides

1. Tap the **Docs** tab, then **Guides**.
1. Tap a guide to open it.

There are five short guides: **Naming Rules**, **Command Conventions**,
**Piping Techniques**, **Variables and Quoting**, and **Comparison
Operators**. **Naming Rules** covers the Verb-Noun pattern, approved verbs,
singular nouns, capitalization, parameter names and aliases, and how to name
your own functions. Each guide has worked examples with their output. Tap
**Copy** beside a command to paste it into the emulator.

<!-- Verified from: platform/ios/powershell-practice/Models/GuideLibrary.swift [GuideLibrary.all] -->
<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [GuideSections, GuideView] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/docs/DocsScreen.kt [DocsScreen, GuideListItem] -->

### Read the Privacy Information

1. Tap the **Docs** tab, then **Guides**.
1. In the **About** section below the guides, tap **Privacy**.
1. Read the privacy information. It is available without a network
   connection.
1. At the end, tap **Contact Plain Text Office** to open the developer's
   website. On iPhone and iPad, **Send Feedback** above it opens the feedback
   screen.

On iPhone and iPad, the screen ends with an **About** note: PowerShell is a
trademark of Microsoft Corporation, and PowerShell Practice is an independent
study aid by Plain Text Office LLC that is not affiliated with or endorsed by
Microsoft. It also says that the commands and aliases are for PowerShell 7 on
Windows.

<!-- Verified from: platform/ios/powershell-practice/PrivacyPolicyView.swift [PrivacyPolicyButton, PrivacyPolicyView, About] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/privacy/PrivacyScreen.kt [PrivacyScreen] -->

### Reset All Progress

**Reset All Progress** clears every learned mark and every cmdlet's quiz
record, so you can start over.

1. Tap the **Docs** tab, then **Guides**.
1. In the **About** section below the guides, tap **Reset All Progress**.
1. When the app asks **Reset all progress?**, tap **Reset**. To keep your
   progress, tap **Cancel** instead.

This cannot be undone. **Reset All Progress** is unavailable until you have
marked a cmdlet as learned or answered a quiz question. If the reset fails,
the app shows **Couldn't reset progress** and leaves your progress unchanged.
The pipeline question count is a setting, not progress, and stays as it is.

<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [GuideSections, ResetProgressButton] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/docs/DocsScreen.kt [ResetRow, ResetDialog] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/docs/CommandListViewModel.kt [resetProgress, canReset] -->
<!-- Verified from: platform/android/app/src/main/res/values/strings.xml [reset_all_progress, reset_title, reset_text, reset_confirm, reset_failed_title, cancel] -->

## Settings and Preferences

The app has one setting that it keeps between sessions: the number of
questions in a pipeline round. The quiz options on the **Practice** tab apply
only to the quiz you start and reset when the app closes.

| Setting | Default | Accepted values | How to change it |
| --- | --- | --- | --- |
| Pipeline **Questions** | 10 | 1 to 14, in steps of 1 | On the **Practice** tab, under **Pipelines**, tap **Fewer questions** (minus) or **More questions** (plus) |

The new number applies to the next round you start and is kept when the app
closes. **Reset All Progress** does not change it.

<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/practice/PracticeViewModel.kt [stepPipelineQuestionCount] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/data/PracticeSettingsStore.kt [SharedPreferencesPracticeSettingsStore] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [savedPipelineQuestionCount, @State mode, scope, questionCount] -->
<!-- Verified from: platform/ios/powershell-practice/Models/Pipeline.swift [PipelineSession.questionCount(saved:)] -->

## Importing and Exporting

Not Applicable.
<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift, platform/ios/powershell-practice/Views/DocsView.swift, docs/PRIVACY.md -->

## Commands and Shortcuts

The app has no keyboard shortcuts or menu commands. These on-screen controls
perform its main actions.

| Control | Where | What it does |
| --- | --- | --- |
| **Home**, **Practice**, **Emulator**, and **Docs** | Tab bar | Switch between the main screens |
| **Practice**, **Emulator**, and **Docs** cards | **Home** | Switch to that tab |
| **Send Feedback** | **Home**; **Docs**, **Guides**, **About** section; on iPhone and iPad, also the end of **Privacy** | Opens the feedback screen |
| **Commands** / **Guides** | **Docs**, top of the screen | Switches between the cmdlet library and the guides |
| Search field | **Docs**, **Commands** | Filters cmdlets by name, alias, or description |
| **Privacy** | **Docs**, **Guides**, **About** section | Opens the privacy information |
| **Reset All Progress** | **Docs**, **Guides**, **About** section | Clears learned marks and quiz records, after you confirm |
| **Copy** | Cmdlet detail or a guide | Copies the syntax or an example to the clipboard |
| **Mark as Learned** / **Learned** | Cmdlet detail | Marks or unmarks the cmdlet as learned |
| **Start Quiz** | **Practice** | Starts a quiz with the chosen options |
| **Check** | Quiz, **Type the Command** | Checks your typed answer |
| **Next Question** / **See Results** | Quiz or pipeline round | Moves to the next question or the results |
| **Close** | Quiz, top left | Leaves the quiz |
| **Start Pipeline Quiz** | **Practice**, **Pipelines** section | Starts a pipeline round with the chosen options |
| **Check Answer** | Pipeline round | Checks your pipeline |
| **End Practice** | Pipeline round, top of the screen | Leaves the pipeline round, after you confirm |
| **Run** | **Emulator** | Shows the recorded output for the command you typed |
| **Try an Example** | **Emulator**, top of the screen | Fills in a random example |
| **Clear Screen** | **Emulator**, top of the screen | Clears the commands and output shown |

<!-- Verified from: platform/ios/powershell-practice/ContentView.swift [ContentView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/HomeView.swift [HomeView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [DocsView, CommandSearchField, GuideSections] -->
<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [CodeBlock, learnedButton] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [Start Quiz, Start Pipeline Quiz] -->
<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [typedInput, toolbar, safeAreaInset] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PipelineView.swift [Check Answer, End Practice] -->
<!-- Verified from: platform/ios/powershell-practice/Views/EmulatorView.swift [toolbar, inputRow] -->
<!-- Verified from: platform/android/app/src/main/res/values/strings.xml [tab_home, tab_practice, tab_emulator, tab_docs, feedback, docs_commands, docs_guides, terminal_run, terminal_try, terminal_clear] -->

## Your Data Files

The app keeps its records inside its own storage on your device. You do not
open or edit these records by hand, and the app does not show their location.

| Data | Where it is stored | Can you edit it? |
| --- | --- | --- |
| Cmdlet library | Included with the app | No |
| Learned cmdlets and quiz answers for each cmdlet | The app's private storage on your device: an on-device library on iPhone and iPad, and the `progress.db` database on Android | No; change it through the app |
| Pipeline question count | The app's settings, in its private storage on your device | No; change it on the **Practice** tab |

<!-- Verified from: platform/ios/powershell-practice/powershell_practiceApp.swift [StorageRecovery schema] -->
<!-- Verified from: platform/ios/powershell-practice/StorageRecovery.swift [ModelContainer, isStoredInMemoryOnly: false] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/di/AppModule.kt [Room.databaseBuilder "progress.db"] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [CommandProgress] -->
<!-- Verified from: docs/PRIVACY.md [On your device] -->

To remove your learned marks and quiz records, use
[Reset All Progress](#reset-all-progress). To remove everything the app
stores, delete the app; on Android, you can instead clear the app's storage in
the device settings. Device backups may keep earlier copies.
On iPhone and iPad, iCloud Backup and computer backups can include the app's
data; on Android, Android backup and device transfer can include it. The app
has no user-visible log files.

<!-- Verified from: platform/ios/powershell-practice/PrivacyPolicyView.swift [Removing data] -->
<!-- Verified from: platform/android/app/src/main/res/values/strings.xml [privacy_removing_body] -->
<!-- Verified from: platform/android/app/src/main/AndroidManifest.xml [android:allowBackup] -->
<!-- Verified from: platform/ios/powershell-practice/AppDiagnostic.swift [AppDiagnostic] -->

## Troubleshooting

| Symptom | Likely Cause | Resolution |
| --- | --- | --- |
| **Your data couldn't be opened** appears when the app starts. | The app could not open its saved progress. Your saved data stays on the device unchanged. | Tap **Retry**. If it still fails, tap **Continue Without Saving** to use the app, but anything you add or change in that session is not saved. |
| A banner says **Your data couldn't be opened. Changes won't be saved.** | You chose **Continue Without Saving**. | Fully close the app and open it again to retry opening your saved progress. |
| **Start Quiz** is unavailable. | The chosen **Practice** selection has no cmdlets, such as **Needs Review** before you have missed any questions. | Choose **All Commands**, **Not Yet Learned**, or a category. |
| A quiz has fewer questions than you chose. | The selection has fewer cmdlets than the **Questions** value. | Choose a larger selection to get more questions. |
| **Couldn't update progress** appears. | The learned status could not be saved. | Tap **OK** and try again. Your progress was not changed. |
| **Couldn't save your answer** appears during a quiz. | The answer could not be recorded. | Tap **OK** and continue. That question's result was not recorded. |
| The emulator says a command is outside the cmdlet library. | The emulator only knows the cmdlets in the app and their examples. | Look up a cmdlet in **Docs** and type one of its examples, or tap **Try an Example**. |
| There is no **Progress** tab. | The layout that is in development does not have one. | See a cmdlet's **Quiz record** on its detail screen, and its learned mark in **Docs**. To clear your records, use **Reset All Progress** under **Docs**, **Guides**, **About**. |
| **Reset All Progress** is unavailable. | There are no learned marks or quiz records to clear. | Nothing needs resetting. |
| **Couldn't reset progress** appears. | The records could not be cleared. | Tap **OK** and try again. Your progress was not changed. |

<!-- Verified from: platform/ios/powershell-practice/StorageRecovery.swift [StorageRecoveryGate] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [Start Quiz, footer] -->
<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizBuilder.makeQuestions, isCorrect] -->
<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [alert, Quiz record] -->
<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [alert] -->
<!-- Verified from: platform/ios/powershell-practice/Views/EmulatorView.swift [EntryView unknown] -->
<!-- Verified from: platform/android/app/src/main/res/values/strings.xml [terminal_unknown] -->

## FAQ

### Does the app run PowerShell commands?

No. The app does not run PowerShell commands or connect to a PowerShell
server. The emulator shows recorded output for the examples and never runs
what you type. Try the examples in PowerShell on a computer.

<!-- Verified from: docs/PRIVACY.md [On your device] -->
<!-- Verified from: platform/ios/powershell-practice/Views/EmulatorView.swift [transcript] -->

### Do I need an internet connection?

No. The cmdlet library is included with the app, and answers are checked on
the device. Only the contact links, such as **Contact Plain Text Office** and
**Open contact form**, open a website, and sending feedback opens your email
app.

<!-- Verified from: docs/PRIVACY.md [On your device] -->
<!-- Verified from: platform/ios/powershell-practice/PrivacyPolicyView.swift [Link] -->
<!-- Verified from: platform/ios/powershell-practice/Feedback.swift [FeedbackView] -->

### Do aliases count as answers?

In a **Type the Command** quiz, yes: the full cmdlet name or any listed alias
is correct. In a **Multiple Choice** alias question, you choose the cmdlet
that the alias runs.

<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizMode.blurb, QuizQuestion.isCorrect] -->

### How does a cmdlet get into the Needs Review selection?

A cmdlet is included after you miss it at least once and your correct
answers for it fall below 70%. It leaves the selection when your accuracy for
it reaches 70% or more.

<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [needsReview] -->

### Does the app collect analytics or require an account?

No. The app contains no analytics, advertising, or tracking code and has no
accounts or sign-in.

<!-- Verified from: docs/PRIVACY.md [Developer services] -->

## Feedback

To report a bug or request a feature, email
[support@plaintxtoffice.com](mailto:support@plaintxtoffice.com), use the
contact page at <https://plaintxtoffice.com/contact/>, or use the feedback
screen in the app. The **Home** button is part of the layout that is in
development.

| Platform | How to open feedback |
| --- | --- |
| iOS | Tap **Send Feedback** on the **Home** tab, or tap the **Docs** tab, then **Guides**, then **Send Feedback** in the **About** section. In version 1.1.0, **Send Feedback** is in the **About** section of the **Docs** tab; in version 1.0.0, it is on the **Learn** tab's toolbar. |
| Android | Tap **Send Feedback** on the **Home** tab, or tap the **Docs** tab, then **Guides**, then **Send Feedback** in the **About** section. In version 1.1.0, tap the **Docs** tab, then **Send feedback** in the **About** section, or tap **More options** (three dots) on any tab, then **Send feedback**. |

<!-- Verified from: platform/ios/powershell-practice/Feedback.swift [Feedback, FeedbackButton, FeedbackView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/HomeView.swift [HomeView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [GuideSections] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/home/HomeScreen.kt [FeedbackPill] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/docs/DocsScreen.kt [DocsScreen] -->

### Send Feedback from the App

1. Tap **Send Feedback** on the **Home** tab or in the **About** section
   under **Docs**, **Guides**.
1. On iPhone and iPad, tap **Report a bug** or **Request a feature** to open a
   draft in your email app, or **Open contact form** to open the contact page
   in your browser.
1. On Android, choose **Bug report** or **Feature request**, describe it in
   **Details**, and tap **Send by email**, or tap **Use the contact page
   instead**.
1. Review the draft and send it from your email app.

The draft is addressed to `support@plaintxtoffice.com` and includes the app
version, the iOS or Android version, and the device model. It never includes
your learned cmdlets, quiz answers, or progress. Nothing is sent unless you
send it.

<!-- Verified from: platform/ios/powershell-practice/Feedback.swift [Feedback, FeedbackView] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/feedback/FeedbackScreen.kt [FeedbackScreen] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/home/HomeScreen.kt [FeedbackPill] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/docs/DocsScreen.kt [DocsScreen] -->

## Glossary

| Term | Meaning |
| --- | --- |
| Alias | A short alternative name for a cmdlet, such as `ls` for `Get-ChildItem`. |
| Cmdlet | A PowerShell command named in Verb-Noun form, such as `Get-Process`. |
| Emulator | The tab where you type examples and see their recorded output. It never runs commands. |
| Learned | A cmdlet you marked with **Mark as Learned**. |
| Needs Review | Cmdlets you missed at least once and answer correctly less than 70% of the time. |
| Pipeline | Cmdlets joined with `\|`, so that each one works on the objects the one before it sends. |
| Quiz record | The count of your correct and total quiz answers for one cmdlet, shown on its detail screen. |
| Syntax | The pattern for running a cmdlet, with its common parameters. |

<!-- Verified from: platform/ios/powershell-practice/Models/Command.swift [Command] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandLibrary.swift [Get-ChildItem aliases] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [needsReview] -->
<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [Quiz record] -->

---
last_updated: 2026-11-22
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
read about each cmdlet, mark it as learned, take quizzes, and follow your
progress.

| Item | Details |
| --- | --- |
| Platform | Android, on phones and tablets; iOS, on iPhone and iPad |
| Interface | Touch interface with four tabs: **Learn**, **Practice**, **Progress**, and **Docs** |
| Version | Android 1.1.0, iOS 1.1.0. The App Store has iOS 1.0.0; 1.1.0 is waiting for App Review |

<!-- Verified from: platform/ios/powershell-practice.xcodeproj/project.pbxproj [MARKETING_VERSION, TARGETED_DEVICE_FAMILY, INFOPLIST_KEY_CFBundleDisplayName] -->
<!-- Verified from: platform/ios/powershell-practice/ContentView.swift [ContentView] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandLibrary.swift [CommandLibrary.all] -->
<!-- Verified from: platform/ios/powershell-practice/Models/Command.swift [CommandCategory] -->

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
The App Store has version 1.0.0; version 1.1.0, described in this manual,
is waiting for App Review.

<!-- Verified from: platform/ios/powershell-practice.xcodeproj/project.pbxproj [PRODUCT_BUNDLE_IDENTIFIER, MARKETING_VERSION] -->

### Set Up the App

No setup is needed. The command library is included with the app, and your
progress starts empty the first time you open it.

<!-- Verified from: docs/PRIVACY.md [On your device] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [CommandProgress] -->

## Starting the Program

### Open PowerShell Practice

1. On your Home Screen or in the App Library, tap **PowerShell Practice**.
1. The app opens on the **Learn** tab, which lists the cmdlets by category.

<!-- Verified from: platform/ios/powershell-practice.xcodeproj/project.pbxproj [INFOPLIST_KEY_CFBundleDisplayName] -->
<!-- Verified from: platform/ios/powershell-practice/ContentView.swift [ContentView] -->

If the app cannot open your saved progress, it shows **Your data couldn't be
opened** instead. See [Troubleshooting](#troubleshooting).

<!-- Verified from: platform/ios/powershell-practice/StorageRecovery.swift [StorageRecoveryGate] -->

### Close PowerShell Practice

The app has no quit command. Leave it the way you leave any iOS app, such as
by returning to the Home Screen. Learned commands and quiz answers are saved
as you go.

<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [learnedButton] -->
<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [submit] -->

## Getting Around

The app has four tabs. On Android, wider windows may show them along the side.

| Tab | What you find there |
| --- | --- |
| **Learn** | The cmdlet library, grouped by category, with a search field |
| **Practice** | Quiz options, the **Start Quiz** button, pipeline practice, and the **Practice Terminal** |
| **Progress** | Your learned count, quiz accuracy, progress by category, commands that need review, and **Reset All Progress** |
| **Docs** | Guides to PowerShell conventions, and an **About** section with **Privacy**, **Send Feedback**, and the app version |

<!-- Verified from: platform/ios/powershell-practice/ContentView.swift [ContentView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/LearnView.swift [LearnView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [DocsView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [PracticeView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/StatsView.swift [StatsView] -->

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

Tap a cmdlet to open its detail screen. Use the back button at the top left to
return to the list. The guides in **Docs** explain PowerShell conventions, and
the **Privacy** screen there explains how the app handles your data.

<!-- Verified from: platform/ios/powershell-practice/Views/LearnView.swift [navigationDestination] -->

## Everyday Tasks

### Browse and Search the Cmdlet Library

1. Tap the **Learn** tab.
1. Scroll through the categories, or tap the search field, which shows
   **Cmdlet, alias, or task**.
1. Type part of a cmdlet name, an alias, or words from its description. The
   list shows only matching cmdlets.
1. Tap a cmdlet to open it.

A check mark next to a cmdlet means you marked it as learned. If nothing
matches your search, the app shows a no-results message.

<!-- Verified from: platform/ios/powershell-practice/Views/LearnView.swift [results(in:), searchable, CommandRow] -->

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

Learned cmdlets show a check mark in the **Learn** list and count toward the
**Learned** total on the **Progress** tab. If the change cannot be saved, the
app shows **Couldn't update progress** and leaves your progress unchanged.

<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [learnedButton] -->

### Take a Quiz

1. Tap the **Practice** tab.
1. Under **Quiz Type**, choose a quiz type:
   - **Multiple Choice**: pick the right cmdlet from four choices.
   - **Type the Command**: read the description and type the cmdlet. Aliases
     count as correct answers.
1. Under **Commands**, use **Practice** to choose which cmdlets to include.
1. Use the **Questions** stepper to choose how many questions to ask.
1. Tap **Start Quiz**.

<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [PracticeView] -->
<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizMode] -->

| Option | Default | Accepted values |
| --- | --- | --- |
| Quiz Type | **Multiple Choice** | **Multiple Choice** or **Type the Command** |
| Practice | **All Commands** | **All Commands**, **Not Yet Learned**, **Needs Review**, or one category |
| Questions | 10 | 5 to 30, in steps of 5 |

<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [mode, scope, questionCount, PracticeScope] -->

Each question in a quiz is about a different cmdlet. If your selection has
fewer cmdlets than the number of questions, the quiz asks one question per
cmdlet. The **Practice** list shows how many cmdlets each of the first three
choices contains. **Start Quiz** is unavailable when the selection is empty.
For **Needs Review**, the app explains that commands you miss in quizzes will
show up there.

<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizBuilder.makeQuestions] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [Start Quiz, footer] -->

These choices apply only to the quiz you start. The app does not keep them
after it closes.

<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [@State mode, scope, questionCount] -->

### Answer Quiz Questions

The quiz opens full screen and shows the question number, such as **1 of 10**,
and a progress bar.

<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [toolbar, questionView] -->

In a **Multiple Choice** quiz, each question is one of two kinds:

- **Which cmdlet does this?** shows a cmdlet's description.
- **Alias** asks **Which cmdlet does the alias ... run?** For this kind, only
  the full cmdlet name is correct.

Tap one of the four choices. The correct choice is marked in green, and a
wrong choice you picked is marked in red.

<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizQuestion.prompt, isCorrect, makeChoices] -->
<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [questionHeading, choices] -->

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
**Practice** tab has two ways to practice them. Each round asks 10 questions
about everyday tasks, such as listing the services that are running.

- **Pick the Pipeline**: choose the pipeline that does the task from four.
  Each wrong choice has one cmdlet swapped for a likely mistake.
- **Build the Pipeline**: tap the commands into order. One command is a decoy
  that the pipeline does not need. Tap a command you placed to take it back
  out. Once every stage is in place, tap **Check** on Android or **Check
  Answer** on iPhone.

After each answer, the app shows the right pipeline and explains how it
works. At the end, the results list the pipelines you missed. Pipeline
answers are not added to your accuracy, answer count, or **Needs Review**
list. To leave early, tap **Close** on Android or **End Practice** on iPhone.

<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/domain/Pipeline.kt [PipelineQuizBuilder, PipelineLibrary] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/pipeline/PipelineScreen.kt [PipelineBuilder, PipelineFeedback, PipelineResults] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PipelineView.swift [builder, feedback, PipelineSummary] -->

### Use the Practice Terminal

The practice terminal lets you type commands as you would at a
PowerShell prompt and see what they print. It knows the examples from the cmdlet
pages and the guides, and it never runs anything.

1. Tap the **Practice** tab, then **Practice Terminal**.
1. Type an example, such as `Get-Location`, and tap **Run** or use the keyboard
   submit key.
1. Read the output under your command. Like PowerShell, the terminal ignores
   capitalization and extra spaces.

If you type a cmdlet or alias the terminal knows but an example it doesn't, it
lists that cmdlet's examples; tap one to fill it in. **Try an Example** fills in
a random example. Use **Clear Screen**, `cls`, or `Clear-Host` to clear the
history. You can paste a command with its prompt, such as
`PS C:\Users\alex> Get-Location`.

<!-- Verified from: platform/ios/powershell-practice/Views/TerminalView.swift [TerminalView] -->
<!-- Verified from: platform/ios/powershell-practice/Models/PracticeTerminal.swift [PracticeTerminal.reply] -->

### Read the Guides

The **Docs** tab has five short guides: **Naming Rules**, **Command
Conventions**, **Piping Techniques**, **Variables and Quoting**, and
**Comparison Operators**. **Naming Rules** covers the Verb-Noun pattern,
approved verbs, singular nouns, capitalization, parameter names and aliases,
and how to name your own functions. Each guide has worked examples with their
output. Tap **Copy** beside a command to paste it into the practice terminal.

<!-- Verified from: platform/ios/powershell-practice/Models/GuideLibrary.swift [GuideLibrary.all] -->
<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [GuideView] -->

### Check Your Progress

Tap the **Progress** tab to see:

- **Learned**: how many of the 38 cmdlets you marked as learned.
- **Accuracy**: the percentage of all quiz answers that were correct.
- **Answers**: the total number of quiz answers you have given.
- **By Category**: learned cmdlets in each category, with a progress bar.
- **Needs Review**: cmdlets you have missed at least once and answer
  correctly less than 70% of the time, listed with your correct and total
  answers. The lowest accuracy is listed first. Tap one to open its detail
  screen.

<!-- Verified from: platform/ios/powershell-practice/Views/StatsView.swift [StatsView] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [needsReview, accuracy] -->

### Reset All Progress

1. Tap the **Progress** tab.
1. Scroll down and tap **Reset All Progress**.
1. In **Reset all progress?**, tap **Reset**.

This clears learned commands and quiz history, and it cannot be undone. The
button is unavailable when there is no progress to clear. If the reset fails,
the app shows **Couldn't reset progress** and leaves your progress unchanged.

<!-- Verified from: platform/ios/powershell-practice/Views/StatsView.swift [Reset All Progress, confirmationDialog, alert] -->

### Read the Privacy Information

1. Tap the **Docs** tab.
1. In the **About** section, tap **Privacy**.
1. Read the privacy information. It is available without a network
   connection.
1. Names of buttons appear in bold. At the end, tap **Send Feedback** to open
   the feedback screen, or **Contact Plain Text Office** to open the
   developer's website.

The screen ends with an **About** note: PowerShell is a trademark of Microsoft
Corporation, and PowerShell Practice is an independent study aid by Plain Text
Office LLC that is not affiliated with or endorsed by Microsoft. It also says
that the commands and aliases are for PowerShell 7 on Windows.

<!-- Verified from: platform/ios/powershell-practice/PrivacyPolicyView.swift [PrivacyPolicyButton, PrivacyPolicyView, About] -->

## Settings and Preferences

Not Applicable.
<!-- Verified from: platform/ios/powershell-practice/ContentView.swift, platform/ios/powershell-practice/Views/PracticeView.swift -->

## Importing and Exporting

Not Applicable.
<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift, platform/ios/powershell-practice/Views/StatsView.swift, docs/PRIVACY.md -->

## Commands and Shortcuts

The app has no keyboard shortcuts or menu commands. These on-screen controls
perform its main actions.

| Control | Where | What it does |
| --- | --- | --- |
| **Learn**, **Practice**, **Progress**, and **Docs** | Tab bar | Switch between the main screens |
| Search field | **Learn** | Filters cmdlets by name, alias, or description |
| **Privacy** | **Docs**, **About** section | Opens the privacy information |
| **Send Feedback** | **Docs**, **About** section, or the end of **Privacy** | Opens the feedback screen |
| **Practice Terminal** | **Practice** | Opens the practice terminal |
| **Copy** | Cmdlet detail or a guide | Copies the syntax or an example to the clipboard |
| **Mark as Learned** / **Learned** | Cmdlet detail | Marks or unmarks the cmdlet as learned |
| **Start Quiz** | **Practice** | Starts a quiz with the chosen options |
| **Check** | Quiz, **Type the Command** | Checks your typed answer |
| **Next Question** / **See Results** | Quiz | Moves to the next question or the results |
| **Close** | Quiz, top left | Leaves the quiz |
| **Reset All Progress** | **Progress** | Clears learned commands and quiz history after confirmation |

<!-- Verified from: platform/ios/powershell-practice/ContentView.swift [ContentView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/LearnView.swift [searchable] -->
<!-- Verified from: platform/ios/powershell-practice/Views/DocsView.swift [DocsView] -->
<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [CodeBlock, learnedButton] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [Start Quiz] -->
<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [typedInput, toolbar, safeAreaInset] -->
<!-- Verified from: platform/ios/powershell-practice/Views/StatsView.swift [Reset All Progress] -->

## Your Data Files

The app keeps its records inside its own storage on your device. You do not
open or edit these records by hand, and the app does not show their location.

| Data | Where it is stored | Can you edit it? |
| --- | --- | --- |
| Cmdlet library | Included with the app | No |
| Learned cmdlets and quiz answers for each cmdlet | The app's private storage on your device: an on-device library on iPhone and iPad, and the `progress.db` database on Android | No; change it through the app |

<!-- Verified from: platform/ios/powershell-practice/powershell_practiceApp.swift [StorageRecovery schema] -->
<!-- Verified from: platform/ios/powershell-practice/StorageRecovery.swift [ModelContainer, isStoredInMemoryOnly: false] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/di/AppModule.kt [Room.databaseBuilder "progress.db"] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [CommandProgress] -->
<!-- Verified from: docs/PRIVACY.md [On your device] -->

To remove your records, use **Reset All Progress** or delete the app. Device
backups may keep earlier copies. On iPhone and iPad, iCloud Backup and
computer backups can include the app's data; on Android, Android backup and
device transfer can include it. The app has no user-visible log files.

<!-- Verified from: docs/PRIVACY.md [Removing data] -->
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
| **Couldn't reset progress** appears. | The reset could not be saved. | Tap **OK** and try again. Your progress was not changed. |
| **Reset All Progress** is unavailable. | There is no progress to clear. | No action is needed. |

<!-- Verified from: platform/ios/powershell-practice/StorageRecovery.swift [StorageRecoveryGate] -->
<!-- Verified from: platform/ios/powershell-practice/Views/PracticeView.swift [Start Quiz, footer] -->
<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizBuilder.makeQuestions, isCorrect] -->
<!-- Verified from: platform/ios/powershell-practice/Views/CommandDetailView.swift [alert] -->
<!-- Verified from: platform/ios/powershell-practice/Views/QuizView.swift [alert] -->
<!-- Verified from: platform/ios/powershell-practice/Views/StatsView.swift [alert, disabled] -->

## FAQ

### Does the app run PowerShell commands?

No. The app does not run PowerShell commands or connect to a PowerShell
server. The practice terminal shows recorded output for the examples and
never runs what you type. Try the examples in PowerShell on a computer.

<!-- Verified from: docs/PRIVACY.md [On your device] -->

### Do I need an internet connection?

No. The cmdlet library is included with the app, and answers are checked on
the device. Only **Contact Plain Text Office** and **Open contact form** open a
website, and **Report a bug** and **Request a feature** open your email app.

<!-- Verified from: docs/PRIVACY.md [On your device] -->
<!-- Verified from: platform/ios/powershell-practice/PrivacyPolicyView.swift [Link] -->
<!-- Verified from: platform/ios/powershell-practice/Feedback.swift [FeedbackView] -->

### Do aliases count as answers?

In a **Type the Command** quiz, yes: the full cmdlet name or any listed alias
is correct. In a **Multiple Choice** alias question, you choose the cmdlet
that the alias runs.

<!-- Verified from: platform/ios/powershell-practice/Models/Quiz.swift [QuizMode.blurb, QuizQuestion.isCorrect] -->

### How does a cmdlet get on the Needs Review list?

A cmdlet appears there after you miss it at least once and your correct
answers for it fall below 70%. It leaves the list when your accuracy for it
reaches 70% or more.

<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [needsReview] -->

### Does the app collect analytics or require an account?

No. The app contains no analytics, advertising, or tracking code and has no
accounts or sign-in.

<!-- Verified from: docs/PRIVACY.md [Developer services] -->

## Feedback

To report a bug or request a feature, email
[support@plaintxtoffice.com](mailto:support@plaintxtoffice.com), use the
contact page at <https://plaintxtoffice.com/contact/>, or use the feedback
screen in the app:

| Platform | How to open feedback |
| --- | --- |
| iOS | Tap the **Docs** tab, then **Send Feedback** in the **About** section. In version 1.0.0, **Send Feedback** is on the **Learn** tab's toolbar. |
| Android | Tap the **Docs** tab, then **Send feedback** in the **About** section, or tap **More options** (three dots) on any tab, then **Send feedback**. |

<!-- Verified from: platform/ios/powershell-practice/Feedback.swift [Feedback, FeedbackView] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/home/HomeScreen.kt [HomeMenu] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/docs/DocsScreen.kt [DocsScreen] -->

### Send Feedback from the App

1. Tap the **Docs** tab, and in the **About** section tap **Send Feedback**
   (**Send feedback** on Android). On Android, you can also tap **More
   options** (three dots) on any tab and then **Send feedback**. In iOS
   version 1.0.0, **Send Feedback** is on the **Learn** tab's toolbar.
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
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/home/HomeScreen.kt [HomeMenu] -->
<!-- Verified from: platform/android/app/src/main/kotlin/com/plaintxtoffice/powershellpractice/feature/docs/DocsScreen.kt [DocsScreen] -->

## Glossary

| Term | Meaning |
| --- | --- |
| Alias | A short alternative name for a cmdlet, such as `ls` for `Get-ChildItem`. |
| Cmdlet | A PowerShell command named in Verb-Noun form, such as `Get-Process`. |
| Learned | A cmdlet you marked with **Mark as Learned**. |
| Accuracy | The share of your quiz answers that were correct. |
| Needs Review | Cmdlets you missed at least once and answer correctly less than 70% of the time. |
| Syntax | The pattern for running a cmdlet, with its common parameters. |

<!-- Verified from: platform/ios/powershell-practice/Models/Command.swift [Command] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandLibrary.swift [Get-ChildItem aliases] -->
<!-- Verified from: platform/ios/powershell-practice/Models/CommandProgress.swift [accuracy, needsReview] -->

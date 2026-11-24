---
last_updated: 2026-11-24
---

<!-- Authoring guidance: dev-docs/specs/README_SPEC.instructions.md -->
<!-- rumdl-disable MD033 MD041 -->
<p align="center">
  <img src="assets/icons/icon-github-readme.svg" alt="PowerShell Practice icon" width="96">
</p>

<h1 align="center">PowerShell Practice</h1>

<p align="center">
  An app that helps PowerShell beginners learn everyday cmdlets and test
  themselves with quick quizzes.
</p>

<p align="center">
  <a href="https://play.google.com/store/apps/details?id=com.plaintxtoffice.powershellpractice"><img src="https://img.shields.io/badge/release-Google%20Play-blue" alt="Android release: Google Play"></a>
  <a href="https://apps.apple.com/app/id6837567736"><img src="https://img.shields.io/badge/release-App%20Store-blue" alt="iOS release: App Store"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-Proprietary-informational" alt="License: Proprietary"></a>
  <a href="#download"><img src="https://img.shields.io/badge/platform-Android%20%7C%20iOS-3DDC84" alt="Platforms: Android and iOS"></a>
</p>
<!-- rumdl-enable MD033 MD041 -->

---

## About

PowerShell has hundreds of commands, and remembering their names, aliases, and
syntax takes practice. PowerShell Practice gives you a pocket reference of
common cmdlets, from getting help and working with files to the pipeline,
processes, output, and networking, along with quizzes that check what you
remember. Everything works on your device, with no account and no PowerShell
connection needed. The app runs on Android phones and tablets and on iPhone
and iPad, and is available on
[Google Play](https://play.google.com/store/apps/details?id=com.plaintxtoffice.powershellpractice)
and the [App Store](https://apps.apple.com/app/id6837567736).

## Features

- Browse common cmdlets in seven categories, or search by name, alias, or task.
- Read each cmdlet's summary, syntax, aliases, examples, and tips, and copy
  any command to the clipboard.
- Mark cmdlets as learned; learned cmdlets show a check mark in the list.
- Take multiple-choice or type-the-command quizzes of 5 to 30 questions on all
  cmdlets, ones you have not learned yet, ones that need review, or a single
  category.
- See your score and the cmdlets you missed at the end of each quiz.
- Practice pipelines: pick the pipeline that does a task, or build it by
  tapping cmdlets into order.
- See each cmdlet's quiz record, and quiz yourself on the cmdlets that need
  review.
- Create sandbox projects in the emulator: virtual Windows computers where file
  commands such as `New-Item`, `Set-Content`, and `Remove-Item` create, change,
  and remove folders and files. Projects are saved on your device.
- Read five short guides in the **Docs** tab, on naming rules, command
  conventions, piping techniques, variables and quoting, and comparison
  operators, each with worked examples and their output.
- Type examples into the emulator to see their recorded output. Nothing you
  type runs on your device.
- Send a bug report or feature request from inside the app.

Version 1.2.0 arranges the app into four tabs: **Home**, **Practice**,
**Emulator**, and **Docs**. **Docs** holds the cmdlet library under **Commands**
and the guides under **Guides**, **Emulator** replaces the **Practice Terminal**
and adds sandbox projects, and **Home** adds a **Send Feedback** button. The
**Progress** tab and its totals are not part of that layout; learned marks and
quiz records carry over, and **Reset All Progress** moves to the **About**
section under **Docs**, **Guides**. Pipeline rounds can have 1 to 14 questions,
and the app remembers the number you choose. Version 1.2.0 is on the App Store
and Google Play. Version 1.1.0 has the tabs **Learn**,
**Practice**, **Progress**, and **Docs**.

## Download

| Platform | Download | Notes |
| --- | --- | --- |
| Android | [Google Play](https://play.google.com/store/apps/details?id=com.plaintxtoffice.powershellpractice) | Version 1.2.0, with the four-tab layout and sandbox projects. Requires Android 8.0 or later. |
| iOS | [App Store](https://apps.apple.com/app/id6837567736) | Version 1.2.0, with the four-tab layout and sandbox projects. Requires iOS 26.5 or later on iPhone or iPad. |

## User Manual

See the [User Manual](docs/USER_MANUAL.md) for installation, setup, usage, and
troubleshooting.

## Feedback

Send bug reports and feature requests to
[feedback@plaintxtoffice.com](mailto:feedback@plaintxtoffice.com), through the
[contact page](https://plaintxtoffice.com/contact/), or in
[GitHub Issues](https://github.com/PlainTxtOffice/powershell-practice/issues).
In the app, **Send Feedback** prepares an email for you to send; version 1.2.0
and earlier address it to `support@plaintxtoffice.com`. In version 1.2.0, find
it on the **Home** tab and under **About** in **Docs**, **Guides**. In version
1.1.0, it is under **About** in **Docs**, and on Android also in
**More options** (three dots) on any tab. In iOS version 1.0.0, it is on the
**Learn** tab's toolbar.

## License

PowerShell Practice is proprietary software owned by Plain Text Office LLC. See
[LICENSE](LICENSE) for the terms; all rights reserved.

# Wasal Build

Public build and test automation for the Wasal Android messenger. Application and backend source stay in the private `ahmed9461/Wasal` repository.

The **Build and test Wasal** workflow can be started by the repository owner using **Actions → Run workflow**. It reads the private main branch using a repository-specific, read-only deploy key. Forks and pull requests do not run this workflow with secrets.

The workflow tests registration, email verification, private messaging, device token ownership and audio call signaling against a disposable PostgreSQL database and a local SMTP fixture. This proves application behavior with synthetic email; it does not prove Gmail inbox delivery. Source, backend configuration, keystores and detailed build logs are never uploaded as public artifacts. Only the signed Android APK and checksums are published as build artifacts.

Current application version: `0.3.0-rc3`. Real Gmail verification and two-account device messaging have passed. Background notifications, incoming/outgoing phone audio and the stopped call timer passed separate live device checks. The redesigned interface is a preview awaiting owner review. This is a release candidate.

The rc3 preview addresses owner feedback on native audio waveforms, chat wallpaper, the Calls tab, and direct entry for saved sessions. Design review remains active; this is not a stable release.

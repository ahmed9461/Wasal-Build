# Wasal Build

Public build and test automation for the Wasal Android messenger. Application and backend source stay in the private `ahmed9461/Wasal` repository.

The **Build and test Wasal** workflow can be started by the repository owner using **Actions → Run workflow**. It reads the pinned private source revision using a repository-specific, read-only deploy key. Forks and pull requests do not run this workflow with secrets.

The workflow tests registration, email verification, private messaging, device token ownership and audio call signaling against a disposable PostgreSQL database and a local SMTP fixture. This proves application behavior with synthetic email; it does not prove Gmail inbox delivery. Source, backend configuration, keystores and detailed build logs are never uploaded as public artifacts. Only the signed Android APK and checksums are published as build artifacts.

Current application version: `0.4.0-rc1`. Real Gmail verification and two-account device messaging have passed. Background notifications, incoming/outgoing phone audio and the stopped call timer passed separate live device checks. The redesigned interface is a preview awaiting owner review. This is a release candidate.

This preview adds synchronized replies, time-limited editing, personal/global deletion, editable profiles, account-scoped offline media and redesigned navigation/settings. Design review remains active; this is not a stable release.

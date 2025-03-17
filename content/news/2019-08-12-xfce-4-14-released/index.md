---
title:     "Xfce 4.14 released"
date:      2019-08-12
version:   "4.14"
author:    "Release Manager"
timestamp: 1565568000
---

Today, after 4 years and 5 months of work, we are pleased to announce the release of the Xfce desktop 4.14, a new stable version that supersedes Xfce 4.12.

In this 4.14 cycle the main goal was to port all core components to Gtk3 (over Gtk2) and GDBus (over D-Bus GLib). Most components also received GObject Introspection support. Along the way we ended up polishing our user experience, introducing quite a few new features and improvements (read below) and fixings a boatload of bugs (read changelog).

The <strong>main highlights of this release</strong> are:

* The <a href="https://docs.xfce.org/xfce/xfwm4/start">window manager</a> received a slew of updates and features, including support for VSync (using either Present or OpenGL as backend) to reduce or remove display flickering, HiDPI support, improved GLX support with NVIDIA proprietary/closed source drivers, support for XInput2, various compositor improvements and a new default theme.
* The <a href="https://docs.xfce.org/xfce/xfce4-panel/start">panel</a> got support for RandR's primary monitor feature, improved window grouping in the tasklist plugin (better UX, visual group indicator etc), a per-panel “icon-size” setting, a new default clock format and clock format evaluator as well as an improved default panel layout.
* The <a href="https://docs.xfce.org/xfce/xfdesktop/start">desktop</a> now has support for RandR's primary monitor feature, an orientation option for icon arrangement, a “Next Background” context menu option to advance the wallpaper and it now syncs the user's wallpaper selection to AccountsService.
* A completely new settings dialog to <a href="https://docs.xfce.org/xfce/xfce4-settings/color">manage color profiles</a> has been created. For most users this means out of the box support for color-managed printing (through cupsd) and scanning (through saned). For monitor profiles you will have to install an additional service like xiccd.
* The <a href="https://docs.xfce.org/xfce/xfce4-settings/display">display dialog</a> received a lot of attention during this cycle and a big feature: Users are now able to save and (automatically) restore complete multi-display configurations, which is especially helpful for those who frequently connect their laptop to varying docking stations or setups. Furthermore a lot of time was spent on making the user interface more intuitive and a hidden option was added to support RandR display scaling (configured via Xfconf).
* We added an option to enable Gtk window scaling to the <a href="https://docs.xfce.org/xfce/xfce4-settings/appearance">appearance dialog</a> and a monospace font option as well. However we had to drop theme previews as they didn\'t produce consistent results with Gtk3.
* While we decided to drop splash screens from the <a href="https://docs.xfce.org/xfce/xfce4-session/start">session manager</a>, we added lots of features and fixes instead. Among them are hybrid sleep support, improvements to the default session startup avoiding race conditions, a feature to add and edit autostart entries, a switch user button in the logout dialog and improved session chooser and settings dialogs (the latter with a new tab that shows saved sessions). Furthermore you can now run commands not only "autostart style" at login time, but also when your computer suspends, logs out etc. Finally Gtk applications are now session-managed over DBus and screensavers are also communicated with (e.g. inhibited) over DBus.
* As always, <a href="https://docs.xfce.org/xfce/thunar/start">Thunar</a> - our file manager - received a lot of features and fixes. Among the visible changes are the completely reworked pathbar, support for larger thumbnails as well as support for a "folder.jpg" file altering the folder\'s icon (e.g. for music album covers). Power users will also notice the improved keyboard navigation (zooming, tab navigation). Thunar\'s volume manager has gained Bluray support.
* Our <a href="https://docs.xfce.org/xfce/thunar/tumbler">thumbnailing service tumbler</a> received a lot of fixes and support for the Fujifilm RAF format.
* The <a href="https://docs.xfce.org/xfce/xfce4-appfinder/start">application finder</a> can now optionally be opened as a single window and can now be more easily navigated with the keyboard only.
* The <a href="https://docs.xfce.org/xfce/xfce4-power-manager/start">power manager</a> received a lot of bugfixes and some smaller features, including support for the XF86Battery button and for the newly created xfce4-screensaver. The panel plugin also saw several improvements: it can now optionally show the remaining time and/or percentage and it now relies on UPower's standard icon names to work with more icon themes out of the box. With LXDE moving on to a QT base the LXDE panel plugin was dropped.

A lot of <strong>applications and plugins</strong> that are part of the Xfce eco-system - often dubbed "goodies" - are part of what makes Xfce great. A lot of those have also seen important changes along the timeline of the 4.14 release. To highlight a few:

* Our <a href="https://docs.xfce.org/apps/notifyd/start">notification service</a> has gained support for persistence - in other words: notification logging - and a "Do Not Disturb" mode, which suppresses all notifications. A new panel plugin was created that shows missed notifications (especially helpful during "Do Not Disturb" mode) and gives quick access to toggling "Do Not  Disturb" mode. Finally support for showing notifications on RandR's primary monitor was added.
* Our media player <a href="https://docs.xfce.org/apps/parole/start">Parole</a> received improved support for network streams and podcasts, as well as a new "mini mode" and automatic choosing of the best available video backend. Furthermore it also inhibits both screensavers and power managers during video playback now, making sure users don\'t have to go wiggle their mouse periodically while enjoying a movie.
* Our image viewer <a href="https://docs.xfce.org/apps/ristretto/start">Ristretto</a> has seen various user interface improvements and support for setting the desktop wallpaper. It has recently also seen its first Gtk3-based development release.
* The <a href="https://docs.xfce.org/apps/screenshooter/start">screenshooter</a> now allows users to move the selection rectangle and at the same time displays its width and height. The imgur upload dialog was revamped and the command line allows for more flexibility.
* Our <a href="https://docs.xfce.org/panel-plugins/clipman/start">clipboard manager</a> now has improved keyboard shortcut support (through a port to GtkApplication), improved and more consistent icon sizing as well as a new application icon.
* The <a href="https://docs.xfce.org/apps/pulseaudio-plugin/start">pulseaudio panel plugin</a> received MPRIS2 support to be able to remotely control media players and desktop-wide multimedia key support, essentially rendering xfce4-volumed-pulse a superfluous additional daemon.
* And finally the <a href="https://docs.xfce.org/apps/terminal/start">terminal emulator</a> saw a huge amount of bug fixes and improvements since Xfce 4.12.

There is also a group of <strong>new projects</strong> that have become part of our project. Say hi to:

*  We finally have our own <a href="https://docs.xfce.org/apps/screensaver/start">screensaver</a> (yes - we realize it's 2019 ;)). With lots of features and tight Xfce integration (obviously) it is a great addition to our catalog.
* The <a href="https://goodies.xfce.org/projects/panel-plugins/xfce4-statusnotifier-plugin">status notifier panel plugin</a> provides a next-generation system tray where applications can show indicators. It supersedes the Ubuntu-centric xfce4-indicator-plugin for most application indicators.
* <a href="https://docs.xfce.org/apps/catfish/start">Catfish file search</a> is like an old friend for most Xfce users - now it's officially part of Xfce!
* Finally <a href="https://git.xfce.org/apps/xfce4-panel-profiles/about/">Panel Profiles</a>, which allows you to backup and restore your panel layouts, has moved under the Xfce umbrella.

As always it's also time to say goodbye to some older <strong>unmaintained or deprecated projects</strong>. (Luckily our projects only go to the attic aka the archive on git.xfce.org when they die.) With a salty teardrop of sadness we bid farewell to:

* garcon-vala, gtk-xfce-engine, pyxfce, thunar-actions-plugin, xfbib, xfc, xfce4-kbdleds-plugin, xfce4-mm, xfce4-taskbar-plugin, xfce4-windowlist-plugin, xfce4-wmdock-plugin and xfswitch-plugin

An online tour of the changes in Xfce 4.14 can be viewed here:

<a href="https://xfce.org/about/tour">https://xfce.org/about/tour</a>

A detailed overview of the changes between Xfce 4.12 and Xfce 4.14 releases can be found on the following page:

<a href="https://xfce.org/download/changelogs">https://xfce.org/download/changelogs</a>

This release can be downloaded either as a set of individual packages or as a single fat tarball including all these individual versions:

<a href="http://archive.xfce.org/xfce/4.14">http://archive.xfce.org/xfce/4.14</a>

Best regards,<br />
The Xfce development team

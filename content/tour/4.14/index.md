---
title:     "Xfce 4.14 tour"
version:   "4.14"
---

This tour will introduce you to new major features of Xfce 4.14. It only covers improvements made on the surface; for the full list of changes, see the {{< changelog version="4.14" >}}.

## Settings Manager (xfce4-settings)

### Color Profiles Dialog

A new dialog for setting <a href='https://docs.xfce.org/xfce/xfce4-settings/4.14/color'>color profiles</a> for monitors, printers and scanners was introduced. It acts as a frontend to various daemons that talk directly to colord, e.g. saned (scanners), cupsd (printers) or xiccd (monitors).

{{< figure src="color-profiles.png" caption="The new color profiles dialog" >}}

### Display Dialog

Several improvements were made to the <a href='https://docs.xfce.org/xfce/xfce4-settings/4.14/display'>display dialog</a>. Apart from tweaks to the user interface to make the interaction more intuitive (introducing display numbering, showing a primary indicator with quick access to panel, notification and desktop settings etc.) a feature to save and restore complete display profiles was added. If a single profile exists for a setup, the Xfce settings daemon will automatically enable it. If multiple profiles exist, it will pop up the minimal dialog and offer all profiles in addition to the previously available pre-sets (internal only, mirror, extend and external only).

{{< figure src="display-general.png" caption="The primary indicator" >}}
{{< figure src="display-advanced.png" caption="The display profile list" >}}
{{< figure src="display-minimal.png" caption="The improved minimal dialog - in this case only showing one profile only which never happens anymore now ;)" >}}

### Accessibility

One <a href='https://docs.xfce.org/xfce/xfce4-settings/4.14/accessibility'>accessibility</a> feature that people coming from other desktop environments or operating systems were still missing is to set a (custom) keyboard shortcut (by default: Super+F1) to visually locate the mouse pointer. This feature was added in Xfce 4.14.

{{< figure src="locate-mouse.gif" caption="The mouse pointer location animation" >}}

## Panel (xfce4-panel)

### General: Icon size

A new feature that we introduced in the <a href='https://docs.xfce.org/xfce/xfce4-panel/4.14/start'>panel</a> is being able to control the icon size of all plugins. ('All' may not be technically correct, as not all plugins support the new API as of now, but now they <i>can</i>. Plus the Window buttons plugin is an exception, because libwnck doesn't allow anything other than 16px or 32px.) This means setups that were previously impossible, because icons would upscale automatically according to size-steps hard-coded in the panel, are now possible (see below).

{{< figure src="panel-iconsize.png" caption="A 32px tall panel with 16px icons" >}}

### Window buttons: Grouping

Grouping was improved in the <a href='https://docs.xfce.org/xfce/xfce4-panel/4.14/tasklist'>Window buttons plugin</a>, both functionally (by improving the matching and icon-finding) and visually by providing a new group indicator that is less likely to clash with window titles containing an enumeration in brackets.

{{< figure src="panel-group.png" caption="The new group indicator (two terminal windows)" >}}

## Session (xfce4-session)

### Settings Dialog

As soon as a <a href='https://docs.xfce.org/xfce/xfce4-session/4.14/preferences'>session</a> has been saved a new tab is dynamically added to the settings dialog displaying all saved sessions and allowing to delete one or all of them. This should make it way more discoverable for users if they actually have saved sessions that influence the startup behavior - previously this had to be checked manually in the filesystem.

{{< figure src="session-saved.png" caption="The settings dialog after saving a session" >}}

## File Manager (thunar)

### Pathbar

Up to Xfce 4.12 <a href='https://docs.xfce.org/xfce/thunar/4.14/start'>Thunar</a> offered two options for the pathbar/locationbar. The best of both worlds has now been mixed into one powerful pathbar, featuring both clickable breadcrumbs (i.e. folders), an easily accessible way to hand-type a path as well as an improved look.

{{< figure src="thunar-pathbar.png" caption="Thunar's new pathbar" >}}

### Folder Thumbnailer

Same as on the Desktop you can now save an image with the name 'folder.jpg' in a folder and get it displayed as its icon in the File Manager. Note: <a href='https://docs.xfce.org/xfce/tumbler/available_plugins#customized_thumbnailer_for_folders'>Please read the docs</a> on how to set this up (if your distribution hasn't enabled it by default).

{{< figure src="thunar-folder-jpg.png" caption="Thunar's new folder thumbnails" >}}

## Power Manager (xfce4-power-manager)

### Panel Plugin

The <a href='https://docs.xfce.org/xfce/xfce4-power-manager/4.14/panel-plugin'>Power Manager's panel plugin</a> supports symbolic icons now and uses the standard UPower icon names (making it more compatible with all icon themes). It also shows an indicator if applications inhibit power management functions like suspend (when power is low) or display dimming (after a defined timeout).

{{< figure src="xfpm-inhibitors.png" caption="Parole's video playback is inhibiting power management" >}}

## Notification Service (xfce4-notifyd)

### Settings

Several new features have been added in Xfce's <a href='https://docs.xfce.org/apps/notifyd/start'>Notification service</a>, including a notifications log, the possibility to disable notifications per application, a global 'Do Not Disturb' mode, which inhibits all notifications, and finally a new animation ('slide out').

{{< figure src="notifyd-slideout.gif" caption="The new notification animation 'slide out'" >}}

### Panel Plugin

Furthermore a new panel plugin was added which provides quick access to both the 'Do Not Disturb' mode as well as the log of recent notifications.

{{< figure src="notifyd-panel.png" caption="The new panel plugin" >}}

## Media Player (parole)

### Mini Mode

<a href='https://docs.xfce.org/apps/parole/start'>Parole</a> now features a 'Mini Mode', where the interface is simplified to just display the album artwork and can be positioned over other windows without getting in the way.

{{< figure src="parole-normal-mode.png" caption="Just right-click anywhere in the player window to select 'Mini Mode'..." >}}

{{< figure src="parole-mini-mode.png" caption="Afterwards, enjoy a truly minimalistic playback experience!" >}}

## Screensaver (xfce4-screensaver)

### A Modern Locking Experience

The new Xfce <a href='https://docs.xfce.org/apps/screensaver/start'>Screensaver</a> provides a configurable lockscreen experience. You can selectively toggle the lock screen and screensaver, and all Xscreensaver themes are supported (with configuration options) out of the box. If you prefer a blank screen, Xfce Screensaver also includes a blank screen option with DPMS integration.

{{< figure src="saver-dialog.png" caption="The new lock screen, sharing styles with LightDM GTK+ Greeter for a consistent experience." >}}
{{< figure src="saver-preferences.png" caption="Make it your own. Xfce Screensaver supports a multitude of configuration options." >}}

## Terminal (xfce4-terminal)

Lots and lots of features have accumulated in the <a href='https://docs.xfce.org/apps/terminal/start'>Terminal</a> over the last years. Amongst them 'Undo Close Tab' and 'Close Other Tabs' functionality (similar to web browsers), 'Copy Input to All Tabs', 'Set Title Color' (allows to customize tab text color), 'Save Contents' (saves tab contents to a file), an 'Unsafe Paste' dialog (which prevents the terminal from auto-executing pasted text as a command) and support for zooming. Finally when closing a tab or window, there is a new check for running processes which prevents accidentally closing a terminal that is running a process.

{{< figure src="terminal.png" caption="Zooming, 'Save Contents' and much more!" >}}

## Screenshooter (xfce4-screenshooter)

The Xfce <a href='https://docs.xfce.org/apps/screenshooter/start'>Screenshooter</a> gained several notable features, amongst others seeing the size of the screenshot while dragging, moving the selection with the mouse and better <a href='https://imgur.com'>imgur</a> integration.

{{< figure src="screenshooter.gif" caption="I can drag and move the screenshot area, whoop whoop!" >}}

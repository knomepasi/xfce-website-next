---
title:     "Xfce 4.16 tour"
version:   "4.16"
---

This tour will introduce you to new major features of Xfce 4.16. It only covers improvements made on the (user-visible) surface; for the full list of changes, see the {{< changelog version="4.16" >}}</p>

## Visual identity: New icons and palette

In order to make Xfce shine a little more out of the box and to strengthen its visual identity we created new icons for all of our core applications and based them on a shared palette to ensure consistency. We also set some further (implicit) design constraints, loosely following Adwaita's principles.

{{< figure src="palette.png" caption="The Xfce palette" >}}
{{< figure src="upstream-icons.png" caption="New upstream Xfce icons, coming in many sizes for sharp appearance" >}}

## Settings Manager (xfce4-settings)

The Settings Manager itself received a visual refresh of its filter box, which can now be hidden permanently. At the same time the search capabilities of the filter box were improved by searching the descriptive 'Comments' part of each dialog's launcher (aka <a href='https://specifications.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html'>.desktop</a>) file.

{{< figure src="settings-manager.png" caption="Visually cleaner, more powerful filter box" >}}

### Default Applications

This new dialog represents a merger between the previously available 'Mime Settings' and the 'Preferred Applications' dialogs. Consolidating both in one place means users have an easier time setting default applications to handle certain file types.

{{< figure src="default-applications.png" caption="The new Default Applications dialog" >}}

### Display Dialog

To better support high-density displays - which come in various sizes and densities - we added fractional scaling based on the RandR extension of X11. Furthermore the preferred mode of a display is now marked with an asterisk and aspect ratios are shown along display resolutions.

{{< figure src="display-dialog.png" caption="Fractional scaling support" >}}

### Keyboard Shortcuts

In order to make things easier for our users we added more default keyboard shortcuts out of the box, for instance for window tiling or to open Thunar. The keyboard shortcuts dialog itself was also visually updated.

{{< figure src="keyboard-shortcuts.png" caption="Visually updated keyboard shortcuts dialog" >}}

## File Manager (thunar)

In Thunar's copy and move dialogs users can now easily pause the respective file operation. Furthermore support for queued file transfer, remembering view settings per folder and support for transparency in Gtk themes was added.

{{< figure src="thunar-copy.png" caption="Thunar can now pause copying/moving files" >}}

## Panel (xfce4-panel)

The panel received quite a few noteworthy updates, an animation for autohide and intellihide, a new 'Status Tray' plugin that combines both legacy Systray item support with modern StatusNotifier item support, dark mode support, launchers showing additional actions on right-click, window buttons offering to 'Launch a new instance...' and much more.

{{< figure src="panel-dark.png" caption="Dark mode enabled in the panel's settings dialog" >}}
{{< figure src="panel-statustray.png" caption="The new statustray plugin" >}}
{{< figure src="panel-autohide.gif" caption="Autohide animation" >}}
{{< figure src="panel-launch.png" caption="Launch a new instance!" >}}

## About Dialog (xfce4-about)

Not only was the Xfce tab reworked to be more visually appealing and easily parsable, a separate tab showing basic information about the user's system was also added.

{{< figure src="about-xfce.png" caption="About Xfce" >}}
{{< figure src="about-system.png" caption="About System" >}}

## Power Manager (xfce4-power-manager)

The settings dialog of the power manager was cleaned up and shows either 'on battery' or 'plugged in' settings as opposed to both in a huge table.

{{< figure src="powermanager.png" caption="Power Manager settings" >}}

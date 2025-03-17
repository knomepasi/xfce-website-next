---
title:     "Xfce 4.10 tour"
version:   "4.10"
---

This tour will introduce you to new major features of Xfce 4.10. It only covers the visual part of what has been done; for the full list of changes, see the {{< changelog version="4.10" >}}.

## Online Documentation

During the 4.10 development we've decided to remove user manuals from the packages and move them to an online wiki at <a href=\"https://docs.xfce.org\">docs.xfce.org</a>. The reason for this change is to make <a href=\"https://docs.xfce.org/wiki/documentation\">contributing</a> and updating the documentation easier.

{{< figure src="online-help.png" caption="When you click a Help button Xfce will ask you to go to an online wiki page" >}}

We hope that with the introduction of the wiki it will be easier for developers and contributors to maintain the documentation.

## Application Finder (xfce4-appfinder)

{{< figure src="appfinder-collapsed.png" caption="Collapsed view of the Application Finder" >}}

The application finder has been completely rewritten and combines the functionality of the old appfinder and xfrun4. Apart from user interface improvements, it now allows creating custom actions matching a prefix or a regex pattern.

{{< figure src="appfinder-expanded.png" caption="Expanded view of the Application Finder" >}}

## Panel (xfce4-panel)

### Multiple Rows

In 4.10 there is a single panel-wide option for configuring the number of  rows in the panel. Some plugins (e.g. _launchers_) fit a single row, while others, like window buttons are allowed to occupy full width of the panel.

{{< figure src="panel-rows.png" caption="A horizontal panel with a number of rows set to three" >}}

### Deskbar Mode

The panel features a new configuration called a _deskbar_ mode. In the deskbar  mode the panel is aligned vertically, just like in the vertical mode, but the plugins are laid out horizontally. With multiple rows, it allows creating wide vertical panels suitable for wide-screen setups.

{{< figure src="panel-deskbar.png" caption="A panel in Deskbar mode with a number of rows set to five" >}}

### Actions Plugin

Session plugin from the xfce4-session package has been merged with a rewritten _actions_ plugin

{{< figure src="panel-actions.png" caption="Action plugin in a menu mode (left), and in a button mode (right)" >}}

### Window Buttons

The _window buttons_ plugin no longer expands, which makes the plugin positioning more flexible. In order to restore the previous behavior please add a transparent _separator_ plugin with the **Expand** option enabled just behind the window buttons plugin.

## File Manager (thunar)

There are few visual changes in this release of Thunar. The window has less padding and the position of the status bar has been adjusted.

## Session Manager (xfce4-session)

The _session manager_&apos;s settings dialog has a button for clearing the saved session (no more <tt>rm -r ~/.config/sessions</tt>). Xfce4-tips has been removed and the session manager can now lock the screen before suspending or hibernating the system.

### Applications Autostart

Another noticeable change is the way GNOME and KDE compatibility works. Compatibility check boxes only enable services, which have to be started before other applications (_gnome-keyring_ and _gconf_ for GNOME and _kdeinit_ for KDE). All other autostart applications are available from **Applications Autostart**, but they are listed using an italic font and not enabled by default in order to distinguish them from Xfce applications. Unlike in previous versions of Xfce, compatibility services can be started independently from each other.

{{< figure src="session-autostart.png" caption="Applications, which are not a part of Xfce, are listed using an italic font" >}}

## Settings (xfce4-settings)

### Settings Daemon

Xfce 4.8 used two processes for applying settings: <tt>xfce4-settings-helper</tt> and <tt>xfsettingsd</tt>. In 4.10 they have been merged into xfsettingsd, which now handles all system settings.

### Settings Manager

The new _settings manager_ groups configuration dialogs in categories and allows you to search for their names or descriptions. Most of the dialogs are also now embedded in the settings manager window (this was a compile-time option in Xfce 4.8).

{{< figure src="settings-manager.png" caption="The settings manager with icons grouped by category and a search filter applied" >}}

### Settings Editor

The _settings editor_ no longer collapses the entire tree when you edit a property (this is because it now reloads a single cell rather than the whole tree). Most properties can now be edited in-place, making it easier to quickly adjust settings.

Using settings editor you can also monitor changes of settings in a selected channel. Right-click on a channel in the main window, and select **Monitor** to display the monitor window.

{{< figure src="settings-editor.png" caption="Settings editor with an open channel monitor, while editing a property in-place" >}}

### MIME Type Editor

In the last couple of years, many people were asking for a tool to manage their file type associations. The new _MIME type editor_ does just that. It allows you to easily assign a default application to a file type, see your changes and reset them to default settings when necessary. Note that it does not allow you to change the system MIME Type definitions (add or remove types and change icons).

{{< figure src="settings-mime.png" caption="MIME types matching a pattern and a menu for selecting a default application" >}}

### Mouse and Touchpad

The _mouse and touchpad_ dialog is capable of handling basic Synaptics and Wacom properties in the GUI. A settings daemon running in the background handles all kinds of device properties, as documented in the <a href=\"https://docs.xfce.org/xfce/xfce4-settings/mouse\">mouse settings</a> wiki.

{{< figure src="settings-mouse.png" caption="Synaptics touchpad settings in the _mouse and touchpad_ dialog" >}}

### Appearance Settings

In 4.10 you can drag and drop a tarball with a downloaded theme onto the _style_ or _icon_ list. Xfce will attempt to extract and install the files into the <tt>~/.themes</tt> or <tt>~/.icons</tt> directory.

## Desktop Manager  (xfdesktop)

Although the initial plan for Xfce 4.10 was to integrate desktop handling in Thunar, we have decided not to do it at this time yet. Meanwhile, Xfdesktop has gained support for single-click operation, automated background image cycling and thumbnail rendering.

{{< figure src="xfdesktop.png" caption="Desktop with image thumbnails and support for single-click operation" >}}

Xfdesktop is now shipped with a new default background image.

## Window Manager (xfwm4)

Xfwm4 can now tile a window when you drag it to the edge of the screen. This feature is optional and is disabled by default. In such a case windows can still be tiled using a keyboard shortcut. Another improvement is a better theming support and cursor key navigation in the tab window (Alt+Tab).

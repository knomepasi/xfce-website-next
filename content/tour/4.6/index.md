---
title:     "Xfce 4.6 tour"
version:   "4.16"
---

The long awaited 4.6.0 version of the Xfce Desktop Environment is finally available. We will try to highlight some of the new features which have been added since the last stable release.

## Desktop Manager (xfdesktop)

Since desktop icons have been introduced in Xfce 4.4, people have expressed the need to allow the selection of multiple icons (rubber banding). With **Xfce 4.6**, the **Xfdesktop** manager finally implements this feature: you can select multiple icons, remove them, etcetera...

{{< figure src="xfdesktop-rubberbanding.png" caption="Multiple icons selection" >}}

**Xfce 4.6** features a brand new desktop menu which allows you to manipulate files as with the **Thunar** filemanager contextual menu, but also to open applications, exit your session, or access the help documentation.

{{< figure src="xfdesktop-menu.png" caption="New desktop menu" >}}

## Panel (xfce4-panel)

A lot of long standing bugs have been fixed in **Xfce4 Panel**, particularly for multiple screen setups, but this new release also brings an improved set of panel plugins.

{{< figure src="xfce4-panel-clock.png" caption="New binary clock" >}}

The **clock plugin** has been rewritten to consume fewer system resources and to fix some display bugs, but there is also a new clock mode for the geek in you: binary clock! The new **notification area plugin** allows you to hide selected notification icons to keep your notification area clean and readable.

## Sound Mixer (xfce4-mixer)

**Xfce4 Mixer** has been rewritten from scratch to use <a href="https://gstreamer.freedesktop.org/">Gstreamer</a>. This allows us to more easily support multiple sound systems, the user interface is more polished, and you can manage several different sound cards. Additionally, a panel plugin allows you to set the system sound quickly using the mouse scroll wheel.

{{< figure src="xfce4-mixer.png" caption="New sound mixer" >}}

## Session Manager (xfce4-session)

**Xfce 4.6** comes with an enhanced session manager: your session should be started faster, and the settings dialog has been reworked to ease the management of session-aware applications.  Additionally, the session manager will now automatically restart session applications which crashed so that you are not left without a desktop, panel, window manager, etcetera, if a crash occurs.

{{< figure src="xfce4-session-settings.png" caption="Session settings dialog" >}}

The session manager also includes a new long-awaited feature: support for **suspend** and **hibernate** "out of the box."  The logout dialog now has two additional buttons which offer to suspend or hibernate your computer.

{{< figure src="xfce4-session-logout.png" caption="Session logout dialog" >}}

## Window Manager (xfwm4)

As usual, **Xfwm4** has matured quite a bit during this release cycle: many bugs have been fixed, support for multiple displays has been added, and overall performance has been improved.

In addition to some other new features, **Xfwm4** is now able to detect windows that do not respond and offer to terminate them.

{{< figure src="xfwm4-net-ping.png" caption="Dialog to terminate busy applications" >}}

There is also a new **actions menu** which allows you to quickly move and resize windows, put them above or below other windows, or fullscreen them.

{{< figure src="xfwm4-new-menu.png" caption="New actions menu" >}}

A new **fill** operation has been implemented; it expands a given window to the available space without overlapping other adjacent windows.

{{< figure src="xfwm4-fill-operation.png" caption="Fill operation" >}}

The **compositor** has been optimized to reduce window flickering duringresize operations.

{{< figure src="xfwm4-resize.png" caption="Flicker free resizing" >}}

Some **tweakable options** have also been added: for example, you can now disable the blinking of windows when they receive an urgency hint.

{{< figure src="xfwm4-new-tweaks.png" caption="New tweakable options" >}}

## File Manager (thunar)

There have been many bug fixes and performance improvements in **Thunar**. It can use the mouse forward and backward buttons (if available) to navigate, and it includes a new plugin that allows you to set an image as wallpaper from the context menu.

{{< figure src="thunar-wallpaper-plugin.png" caption="Set an image in a Thunar folder as wallpaper" >}}

**Thunar** now follows the <a href="https://freedesktop.org/wiki/Software/xdg-user-dirs"> XDG user directories</a> specification; this allows you to have themed and localized user folders to store your music, documents, videos, templates, etcetera...

{{< figure src="thunar-xdg-user-dirs.png" caption="Thunar menu for user directories" >}}

**Thunar** will now display a translucent icon for drives or volumes that are not mounted, so that you can distinguish them from the mounted ones.

{{< figure src="thunar-mounting.png" caption="Translucent icons for unmounted drives and volumes" >}}

Last, but not least, **Thunar** now supports encrypted devices!

{{< figure src="thunar-encrypted.png" caption="Thunar support for encrypted devices" >}}

## Settings (xfce4-settings)

Xfce 4.6 features a new settings interface, **Xfce Settings Manager**, which allows you to configure your desktop environment much more easily than before. The dialogs which are accessible by single clicking on the icons have been designed to be more compact and to allow you to customize your desktop quickly and in a more intuitive way.

{{< figure src="xfce4-settings-manager.png" caption="Xfce4 Settings Manager" >}}

### Accessibility settings

{{< figure src="xfce4-accessibility-settings.png" caption="Accessibility settings dialog" >}}

The **Accessibility settings** dialog allows you to set the accessibility related mouse and keyboard options, such as sticky keys, bounce keys, or mouse emulation.

### Appearance settings

{{< figure src="xfce4-appearance-settings.png" caption="Appearance settings dialog" >}}

The **Appearance settings** dialog allows you to set the widget style, the icon theme, and font, toolbar and menu options.

### Display settings

{{< figure src="xfce4-display-settings.png" caption="Display settings dialog" >}}

The **Display settings** dialog allows you to set the resolution, refresh rate, and the rotation for each screen that is connected.

### Keyboard settings

{{< figure src="xfce4-keyboard-settings-layout.png" caption="Keyboard settings dialog, layout tab" >}}

The **Keyboard settings** dialog allows you to set keyboard preferences such as key repeating, keyboard shortcuts, and your keyboard layout.

{{< figure src="xfce4-keyboard-settings-shortcuts.png" caption="Keyboard settings dialog, shortcuts tab" >}}

You can now configure shortcuts more simply, and any shortcut conflicts are automatically detected.

### Mouse settings

{{< figure src="xfce4-mouse-settings.png" caption="Mouse settings dialog" >}}

The **Mouse settings** dialog allows you to configure the different mice connected to your computer: button order, acceleration, double-click speed, mouse cursor theme, etcetera...

### Desktop settings

{{< figure src="xfdesktop-settings.png" caption="Desktop settings dialog" >}}

The **Desktop settings** dialog is now much more compact; it allows you to configure per-screen settings: wallpaper, brightness, desktop menu, displayed icons, etcetera...

## Application Finder (xfce4-appfinder)

**Xfce 4.6** also comes with a brand new application finder which features a cleaner user interface.  It is also easier to use it with the keyboard, and it monitors installed applications to update the list "on the fly."  It also allows you to create panel launchers quickly by dragging an application icon to the launcher creation window.

{{< figure src="xfce4-appfinder.png" caption="New application finder" >}}

## Links

* [Xfce website](https://xfce.org/)
* [Thunar website](https://xfce.org/projects/thunar)

## Credits

* Written by Jérôme Guelfucci (February 2009)
* Screenshots by Jannis Pohlmann

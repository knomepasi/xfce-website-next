---
title:     "Xfce 4.12 tour"
version:   "4.12"
---

This tour will introduce you to new major features of Xfce 4.12. It only covers improvements made on the surface; for the full list of changes, see the {{< changelog version="4.12" >}}.

## Window Manager (xfwm4)

### Window Switcher Dialog

The window manager's Alt+Tab dialog is now fully themeable and also gained two new modes: a 'List' mode and a 'Window Preview' mode. Furthermore users use their mouse to click/select the window they want to give focus to.

{{< figure src="tabwin-simple-crop.png" caption="The traditional dialog is fully themable now" >}}

The List mode of the Alt-Tab dialog.

{{< figure src="tabwin-list-crop.png" caption="List mode of Alt-Tab, showing all window titles" >}}

The Window Preview mode shows thumbnails of windows' content alongside their icon. Activating the compositor is a prerequisite for this mode.

{{< figure src="tabwin-preview-crop.png" caption="Window thumbnails" >}}

### Tiling, Zooming, Client-side Decorations

Support for Client-Side Decorations (CSDs) has been improved. They now properly snap to screen and panel borders, and tile correctly, even with shadows.

{{< figure src="xfwm4-csd.png" caption="Gtk3 apps with their decorations drawn by the client" >}}

Window tiling mode was improved by providing support for corner-tiling, and a new zooming mode was added using Alt + Mouse Wheel.

{{< figure src="xfwm4-tiling-small.png" caption="Drag and drop a window to a corner to tile it" >}}

### HiDPI Support

In order to better support modern hi-resolution screens, two new Xfwm4 themes were added (hdpi, xhdpi).

## Panel (xfce4-panel)

### Intelligent Hiding

The panel can now intelligently hide itself when a window is dragged near it.

{{< figure src="panel-shown.png" caption="Oh what is this window??" >}}

{{< figure src="panel-shown-stack.png" caption="Don't come closer!" >}}

{{< figure src="panel-hidden.png" caption="Hah! Now you don't see me!" >}}

### Gtk3 plugins

Infrastructure was added to be able to load Gtk3 plugins alongside Gtk2 plugins.

## Desktop Manager (xfdesktop)

The desktop has a new wallpaper settings dialog with many new options and better multi-monitor support. Drag the dialog to the display or workspace where you want to change the wallpaper.

{{< figure src="xfdesktop-properties-multiworkspace.png" caption="Better multi-monitor support" >}}

Uncheck 'apply to all workspaces' to set a different wallpaper for each workspace.

## Settings (xfce4-settings)

### Display Settings

Support for multi-monitor use was vastly improved in the display settings dialog. Upon connecting a new display, a quick setup popup offers some of the most-used modes for users to quickly change their layout.

{{< figure src="xfce4-display-settings-twoscreens.png" caption="Configure multiple displays" >}}
{{< figure src="xfce4-display-layout.png" caption="Choose your layout when plugging in a new display" >}}

### Appearance Settings

The appearance dialog now showcases previews for styles and icons.

{{< figure src="xfce4-appearance-settings-style.png" caption="Gtk style preview" >}}

{{< figure src="xfce4-appearance-settings-icons.png" caption="Icon theme preview" >}}

## Power Manager (xfce4-power-manager)

### Panel Plugin

A new panel plugin was created which allows you to quickly control your screen brightness, either via the menu or by simply using your mouse's scroll wheel over the plugin. The plugin's menu also shows all other connected devices with a power status, e.g. bluetooth keyboards or wireless mice. It still offers quick access to the presentation mode, which inhibits your screensaver for as long as the option is active.

{{< figure src="xfpm-plugin-crop.png" caption="The plugin's menu allows users to control screen brightness and check on the remaining uptime their battery provides." >}}

### Settings Dialog

The settings dialog was completely restructured (separating button/lid events from system and display behavior) and offers a clearer way of setting your preferences.

{{< figure src="xfpm-prefs-general.png" caption="Configure what action to take when certain buttons are pressed or the laptop lid is closed" >}}
{{< figure src="xfpm-prefs-system.png" caption="Configure what to do when the user is inactive or battery is drained" >}}
{{< figure src="xfpm-prefs-display.png" caption="Manage display power management" >}}
{{< figure src="xfpm-prefs-devices.png" caption="Display information on all connected devices" >}}

When light-locker is available, you can control its settings directly via the power manager.

{{< figure src="xfpm-prefs-security.png" caption="Setup light-locker integration" >}}

## File Manager (thunar)

### Tab Support

A long-awaited feature was added: you can now open multiple folders in the same Thunar window.

{{< figure src="thunar-tabs.png" caption="Browse multiple directories" >}}

Thunar now displays the remaining free space with a bar in a folder properties.

{{< figure src="thunar-freespace.png" caption="Freespace bar" >}}

And you can select multiple files to see their properties at once.

{{< figure src="thunar-multifiles-props.png" caption="Multiple File Properties" >}}

## Goodies

There have been lots of improvements to our goodies, and some new and shiny applications have been added by new contributors.

### Alternative panel menu plugin (xfce4-whiskermenu)

The whisker menu is an alternative to the traditional menu plugin, showing favourites, allowing to search through existing apps and much more.

{{< figure src="whiskermenu-default.png" caption="Browse through categories" >}}

{{< figure src="whiskermenu-search.png" caption="Search for an application" >}}

### Task Manager (xfce4-taskmanager)

The task manager got a revamped user interface, a filter and also supports Gtk3 now.

{{< figure src="taskman-tree.png" caption="Show processes as a tree" >}}

{{< figure src="taskman-filter.png" caption="Filter processes by name" >}}

### Media Player (parole)

Parole's UI was totally redone in Gtk3. It now supports multiple video backends, makes more efficient use of your resources and contains a few novel plugins.

{{< figure src="parole.png" caption="Watch videos" >}}

The media controls are now contained in a slide-over overlay (with a configurable timeout).

{{< figure src="parole-audio.png" caption="Listen to music" >}}

### Text Editor (mousepad)

Mousepad was totally rewritten, gained a settings dialog and now supports Gtk3.

{{< figure src="mousepad-prefs.png" caption="New mousepad settings" >}}

## A note on Xfce's portability

All but one of those screenshots were taken on machines running OpenBSD -current, a good proof that Xfce is still portable and friendly to all Unix systems.

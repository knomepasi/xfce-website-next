---
title:     "Xfce 4.4. tour"
version:   "4.4"
---

As of today, the long awaited version 4.4.0 of the Xfce Desktop Environment is finally available. I will try to highlight some of the new features which have been added since the last stable release.

## Desktop Icons

One of the most often requested features during the 4.0 and 4.2 was support for icons on the desktop. Now, with Xfce 4.4.0, this feature was finally added to the desktop manager **Xfdesktop**.

{{< figure src="desktop-icons.png" caption="Desktop Icons" >}}

The desktop manager utilizes **Thunar**'s libraries to handle application launchers and regular files/folders on the desktop. The desktop manager is also able to display icons for minimized windows on the desktop, which is quite a popular feature from the CDE world. Of course, you can disable the desktop icons altogether if you prefer a clean desktop.

{{< figure src="desktop-settings.png" caption="Desktop Settings" >}}

**Xfdesktop** also continues to provide access to the applications menu, as it did in the previous Xfce releases.

## File Manager

The desktop icon support goes hand in hand with the new file manager <a href="http://thunar.xfce.org/">Thunar</a> which replaces the previous file manager **Xffm**.

{{< figure src="thunar.png" caption="Thunar File Manager" >}}

**Thunar** was written from scratch to provide an easy to use, but still very lightweight file manager for Xfce. Its user interface was designed to look similar to the file chooser which was introduced with GTK+ 2.4, and other file managers such as **Nautilus** and **pcmanfm** already picked up that idea as well.

**Thunar** supports all the file management functionality which users will expect, and also several advanced features. For example, a so-called <i>Bulk Renamer</i> is included which allows users to rename multiple files at once using a certain criterion.

{{< figure src="thunar-bulk-rename.png" caption="Thunar Bulk Rename" >}}

## Removable Drives and Media

Xfce 4.4.0 provides easy access to data on removable drives and media. Just insert the media into the drive or plug the new drive in to the computer and an icon representing the removable volume will appear on the desktop and in **Thunar**'s side pane.

{{< figure src="removable-volumes.png" caption="Removable Volumes" >}}

Click on the icon to automatically mount the volume. Right-click the icon to unmount the drive or eject the media from the drive. Note however that this feature requires <a href="https://freedesktop.org/wiki/Software_2fhal">HAL</a> and is therefore only available for Linux 2.6.x and FreeBSD 6.x and above at the time of this writing (there is limited removable media support for FreeBSD 4.x and 5.x which does not require HAL).

## Text Editor

The new text editor **MousePad** is included with this release. **MousePad** provides all the basic editor functionality, nothing more, nothing less.

{{< figure src="mousepad.png" caption="MousePad" >}}

You can think of **MousePad** as the equivalent to **NotePad** on Windows. It starts up very fast, usually in less than one second, even on older systems.

## Window Manager

**Xfwm4** continues to be the window manager of the hearts.

{{< figure src="xfwm4-argb32.png" caption="Xfwm4 ARGB32" >}}

This release features an enhanced compositor, supporting transparent ARGB windows, shadows, window frame transparency and much more.

{{< figure src="xfwm4-switcher.png" caption="Xfwm4 Switcher" >}}

**Xfwm4** also includes a brand new application switcher, as shown in the screenshot above, which displays all windows from the current workspace with icons and window titles.

{{< figure src="xfwm4-themes.png" caption="Xfwm4 Themes" >}}

Further on support for multiple image formats for window decoration themes was added, including <tt>PNG</tt>, <tt>GIF</tt> and <tt>SVG</tt> images.

{{< figure src="xfwm4-tweaks.png" caption="Xfwm4 Tweaks" >}}

Advanced controls for the window manager were also added, allowing thorough tweaking of window behavior.

## Panel

The **Xfce4-panel** was completely rewritten for the Xfce 4.4 release. Multiple panels are supported <i>out of the box</i> now and can easily be configured using the new **Panel Manager** shown in the screenshot below.

{{< figure src="panel-manager.png" caption="Panel Manager" >}}

One of the major problems in previous Xfce releases was that every plugin had to be run in the same process as the panel, and hence every plugin was able to crash the whole panel. To address this issue, support for external plugins was added to the panel.

{{< figure src="panel-additem.png" caption="Panel Add Item Dialog" >}}

Developers of panel plugins can now decide whether the plugin should run as external process or as part of the panel process, depending on the stability of the plugin.

{{< figure src="panel-iconbox.png" caption="Panel Icon Box Plugin" >}}

Since there is now support for multiple panels, the separate **Xftaskbar4** and **Xfce4-iconbox** utilities are no longer required. Instead, both the taskbar and the iconbox are available as panel plugins now.

Most of the additional panel plugins, available via the <a href="https://goodies.xfce.org/">Xfce Goodies Project</a>, have been updated for the new panel, and several new plugins were added. For example, the brand new **xfce4-xfapplet-plugin** allows users to add GNOME panel applets to the Xfce panel.

## Time Management

The new time management application **Orage** replaces the **Xfcalendar**, which was introduced with Xfce 4.2.0. **Orage** provides several features to efficiently manage your time.

{{< figure src="orage.png" caption="Orage" >}}

While **Orage** is very lightweight and easy to use, it supports all the important features found in larger calendar applications like **Outlook** or **Evolution**. While **Xfcalendar** used the custom <tt>dbh</tt> format in the past to store your settings, **Orage** is based on <tt>ical</tt> and therefore compatible with other calendar applications.

## Terminal Emulator

While **Terminal** was already available during the 4.2 days, it was not mature enough at that time to be part of the core. With this major release, it was moved into the core desktop.

{{< figure src="terminal.png" caption="Terminal" >}}

Besides the basic features which you might expect from a terminal emulator, it includes some nice additional features, like multiple tabs per window, customizable toolbars and the ability to configure nearly every aspect of the application via <i>hidden options</i>. As can be seen in the screenshot above, this release also supports real transparency using **Xfwm4**'s integrated composition manager.

## Printing

**Xfprint**, the Xfce printing management application, saw several small improvements with this release. First, the <tt>a2ps</tt> converter is not mandatory anymore, whilst still recommended. Support for <tt>CUPS</tt> 1.2 was added and **Xfprint** is now able to display the printer state with the <tt>CUPS</tt>-backend.

{{< figure src="xfprint.png" caption="Xfce Printing" >}}

**Xfprint** also integrates with **MousePad** to provide generic printing support for different kinds of text documents using the <tt>a2ps</tt> converter.

{{< figure src="xfprint-dialog.png" caption="Xfce Print Dialog" >}}

As you can see the print dialog still looks relatively similar to that of Xfce 4.2, but the internal workings of the printing support were improved, especially the <tt>CUPS</tt> support. Besides that, the printing management functionality was moved to a library, so other applications can use the API to access the printer configuration.

## Autostart

Xfce 4.4.0 implements the new <a href="https://freedesktop.org/wiki/Standards_2fautostart_2dspec">Autostart Specification</a> - actually Xfce was the first desktop to implement said feature, but the others were faster to release. ;-)

{{< figure src="autostart.png" caption="Xfce Autostart Editor" >}}

The specification consists of two parts, the <i>Autostart of Applications During Startup</i>, which is implemented in **xfce4-session** and the <i>Autostart Of Applications After Mount</i> which is implemented in <a href="http://foo-projects.org/~benny/projects/thunar-volman/index.html">thunar-volman</a>. This release also includes the **xfce4-autostart-editor**, shown in the screenshot above, which allows users to easily add, remove or disable autostarted applications.

## Settings

This release introduces new options to customize the desktop to your needs. Some examples of new settings dialogs were already shown in the sections above.

{{< figure src="preferences-applications.png" caption="Preferred Applications" >}}

The preferred applications framework, which was previously only available in **Terminal**, was imported into Xfce, so users no longer need to edit shell profiles to specify which browser and terminal emulator should be used by Xfce applications. The goal was to make it as easy as possible to change an application for a certain category (GNOME users may have already noticed that GNOME adopted this approach, because it is such simple).

{{< figure src="preferences-keyboard.png" caption="Keyboard Shortcuts" >}}

And then there was the problem with the keyboard shortcuts in Xfce 4.2... Xfce 4.2 limited the number of freely available keyboard shortcuts, while people wanted to assign any number of keyboard shortcuts. With Xfce 4.4 this limitation is history and the application shortcuts are now separated from the window manager shortcuts.

## Feedback

Please post comments on this article in my <a href="http://xfce-diary.blogspot.com/2007/01/visual-tour-of-xfce-440.html">blog</a> and use the <a href="/community/lists">xfce</a> mailinglist if you have questions about Xfce 4.4.0 or trouble with the installation.

## Links

* [Xfce website](https://xfce.org/)
* [Thunar website](http://thunar.xfce.org/)

## Credits

Written by Benedikt Meurer, 21 Jan 2007

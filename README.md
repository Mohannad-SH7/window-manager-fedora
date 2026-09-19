# Fedora Desktop Settings

This repository contains my personal Fedora desktop configuration files.

The purpose of this repository is to keep my desktop settings backed up and make it easy to restore them after reinstalling Fedora or moving to another Fedora system.

## 📁 Contents

```text
window-manager-fedora/
├── kitty/
│   ├── kitty.conf
│   ├── theme.conf
│   ├── current-theme.conf
│   └── dark-theme.auto.conf
│
└── tiling-shell/
    └── settings.dconf
```

### Kitty

The `kitty/` directory contains my Kitty terminal configuration and theme files.

Location on Fedora:

```text
~/.config/kitty/
```

### Tiling Shell

The `tiling-shell/settings.dconf` file contains my Tiling Shell settings, including:

* Keyboard shortcuts
* Window movement shortcuts
* Window focus shortcuts
* Gaps
* Window borders
* Tiling layouts
* Snap settings
* Other Tiling Shell preferences

The settings are stored using **dconf**.

Don't forget to create these shortcuts from the settings: 😃
- Alt+Q --> Quit Window 
- Alt+Enter --> Open Kitty

---

# 🔄 Restore Settings

## Kitty

Create the Kitty configuration directory if it doesn't exist:

```bash
mkdir -p ~/.config/kitty
```

Then copy the saved configuration:

```bash
cp ./kitty/*.conf ~/.config/kitty/
```

## Tiling Shell

Restore the saved Tiling Shell settings:

```bash
dconf load /org/gnome/shell/extensions/tilingshell/ \
< ./tiling-shell/settings.dconf
```

You may need to restart GNOME Shell or log out and log back in for some changes to appear.

* Or you can import the setting.dconf in the gnome extensions - tiling shell 😃 
---

# 🚀 Quick Setup After Fedora Reinstall

Clone the repository:

```bash
git clone <YOUR-REPOSITORY-URL>
cd window-manager-fedora
```

Restore Kitty:

```bash
mkdir -p ~/.config/kitty
cp ./kitty/*.conf ~/.config/kitty/
```

Restore Tiling Shell:

```bash
dconf load /org/gnome/shell/extensions/tilingshell/ \
< ./tiling-shell/settings.dconf
```

That's it.

---

## ⚠️ Notes

* These files contain my personal desktop preferences.
* The Tiling Shell settings require the **Tiling Shell GNOME extension** to be installed.
* Kitty must be installed before restoring its configuration.
* Do not store passwords, API keys, tokens, or other sensitive information in this repository.
* The configuration paths may be different on other Linux distributions or desktop environments.

## 🛠️ Current Setup

* Fedora Linux
* GNOME
* Kitty
* Tiling Shell

---

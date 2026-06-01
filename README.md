# User Configuration Manager

## Overview

The User Configuration Manager is a simple Python application that allows users to manage configuration settings such as theme, language, notifications, and other preferences.

The project provides functions to:

* Add new settings
* Update existing settings
* Delete settings
* View all current settings

All setting names and values are automatically converted to lowercase to maintain consistency.

---

## Features

### Add a Setting

Adds a new key-value pair to the settings dictionary.

* Converts the key and value to lowercase.
* Prevents duplicate settings from being added.

Example:

```python
add_setting(settings, ("Theme", "Dark"))
```

---

### Update a Setting

Updates the value of an existing setting.

* Converts the key and value to lowercase.
* Returns an error if the setting does not exist.

Example:

```python
update_setting(settings, ("theme", "light"))
```

---

### Delete a Setting

Removes a setting from the dictionary.

* Converts the key to lowercase.
* Returns an error message if the setting cannot be found.

Example:

```python
delete_setting(settings, "theme")
```

---

### View Settings

Displays all current settings in a readable format.

Example output:

```
Current User Settings:
Theme: dark
Language: english
Notifications: enabled
```

If no settings exist:

```
No settings available.
```

---

## Example

```python
test_settings = {
    "theme": "dark",
    "language": "english",
    "notifications": "enabled"
}

print(view_settings(test_settings))
```

Output:

```
Current User Settings:
Theme: dark
Language: english
Notifications: enabled
```

---

## Functions

### add_setting(settings, pair)

Adds a new setting if the key does not already exist.

### update_setting(settings, pair)

Updates an existing setting.

### delete_setting(settings, key)

Deletes a setting by key.

### view_settings(settings)

Returns a formatted string containing all settings.

---

## Requirements

* Python 3.x

---

## License

This project is intended for educational and learning purposes.

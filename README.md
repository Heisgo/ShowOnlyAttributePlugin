# ShowOnlyAttributePlugin

# ShowOnly Plugin
The ShowOnly Plugin is a simple Unity Editor extension that allows you to display serialized field values in the Inspector as read-only labels. This is particularly useful when you want to display internal state or debug values without allowing modifications at runtime.

# Overview
This plugin uses a custom property drawer in Unity to render fields marked with the ShowOnlyAttribute as non-editable labels. It supports a variety of serialized property types including:

Boolean
String
Integer
Float (formatted to four decimal places)
Vector2
Vector3
Color
Enum
For any unsupported types, the plugin will display "Not Supported Type." instead.

# Features
Read-Only Display: Marks properties as read-only in the Inspector.
Type-Specific Formatting: Converts property values to strings with appropriate formatting.
Easy Integration: Simply apply the ShowOnlyAttribute to any serialized field.

# How It Works
The plugin defines a custom property drawer for the ShowOnlyAttribute.
It uses a dictionary to map various SerializedPropertyType values to corresponding conversion functions.
During the Inspector rendering, the property drawer retrieves the property value, converts it to a string, and displays it using EditorGUI.LabelField.

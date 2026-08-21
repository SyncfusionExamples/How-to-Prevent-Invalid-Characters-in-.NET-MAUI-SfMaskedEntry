# How-to-Prevent-Invalid-Characters-in-.NET-MAUI-SfMaskedEntry

## Overview

The Syncfusion .NET MAUI **SfMaskedEntry** control enables developers to restrict user input by applying predefined masks. This feature is particularly useful when applications require data to follow a specific format or character type. By preventing invalid characters from being entered, developers can improve data quality, reduce validation errors, and provide a more intuitive user experience.

In many business applications, users are expected to enter alphabetic-only values such as names, department codes, country abbreviations, or employee initials. Allowing users to enter numbers or special characters in these fields can lead to inconsistent data and additional validation requirements. The SfMaskedEntry control simplifies this process by enforcing character restrictions directly during input.

In this example, the SfMaskedEntry control uses an alphabetic mask to ensure that users can enter only letters. Any numeric values or unsupported characters are automatically rejected by the control. This helps maintain consistent and validated user input without requiring additional custom validation logic.

The control also includes a placeholder to guide users by indicating the type of information expected. As users type, the mask actively filters input and prevents invalid characters from being entered into the field.

## XAML

```xml
<inputs:SfMaskedEntry HorizontalOptions="Start"
                      WidthRequest="250"
                      Mask="AAAAAA"
                      Placeholder="Enter name" />
```

## Understanding the Properties

### Mask

The `Mask` property defines the permitted input format.

```xml
Mask="AAAAAA"
```

In this example, each `A` placeholder accepts only alphabetic characters. Since the mask contains six `A` characters, users can enter up to six letters.

Example valid inputs:

```text
Johns
Martin
Robert
```

Example invalid inputs:

```text
John12
A123BC
Name@1
```

The control automatically prevents characters that do not match the mask definition.

### Placeholder

The `Placeholder` property displays instructional text when the control is empty.

```xml
Placeholder="Enter name"
```

This text helps users understand the expected input before they begin typing.

### WidthRequest

The `WidthRequest` property specifies the preferred width of the control.

```xml
WidthRequest="250"
```

This allows the control to maintain a consistent appearance across different screen sizes and layouts.

### HorizontalOptions

The `HorizontalOptions` property controls the horizontal alignment of the SfMaskedEntry.

```xml
HorizontalOptions="Start"
```

Setting this property to `Start` aligns the control to the beginning of the available horizontal space within its parent container.

## How Invalid Characters Are Prevented

When a user attempts to enter data into the SfMaskedEntry control:

- Only alphabetic characters are accepted.
- Numeric characters are rejected.
- Special characters are rejected.
- Input automatically follows the defined mask.
- Invalid values are prevented before they can be entered.
- The need for manual validation is reduced.

Because the validation occurs during data entry, users immediately understand what type of input is allowed.

## Output

When the application runs:

- The control displays the placeholder text **"Enter name"**.
- Users can enter only alphabetic characters.
- Numbers and special characters are prevented.
- Input follows the six-character alphabetic mask.
- Data entered into the control remains consistent and properly formatted.

## Benefits of Restricting Invalid Characters

Using an alphabetic mask provides several advantages:

- Improves data accuracy.
- Eliminates unwanted characters.
- Reduces validation errors.
- Enhances user experience.
- Simplifies form processing.
- Maintains consistent data formatting.
- Minimizes backend validation requirements.
- Prevents accidental data entry mistakes.

## Use Cases

Preventing invalid characters is useful in many scenarios, including:

- Name entry forms.
- Employee code inputs.
- Country code fields.
- Registration forms.
- Customer information screens.
- Healthcare applications.
- Educational management systems.
- Human resource portals.
- Membership registration forms.

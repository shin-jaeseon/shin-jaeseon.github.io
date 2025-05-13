---
layout: page
title: Getting Started
permalink: /docs/getting-started/
---

# Getting Started with XamlDS.ITK

This guide explains how to start development using XamlDS.ITK.

## Prerequisites

- Visual Studio 2022 or later
- .NET 6.0 or later
- Depending on your chosen XAML framework:
  - WPF: Windows OS
  - WinUI3: Windows 10 version 1809 or later
  - AvaloniaUI: All supported platforms (Windows, macOS, Linux)

## Installation

### Via NuGet Package Manager UI

1. Right-click on your project in Solution Explorer
2. Select "Manage NuGet Packages..."
3. Search for "XamlDS.ITK"
4. Install the following packages:
   - XamlDS.ITK.Core (required)
   - XamlDS.ITK.WPF (for WPF projects)
   - XamlDS.ITK.WinUI3 (for WinUI3 projects)
   - XamlDS.ITK.AvaloniaUI (for AvaloniaUI projects)

### Via Package Manager Console

```
Install-Package XamlDS.ITK.Core
# Then, based on your platform:
Install-Package XamlDS.ITK.WPF
# or
Install-Package XamlDS.ITK.WinUI3
# or
Install-Package XamlDS.ITK.AvaloniaUI
```

## Project Setup

### WPF Project

Add the following to your App.xaml:

```xml
<Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <ResourceDictionary Source="pack://application:,,,/XamlDS.ITK.WPF;component/Themes/XDSTheme.xaml" />
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
</Application.Resources>
```

Add namespaces to your XAML files:

```xml
xmlns:xamlds="clr-namespace:XamlDS.ITK.Controls;assembly=XamlDS.ITK.WPF"
```

### WinUI3 Project

Add the following to your App.xaml:

```xml
<Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <ResourceDictionary Source="ms-appx:///XamlDS.ITK.WinUI3/Themes/XDSTheme.xaml" />
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
</Application.Resources>
```

Add namespaces to your XAML files:

```xml
xmlns:xamlds="using:XamlDS.ITK.Controls"
```

### AvaloniaUI Project

Add the following to your App.axaml:

```xml
<Application.Styles>
    <StyleInclude Source="avares://XamlDS.ITK.AvaloniaUI/Themes/XDSTheme.axaml" />
</Application.Styles>
```

Add namespaces to your XAML files:

```xml
xmlns:xamlds="clr-namespace:XamlDS.ITK.Controls;assembly=XamlDS.ITK.AvaloniaUI"
```

## Basic Usage

Here's a simple example using XamlDS.ITK controls:

```xml
<xamlds:XDSPanel>
    <xamlds:XDSCard Padding="16">
        <xamlds:XDSStackPanel Spacing="8">
            <xamlds:XDSTextBlock Text="Hello, XamlDS.ITK!" FontSize="20" />
            <xamlds:XDSButton Content="Click Me" Click="OnButtonClick" />
        </xamlds:XDSStackPanel>
    </xamlds:XDSCard>
</xamlds:XDSPanel>
```

## Next Steps

Now that you have XamlDS.ITK set up in your project, explore the following resources:

- [Components Documentation](/docs/components/) - Learn about available UI components
- [Theme System](/docs/themes/) - Customize the look and feel of your application
- [Sample Projects](https://github.com/xamldesignstudio/XamlDS.ITK.Samples) - See XamlDS.ITK in action

---
layout: post
title: "Introduction to XamlDS.ITK Project"
date: 2025-05-13
categories: project
tags: xamlds itk wpf winui3 avalonia
---

# Introduction to XamlDS.ITK Project

[Enter content: Introduction to the XamlDS.ITK project]

## Project Background

[Enter content: Background and motivation for starting the project]

## Key Features

### 1. Cross-Platform Support

[Enter content: Description of how various platforms like WPF, WinUI3, AvaloniaUI are supported]

### 2. Unified Component Architecture

[Enter content: Description of the unified component architecture]

### 3. Modern Design System

[Enter content: Description of the modern design system]

## Getting Started

To start using XamlDS.ITK, you can install it via NuGet:

```csharp
// Install via Package Manager
Install-Package XamlDS.ITK.Core
Install-Package XamlDS.ITK.WPF // For WPF projects
Install-Package XamlDS.ITK.WinUI3 // For WinUI3 projects
Install-Package XamlDS.ITK.AvaloniaUI // For AvaloniaUI projects
```

## Code Example

Here's a simple example of using a XamlDS control in XAML:

```xml
<Window 
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:xamlds="clr-namespace:XamlDS.ITK.Controls;assembly=XamlDS.ITK.WPF">
    
    <xamlds:XDSCard Padding="16">
        <xamlds:XDSButton Content="Click Me" />
    </xamlds:XDSCard>
</Window>
```

## Roadmap

[Enter content: Future plans for the project]

We're excited to continue developing XamlDS.ITK and welcome community contributions!

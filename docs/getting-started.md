---
layout: page
title: 시작하기
permalink: /docs/getting-started/
---

# XamlDS.ITK 시작하기

이 가이드는 XamlDS.ITK를 사용하여 개발을 시작하는 방법을 설명합니다.

## 필수 조건

- Visual Studio 2022 이상
- .NET 6.0 이상
- 선택한 XAML 프레임워크에 따라:
  - WPF: Windows OS
  - WinUI3: Windows 10 버전 1809 이상
  - AvaloniaUI: 모든 지원 플랫폼 (Windows, macOS, Linux)

## 설치

### NuGet 패키지 설치하기

Visual Studio의 NuGet 패키지 관리자를 사용하거나 다음 명령어를 입력하세요:

```powershell
# 코어 라이브러리 설치
Install-Package XamlDS.ITK.Core

# 프레임워크별 라이브러리 설치
# WPF의 경우:
Install-Package XamlDS.ITK.WPF
# WinUI3의 경우:
Install-Package XamlDS.ITK.WinUI3
# AvaloniaUI의 경우:
Install-Package XamlDS.ITK.AvaloniaUI
```

## 프로젝트 설정

### WPF 프로젝트

```xml
<!-- App.xaml -->
<Application x:Class="YourNamespace.App"
             xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
             xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
             xmlns:itk="clr-namespace:XamlDS.ITK.WPF;assembly=XamlDS.ITK.WPF">
    <Application.Resources>
        <ResourceDictionary>
            <ResourceDictionary.MergedDictionaries>
                <!-- ITK 스타일 사전 추가 -->
                <itk:ITKResourceDictionary />
            </ResourceDictionary.MergedDictionaries>
        </ResourceDictionary>
    </Application.Resources>
</Application>
```

### WinUI3 프로젝트

[내용 입력: WinUI3 프로젝트 설정 방법]

### AvaloniaUI 프로젝트

[내용 입력: AvaloniaUI 프로젝트 설정 방법]

## 첫 번째 ITK 컴포넌트 사용하기

### 기본 컨트롤 추가

```xml
<!-- MainWindow.xaml (WPF) -->
<Window x:Class="YourNamespace.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:itk="clr-namespace:XamlDS.ITK.WPF.Controls;assembly=XamlDS.ITK.WPF">
    <Grid>
        <itk:ITKButton Content="ITK 버튼" 
                       Margin="10" 
                       HorizontalAlignment="Center" 
                       VerticalAlignment="Center"
                       Click="ITKButton_Click"/>
    </Grid>
</Window>
```

```csharp
// MainWindow.xaml.cs
private void ITKButton_Click(object sender, RoutedEventArgs e)
{
    MessageBox.Show("ITK 버튼이 클릭되었습니다!");
}
```

## 다음 단계

- [컴포넌트 목록](/docs/components/) 살펴보기
- [테마 시스템](/docs/themes/) 알아보기
- [고급 사용법](/docs/advanced/) 학습하기

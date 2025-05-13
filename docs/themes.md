---
layout: page
title: 테마 시스템
permalink: /docs/themes/
---

# XamlDS.ITK 테마 시스템

XamlDS.ITK는 강력한 테마 시스템을 제공하여 애플리케이션의 시각적 모양을 쉽게 사용자 정의할 수 있습니다.

## 테마 기본 개념

XamlDS.ITK 테마 시스템은 다음 주요 개념을 기반으로 합니다:

- **ThemeManager**: 전역 테마 관리를 위한 싱글톤 클래스
- **ThemeResources**: 테마별 리소스 정의
- **ThemeMode**: Light, Dark, System 모드 지원

## 기본 테마

XamlDS.ITK는 다음과 같은 기본 테마를 제공합니다:

- **Standard**: 기본 중립 테마
- **Modern**: 현대적인 디자인 테마
- **Classic**: 전통적인 디자인 테마
- **Minimal**: 미니멀한 디자인 테마

## 테마 적용하기

### 애플리케이션 전체 테마 설정

```csharp
// App.xaml.cs
protected override void OnStartup(StartupEventArgs e)
{
    base.OnStartup(e);
    
    // 앱 전체에 Modern 테마 적용
    ITKThemeManager.Current.SetTheme(ITKThemeType.Modern);
    
    // 다크 모드 설정
    ITKThemeManager.Current.SetThemeMode(ThemeMode.Dark);
}
```

### XAML에서 테마 설정

```xml
<!-- App.xaml -->
<Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <itk:ITKThemeResources ThemeType="Modern" ThemeMode="Dark" />
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
</Application.Resources>
```

### 런타임에 테마 변경

```csharp
// 테마 변경
ITKThemeManager.Current.SetTheme(ITKThemeType.Minimal);

// 테마 모드 변경
ITKThemeManager.Current.SetThemeMode(ThemeMode.Light);

// 시스템 설정에 따라 자동 테마 모드 설정
ITKThemeManager.Current.SetThemeMode(ThemeMode.System);
```

## 사용자 정의 테마 만들기

### 1. 커스텀 테마 리소스 정의

```xml
<!-- CustomTheme.xaml -->
<ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
                    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
                    xmlns:itk="clr-namespace:XamlDS.ITK.Core.Theming;assembly=XamlDS.ITK.Core">

    <!-- 색상 정의 -->
    <Color x:Key="PrimaryColor">#3498db</Color>
    <Color x:Key="SecondaryColor">#2ecc71</Color>
    <Color x:Key="AccentColor">#e74c3c</Color>
    
    <!-- 브러시 정의 -->
    <SolidColorBrush x:Key="PrimaryBrush" Color="{StaticResource PrimaryColor}" />
    <SolidColorBrush x:Key="SecondaryBrush" Color="{StaticResource SecondaryColor}" />
    <SolidColorBrush x:Key="AccentBrush" Color="{StaticResource AccentColor}" />
    
    <!-- 컨트롤 스타일 재정의 -->
    <Style x:Key="CustomButtonStyle" TargetType="itk:ITKButton" BasedOn="{StaticResource {x:Type itk:ITKButton}}">
        <Setter Property="Background" Value="{StaticResource PrimaryBrush}" />
        <Setter Property="Foreground" Value="White" />
        <Setter Property="BorderThickness" Value="0" />
        <Setter Property="CornerRadius" Value="4" />
    </Style>
    
    <!-- 추가 스타일 정의 -->
</ResourceDictionary>
```

### 2. 커스텀 테마 등록

```csharp
// 커스텀 테마 등록
var customTheme = new ITKTheme("Custom");
customTheme.AddResourceDictionary("light", new Uri("/YourApp;component/Themes/CustomThemeLight.xaml", UriKind.Relative));
customTheme.AddResourceDictionary("dark", new Uri("/YourApp;component/Themes/CustomThemeDark.xaml", UriKind.Relative));

ITKThemeManager.Current.RegisterTheme(customTheme);
ITKThemeManager.Current.SetTheme("Custom");
```

## 테마 리소스 키

XamlDS.ITK 테마 시스템에서 사용되는 주요 리소스 키 목록입니다:

### 색상 리소스 키

- **PrimaryColor**: 주요 색상
- **SecondaryColor**: 보조 색상
- **AccentColor**: 강조 색상
- **BackgroundColor**: 배경 색상
- **ForegroundColor**: 전경 색상
- **BorderColor**: 테두리 색상
- **DisabledColor**: 비활성화 색상

### 브러시 리소스 키

- **PrimaryBrush**: 주요 브러시
- **SecondaryBrush**: 보조 브러시
- **AccentBrush**: 강조 브러시
- **BackgroundBrush**: 배경 브러시
- **ForegroundBrush**: 전경 브러시
- **BorderBrush**: 테두리 브러시
- **DisabledBrush**: 비활성화 브러시

### 여백 및 크기 리소스 키

- **DefaultMargin**: 기본 여백
- **SmallMargin**: 작은 여백
- **LargeMargin**: 큰 여백
- **DefaultPadding**: 기본 패딩
- **SmallPadding**: 작은 패딩
- **LargePadding**: 큰 패딩

### 폰트 리소스 키

- **DefaultFontFamily**: 기본 폰트 패밀리
- **HeadingFontFamily**: 제목 폰트 패밀리
- **DefaultFontSize**: 기본 폰트 크기
- **SmallFontSize**: 작은 폰트 크기
- **LargeFontSize**: 큰 폰트 크기
- **HeaderFontSize**: 헤더 폰트 크기

## 테마 전환 애니메이션

[내용 입력: 테마 전환 애니메이션 설명]

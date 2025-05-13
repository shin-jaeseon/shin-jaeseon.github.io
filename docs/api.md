---
layout: page
title: API 문서
permalink: /docs/api/
---

# XamlDS.ITK API 문서

XamlDS.ITK 라이브러리의 API 문서입니다. 각 네임스페이스와 주요 클래스에 대한 정보를 제공합니다.

## 핵심 네임스페이스

### XamlDS.ITK.Core

기본 인터페이스, 추상 클래스 및 유틸리티를 포함하는 핵심 네임스페이스입니다.

- [ITKObject](/docs/api/core/itkobject) - 모든 ITK 객체의 기본 클래스
- [INotifyPropertyChangedEx](/docs/api/core/inotifypropertychangedex) - 확장된 속성 변경 알림 인터페이스
- [ITKEventArgs](/docs/api/core/itkeventargs) - 이벤트 인수 기본 클래스
- [ITKException](/docs/api/core/itkexception) - ITK 예외 클래스

### XamlDS.ITK.Core.MVVM

MVVM 패턴을 지원하는 클래스들을 포함합니다.

- [ViewModelBase](/docs/api/mvvm/viewmodelbase) - 뷰모델 기본 클래스
- [ValidatableViewModel](/docs/api/mvvm/validatableviewmodel) - 검증 기능이 있는 뷰모델
- [RelayCommand](/docs/api/mvvm/relaycommand) - ICommand 구현체

### XamlDS.ITK.Core.DI

의존성 주입 기능을 제공하는 네임스페이스입니다.

- [ITKServiceCollection](/docs/api/di/itkservicecollection) - 서비스 컬렉션
- [ITKServiceProvider](/docs/api/di/itkserviceprovider) - 서비스 공급자
- [IServiceRegistration](/docs/api/di/iserviceregistration) - 서비스 등록 인터페이스

### XamlDS.ITK.Core.Messaging

컴포넌트 간 통신을 위한 메시징 시스템을 제공합니다.

- [ITKMessenger](/docs/api/messaging/itkmessenger) - 메신저 클래스
- [ITKMessage](/docs/api/messaging/itkmessage) - 메시지 기본 클래스

### XamlDS.ITK.Core.Theming

테마 시스템을 지원하는 클래스들을 포함합니다.

- [ITKThemeManager](/docs/api/theming/itkthememanager) - 테마 관리자
- [ITKTheme](/docs/api/theming/itktheme) - 테마 클래스
- [ThemeResourceDictionary](/docs/api/theming/themeresourcedictionary) - 테마 리소스 사전

## 프레임워크별 네임스페이스

### XamlDS.ITK.WPF

WPF 프레임워크를 위한 구현체를 포함합니다.

- [WPF 컨트롤 목록](/docs/api/wpf/controls)
- [WPF 컨버터 목록](/docs/api/wpf/converters)
- [WPF 행동 목록](/docs/api/wpf/behaviors)

### XamlDS.ITK.WinUI3

WinUI3 프레임워크를 위한 구현체를 포함합니다.

- [WinUI3 컨트롤 목록](/docs/api/winui3/controls)
- [WinUI3 컨버터 목록](/docs/api/winui3/converters)
- [WinUI3 행동 목록](/docs/api/winui3/behaviors)

### XamlDS.ITK.AvaloniaUI

AvaloniaUI 프레임워크를 위한 구현체를 포함합니다.

- [AvaloniaUI 컨트롤 목록](/docs/api/avalonia/controls)
- [AvaloniaUI 컨버터 목록](/docs/api/avalonia/converters)
- [AvaloniaUI 행동 목록](/docs/api/avalonia/behaviors)

## 주요 이넘 값

[내용 입력: 주요 열거형 값 설명]

## 예외 목록

[내용 입력: 예외 목록 설명]

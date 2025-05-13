---
layout: page
title: 고급 사용법
permalink: /docs/advanced/
---

# XamlDS.ITK 고급 사용법

XamlDS.ITK의 고급 기능과 활용 방법에 대해 설명합니다.

## MVVM 패턴 지원

XamlDS.ITK는 MVVM(Model-View-ViewModel) 패턴을 완벽하게 지원합니다.

### ViewModelBase 클래스

```csharp
// 기본 ViewModel 구현
public class MainViewModel : ITKViewModelBase
{
    private string _title;
    public string Title
    {
        get => _title;
        set => SetProperty(ref _title, value);
    }
    
    private ICommand _saveCommand;
    public ICommand SaveCommand => _saveCommand ??= new ITKRelayCommand(ExecuteSave, CanExecuteSave);
    
    private bool CanExecuteSave() => !string.IsNullOrEmpty(Title);
    
    private void ExecuteSave()
    {
        // 저장 로직
    }
}
```

### 바인딩 사용

```xml
<itk:ITKTextBox Text="{Binding Title, UpdateSourceTrigger=PropertyChanged}" />
<itk:ITKButton Content="저장" Command="{Binding SaveCommand}" />
```

## 의존성 주입 지원

XamlDS.ITK는 내장된 DI(Dependency Injection) 컨테이너를 제공합니다.

### 서비스 등록

```csharp
// App.xaml.cs
protected override void OnStartup(StartupEventArgs e)
{
    base.OnStartup(e);
    
    var serviceCollection = new ITKServiceCollection();
    
    // 서비스 등록
    serviceCollection.RegisterSingleton<ISettingsService, SettingsService>();
    serviceCollection.RegisterTransient<IDataService, DataService>();
    serviceCollection.RegisterTransient<MainViewModel>();
    
    // 서비스 공급자 빌드
    ITKServiceProvider.Initialize(serviceCollection);
}
```

### 서비스 사용

```csharp
// 생성자 주입
public class MainViewModel : ITKViewModelBase
{
    private readonly ISettingsService _settingsService;
    private readonly IDataService _dataService;
    
    public MainViewModel(ISettingsService settingsService, IDataService dataService)
    {
        _settingsService = settingsService;
        _dataService = dataService;
    }
}

// 서비스 로케이터 패턴
var settingsService = ITKServiceProvider.Current.GetService<ISettingsService>();
```

## 메시징 시스템

XamlDS.ITK는 컴포넌트 간 통신을 위한 메시징 시스템을 제공합니다.

### 메시지 정의

```csharp
// 사용자 정의 메시지
public class UserLoggedInMessage : ITKMessage
{
    public string Username { get; }
    
    public UserLoggedInMessage(string username)
    {
        Username = username;
    }
}
```

### 메시지 구독

```csharp
// 메시지 구독
public class ProfileViewModel : ITKViewModelBase
{
    public ProfileViewModel()
    {
        // 메시지 구독
        ITKMessenger.Default.Subscribe<UserLoggedInMessage>(this, OnUserLoggedIn);
    }
    
    private void OnUserLoggedIn(UserLoggedInMessage message)
    {
        // 메시지 처리
        Username = message.Username;
    }
    
    protected override void Dispose(bool disposing)
    {
        if (disposing)
        {
            // 구독 해제
            ITKMessenger.Default.Unsubscribe<UserLoggedInMessage>(this);
        }
        
        base.Dispose(disposing);
    }
}
```

### 메시지 발행

```csharp
// 메시지 발행
ITKMessenger.Default.Publish(new UserLoggedInMessage("user123"));
```

## 네비게이션 서비스

```csharp
// 네비게이션 서비스 사용
public class MainViewModel : ITKViewModelBase
{
    private readonly INavigationService _navigationService;
    
    public MainViewModel(INavigationService navigationService)
    {
        _navigationService = navigationService;
    }
    
    private ICommand _navigateCommand;
    public ICommand NavigateCommand => _navigateCommand ??= new ITKRelayCommand<string>(ExecuteNavigate);
    
    private void ExecuteNavigate(string pageKey)
    {
        _navigationService.Navigate(pageKey);
    }
}
```

## 데이터 검증

XamlDS.ITK는 속성 검증을 위한 강력한 시스템을 제공합니다.

```csharp
public class RegisterViewModel : ITKValidatableViewModel
{
    private string _email;
    [Required(ErrorMessage = "이메일은 필수 항목입니다.")]
    [EmailAddress(ErrorMessage = "올바른 이메일 형식이 아닙니다.")]
    public string Email
    {
        get => _email;
        set => SetProperty(ref _email, value, true); // true는 검증 활성화
    }
    
    private string _password;
    [Required(ErrorMessage = "비밀번호는 필수 항목입니다.")]
    [MinLength(8, ErrorMessage = "비밀번호는 최소 8자 이상이어야 합니다.")]
    public string Password
    {
        get => _password;
        set => SetProperty(ref _password, value, true);
    }
    
    private ICommand _registerCommand;
    public ICommand RegisterCommand => _registerCommand ??= new ITKRelayCommand(ExecuteRegister, CanExecuteRegister);
    
    private bool CanExecuteRegister() => !HasErrors;
    
    private void ExecuteRegister()
    {
        // 등록 로직
    }
}
```

## 성능 최적화

[내용 입력: 성능 최적화 방법]

## 국제화 및 지역화

[내용 입력: 국제화 및 지역화 지원]

## 단위 테스트

[내용 입력: 단위 테스트 방법]

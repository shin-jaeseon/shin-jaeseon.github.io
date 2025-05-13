---
layout: page
title: 컴포넌트
permalink: /docs/components/
---

# XamlDS.ITK 컴포넌트

XamlDS.ITK는 다양한 UI 컴포넌트를 제공합니다. 여기서는 주요 컴포넌트들의 사용법을 설명합니다.

## 기본 컨트롤

### ITKButton

기본적인 버튼 컴포넌트로, 향상된 시각적 피드백과 애니메이션을 제공합니다.

```xml
<itk:ITKButton Content="클릭하세요" 
               Theme="Primary" 
               Size="Medium" 
               Click="OnButtonClick" />
```

#### 속성

- **Theme**: 버튼의 테마 (Primary, Secondary, Success, Danger, Warning, Info)
- **Size**: 버튼 크기 (Small, Medium, Large)
- **IsRounded**: 둥근 모서리 적용 여부
- **HasShadow**: 그림자 효과 적용 여부

### ITKTextBox

사용자 입력을 위한 향상된 텍스트 박스 컴포넌트입니다.

```xml
<itk:ITKTextBox Placeholder="여기에 입력하세요" 
                IsSpellCheckEnabled="True"
                TextChanged="OnTextChanged" />
```

#### 속성

- **Placeholder**: 입력 전 표시되는 힌트 텍스트
- **IsSpellCheckEnabled**: 맞춤법 검사 활성화 여부
- **ValidationType**: 입력 유효성 검사 유형 (None, Email, Phone, Number, Custom)
- **ValidationRegex**: 사용자 정의 유효성 검사 정규식

## 레이아웃 컴포넌트

### ITKGrid

반응형 그리드 레이아웃 시스템을 제공합니다.

```xml
<itk:ITKGrid Columns="12">
    <itk:ITKGridItem ColumnSpan="6">
        <!-- 절반 너비의 콘텐츠 -->
    </itk:ITKGridItem>
    <itk:ITKGridItem ColumnSpan="3">
        <!-- 1/4 너비의 콘텐츠 -->
    </itk:ITKGridItem>
    <itk:ITKGridItem ColumnSpan="3">
        <!-- 1/4 너비의 콘텐츠 -->
    </itk:ITKGridItem>
</itk:ITKGrid>
```

### ITKStackPanel

향상된 스택 패널로, 고급 스택 레이아웃 기능을 제공합니다.

```xml
<itk:ITKStackPanel Orientation="Horizontal" 
                   Spacing="10">
    <!-- 내용물 -->
</itk:ITKStackPanel>
```

## 복합 컴포넌트

### ITKDataGrid

데이터 표시를 위한 고급 그리드 컴포넌트입니다.

```xml
<itk:ITKDataGrid ItemsSource="{Binding Items}"
                 IsFilterable="True"
                 IsSortable="True"
                 SelectionMode="Multiple">
    <itk:ITKDataGrid.Columns>
        <itk:ITKDataGridTextColumn Header="이름" 
                                   Binding="{Binding Name}" />
        <itk:ITKDataGridTextColumn Header="나이" 
                                   Binding="{Binding Age}" />
    </itk:ITKDataGrid.Columns>
</itk:ITKDataGrid>
```

### ITKDialog

모달 다이얼로그 컴포넌트입니다.

```xml
<itk:ITKDialog Title="알림" 
               IsOpen="{Binding IsDialogOpen}"
               CloseButtonText="닫기"
               PrimaryButtonText="확인"
               SecondaryButtonText="취소"
               PrimaryButtonClick="OnConfirmClick">
    <TextBlock Text="작업을 수행하시겠습니까?" />
</itk:ITKDialog>
```

## 내비게이션 컴포넌트

### ITKNavigationView

앱 메뉴와 내비게이션을 위한 컴포넌트입니다.

```xml
<itk:ITKNavigationView>
    <itk:ITKNavigationView.MenuItems>
        <itk:ITKNavigationViewItem Icon="Home" Content="홈" Tag="home" />
        <itk:ITKNavigationViewItem Icon="Settings" Content="설정" Tag="settings" />
        <itk:ITKNavigationViewItem Icon="Document" Content="문서" Tag="docs" />
    </itk:ITKNavigationView.MenuItems>
    
    <Frame x:Name="ContentFrame" />
</itk:ITKNavigationView>
```

## 고급 컴포넌트

[내용 입력: 고급 컴포넌트 설명]

## 프레임워크별 구현 차이

[내용 입력: WPF, WinUI3, AvaloniaUI 구현 차이점]

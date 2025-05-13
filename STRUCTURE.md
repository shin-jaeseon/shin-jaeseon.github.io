# Xaml Design Studio Website Structure

## 주요 구성 요소

### 페이지

- **홈페이지 (index.html)**: 메인 페이지
- **소개 (about.md)**: Xaml Design Studio 소개
- **프로젝트 (projects.md)**: 프로젝트 목록
- **문서 (docs.md)**: 문서 메인 페이지
  - **시작하기 (docs/getting-started.md)**: 시작 가이드
  - **컴포넌트 (docs/components.md)**: 컴포넌트 문서
  - **테마 시스템 (docs/themes.md)**: 테마 시스템 문서
  - **고급 사용법 (docs/advanced.md)**: 고급 기능 문서
  - **API 문서 (docs/api.md)**: API 참조 문서
- **블로그 (blog.md)**: 블로그 메인 페이지
- **쇼케이스 (showcases.md)**: 프로젝트 쇼케이스
- **커뮤니티 (community.md)**: 커뮤니티 페이지
- **다운로드 (downloads.md)**: 다운로드 페이지
- **연락처 (contact.md)**: 연락처 정보

### 블로그 포스트

- **XamlDS.ITK 프로젝트 소개**: 2025-05-13
- **XAML UI 디자인 패턴: MVVM의 실전 활용**: 2025-05-12
- **효과적인 XAML 컴포넌트 아키텍처 설계**: 2025-05-10

### 레이아웃 및 디자인

- **기본 레이아웃 (default.html)**
- **페이지 레이아웃 (page.html)**
- **포스트 레이아웃 (post.html)**
- **프로젝트 레이아웃 (projects.html)**

### 디렉토리 구조

```
Repo_XamlDesignStudio/
├── _config.yml                # 사이트 설정
├── index.html                 # 메인 페이지
├── about.md                   # 소개 페이지
├── projects.md                # 프로젝트 목록
├── docs.md                    # 문서 메인
├── blog.md                    # 블로그 메인
├── showcases.md               # 쇼케이스
├── community.md               # 커뮤니티
├── downloads.md               # 다운로드
├── contact.md                 # 연락처
├── 404.html                   # 404 오류 페이지
├── _posts/                    # 블로그 포스트
│   ├── 2025-05-13-xamlds-itk-project-introduction.md
│   ├── 2025-05-12-xaml-ui-design-patterns-mvvm.md
│   └── 2025-05-10-effective-xaml-component-architecture.md
├── _projects/                 # 프로젝트 컬렉션
│   └── xamlds-itk.md
├── docs/                      # 문서 섹션
│   ├── getting-started.md
│   ├── components.md
│   ├── themes.md
│   ├── advanced.md
│   └── api.md
├── projects/                  # 프로젝트 상세 페이지
│   └── xamlds-itk.md
├── _layouts/                  # 레이아웃 템플릿
│   ├── default.html
│   ├── page.html
│   ├── post.html
│   └── projects.html
├── _includes/                 # 재사용 가능한 HTML 조각
│   ├── footer.html
│   ├── header.html
│   ├── social-share.html
│   └── ...
└── assets/                    # 정적 파일
    ├── css/
    │   └── main.scss
    ├── images/
    │   ├── logo/
    │   ├── screenshots/
    │   ├── showcases/
    │   ├── icons/
    │   ├── posts/
    │   └── team/
    └── favicon/
```

## 기능 목록

- 반응형 디자인
- 블로그 기능
- 프로젝트 쇼케이스
- 문서 시스템
- 다크/라이트 테마 지원 (추가 예정)
- 검색 기능 (추가 예정)
- 다국어 지원 (추가 예정)
- 소셜 미디어 공유

## 향후 계획

- 검색 기능 추가
- 다국어 지원 추가
- 사용자 포럼 통합
- API 문서 자동화

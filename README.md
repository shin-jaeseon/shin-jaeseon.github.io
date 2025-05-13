# Xaml Design Studio Website

이 저장소는 [Xaml Design Studio](https://www.xamldesign.studio) 웹사이트를 위한 것으로, GitHub Pages를 사용하여 호스팅됩니다.

## 로컬에서 사이트 실행하기

이 사이트는 Jekyll을 사용하여 구축되었습니다. 로컬에서 실행하려면 다음 단계를 따르세요:

1. Ruby 설치 (https://www.ruby-lang.org/en/downloads/)
2. Jekyll 및 Bundler 설치:
   ```
   gem install jekyll bundler
   ```
3. 저장소를 클론하고 해당 디렉토리로 이동:
   ```
   git clone https://github.com/shin-jaeseon/shin-jaeseon.github.io.git
   cd shin-jaeseon.github.io
   ```
4. 의존성 설치:
   ```
   bundle install
   ```
5. 로컬 서버 실행:
   ```
   bundle exec jekyll serve
   ```
6. 브라우저에서 `http://localhost:4000` 접속

## 사이트 구조

- `_posts/`: 블로그 포스트
- `_projects/`: 프로젝트 정보
- `assets/`: 이미지, CSS 등의 정적 파일
- `_layouts/`: 레이아웃 템플릿
- `_includes/`: 재사용 가능한 HTML 컴포넌트

## 콘텐츠 추가하기

### 블로그 포스트 추가

`_posts` 디렉토리에 `YYYY-MM-DD-title.md` 형식의 마크다운 파일을 생성하고 다음과 같은 YAML 프론트매터를 추가하세요:

```yaml
---
layout: post
title: "포스트 제목"
date: YYYY-MM-DD
categories: category_name
tags: tag1 tag2
---
```

그 다음 마크다운으로 콘텐츠를 작성하세요.

### 프로젝트 추가

`projects` 디렉토리에 새 마크다운 파일을 생성하세요.

## 라이센스

[내용 입력: 라이센스 정보]

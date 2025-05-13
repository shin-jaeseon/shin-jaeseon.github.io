---
layout: page
title: Contact
permalink: /contact/
---

# 연락처

Xaml Design Studio 팀에게 연락하고 싶으시다면 아래 방법을 이용해 주세요.

## 이메일

[내용 입력: 이메일 주소]

## 소셜 미디어

- GitHub: [내용 입력: GitHub 프로필 링크]
- Twitter: [내용 입력: Twitter 계정]
- LinkedIn: [내용 입력: LinkedIn 프로필]

## 문의 양식

<form action="[내용 입력: 폼 처리 URL]" method="POST">
  <div class="form-group">
    <label for="name">이름</label>
    <input type="text" id="name" name="name" required>
  </div>
  
  <div class="form-group">
    <label for="email">이메일</label>
    <input type="email" id="email" name="email" required>
  </div>
  
  <div class="form-group">
    <label for="subject">제목</label>
    <input type="text" id="subject" name="subject" required>
  </div>
  
  <div class="form-group">
    <label for="message">메시지</label>
    <textarea id="message" name="message" required></textarea>
  </div>
  
  <button type="submit" class="btn">보내기</button>
</form>

<style>
  .form-group {
    margin-bottom: 20px;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
  }
  
  input, textarea {
    width: 100%;
    padding: 8px;
    border: 1px solid #ddd;
    border-radius: 4px;
  }
  
  textarea {
    min-height: 150px;
  }
</style>

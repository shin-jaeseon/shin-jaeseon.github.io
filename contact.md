---
layout: page
title: Contact
permalink: /contact/
---

# Contact

If you would like to contact the Xaml Design Studio team, please use the methods below.

## Email

[Enter content: Email address]

## Social Media

- GitHub: [Enter content: GitHub profile link]
- Twitter: [Enter content: Twitter account]
- LinkedIn: [Enter content: LinkedIn profile]

## Contact Form

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

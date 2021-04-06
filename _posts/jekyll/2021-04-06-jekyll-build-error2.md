---
layout: post
title: "jekyll 새로운 장소에서 세팅시 에러"
date: 2021-04-06 23:25:32 +0900
categories: jekyll
tags: [jekyll, jekyll-build-error]
---

## 에러메세지

- Could not find public_suffix-3.0.2 in any of the sources (Bundler::GemNotFound)

## 개발환경

- ruby(with DevKit) 2.5.5p157 (2019-03-15 revision 67260) [x64-mingw32]
- Bundler version 2.2.15
- jekyll 4.2.0

## 에러해결

- 에러에 나오는 영어 그대로 일치하는 버전을 `install` 해주면 됨!
- 인스톨 후 bundle update 해주고
- bundle exec jekyll serve 서버실행
  {% highlight js %}
  gem install public_suffix --version 3.0.2
  bundle update
  bundle exec jekyll serve
  {% endhighlight %}

# seismin91.github.io

[사이트 열기](https://seismin91.github.io) · [Chirpy 문서](https://chirpy.cotes.page/posts/getting-started/)

Jekyll + Chirpy 7.6.0 기반의 개인 포트폴리오입니다. 원래 저장소의 Git 이력은 유지되어 있습니다.

## 내 정보 바꾸기

| 바꿀 내용 | 파일 |
| --- | --- |
| 사이트 이름, 설명, GitHub, 공개 이메일 | `_config.yml` |
| 첫 화면 소개와 대표 프로젝트 | `_includes/portfolio-intro.html` |
| 자세한 자기소개 | `_tabs/about.md` |
| 프로젝트 목록 | `_tabs/projects.md` |
| 사이드바 연락처 | `_data/contact.yml` |
| 추가 스타일 | `assets/css/portfolio.css` |
| 프로필 그림 | `assets/img/avatar.svg` |

이름·직무·경력·프로젝트 세부 정보는 임의로 넣지 않았습니다. 현재 표시 이름은 GitHub 아이디입니다.

## 글 쓰기

`_posts/YYYY-MM-DD-title.md` 파일을 만들고 다음 형태로 작성합니다. 날짜는 실제 게시일로 바꿔주세요.

```yaml
---
title: 글 제목
date: 2026-10-04 18:00:00 +0900
categories: [기록]
tags: [학습]
description: 글을 소개하는 한 문장
---
```

위 설정 아래에 Markdown 본문을 작성합니다. `pin: true`를 추가하면 글을 홈 상단에 고정할 수 있습니다.
실제 게시물이 아직 없으므로 홈에는 첫 기록을 준비 중이라는 문구를 표시합니다.

## 미리보기

Ruby 3.4와 Bundler가 필요합니다.

```sh
bundle install
bundle exec jekyll serve
```

브라우저에서 `http://127.0.0.1:4000`을 엽니다.

## 배포

저장소의 **Settings → Pages → Build and deployment → Source**를 **GitHub Actions**로 설정합니다.
`main`에 변경사항을 올리면 `.github/workflows/pages-deploy.yml`이 빌드, 내부 링크 검사, 배포를 순서대로 실행합니다.

개인 사이트이므로 `_config.yml`의 `url`은 `https://seismin91.github.io`, `baseurl`은 빈 문자열입니다.
Chirpy의 기본 검색·다크 모드·반응형 레이아웃을 사용합니다. 댓글, 통계, PWA 캐시는 초기 설정에서 꺼져 있습니다.

## 테마 업데이트

테마는 `Gemfile`에서 7.6.0으로 고정했습니다. 업데이트할 때 공식 Starter와 변경 내용을 확인하고,
홈 소개를 추가하기 위해 재정의한 `_layouts/home.html`과 한국어 `_data/locales/ko-KR.yml`도 함께 비교해주세요.

## 출처

- [Chirpy Starter](https://github.com/cotes2020/chirpy-starter)
- [Chirpy Theme](https://github.com/cotes2020/jekyll-theme-chirpy)
- 테마 라이선스: MIT (`LICENSE`)

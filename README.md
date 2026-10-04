# seismin91.github.io

[사이트 열기](https://seismin91.github.io) · [Chirpy 문서](https://chirpy.cotes.page/posts/getting-started/)

Jekyll + Chirpy 7.6.0 기반의 Sumin Kim 개인 사이트입니다. 원래 저장소의 Git 이력은 유지되어 있습니다.

## 사이트 구성

- **소개·연구**: 소개·이력(`/about/`)에 자기소개, 경력, 학위, 연구 관심 분야를 정리하고, 논문·발표(`/publications/`)에서 전체 연구 성과를 보여줍니다.
- **개인 기록**: 블로그(`/blog/`)와 프로젝트(`/projects/`)를 별도로 운영합니다. 카테고리, 태그, 연도별 기록은 블로그 안에서 이동합니다.
- **홈**: 프로필 요약, 두 영역으로 가는 링크, 최근 논문 2편과 최근 글 3개를 보여줍니다.

프로필과 논문 목록은 제공된 Google Scholar 공개 프로필을 2026-10-04에 확인해 반영했습니다.
학술지 논문 15편과 학회·발표 9건을 구분했고, 각 제목은 Scholar의 해당 상세 페이지로 연결합니다.
학위와 이전 경력은 자료가 없어 임의로 채우지 않았습니다. 인용 횟수는 표시하지 않으며, Scholar와 자동 동기화되지는 않습니다.

## 내 정보 바꾸기

| 바꿀 내용 | 파일 |
| --- | --- |
| 사이트 이름, 설명, GitHub, 공개 이메일 | `_config.yml` |
| 이름·소속·자기소개·경력·학위·관심 분야 | `_data/profile.yml` |
| 논문·학회 발표 목록 | `_data/publications.json` |
| 첫 화면 소개와 두 영역의 이동 링크 | `_includes/portfolio-intro.html` |
| 소개 페이지의 섹션 구성 | `_includes/profile.html` |
| 프로젝트 목록 | `_tabs/projects.md` |
| 블로그 목록 | `_tabs/blog.html` |
| 메뉴 그룹과 항목 | `_data/navigation.yml` |
| 사이드바 연락처 | `_data/contact.yml` |
| 추가 스타일 | `assets/css/portfolio.css` |
| 프로필 그림 | `assets/img/avatar.svg` |

공개 이메일과 상세 학위·경력은 확인 후 추가합니다. 이름을 바꾸면 `_config.yml`의 `title`과 `social.name`도 함께 바꿔주세요.

`_data/profile.yml`의 `education: []`는 학위가 확인되면 다음 필드를 가진 목록으로 바꿉니다: `degree`(학위), `institution`(학교), `field`(전공), `period`(기간). 경력은 `experience` 목록에 `role`, `organization`, `period`를 추가합니다.

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

위 설정 아래에 Markdown 본문을 작성합니다. `pin: true`를 추가하면 블로그 목록 상단에 고정할 수 있습니다.
홈은 최신 글 3개를, 블로그는 전체 글을 표시합니다. 현재 별도 페이지 나누기는 사용하지 않습니다.
`hidden: true`인 글은 홈과 블로그 목록에서 제외되지만, 비공개 글이 되는 것은 아닙니다.
실제 게시물이 아직 없으므로 홈과 블로그에는 첫 기록을 준비 중이라는 문구를 표시합니다.

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
재정의한 `_layouts/home.html`, `_includes/sidebar.html`, 한국어 `_data/locales/ko-KR.yml`도 함께 비교해주세요.

## 출처

- [Chirpy Starter](https://github.com/cotes2020/chirpy-starter)
- [Chirpy Theme](https://github.com/cotes2020/jekyll-theme-chirpy)
- 테마 라이선스: MIT (`LICENSE`)

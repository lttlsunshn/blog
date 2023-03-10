# ๐ป ๊ณ ๋์ฃผ ๋ธ๋ก๊ทธ

- [๋งํฌ๋ค์ด ์ฌ์ฉ๋ฒ](https://gist.github.com/ihoneymon/652be052a0727ad59601)

## Quick Start Guide

0. ๋ก์ปฌ์์ ์คํํ๊ธฐ
1. ๊ฐ์ธ ์ ๋ณด ์๋ฐ์ดํธํ๊ธฐ - `siteMetadata.js` (์ฌ์ดํธ ๊ด๋ จ ์ ๋ณด)
2. ๊ฐ์ธ ์ ๋ณด ์๋ฐ์ดํธํ๊ธฐ - `authors/default.md` (์์ฑ์ ์ ๋ณด)
3. ํ๋ก์ ํธ ๋ด์ฉ ์์ ํ๊ธฐ - `projectsData.js` 
4. ๋ธ๋ก๊ทธ ๊ธ ์์ฑํ๊ธฐ
5. Vercel์์ ๋ฐฐํฌํ๊ธฐ

---
## ๋ก์ปฌ์์ ์คํํ๊ธฐ

```bash
# Repository ๋ณต์ ํ๊ธฐ
$ git clone https://github.com/GoRyangJu/blog.git

# Repository๋ก ์ด๋ํ๊ธฐ
$ cd blog

# Dependencies ์ค์นํ๊ธฐ
$ npm install

# ์คํํ๊ธฐ
$ npm run dev
```

์ด์  ๋ก์ปฌ์์ ๋ธ๋ก๊ทธ๊ฐ ์คํ๋๋ ๊ฒ์ ๋ณด์ค ์ ์๋ ๋ฐ์. ๋ธ๋ผ์ฐ์ ์์ [http://localhost:3000](http://localhost:3000)์ ์ด์ด๋ณด์๋ฉด ํ์ธํ์ค ์ ์์ต๋๋ค.

---
## `siteMetadata.js` ์๋ฐ์ดํธ ํ๊ธฐ - data ํด๋์ ์กด์ฌ

```js
/* ์์) */

const siteMetadata = {
  title: 'GO Lee Blog',
  author: 'GO Lee',
  headerTitle: 'GO.',
  description: '์ง์๊ณผ ์๊ฐ์ ์ ๋ฆฌํฉ๋๋ค.',
  language: 'ko-KR',
  siteUrl: 'https://www.golee.tech',
  siteRepo: 'https://github.com/goleedev/blogo',
  siteLogo: '/static/images/logo.png',
  image: '/static/images/avatar.png',
  socialBanner: '/static/images/social-banner.png',
  email: 'golee.dev@gmail.com',
  github: 'https://github.com/goleedev',
  linkedin: 'https://www.linkedin.com/in/goleedev',
  locale: 'ko-KR',
  analytics: {
    googleAnalyticsId: 'G-3FV4PPZMLG',
  },
  comment: {
    provider: 'utterances',
    utterancesConfig: {
      repo: 'goleedev/blog',
      issueTerm: 'title',
      label: 'Comment ๐ฌ',
      theme: 'github-light',
      darkTheme: 'github-dark',
    },
  },
}
```

์๊ธฐ ์์์ฒ๋ผ ๋ณธ์ธ์ ์ ๋ณด๋ฅผ `siteMetadata.js`์ ์ถ๊ฐํด์ฃผ์๋ฉด ๋ฉ๋๋ค. 

`comment`๋ ๋ณธ์ธ์ ์ ์ ๋ค์/ํด๋น repository๋ฅผ ์ ์ด ์ฃผ์๋ฉด ๋ฉ๋๋ค :)

---
## `authors/default.md` ์๋ฐ์ดํธํ๊ธฐ - data/authors ํด๋์ ์กด์ฌ

```md
/* ์์) */

---
name: GO Lee
avatar: /static/images/avatar.png
occupation: Jr.Frontend Developer
company: UoL
email: golee.dev@gmail.com
linkedin: https://www.linkedin.com/goleedev
github: https://github.com/goleedev
---

๐ ์ ๋๋ ๋คํ๋ฉํ์ด์์ ์งํฅํ๊ณ  ๐ฅฐ ์๋ก์ด ๊ธฐ์ ๊ณผ ํธ๋ ๋๋ฅผ ์ตํ๋ ๊ฒ์ ์ข์ํ๋ ๐ง๐ปโ๐ป ํ๋ก ํธ์๋ ๊ฐ๋ฐ์์๋๋ค.

ํ ๋ด์์๋ ๐๐ปโโ๏ธ ๋ฅ๋์ ์ผ๋ก ํ๋ก์ ํธ๋ฅผ ์ํํ๊ณ  ๋ค์ํ ๊ธฐ์ ๊ณผ ํ์ ๋ฅ๋ ฅ์ ์์๊ฐ๋ ๊ฒ์ ๐ฃ๏ธ ์งํฅ์ ์ผ๋ก ์ผ๊ณ  ์์ผ๋ฉฐ, ์ฌ์ฉ์์๊ฒ๋ ๊ฐ์ฅ ํฉ๋ฆฌ์ ์ธ ๋์์ธ๊ณผ ์๋น์ค๋ฅผ ๐คฒ ์ ๊ณตํ๋ ๊ฐ๋ฐ์๊ฐ ๋๋ ๊ฒ์ ๋ชฉํ๋ก ๋ธ๋ ฅํ๊ณ  ์์ต๋๋ค.

```
---
## `projectsData.js` ์์ ํ๊ธฐ

์ด ๋ถ๋ถ์ ์ถํ์ ํ๋ก์ ํธ๋ฅผ ์ ์ํ ํ์ ์ถ๊ฐํด์ฃผ์๋ฉด ๋ฉ๋๋ค.

---
## ๋ธ๋ก๊ทธ ๊ธ ์์ฑํ๊ธฐ

```mdx
// ์์ 

---
title: '๐ WECLOME! ๋ธ๋ก๊ทธ๋ฅผ ๋ง๋์  ๊ฑธ ํฅ์ํฉ๋๋ค!'
thumbSrc: '/static/images/welcome.webp'
date: '2022-02-21'
tags: ['FE']
draft: false
summary: '๋ธ๋ก๊ทธ ์์ฑ๋ฒ์ ์ค๋ชํฉ๋๋ค.'
images: ['/static/images/welcome.webp']
---

# ๐ ๋ชฉ์ฐจ

![Welcome](/static/images/welcome.webp)

- **๐๐ป ๋ธ๋ก๊ทธ ์์ฑ๋ฒ**

---

# ๐๐ป ๋ธ๋ก๊ทธ ์์ฑ๋ฒ

๋ธ๋ก๊ทธ ์์ฑ๋ฒ์ด ๋ค์ด๊ฐ๋๋ค.
๋ธ๋ก๊ทธ ๋ด์ฉ์ ![๋งํฌ๋ค์ด ์ฌ์ฉ๋ฒ](https://gist.github.com/ihoneymon/652be052a0727ad59601)์ ์ฐธ์กฐํด์ ์์ฑํด์ฃผ์ธ์.

```

---
## Vercel์์ ๋ฐฐํฌํ๊ธฐ

[Vercel](https://vercel.com/login)์ Github ์์ด๋๋ก ๊ฐ์ํ๊ณ , repository๋ฅผ ์ ํํ๊ณ  ๋ฐฐํฌํด์ค๋๋ค.

---
## Licence

[MIT](https://github.com/timlrx/tailwind-nextjs-starter-blog/blob/master/LICENSE)
# blog

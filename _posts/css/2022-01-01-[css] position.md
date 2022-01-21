---
layout: post
title:  "[css] position"
subtitle:   "position - static, relative, absolute, fixed"
tags: css position relative absolute fixed
background: '/img/posts/01.jpg'
toc: true
toc_sticky: true
toc_label: "목차"
comments: true
---

## position 속성
---
__static__ : position 속성을 부여하지 않았을 때 가지는 디폴드 값.
__relative__ : 현재 위치에서 상대적인 offset 속성을 줄 수 있다.
__absolute__ : 부모 중에 static이 아닌 요소의 위치를 기준으로 상대적인 offset 속성을 줄 수 있다, 하지만 현재 위치가 변하는 것은 아니다.
__fixed__ : 브라우저에 대해서 위치를 잡는다. 스크롤에 영향을 받지 않고 고정된 위치를 가진다.

---
### static
{% include codepen.html hash="KKXomoG" title="static" %}
static은 position 속성을 부여하지 않았을 때 가지는 디폴드 값입니다.

---
### relative
{% include codepen.html hash="QWqmvrB" title="relative" %}
second의 position을 relative로 변경하고 아래로 10px 오른쪽으로 10px만큼 offset을 주었습니다.

---
### absolute
{% include codepen.html hash="BawrRPY" title="absolute" %}
absolute 속성을 주는 순간 z축이 변경되었고 이로 인해서 남은 빈 공간에 third가 채워져 들어갔습니다. 이 때 (x, y) 의 위치는 변하지 않았습니다

---
### fixed
{% include codepen.html hash="poWLPxq" title="fixed" %}
first에 fixed 속성을 주었습니다. 스크롤을 움직여도 똑같은 자리에 있는걸 확인할수 있습니다.




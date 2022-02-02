---
title:  "[css] display"
subtitle:   "inline, inline-block, block"
categories:
  - css
tags:
  - [css, blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## block
---
+ block 속성은 inline 과는 달리 __한 줄에 나열되지 않고 그 자체로 한 줄을 완전히 차지한다.__
+ block 속성을 가지고 있는 태그는 __기본적으로 너비 100%(width: 100%)속성을 가지고 있다.__
+화면의 가로 폭을 100%로 완전히 차지하기 때문에, 다음 요소가 양 옆으로 붙을 공간이 없어서 자연히 줄 넘김이 된다.
+ 인라인 요소와 다르게 margin, width, height 속성을 정의하면 모두 적용된다.
{% include codepen.html hash="LYzdLEx" title="block" %}

#### block 요소 종류
+ address, article, aside, audio, blockquote, canvas, dd, div, dl, fieldset, figcaption, figure, footer, form, h1, h2, h3, h4, h5, h6, header, hgroup, hr, noscript, ol, output, p, pre, section, table, ul, video

## inline
---
+ inline 속성은 __줄을 바꾸지 않고 다른 요소와 함께 한 행에 위치하려는 성향이다.__
+ width, height 속성이 적용되지 않는다.
+ margin-top, margin-bottom 속성이 적용되지 않는다 인라인 요소의 상, 하 여백은 margin이 아닌 line-height 속성에 의해 발생한다.
+ 인라인 속성을 가진 태그끼리 연속으로 사용되는 경우에는 최소한의 간격을 유지하기 위해서 좌, 우에 약 5px 가량의 외부 여백(margin)이 자동으로 발생한다.
{% include codepen.html hash="qBPojEq" title="inline" %}

#### inline 요소 종류 
+ a, abbr, acronym, b, bdo, big, br, button, cite, code, dfn, em, i, img, input, kbd, label, map, object, q, samp, small, script, select, span, strong, sub, sup, textarea, tt, var

## inline-block
---
+ inline-block 은 말그대로 inline의 특징과 block의 특징을 모두 가진 요소입니다.
+ binline 처럼 줄바꿈이 이루어지지 않는다.
+ block 처럼 width, height를 지정 할수 있다.

{% include codepen.html hash="JjrLJoR" title="inline-block" %}
> block인 div를 사용했지만 divplay: inline-block을 적용하니 inline처럼 한 행에 위치한것을 볼수 있다.




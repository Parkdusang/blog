---
title: ":iphone: Trainer assistant application"
layout: post
date: 2016-01-23 22:10
tag:
- android
- jekyll
image:  https://Parkdusang.github.io/blog/assets/images/3_1.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
author: johndoe
externalLink: false
---
## Summary:

실제 트레이너와 고객이 집에서도 좀 더 편하게 운동이나 식단보고등을 하고 조언을 하기 편하게 기능을 제공해주는 앱입니다.
총 3명(개발자 2명 디자인 1명)으로 한 달 동안 진행된 프로젝트 입니다.
구글플레이에 Fitcen이란 이름으로 업로드 되어있습니다.

#### Especial Elements
- [Introduction](#introduction)
- [Screenshot](#screenshot)
- [Link](#link)
- [Skill](#skill)


---
## Introduction

회사소개, 공연영상, 교육 자료, 공연 일정 으로 총 4개의 목록이 있습니다.  
회사소개엔 기업소개와 회장님 인사말이 포함됩니다.  
공연영상엔 Youtube API를 통해서 공연된 영상을 볼 수 있습니다.  
교육자료엔 악보자료나 국악을 들을 수 있습니다.  
공연일정은 WebView로 되어있고 기업의 홈페이지를 Activity안으로 가져옵니다.  

---

## Screenshot

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="{{ site.url }}/{{ 'assets/images/1_2.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>

    <div class="toright">
        <p>게임을 시작하게 되면 빨간색으로 빛나는 부분에 3D Modeling 된 안드로이드가 서 있습니다.  <br />
        안드로이드는  J,L,K,I 키를 통해 움직일 수 있습니다.  <br />  
        기본으로 적용되는 View는 맵 전체가 보이지않고 자기 주변만 볼 수 있습니다. <br />
        안드로이를 움직이게 되면 움직이는 동안은 팔과 다리가 움직이는 에니메이션을 보여줍니다. <br />
        벽에 부딪히면 넘어갈 수 없게 설계되어 있고 캐릭터의 움직임을 멈추게 되면 다시 서있는 애니메이션으로 돌아옵니다.   </p>
    </div>
</div>
---  
<div class="side-by-side">
    <div class="toleft">
        <p>게임의 기능을 더하기 위해서 다음과 같은 2가지 기능을 추가했습니다.</p>
        <span> -벽 점프</span><br />
        <span> -시점 변환</span>
        <p>1. E 버튼을 누르면 벽에서 그 건너편으로 점프를 하게 됩니다. 벽을 넘을때도 에니메이션을 제공합니다.</p>
        <p>1. M 버튼을 누르면 시점을 변경합니다. 전체화면과 자기 주변을 볼 수있는 2가지 View가 있습니다.</p>
    </div>

    <div class="toright">
        <img class="image" src="{{ site.url }}/{{ 'assets/images/1_1.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>
</div>

![Screenshot](https://raw.githubusercontent.com/Parkdusang/blog/gh-pages/assets/images/2_1.jpeg)  

---  

![Screenshot](https://raw.githubusercontent.com/Parkdusang/blog/gh-pages/assets/images/2_2.jpeg)  

---
## Link
이 어플리케이션은 현제 구글플레이에 업로드 되어있습니다.  
- [Google Play](https://play.google.com/store/apps/details?id=com.fitcen.parkdusang.healthtrainer). 하이퍼링크를 클릭하시면 어플리케이션을 다운받으실 수 있습니다.

---

## Skill

- Google Cloud Messaging
- Google+ API
- PHP(Using Background)
- PageView
- Splash
- Dynamic list view(Depending on the database)




---

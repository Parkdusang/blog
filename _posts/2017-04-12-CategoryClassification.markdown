---
title: ":iphone: Category Classification"
layout: post
date: 2016-10-21 22:10
tag:
- Arduino
- jekyll
image:  https://Parkdusang.github.io/blog/assets/images/jekyll-logo-light-solid.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
author: johndoe
externalLink: false
---
## Summary:

이 프로젝트는 일정 형식을 가진 뉴스 기사들이 있을 때, 트레이닝 데이터와 테스트 데이터로 나눕니다.  
트레이닝 데이터에서 그 기사의 카테고리, 그리고 기사 본문을 분리해서 저장합니다.
각각의 기사별로 중복을 제거, 전체 단어에서도 중복을 제거한 후에 카이스퀘어 가중치를 단어별로 매칭시킵니다.  
마지막으로 트레이닝 데이터를 svm float 형식으로 돌리기 위한 방법으로 저장합니다.
테스트 데이터는 위에서 가공한 데이터를 이용해서 텍스트 파일을 만듭니다.

#### Especial Elements
- [Skill](#skill)
- [Introduction](#introduction)
- [Videos](#videos)
- [Link](#link)



---
## Skill

- Python
- Time Complexity
- Data structure

---
## Introduction

<div class="side-by-side">
    <div class="toleft">
        <img class="image" height="400"  src="{{ site.url }}/{{ 'assets/images/4_3.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>

    <div class="toright" style="padding-top:30px;vertical-align:center; ">
        <p>
          이 게임을 진행하기 위해서는 아두이노,8x8LED,Buzer,IRsensor,빨강 노랑 초록색의 LED와 리모콘이 있어야 합니다. <br />
          먼저 실행을 시키게 되면 8x8LED에 귀여운 도트 이미지가 움직이게 됩니다. <br />
          이 게임에 있는 곡은 총 3개의 곡으로 유저는 1,2,3번을 누르게되면 그에 맞는 게임을 플레이하게 됩니다. 이떄 LED화면 개수만큼 노래의 노드가 떨어지므로 총 8개의 키로 게임을 하게 됩니다.
        </p>
    </div>
</div>
---  
<div class="side-by-side">
    <div class="toleft">
        <p>게임을 실행하게 되면 각 노래에 맞게 Buzer에서 노래가 흘러나오면서 LED에 노드가 떨어지기 시작합니다.<br / >
        유저는 노래를 들으면서 노드가 맨 아래줄에 있을때 맞는 버튼을 누르면 게임이 진행됩니다.<br />
        판정에는 perfect와 good, Fail이 있습니다. 이 판정은 빨간색,노란색, 초록색 LED를 통해서 유저가 실시간으로 알 수 있습니다.
        그리고 연속으로 10개를 틀리게되면 게임은 종료되게 됩니다.
        게임이 종료되면 LED화면에 유저가 게임을하면서 전체 노드중에 정확하게(Perfect, good) 누른 비율을 출력해주고 다시 귀여운 도트를 출력시키면서 노래를 선택할 수 있게 구현했습니다.
        </p>
    </div>
    <div class="toright">
        <img class="image" height="400" src="{{ site.url }}/{{ 'assets/images/4_4.gif' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>
</div>

---
## Videos

실제 게임 데모영상 입니다.

**Youtube**

<iframe width="560" height="310" src="https://www.youtube.com/embed/dnNiW8sT0Ig" frameborder="0" allowfullscreen></iframe>


---
## Link
이 게임 코드는 현재 깃허브에 올려놨습니다.
- [Github](https://github.com/Parkdusang/robotProject). 하이퍼링크를 클릭하시면 깃허브 페이지로 이동합니다.

---

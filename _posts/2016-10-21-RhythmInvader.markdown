---
title: ":iphone: Rhythm Inavader (Rhythm Game)"
layout: post
date: 2016-10-21 22:10
tag:
- android
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

아두이노와 8x8LED ,Buzer , IRsensor와 리모콘을 이용한 리듬게임입니다.  
두 명으로 진행한 프로젝트로 2kb의 메모리를 가진 아두이노를 이용해서 어떻게 노래를 저장시키고,실시간 음악에 맞게 노드를 떨어뜨릴지 고민하며 진행한 프로젝트 입니다.

#### Especial Elements
- [Skill](#skill)
- [GameFlowchart](#gameflowchart)
- [Videos](#videos)
- [Introduction](#introduction)
- [Screenshot](#screenshot)
- [Link](#link)



---
## Skill

- Using flash memory
- 8x8LED Control
- memory management with assembly language
- Edit Library (IR sensor , tone)
- C

---
## GameFlowchart

<!-- ![Screenshot](https://raw.githubusercontent.com/Parkdusang/blog/gh-pages/assets/images/4_1.png)   -->
![Screenshot](https://raw.githubusercontent.com/Parkdusang/blog/gh-pages/assets/images/4_2.png)
![](https://raw.githubusercontent.com/Parkdusang/blog/gh-pages/assets/images/4_4.gif)
![](https://raw.githubusercontent.com/Parkdusang/blog/gh-pages/assets/images/4_4.gif)

<div class="toleft">
    <img class="image" height="400"  src="{{ site.url }}/{{ 'assets/images/4_4.gif' }}" alt="Alt Text">
    <figcaption class="caption">Photo by Dusang Park</figcaption>
</div>
<p> 아두이노를 실행하면 대기모드가 실행되고나서 <br />  <span>리모콘으로 노래선택 -> 게임플레이 -> 적중도 출력 -> 대기모드</span>  <br />순서대로 게임이 실행됩니다. </p>
---  
## Introduction

<div class="side-by-side">
    <div class="toleft">
        <img class="image" height="400"  src="{{ site.url }}/{{ 'assets/images/4_3.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>

    <div class="toright">
        <p>
        하나의 어플리케이션에서 트레이너 모드와 고객 모드가 나누어져 있습니다.
        두 모드로 들어가게 되면 각각 제공되는 기능 또한 다르게 제공됩니다.
        먼저 모드를 선택하게되면 아이뒤와 비밀번호를 입력해야합니다.처음에 아이뒤가 없다면 회원가입을 해야하고, 각 모드별로 아이뒤와 비밀번호는 따로 분리되어있고 비밀번호 찾기와 아이뒤 찾기를 제공하고 있습니다.  <br />  
        트레이너 모드 선택후 회원가입을 하게되면 트레이너 기능을 제공, 고객모드로 들어가서 회원가입을 선택하면 고객모드를 제공합니다. <br />
        </p>
    </div>
</div>
---  
<div class="side-by-side">
    <div class="toleft">
        <p>트레이너 모드로 들어오게되면 먼저 고객관리를 할 수 있습니다. <br />
        지금 자신이 관리하고 있는 고객 명단이 뜨고 + 버튼을 눌러서 고객에게 요청을 보낼 수 있습니다. </p>
        <span> 이미지는 관리하는 고객 한명을 클릭했을때 이미지 입니다.</span><br />
        <p>각각의 고객별로 지금까지의 보고서와 오늘 올린 보고서의 내용, 오늘 집에서 해야하는 운동을 운동세트와 세트별 회수, 운동을 하는 방법등에 대해 자세하게 지정해줄 수있고 고객에 맞춰서 피드백을 전송해 줄 수 있습니다.</p>
    </div>

    <div class="toright">
        <img class="image" height="400" src="{{ site.url }}/{{ 'assets/images/3_3.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>
</div>
---   
<div class="side-by-side">
    <div class="toleft">
        <img class="image" height="400" src="{{ site.url }}/{{ 'assets/images/3_4.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>

    <div class="toright">
        <p>고객은 트레이너의 요청을 승락하게되면 다음 이미지와 같은 화면이 등장합니다. 매일 트레이너가 지정해준 목록을 볼 수있고
        초기에 자신이 목표하는 몸무게,현재 몸의 상황을 트레이너가 기입하면 시각화된 그래프로 자신의 BMI,지방량의 정도,현재 몸무게등을 볼 수있습니다. <br />
        일 별로 지정받은 운동에 대해서 자신이 실행한 운동을 체크하고 각 운동에대해 트레이너에게 할 말이 있다면 글을써서 트레이너에게 보고서를 올리게 됩니다. 또한 지금까지 자신이 했던 보고서와 트레이너의 피트백을 각 날자별로 정리해서 어떤운동과 어떤 피드백을 받았는지 확인할 수 있습니다.
        </p>
    </div>
</div>

---
## Videos

실제 어플리케이션 데모영상 입니다.

**Youtube**

<iframe width="560" height="310" src="https://www.youtube.com/embed/a_4i_khlDms" frameborder="0" allowfullscreen></iframe>


---  
## Screenshot

<div class="side-by-side">
    <div class="toleft">
        <img class="image" height="400" src="{{ site.url }}/{{ 'assets/images/3_5.png' }}" alt="Alt Text">
        <figcaption class="caption">Daily Report(Customer)</figcaption>
    </div>
    <div class="toright">
        <img class="image" height="400" src="{{ site.url }}/{{ 'assets/images/3_6.png' }}" alt="Alt Text">
        <figcaption class="caption">Assign Exercise</figcaption>
    </div>
</div>

---
## Link
이 어플리케이션은 현제 구글플레이에 업로드 되어있습니다.  
- [Google Play](https://play.google.com/store/apps/details?id=com.fitcen.parkdusang.healthtrainer). 하이퍼링크를 클릭하시면 어플리케이션을 다운받으실 수 있습니다.

---

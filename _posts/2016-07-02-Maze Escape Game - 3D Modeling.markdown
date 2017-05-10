---
title: ":computer: Maze Escape Game - 3D Modeling"
layout: post
date: 2016-07-02 20:48
image: /assets/images/markdown.jpg
headerImage: false
tag: jekyll
hidden: true # don't count this post in blog pagination
category: project
projects: true
author: Dusang
description: Markdown summary with different options
externalLink: false
---

## Summary:

C언어와 OpenCV를 이용해서 지형과 캐릭터를 모델링하고 미로를 만드는 알고리즘과 View 를 직접 구현했습니다.

#### Especial Elements
- [Gamemanual](#gamemanual)
- [MazeAlgorithm](#mazealgorithm)
- [GameClear](#gameclear)
- [Videos](#videos)


---
## GameManual
**Image** on the left and **Text** on the right:
{% highlight html %}
Left : J
Right : L
Top : I
Bottom : K

Change View : M
Skill(Jump) : E
{% endhighlight %}

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

**Text** on the left and **Image** on the right:

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


---
## MazeAlgorithm

테두리 부분을 전부 벽으로 만듭니다.  
<span class="evidence">1,1의 좌표를 시작점으로, width와 height의 -1 지점을 도착지점으로 설정합니다.</span>  
도착점과 시작점을 설정하게되면 알고리즘에 의해 미로를 maze[y][x]에 저장합니다.  
maze[][] == 2 는 벽으로 그외엔 길로 인식합니다.  
자세한 코드는 깃허브에 올라와 있습니다.

{% highlight cpp %}
void makewall(int y, int x) {
    checkroad[y][x] = false;
    int solutionArray[4] = { 1, 2, 3, 4};
    ShuffleArray(solutionArray);

    for(int i = 0 ; i< 4 ; i++){
        if(solutionArray[i] == 1){
            routetop(y ,x);
        }
        else if(solutionArray[i] == 2){
            routeright(y,x);
        }
        else if(solutionArray[i] == 3){
            routebottom(y ,x);
        }
        else{
            routeleft(y ,x);
        }
    }
    return ;
}
{% endhighlight %}

---

## GameClear

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="{{ site.url }}/{{ 'assets/images/1_3.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>

    <div class="toright">
        <p>게임의 도착지점은 파란색 바닥으로 되어있습니다.</p>
        <br />
        <br />
        <p>캐릭터가 도착 지점에 들어가게 되면 안드로이드는 시작지점까지 점프해서 날아가게 됩니다. </p>
        <p>안드로이드가 시작 지점에 도착하게되면 미로 알고리즘을 다시 동작해서 새로운 미로를 만들어 냅니다. 그리고 새로운 게임을 플레이 할 수 있습니다.</p>
    </div>
</div>

---


## Videos

실제 게임플레이 영상입니다.

**Youtube**

<iframe width="560" height="310" src="https://www.youtube.com/embed/qDNZa_tf7Ic" frameborder="0" allowfullscreen></iframe>

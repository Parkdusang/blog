---
title: ":ramen:Maze Escape Game - 3D Modeling"
layout: post
date: 2016-08-24 20:48
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
- [Game manual](#Game manual)
- [Maze_Algorithm](#Maze_Algorithm)
- [character Modeling](#character Modeling)
- [Star](#star)
- [Especial Breaker](#especial-breaker)
- [Spoiler](#spoiler)
- [Videos](#Videos)


---
## Game manual
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
        <img class="image" src="{{ site.url }}/{{ 'assets/images/1_1.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>

    <div class="toright">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>
</div>

**Text** on the left and **Image** on the right:

<div class="side-by-side">
    <div class="toleft">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>

    <div class="toright">
        <img class="image" src="{{ site.url }}/{{ 'assets/images/1_2.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>
</div>


---
## Maze_Algorithm

테두리 부분을 전부 벽으로 만듭니다.  
<span class="evidence">1,1의 좌표를 시작점으로, width와 height의 -1 지점을 도착지점으로 설정합니다.  </span>
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

## Game Clear

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="{{ site.url }}/{{ 'assets/images/1_3.png' }}" alt="Alt Text">
        <figcaption class="caption">Photo by Dusang Park</figcaption>
    </div>

    <div class="toright">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>
</div>

---


## Videos

Do you want some videos? Youtube, Vimeo or Vevo? Copy the embed code and paste on your post!

**Example**

{% highlight html %}
<iframe width="560" height="310" src="https://www.youtube.com/embed/r7XhWUDj-Ts" frameborder="0" allowfullscreen></iframe>
{% endhighlight %}

<iframe width="560" height="310" src="https://www.youtube.com/embed/qDNZa_tf7Ic" frameborder="0" allowfullscreen></iframe>

---
title: ":computer: Category Classification"
layout: post
date: 2017-04-12 12:10
tag:
- Datamining
- Python
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
- [Link](#link)

---
## Skill

- Python
- Time Complexity
- Data structure

---
## Introduction

모든 뉴스기사의 형식은 아래와 같이 이루워져 있습니다.
```TEXT
@DOCUMENT
#DocID : 1678
#CAT'03: /건강과 의학/의약학/치의학
#CAT'07: /정치/정부부처/보건복지부;/건강과 의학/한의학 전통의학;/건강과 의학/치의학
#TITLE :  치과의원.한의원, 4년사이 폭발적 증가
#TEXT  :
 지난 89년 전국민의료보험 실시이후 국내 의료기관중 치과의원과 한의원은
   4년사이에 폭발적으로 늘어난데 반해 보건소 또는 보건진료소 등의
   공공보건기관과 약국 증가율은 극히 미미한 것으로 나타났다.

    13일 보사부에 따르면 지난해 12월31일 현재 전국 의료기관은 모두 4만8천
   9백64개소로 89년 전국민 의료보험 실시 당시에 비해 7천4백89개소(18.0%)
   가 늘어났다.

    의료기관을 종별로 보면 치과의원과 한의원은 지난 89년에 비해 각각
   59.8%, 48.7% 늘어나고 또 의원 26.2%, 병원 16.1%,종합병원 9.9%의
   증가율을 기록했다.
```
>
```TEXT
@DOCUMENT
```
>모든 기사는 @DOCUMENT 으로 시작합니다.  
```TEXT
#CAT'03: /건강과 의학/의약학/치의학
```
>카테고리는 CAT'03 옆에 맨처음 목록을 카테고리로 선정합니다.  여기선 '건강과 의학'이 카테고리가 됩니다.
```TEXT
#TEXT  :
```
>아래에 있는 부분이 본문으로 이 단어들을 전부 분리해서 기사별로, 그리고 전체 기사의 본문을 저장해서 중복을 제거합니다.   

---
split 으로 #TEXT 분리하고 특수문자를 제거해준 다음, 다음과같이 중복을 제거합니다.

{% highlight python %}
DocumentText = sentence[1].strip().split()
seen1 = set()
result1 = []
for item in DocumentText:
    if item not in seen1:
        item = item.strip()
        seen1.add(item)
        result1.append(item)
DocumentText = result1

for item in DocumentText:
    allOfData.append(item)
{% endhighlight %}
> 각 기사별로 DocumentText에 본문 단어를 저장하고 중복을 제거한 후, 전체적으로 단어를 저장해줍니다.  

---  

전체단어에서 중복을 제거하고 카이스퀘어 가중치를 적용한 후에 트레이닝 데이터셋과 테스트셋을 다음과 같이 저장합니다.
{% highlight python %}
5 8:403.427542 11:373.343612 21:303.420452 31:274.758371 34:266.668932 39:244.188663
3 2:728.241122 3:677.553595 6:491.396359 8:403.427542 16:341.701329 21:303.420452 26:289.720997
1 2:728.241122 6:491.396359 39:244.188663 40:242.245916 49:228.634069 56:216.100218 60:213.196119
...
4 2:728.241122 14:352.112758 21:303.420452 22:303.279107 26:289.720997 28:283.509302
{% endhighlight %}
>맨 왼쪽에 단어는 카테고리 번호입니다. 전체기사의 카테고리를 저장하고 중복을 제거해서 총 개수를 파악,카테고리별로 번호를 매깁니다.  

{% highlight python %}
5 8:403.427542 11:373.343612
{% endhighlight %}
> 전체 단어도 인덱스가 부과됩니다. 이 경우 5번 카테고리에 8번 11번의 단어가 있고 8번은 카이스퀘어 값이 403.427542 11은 373.343612인 경우입니다.  

최종적으로 training File 과 TestFile 이 만들어지면 SVM을 돌려서 결과를 확인합니다.


---
## Link
이 코드는 현재 깃허브에 올려놨습니다.
- [Github](https://github.com/Parkdusang/Categoryclassification). 하이퍼링크를 클릭하시면 깃허브 페이지로 이동합니다.

---

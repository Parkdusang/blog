---
title: ":computer: DrawerDruwa-JavaGame with GUI"
layout: post
date: 2016-08-30 11:10
tag:
- java
- jekyll
image:  https://Parkdusang.github.io/blog/assets/images/drawer/title.png
headerImage: true
projects: true
hidden: true
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
author: Dusang
externalLink: false
---
## Summary:

Java Swing을 이용해서 개발한 게임으로 서로 턴을 돌아가면서 한명이 주어진 문제를 그림으로 표현하고 다른 사람들이 그 그림을 맞춰보면서 진행하는 게임입니다. 총 6개의 방을 만들 수 있고 최대 4명이서 게임을 진행할 수 있습니다.  
아래 깃허브 링크에서 Wifi를 들어가시면 더 자세하게 나와있습니다.

#### Especial Elements
- [Skill](#skill)
- [Introduction](#introduction)
- [Screenshot](#screenshot)
- [Link](#link)

---
## Skill

- Java Swing
- Socket
- Network
- MultiThread


---

## Introduction


#### __Process for executing__  ####

### Step 1 : Login or create new account

>If user doesn't have account, press "join" to create an account. User can select character and input ID & PW.  
Their ID , password and character are stored in database.  
User enters ID and Password and presses "Login". Then, check if ID and password are identified within database.  

### Step 2 : Enter into waiting room and making game room

>If checking is OK, Client socket is connected to server and enter to waiting room!  
In waiting room, user's IDs entered in waiting room are seen in real time!  
Each user can create or enter game room. Each game room can accept 4 users maximum.  
A person who makes a game room is a host of the room.  
Also each room's state is stored in server if users create, enter, or leave game room.  

### Step 3 : Starting game, "Get The Correct Answer"

>If a user presses "Start" button, game starts.
First host is examiner, examiner receives topic from server and can draw related to the topic. Others can see examiner's drawing in real time and analogize the answer.  
If users can't analogize answer at all, users can press "HINT" button to get hint once in a game.  
When users except examiner get the correct answer or fixed time is out, other user becomes examiner. User who gets the correct answer and the examiner get points.  
But if anyone can't solve, there's no points!  

### Step 4 : End of game and exit game room

>Game should be continued for 5 matches. After 5th matches, a user who gets the most points becomes winner.  
And Each user's points in the game room are stored, so if user's points exceed a fixed quantity, user's grade becomes higher.  
User presses "exit" button to exit game room and returns to waiting room.  

---
## Screenshot

![Screenshot](https://raw.githubusercontent.com/Parkdusang/blog/gh-pages/assets/images/drawer/1_1.png)  



![Screenshot](https://raw.githubusercontent.com/Parkdusang/blog/gh-pages/assets/images/drawer/1_2.png)  
---

## Link
이 코드는 현재 깃허브에 업로드 되어있습니다.  
- [Github](https://github.com/JunsooLee/Network_16_TermProject). 하이퍼링크를 클릭하시면 코드를 보실 수 있습니다.

---

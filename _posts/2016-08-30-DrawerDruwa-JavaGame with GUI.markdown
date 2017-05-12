---
title: ":computer: DrawerDruwa-JavaGame with GUI"
layout: post
date: 2016-08-30 11:10
tag:
- java
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
- [Skill](#skill)
- [Videos](#videos)
- [Introduction](#introduction)
- [Screenshot](#screenshot)
- [Link](#link)



---

## Introduction
Process for executing

Step 1 : Login or create new account

If user doesn't have account, press "join" to create an account. User can select character and input ID & PW.

Their ID , password and character are stored in database.

User enters ID and Password and presses "Login". Then, check if ID and password are identified within database.

Step 2 : Enter into waiting room and making game room

If checking is OK, Client socket is connected to server and enter to waiting room!

In waiting room, user's IDs entered in waiting room are seen in real time!

Each user can create or enter game room. Each game room can accept 4 users maximum.

A person who makes a game room is a host of the room.

Also each room's state is stored in server if users create, enter, or leave game room.

Step 3 : Starting game, "Get The Correct Answer"

If a user presses "Start" button, game starts.

First host is examiner, examiner receives topic from server and can draw related to the topic. Others can see examiner's drawing in real time and analogize the answer.

If users can't analogize answer at all, users can press "HINT" button to get hint once in a game.

When users except examiner get the correct answer or fixed time is out, other user becomes examiner. User who gets the correct answer and the examiner get points.

But if anyone can't solve, there's no points!

Step 4 : End of game and exit game room

Game should be continued for 5 matches. After 5th matches, a user who gets the most points becomes winner.

And Each user's points in the game room are stored, so if user's points exceed a fixed quantity, user's grade becomes higher.

User presses "exit" button to exit game room and returns to waiting room.

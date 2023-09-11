# Snake Duel

Online gaming project with use of Vue 3 + SpringBoot 2.7

### Technologies used: 
Front end: Vue 3, vuex, vue-router, bootstrap, WebSocket, jwt-token

Backend: SpringBoot, SpringSecurity, SpringCloud, MyBatis-plus, MySql, WebSocket, Multithread and lock, restTemplate, Maven. 

Operation and deployment: AWS EC2, Git, Docker, Linux. 

### Project Architecture: 
#### SpringBoot Micro service: 
##### BackendApplication: 
Handles all the backend services and uses WebSocket to communicate with the front end. 

##### MatchingSystemApplication: 
Module to detect and match players together to play the game and return the results of the match. 

##### BotRunningSystemApplication: 
The game provides the option to have AI play for the users. Right now it only supports Java code using jOOR Object Oriented Reflection. More details here: https://github.com/jOOQ/jOOR. 


### Diagram: 

![Screenshot 2023-09-10 at 9 27 29 PM](https://github.com/MLi-dev/kob/assets/85410877/c572ad14-2358-4d8b-b81c-ceb105627880)

### Demo of Game: 

![SnakeDuelDemo](https://github.com/MLi-dev/kob/assets/85410877/28c70ecd-8dae-4941-a5b9-387302e59425)

### Sample Bot Code (Let AI Play): 
https://github.com/MLi-dev/kob/wiki/Bot-Code



### Database structure: 
Used 3 tables for users, bots, and recording positions. 
```
create table bot
(
    id          int auto_increment
        primary key,
    user_id     int            not null,
    title       varchar(128)   not null,
    description varchar(356)   null,
    content     varchar(10000) null,
    create_time datetime       null,
    modify_time datetime       null,
    constraint id
        unique (id)
);

create table record
(
    id          int auto_increment
        primary key,
    a_id        int           null,
    a_sx        int           null,
    a_sy        int           null,
    b_id        int           null,
    b_sx        int           null,
    b_sy        int           null,
    a_steps     varchar(1000) null,
    b_steps     varchar(1000) null,
    map         varchar(1000) null,
    loser       varchar(10)   null,
    create_time datetime      null,
    constraint id
        unique (id)
);

create table user
(
    id       int auto_increment
        primary key,
    username varchar(128)     not null,
    password varchar(128)     not null,
    photo    varchar(1024)    null,
    rating   int default 1500 not null,
    constraint id
        unique (id)
);
```

### Final Acknowledgements: 
I am very thankful for having had the opportunity to work on such a big project and exploring both front and backend design. 

# Relative vs Absolute Path

Let's discuss what is relative and absolute path. In order to understand this, we need to take a analogy. Imagine Linux filesystem as a multistory building. Enterance of the building is called root and represented as /. To navigate to room 1 on level 5, we need to first go to main enteramce (/) then we need to go to 5th floor floor5 floor5/ and from there enter the room1. Hence the absolute path to this particular room within a building is /floor5/room1. From here, now we want to move to room 2 then we need to first move out of our room1 by entering ../ and then include room name room2. We took a relative path to room 2 in this case, it is ../room2. As we are already on floor 5, we do not need to leave the building. with respect to main enterance, we have /floor5/room2 that is absolute path.

Absolute path  - /floor5/room2
Relative path  - ../room2 ( I am on 5th floor).

If you want to know your current working directory then run this command

`pwd`{{execute}}

if you want to change your location then you can use cd command.





# Sequencing

Here is the task. The client would like to see a prototype of a mini-game that is completely client-side – you do not need to save to a server. They would like to see what our designer meant by "video squencing game". How the game works is relatively simple.

* You see 5 50x50 thumbnails in a column to the left of the window
* To the right of that column, you see a placeholder for a video
* Under that video placeholder, you see a row of 5 empty squares
* You are to drag the 50x50 thumbnails to the row in the right order
* When you drag an item to the row that is incorrect, it should bounce back 
* When you drag an item to the row that is correct, that items border should turn green indicating you were right
* When all five items are in the right order, we trigger the video play event

Think of this like a puzzle. The items in the column are shuffled and random. When the row is full of those items in the right order, they would make one long image. 

## What we're looking for

We're really just looking for pseudo code here. And, only javascript. It doesn't have to work exactly, we're just looking at your approach to the problem. This is a good example of something that we usually stub out in a chatroom together over 20 - 30 minutes.

![ScreenShot](http://mindspacepdx.s3.amazonaws.com/github-images/video-sequence-diagram.png)

## Guidelines

1. Try not to use jQuery too much, the more native JS the better
2. Modern browsers only, no need for crazy IE 8 stuff
3. Think about whether you want to use data-attributes or not, and why
4. Any fancyness you'd like to add to this is even better.

---
layout: post
title:  "Interview Questions"
date:   2015-12-27 11:39:54 +0000
categories: core
---

```java
public static final boolean isCycle( int[] circularArray){
//look at edge cases
vistPostion(0, circularArray);

}
private int[] vistedPositions;
private valid visitPostion(int index, int[] circularArray){
if(visitedPosition[index]==0){
visitedPositon[index] = 1;
return visitPostion(circularArray[index];
}else{
return false;
}
}


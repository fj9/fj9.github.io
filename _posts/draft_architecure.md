---
layout: post
title:  "Architecture Patterns"
date:   2015-11-27 11:39:54 +0000
categories: architecture
---

Component an encapsulated unit of software specific role and responsibility
Architecture helps you to understand a system at a higher level without requiring intimate knowledge of the modules that make up the system.   Recongizing the architecture of a system allows you to answer various questions such as.
how dot he components interact
is the system scalable
is the system reponisive to change
is there a logical flow 
what are the deployment characteristics
is the system extensible
how testable is the system

Without architecture patterns you would need to dive through all of the code. 

#Layered
prsentation layer - buisness layer- persistence layer- db
Most EE applications without thought to architecture end up with this sort of pattern. 
The layers are closed, so in order to get to the db layer you have to go through the persistence layer.  This results in layers of isolation  which allows you to change the db layer without having to worry about the presentation or buisness lauer
The layers are closed to isolate change.  This leass to seperation of concerncs.
You can add another layer it specifically disallows other layers from accessing layers it shouldnt.  So you can make some layers open so that they can be bypassed by the layer above to go to the layer below.

Vertical layers such as utils, A change in these open layers will probably resulkt in changes across the other layers and has to some extent broken the seperatrion of concerns.

Associated anti pattern - architecture sinkhole. Proxies going down the layers for simple hand offs of data.

Tends to lend it towrds monolithic applications. disadvantage in deployment, coupling, performance.
Agility - Response to change the multiple changes across the layers 
Deployment have to deploy the whole systems
Testing is easier as the other layers can be mocked
erformance and scalability are quite low 
Development is easier as devsknow about the pattern and are farmiliar with it.  It also fits with the skill set 
Complexity is low as people are used to this architecutre
Tightly coupled.


#Event Driven

#Microkernal

#Microservices
Avoid orchestration because once you start implementhing this you will end up with an unintentional SOA
Agile and enables continuous delivery
Scalable
Easier to test and Develop

But can be very complex
Loosly Coupled
#Service Orientated Architecture

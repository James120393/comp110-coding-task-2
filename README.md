# comp110-coding-task-2

This is the repository for COMP110 Coding Task 2.

##What is AI Architecture?
###The Definition of AI.
Computational intelligence is the study of the design of intelligent agents. An agent is something that acts in an environment—it does something. Agents include worms, dogs, thermostats, airplanes, humans, organizations, and society. An intelligent agent is a system that acts intelligently: What it does is appropriate for its circumstances and its goal, it is ﬂexible to changing environments and changing goals, it learns from experience, and it makes appropriate choices given perceptual limitations and ﬁnite computation. The central scientiﬁc goal of computational intelligence is to understand the principles that make intelligent behavior possible, in natural or artiﬁcial systems. The main hypothesis is that reasoning is computation. The central engineering goal is to specify methods for the design of useful, intelligent artifacts.

[Computational Intelligence and Knowledge] (http://people.cs.ubc.ca/~poole/ci/ch1.pdf)

##User Stories
* As a user I need the NPC to react to seeing a player.

* As a user I need the NPC to learn from this and change its behaviour accordingly.

##Which game I will Implement the AI into.
I will be implementing an AI system into out COMP150 game.

##What I will create.
I will be taking on the aspect of learning from experience, the NPC will see something react to it and learn from it. 
When the NPC sees the player it will give chase, one of two things can happen:-

* The player is caught thus a game over is displayed END.

Or

* The Player gets away, this will cause the NPC to go into high alert and revisit the two places where the player was seen and got away more frequently.

Possible stretch goal will be if the player is seen again the NPC will anticipate where the player is going and will try to head there first unless the player goes in a completely new direction.


##Pseudocode for NPC AI

**While (false)** player is not in sight do

        Patrol

        **If** player in sight

		Return true

        **End if**
 
**If** (True) player is in sight do

	Follow player

	**For** each NPC following player do

		**If** NPC is doctor and player has weapon
			Doctor to run

		**Else** if NPC is doctor and catches player
			Player dies and effect is placed
               **End if**

		**If** NPC is guard and catches player
			Player dies

		**End if**

	**End for**

	**If** player goes through door

		Return False

**End while**

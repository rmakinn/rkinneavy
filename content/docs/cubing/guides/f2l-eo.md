---
title: "F2L Edge Orientation"
tags:
- tutorial
- cube
---

Originally posted at [Speedsolving](https://www.speedsolving.com/threads/f2l-edge-orientation-guide.25525/) on 2010-11-15

# F2L Edge-Orientation Tutorial [v1]

{{< hint info >}}
Reading through this again, I'm have some exciting ideas about how to improve the content and presentation 🤓
{{< /hint >}}


A bit like the last thread I made, this guide is going to be text-based and the thinking behind each solve will be more complicated than that which anybody does in a normal speedsolve.

The basic idea of this post is to teach you how to recognise the orientation of f2l edges and also how to effect them so that you can reduce the number of rotations in your solves.
It's actually possible to reduce your f2l rotation average to less than one using this and with quite a few extra tricks (Breandan Vallance's old style is an extreme example).

Scramble WCA (green front, white top) and we're following cross on yellow (deal with it):

Example 1: L R' D R2 U L' B F2 R2 L D' U L' R' U2 R' D B R2 L2 D R2 U B2 U'
Cross: y F L' D L F D2

Here we recognise the orientation of the f2l edges:
First, know/check the colour of the centre pieces on L/R.
Second, look at each f2l edge - the important sticker on each is the one that matches one of the L/R centre pieces.

If this important sticker is either on the U layer orbit (that is, in any of FU, RU, BU, LU positions),
OR
on the L/R face (RU, RF, RB and the mirror),

then it's 'correct' - that is, you can solve the pair it belongs to with with just <L, U, R> moves.

If it's the inverse of these rules - on the U face or on the R orbit - then it's going to require a rotation, a fancy trick, or turns using the F or B faces.

So we apply this to the scramble so far. Since we already rotated before cross, the 'important stickers' for the f2l edges are the green/blue ones. We then check their orientation in relation to the rules we outlined earlier -
BL edge: correct since the sticker is on the L face
FL edge: " "
UL edge: " "
UR edge: incorrect, since the important sticker (here it's green) is on the U face.

And thus the UR edge is a problem we have to consider...

The interesting thing about EO is that we can now do a few different approaches:

Option 1 - flip the bad edge and gogo EOCross style:

U R' F R F' (orients the 'bad' edge and doesn't affect any other f2l edges)
U R' U2 R U' R' U R
R L' U2 R' U L (funky but relatively pointless trick)
U' L U L' U2 L U L'

Option 2 - solve the oriented pairs until you have to rotate (or until it's best to):

U2 R U' R' U R' U' R
L U L' U2 L U L'
y' - here we can rotate because the blue/red sticker in FL can also be solved in <R, U, L> post-rotation - if you don't know, work out why.
R U R2' U' R
U R U R'

Option 3 - abuse some more edge orientation/rotation rules:

Here we can add some more rules to our repertoire -
a) if a 'good' edge is in the U layer, a rotation will make it 'bad'.
b) if a 'bad' edge is in the U layer, a rotation will make it 'good'.
c) if either are in a slot, a rotation will not affect it's orientation.

Knowing this, we can rotate much earlier on:

U2 R U' R' U R' U' R (solving the only good edge on the U layer)
y' L' U L U2 L' U L (the other good edges are in slots, the bad edge in the U layer still)
R U' R' U R U' R'
U' R U2 R2' U' R2 U' R'

.

All of the above are viable, it really just depends on the scramble.

One thing to be aware of however - nobody properly using ZZ does EOCross - the average optimal f2l movecount is boosted from something like 27 to 36.
For this reason be careful of how you approach f2l EO - don't go crazy and effect it all the time - although getting fewer rotations is nice, beware of the fact you can seriously increase your movecount.


Another little interesting thing:
If a good edge is in a slot in it's correct layer, then it can be solved <R, U, L> regardless of rotations, since in either case it's 'important sticker' is correct relative to whichever centre you care about.
Using this knowledge, we can change our f2l very slightly to create these kind of situations more often than we would otherwise, and thus be free to use our rotations for more positive ends. *

Now I really have to go back to the work I was avoiding but I'll post plenty more examples later on today (I will update with a few more examples in my older f2l thread at the same time).

For anybody wanting to learn more about EO and EO detection visit Conrad Rider's site here. You can also learn a bit more about reducing the cube to move groups by reading parts of Mackys 3OP guide.
I strongly recommend Fridrich users to investigate the different steps of at least each main method (ZZ, Petrus, Roux) if not the more obscure ones (Heise, Waterman etc).
The more you understand blockbuilding, edge orientation, different LL methods etc etc the more you understand your own f2l.

Don't ever forget that Fridrich f2l is really blockbuilding with varying degrees of restriction - NOT just dumb pairs -and can be as advanced as you make it.


Hope this is clear and helps someone; all feedback is welcome,

Rowan.

*One great thing that can be done with EO tricks is using keyhole techniques to throw out bad edges and/or put in good edges, so you can preserve or change their orientation after a rotation. Play around with the form: (<D>) (<R, U>/<L, U>) (<D>)' and see what kind of stuff you can come up with 

---
title: "F2L Lookahead"
tags:
- tutorial
- cube
---

Originally posted at [Speedsolving](https://www.speedsolving.com/threads/f2l-and-lookahead-guide-example-solves-not-a-video.24952/) on 2010-10-21

# F2L Lookahead Tutorial [v1]

{{< hint info >}}
Some of the examples in here are great, but man, if only I had access to a decent camcorder at that time! It's easy to see why YouTube made cubing so popular if useful information was trapped in texts like this

Another one where a few modifications and online tools would make this much more pleasant to read
{{< /hint >}}


So I've been thinking of making something like this for ages and now I have to actually do some work here it is.

For brevity's sake a couple of these solves will not be my normal approach and include way more tricks, but I'll make sure a couple are genuine speedsolves.

Most of these tricks are things I've intuited, but any multislotting guides you can find and advanced f2l pages will probably have similar or the same algs.

solve 1:
(scramble WCA position)
L2 D2 R' L' F' D L2 R' D B' L2 D' B R F2 L2 D2 R2 L2 D B R2 L' F' B

Upon inspection I'm basically looking at either white or yellow and quickly checking which is better (I haven't thought or codified how I check, I just do it...), planning a safety cross (in this case D' L' D L' D2 y' U R' F R), then either looking ahead into f2l (I'll describe that process next solve), or planning an x-cross, OR creating/preserving a free pair in the U layer. At the same time as all this, I'm thinking about the moves I'm going to do and which angle they would be fastest from.

The cross in this case is D' U2 L' D' R2 U u' L u.

The U2 at the beginning connects that f2l pair, and the U means that it will end up in a relatively easy to solve position. Since I've noticed that orange/blue corner in DR, I can look around the rest of the cube for the orange/blue edge - which is revealed by that u' cross move.

Next I'll do L R2 U' L2 U L to solve both pairs. This trick combines the effects of L U' L2 U L (which inserts whatever is in the UB position), and just doing a simple R2 to join up the orange/blue pair. My favourite thing about this is that with just 2 extra moves (R2 (x) R2) you solve a case that would take at least 6 with the normal approach, and that the f2l alg for the BL pair returns the cross edge to it's correct position without any extra AUF.

I'll next do R U' R to free up that green/red pair, luckily the next pair cancels with it (though I probably wouldn't notice it and do it - it's just convenient for hand position). I'll insert it with a sledgehammer too; there are 3 misoriented LL edges and orienting them increases the chance of an OLL skip. So: R' U' R2 x' U' R' U x

Then a 3 move Winter Variation case, plus I notice that block in UFR that will be preserved - it will be any of a V, J or A perm. In this case you can actually predict it will be a V or A (but I wouldn't in a speedsolve) because this case joins up the misoriented U layer corner with the block, in UBL, and since the sticker is blue and the UR edge is green it's thus placed diagonally from it's home position.

So, U2 y L' U L. It's a V perm - U (pushing with LH index on LBU to save using the RH index and let it get into position for the R' U R') etc etc.

full solve:
L2 D2 R' L' F' D L2 R' D B' L2 D' B R F2 L2 D2 R2 L2 D B R2 L' F' B

D' U2 L' D' R2 U u' L u (9)
L R2 U' L2 U L (6|15)
R U' R (3|18) (this could cancel - R U2 R2 x' U' R' U, giving a 25 move f2l & 40 move speedsolve)
R' U' R2 x' U' R' U x (6|24)
U2 y L' U L (4|28)

U R' U R' Dw' R' F' R2 U' R' U R' F R F (15|43)

So, a pretty good solve. Whether I would do this in a speedsolve depends on how much I'm warmed up and what cube I'm using; with a very high tps I'd probably do something more standard.

Solve 2:

B' R2 D L2 U2 L' F2 U B F2 D B L' D' B2 L B F2 U2 F2 B D2 F' R' U2

A cruel scramble on inspection.

Cross: y2 x U' R F' U R2 D x'

Notice how the order of putting cross edges in affects stuff: I could just have easily done U' R F D' U R2 and broken up that pair... Usually on this kind of cross I would never bother with looking ahead, it's just not that nice.

Since I know that pair is going to be there I can ignore it for the moment. While executing my cross I notice that the orange/blue edge is in a slot and flipped. I'll know to try and change the rest of my f2l slightly so that the corresponding corner ends up in a better position, perhaps in UBL. The corner appears after that R2 so I can go straight into it after the orange/green pair.

R U' R2 U R. Now I'm presented with a hell of a lot of options - I can either insert the made pair, or join up the red/green with four moves preserving the made pair (but 'generating' two rotations) or just carry on with what I saw earlier.

The first option is probably the best in this scenario - we can insert the made pair using F' L F L' to kick out the edge that is stuck in the FL slot (and also avoid a rotation for this particular slot), and we might be able to do something fun with the next two pairs if it's freed up. So we do:
U2 F' L F L'.

This has left us with a nice 3 move insert in FR slot (albeit with a rotation), but at the same time if you look ahead you'll see that this will leave us with a bad f2l case for the green/red pair (joined up but edge flipped), and it would be especially bad in this case since the nicest way to execute the usual alg for it (R' U2 R2 U R2 U R) is another rotation again after the 3rd pair.

So instead we use a trick from multislotting:
y' L' R' U' R
and then to setup a nice little 3 move case we insert an extra U' in there to move around the corner, and then we rotate again and insert:

(y' L' R' U' R) U' L y' U2 R U R'

And f2l is done! Luckily we've also oriented edges, which we wouldn't have using a more normal approach.

Complete f2l:

B' R2 D L2 U2 L' F2 U B F2 D B L' D' B2 L B F2 U2 F2 B D2 F' R' U2

y2 x U' R F' U R2 D x' (6)
R U' R2' U R (5|11)
U2 F' L F L' (5|16)
y' L' R' U' R U' L (5|21)
y' U2 R U R' (4|25)

(LL is 18 moves inc AUF - 43 move solve)

Solve 3:
Scramble: L' R' U2 F B D U2 R B' U' L2 R' U2 D' R' D' L' U' F' R2 D' F' L D B'

Okay, so on this scramble I notice that if I do y2 L then I'll join a pair, so I'll try to change my cross about a bit to accomodate it.

cross: y2 L F R' D U' L* B' U R'
*at this point I notice the corresponding edge for the green/orange corner is at UB - and I know that by doing that 2nd to last cross edge it will be oriented nicely in relation to it's corner, and that by doing that extra U turn I can set up a 3 mover...

Now the situation is irritating - it looks like it has potential but I really can't see anything to solve both the BR and FR pairs at once. The best I'll do is make sure that when the orange/blue pair gets taken out it also gets broken up; I can use a nice little trick to do this:
y L R U' R' U L'

then an easy 3 move insert (that was quite predictable during that trick):
U' L' U' L

And then a cool, kinda intuitive alg for the last pair: U2 R2 U2 R U R' U R2, then a 6 move OLL and G perm (20 moves in total inc AUF).

So all together:
L' R' U2 F B D U2 R B' U' L2 R' U2 D' R' D' L' U' F' R2 D' F' L D B'

y2 L F R' D U' L B' U R' (9)
y L R U' R' U L' (5|14)
U' L' U' L (4|18)
U2 R2 U2 R U R' U R2 (8|26)

(46 move solve)

I actually have to go and do some work now - but I will edit more solves in later, along with stuff on pair prediction and making extended crosses - I just wanted to get this started and posted so that I actually would do it.

Hopefully this will inspire you to play with Fridrich f2l a bit more and see that it isn't just one spammy alg after another at all...

As soon as I can, which unfortunately will probably be around xmas, I'll make a video (plural if I cba) with more of this sort of stuff in - it's a bit easier to follow than this behemoth.

Cheers,
Rowan.

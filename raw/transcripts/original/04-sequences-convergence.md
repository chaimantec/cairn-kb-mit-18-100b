---
title: Lecture 4: Sequences; Convergence
lecture: 4
video: https://www.youtube.com/watch?v=PzeCGelnheE
source: verbatim YouTube transcript
---

# Lecture 4: Sequences; Convergence — transcript

Verbatim captions as published with the MIT OpenCourseWare video (professionally transcribed and punctuated, with speaker labels), grouped into paragraphs. Timestamps mark the start of each paragraph.

**[0:00]** [SQUEAKING] [RUSTLING] [CLICKING] TOBIAS COLDING: OK. So last time, we talked about at towards the end, we talked about sequences. And so in particular, we talked about square root of 2 by 2 square root of 2. We could think about this if we wanted to think about the square root of 2 on the real line. Then we have here 1 and we have two. And we could define a sequence of numbers where the first one is 1, the second one is 1.4, the third is a 1.4.1,

**[0:55]** and the next one is then the next digit in square root of 2, so 1.4.1.4, et cetera. And so this is like a sequence of numbers that are increasing. And it is square root of 2 where you're taking more and more digits. So square root of 2 is, in some sense, the limit of the sequence. And so precisely, a sequence is--

**[1:43]** so we talked about that last time. But let me just remind you what that is. So a sequence is a function from the natural numbers-- so f goes from the natural numbers into the real. And the value at some natural number n-- the value of this function at a natural number n. This we denote-- usually, it's a standard notation that one denoted like this where the n is a subscript. OK.

**[2:28]** And so let's take a look at a couple of different sequences. So we talked-- so this here really is a sequence. Another example is where you have a n equal to minus 1 to the power n. So n again is this natural number. So this means that this sequence a1 is equal to minus 1, a2 is equal to minus 1 times minus 1, so that's one. a3 is minus 1 times minus 1 times minus 1. So this is minus 1.

**[3:13]** And a4 is minus 1 multiplied itself four 4 So that's 1. Right. So this sequence here, it's alternating between the values minus 1 and 1. So it's starting off at minus 1. And then it goes to 1. Then it goes to minus 1, 1, minus 1, et cetera. OK. And so this sequence here, right, it doesn't really-- it's not-- it doesn't really convert. It's not-- it doesn't really have a limit.

**[3:58]** So this here-- we'll make this precise in just a minute. So this sequence does not have a limit. Another an example of a sequence is a decaying sequence like this. So a n is equal to 1 over n. So a1 is equal to 1, a2 is equal to 1/2, a3 is equal to 1/2, and then a4 is equal to 1/4. So these numbers here are all positive. Right? The values of a is all-- all of them are all positive.

**[4:45]** And they become smaller and smaller. So you could write that suggestively. This here is going down like that. And so it seems obvious that this limit here-- that this sequence has a limit. This here has a limit. And the limit is 0. So now let me make the formal definition. So what does it mean that a sequence is convergent?

**[5:30]** So a sequence. a n is convergent to a. So a is another real number. A sequence a n is convergent to a if the following is the case-- if the following holds. For all epsilon-- for all epsilon greater than 0,

**[6:24]** there exists a natural number such that if little n is bigger than this natural number, then the difference between a n and the supposed limit is bounded by epsilon. So if you think about it-- so if you think about it, here you have on the real line here you have a. And so if you give me an epsilon, so then I'm looking at a here. I'm looking at an interval around a.

**[7:11]** So this is an interval here from a minus epsilon to a plus epsilon. And the claim is that the sequence a n is converging to a if there exists some n so that if little n is larger than this capital N, then all of these a n lands somewhere here. All of them a n is in this little interval for little n bigger than this capital N. Right? That's what it means to be convergent. But it's like for all epsilon. So you allow to-- someone else is allowed to pick the epsilon.

**[7:59]** And then you have to prove that there exists a capital N so that from there on and out, all of the a n lie in this little interval. So this is what it means for a sequence to be convergent. So we say that a n is convergent to a if this is the case. And in that case-- in that case, one also writes that the limit as n goes to infinity of a n is equal to a.

**[8:46]** So if you have a sequence a sequence that is not convergent, it is said to be divergent. And so now let me look at an example. So suppose you're looking at the number 0.99999, et cetera. This number here, this is really--

**[9:35]** this number here, we will think about this number here as 1. This is indistinguishable from 1. And in fact, what you really think about is that you think about that you have a sequence where a1 is 0.9, a2 is 0.99, a3 is 0.999, a4 is equal to 0.9999, et cetera. So a n is where you have zero point and then 9 n times.

**[10:31]** If you're looking at that sequence here, then you have that this sequence a n is convergent to 1. And a n-- this is one also that is convergent to 1 like this. So a n is convergent to 1. Right? So there's various ways of writing that it's convergent. You can write it like this. This means that it's convergent. And the limit is a. You can write it like this. This means that this sequence is convergent and the limit is 1. Or you can write it out in words.

**[11:20]** So this sequence-- I claim that this sequence here defined like this. And this is really how you think about this. When you think about this number, you think about it that this is 0.99 with more and more numbers, nines, added and the limits, which is really what this number here in itself is is 1. Now let me explain why the sequence defined this way, why this is convergent as a limit 1. So now, of course, now you give me an epsilon.

**[12:07]** So given epsilon given epsilon greater than 0, then I need to find a capital N So that from there on and out the An a n within epsilon. So we need to find-- for this epsilon, we need to find capital N so that if little n is bigger than this capital N, then a n minus 1 is less than epsilon. That's what we need to do. Right? But for your epsilon, so to do that, we need to choose this capital N.

**[12:54]** So I'm just choosing-- I just choose capital N. So to do that, choose capital N such that 1 over n is less than epsilon. Right? We can do this by the Archimedean property. So this is-- so we can find such an m and capital N by the Archimedean property that we discussed last time.

**[13:48]** But now you see if you're looking at-- if take-- if you now look at little n that is bigger than capital N, then you have that 1 minus a n. Well, 1 minus a n, actually, for all n, this here is less than 1/10 to the power n because if n is equal to 1, this here, this is within 1/10 of one.

**[14:36]** And likewise, this here is in 1/100 of 1, et cetera. So we have this inequality. It's actually equality in this case. This here is an equality. But now you see that this thing here, this is obviously 1/10 to the power n is less than or equal to-- is less than 1 over n. And so if little n is bigger than capital N, this is therefore less than 1 over capital N. But this is less than epsilon. And that's what we need to prove. Right? So for the given, for your given epsilon,

**[15:23]** I specify a capital N. And then we need to prove that if little n is bigger than our capital N, then we come within epsilon of the limit. OK? Now let me prove a little theorem about convergence sequences. And this is like, if you will, this little Lemma is like the first test for whether a sequence is convergent. So theorem.

**[16:13]** If a n is a convergent sequence, then a n is bounded. Sorry. Let me explain what I mean by that. I mean that then the set of a n-- so let me just explain that. So then the set a1, a2, a3, et cetera, this set here

**[17:00]** is bounded. It's not enough to be bounded to be convergent but it is a necessary criterion. Let me, just as a side remark, say that if you're looking at the sequence a n that we looked at just a minute ago, this here that is alternating between minus 1 and 1, this is a bounded sequence because the value-- there's only two values. So it's obviously bounded but it's not convergent. But it is a necessary for a sequence to be convergent.

**[17:47]** It's necessary that the sequence of numbers here is bounded. So now let's try to prove that. So we have-- so since a n is convergent, then there is some a so that a n converges to this a. Right. And so now I can just focus on one single epsilon. So in particular, if we choose epsilon to be equal to 1,

**[18:53]** then there exist capital N so that if little n is bigger than this capital N, then a little n minus a is less than 1. This is there is convergence just applied to this single epsilon. Right? OK. So this is the first observation. The second observation is that if we now look at all the a n that are not considered here-- so if you're looking at the set, this is the first a capital N minus 1 a n.

**[19:46]** Right. Those are the ones that doesn't fall in under, that this little n is bigger than the capital N. So this set here is finite. So obviously, so for any finite set, you have that so they exist c, a real number such that a n is less than or equal to c for any of these guys, for any a in this, any a n in this finite set.

**[20:43]** In other words, this means that a n is less than or equal to c if n here is between 1 and n minus 1. So now I look at-- so now I look at-- now I want to look at the numbers a n and this number here. And I want to look at-- so I'm thinking about the set a n absolute value and where in here is one of two, 1, 2, cetera.

**[21:33]** Well, I claim that this thing here, I can now prove that this set here is bounded. And this is just because that the first n minus 1, those are bounded by c. So I claim that this set here-- so claim. So that's the sup of this set where n from 1 right over all n's. The sup of this set is less than or equal to the max

**[22:22]** of c and a plus normal, absolute value of a plus 1. So I claim that. Now this is clearly, if you're taking the first n minus 1, then we already know that they are bounded by c. So you just need to worry about the one starting at capital N. Right? So we only need to worry about when. So this is obviously the case for the first capital N minus 1. So we only need to worry about-- only need to show this for little n

**[23:15]** larger than capital N. Larger. Yeah. AUDIENCE: Can you explain in the max over there why there's the absolute value of a plus-- like, the plus 1? TOBIAS COLDING: Yeah. I will explain this. And I'll get to this. This is part of the proof. Yeah. So it hopefully will be clear in a minute. If it's not, you should complain. So I only need to prove that when I'm just looking at the set here. And I'm starting at capital N, then the sup is bounded like that. And so then I-- so I'm looking at a n. But a n I can write as a n. I can write in a stupid way I can write a n as a n minus a plus a.

**[24:06]** Right. So I can write it like that. And then I can just-- right. So I have the sum of two things. The absolute value is less than the absolute value-- the sum of the absolute values. So I have this. Right. But now you see that since little n is bigger than this capital N, this capital N was chosen so that this here was bounded by 1. So this thing here is less than 1. And this here is less than the absolute value of a. Right. And so we have for the whole tail starting at capital N, we have that this thing here is bounded by 1

**[24:53]** plus the absolute value of a. And for the remaining capital N minus 1, those are bounded by C. And so together, all of this is bounded by the maximum of these two things. OK. Now the next thing I want to talk about is some sort of algebraic property of limits that is often very useful. And I will prove-- there's four of these. And I will prove two of them. And the other one I will outline the proof of.

**[25:43]** AUDIENCE: [INAUDIBLE], professor. TOBIAS COLDING: Yep. AUDIENCE: So in that the claim was that the sup is-- the sup is less than. So we don't need to-- TOBIAS COLDING: Yeah. No. You don't need to actually find the sup. Right? Yeah. And the reason I want to write sup and not maximum is that, of course, if it's infinite numbers, it's not clear there is a maximum. So we need to use the terminology sup. So that max of C and S a plus 1 is not the sup. No no that's right. It's a bound for the sup. But the sup presumably is less. AUDIENCE: And one that really is just epsilon. TOBIAS COLDING: And the one really, to some extent, could be almost anything.

**[26:28]** Yeah. It came from the epsilon. But you see if you made that epsilon smaller then probably the c would jump up because that is-- right. Because the c was the maximum of the first n minus 1. So if you are further out, then there are more numbers that you're taking the maximum over. So anyway. Yeah. OK. So we want to prove some algebraic properties. Of limits.

**[27:14]** So the idea is that we take-- so we have four of these. And the first one is that you take a sequence. So maybe I'll just say throughout a n and bn are sequences. And a n is convergent to a and bn is convergent to b. The first one, the first property is that if you take a real number-- sorry. If you take a real number-- c here is a real number-- and you form a new sequence where

**[28:00]** CN is just this real number times a n so each cn is somehow almost like a n except that they're multiplied by this fixed constant c. So this here-- so the first one is that cn is also convergent. And the limit is just c times a. OK. The second one is that if you take-- if you define a sequence-- so this is a different sequence than this one. But if you define a sequence cn by its a n, the n-th element

**[28:46]** is a n plus bn, then this sequence is also convergent. cn is convergent and the limit is a plus b. So that was the second property. The third property is-- the third property is that if you take a product. Sorry. So if you take a n-- if you define cn as a n times bn-- so this is a new sequence.

**[29:33]** Then cn is convergent and the limit is a times b. And the last property is that if the a n are-- all of these are different from 0. So this here is for all n. And also you have that the limit here is not equal to 0. Then if you define a sequence to be 1 over a n, then cn here converge and the limit is 1 over n.

**[30:25]** And so I will prove rigorously the first two. And I will basically tell you how to prove the other two. But the first two I will write out formally, as we talked about last time, how you write a formal proof, whereas what I'm going to discuss for three and four is very, very close to a formal proof but it's more like what you would have on a piece of scrap paper.

**[31:10]** So now let's prove the first one. So proof of one. So given epsilon greater than 0-- so yeah. So first of all, of course, if this capital C-- if this capital C is 0, then everything is 0. So it's trivially the case. So we may as well assume. So may as well assume that capital C--

**[32:03]** that capital C is not 0. So now, given epsilon greater than 0, since this sequence a n is converging to a, this means that there exists n such that-- and now I'm not going to use that epsilon. You gave me that epsilon. I'm not going to use that epsilon in the definition that a n is converging to a. I'm not going to use that one, but I'm going to use one that is closely related. I'm going to use epsilon divided by the norm of z because that's another positive.

**[32:50]** So you gave me an epsilon. I'm going to look at this number here. That's a positive number. And I can use that in the definition that a n converges to a. So I'm going to say that because an converts to a, there exists a capital N such that if little n is bigger than this capital N, then a n minus a is less than epsilon over capital S-- or C, sorry, capital C, a normal capital C. But now I just multiply on both sides.

**[33:35]** So multiply by the absolute value of capital C on both sides. And so if we do that, then this here pops in. Right? It actually goes in as c times a n minus c times a is less than epsilon. And this is as long as this n is-- little n is bigger than that capital N. This is exactly what we wanted to prove. OK. Now the second one is--

**[34:33]** so the reason why I'm doing the first two-- you see that those are pretty straightforward. I mean, it's not like any of these is complicated to prove. The next two is a little bit more-- I mean, I wouldn't say complicated but a little bit more involved, these two. But I want to give you the idea because it's kind of a very simple but useful idea in these two. So I don't want to skip the proof. So we want to approve of the second property.

**[35:27]** So we have that a n is converging to a and bn is converging to b. And so again, you give me an epsilon that I have to work with. So given epsilon-- given epsilon greater than zero, then I'm going to not again use this epsilon in the definition that a n converge to a. And I'm not going to use it in the definition that bn is converging to b, but I'm going to use epsilon over 2 in each of them. So since a n converts to a, there exists a capital N--

**[36:17]** and let me call it capital N subscript a-- such that if little n is bigger than this capital N subscript a, then a n minus a is less than epsilon over 2. Right? Likewise, since being converted to b, then

**[37:16]** there exists a capital N, but denoted by this, it may be different than the one coming from the sequence a n such that if little n is bigger than this capital N subscript b, then bn minus b is smaller than epsilon over 2. And so now I have to choose. So you gave me the epsilon. And I have to choose a capital N. I haven't chosen that yet but I will do that now. So set capital N equal to the maximum of these two N's.

**[38:08]** So you're setting it equal to the maximum of these two. Now if little n-- so then for little n bigger than this capital N, if you're looking at a-- so now we want to look at-- so our sequence cn was the sum of these two. so this here was cn. So we want to prove that-- so we want to look at cn minus a times b. And we want to prove that if little n is bigger than this, then this here is strictly less than epsilon. But this thing here is cn was, by definition, a n plus bn.

**[38:54]** Sorry. And this was not the product. It was the sum. Minus a plus b. But this thing here you can write as a n minus a plus bn minus b. And now you can just take the absolute value of this. It's bounded by the absolute value of the first. So plus the absolute value of this thing.

**[39:45]** And now you see that if little a-- let me keep-- so if little a-- sorry. If little n-- since little n is bigger than capital N, which is bigger than capital N of a, in particular, then this thing here is less than epsilon over 2. So you have that cn minus a plus b is less than epsilon over 2 that comes from this. But you also have that capital N is bigger or equal to n sub b.

**[40:34]** So you also have that this thing here is less than epsilon over 2. Right? So you have that this thing here with little a is big N-- is bigger than this capital N. This thing here, this difference is strictly less than epsilon. That's what we needed to prove in order to prove that the sequence that was the sum of the two sequences converging to the sum of the limits. Yeah. AUDIENCE: We initially defined the n minus [? e ?] or n minus a be less than epsilon over 2. What was the justification for why we would say if we know that the n converge to be within? TOBIAS COLDING: Right. That's right. So because a n or bn, because they converge.

**[41:21]** So let's say a n converges to a. Right. Then for all epsilon, you gave me the epsilon. And I'm using that it's converging not just for that choice of epsilon but also even for epsilon over 2. That epsilon, you gave me the epsilon. Then I'm using that it's converging. So I will have to choose probably an n that is much larger if I'm using epsilon over 2 than if I use directly the epsilon. AUDIENCE: So I'd assume that it increases like epsilon gets smaller. TOBIAS COLDING: As epsilon gets smaller, presumably you need to choose capital N larger. AUDIENCE: OK. So you couldn't run into a case where we're assuming a convergence is like smooth as opposed

**[42:08]** to oscillating about a point? TOBIAS COLDING: Right. That's right. I mean, so-- but I'm using that for-- I'm basically using that for all epsilon, that it wasn't just for a fixed epsilon. And so that's why, when you came to this epsilon, then I'm actually using it for epsilon over 2. Yeah. OK. So that was the first two properties. It's not like the other one is super difficult. But those two are the most straightforward. Let's look at the other two. And so in particular, because it's like, for the next one, there's a little trick that is useful

**[42:56]** in various different settings. And so prove-- but the next two I will just outline. OK. So proof of 3 so outline. So we need to look at a n times bn. Right? So cn is a n times bn. And we want to compare cn with a times b. We want to show that this thing here, if little n is

**[43:44]** sufficiently large-- so given an epsilon, if little n is sufficiently large, then this difference is bounded by epsilon. But this thing here is anbn minus a b. OK. And so the little trick is now that, in itself, it's kind of difficult to compare these two things. But the little trick is that if you're looking at anbn, if you're sort of-- instead of comparing them directly, then comparing this with something that is halfway between this and that, then it gets a lot easier.

**[44:30]** So what you do is you're looking at anbn, and you subtract a and b, and then you add it immediately again. So this is certainly the same. And now I can write this thing here as a n. I can just concentrate on these two first. And then I can factor out a n. So I can write that as this. And this thing here I can factor out a b. So I can write it like that.

**[45:16]** And now you see this. It looks much more promising. This one looks like the problematic one. This one looks like no problem at all because this is just some fixed constant times this difference here. This one looks a little bit more problematic because it's not a fixed constant. But we can deal with this in just a second. But the first thing I can do is I just take the absolute value of this plus the absolute value of that. And now I just take-- so then this here is actually the same for a product. You can just take the product of the absolute value.

**[46:04]** It's the same. Now the next thing is that we're going to use the theorem that we proved earlier that since this sequence here-- since these numbers here, all of these numbers for all, when you take the set--

**[46:51]** when you're looking at this set, since this set here is bounded-- and it's bounded because the sequence was convergent. And so we already proved that then the values, the set of values is a bounded set. Right. So it's bounded. And so we can assume-- so that exists C. So that's a n is the absolute value is bounded by the c.

**[47:38]** So now I have-- and so now I have that cn minus a times b. This is what I had up there. And I'm just using that. This is now bounded by just because these things here are bounded by c, I get cbn minus b plus b over a n minus a. Right. And now you see now it's going to follow like-- so this here was just some observations. Right? And now when you come to the proof, so to prove three, then given epsilon greater than 0,

**[48:34]** now we want to make sure that this thing here is less than epsilon over 2 and that this thing here is less than epsilon over 2. And so I don't want to get in trouble if this set was 0 or if this set was 0. So I'm just-- so given epsilon since a n converges to a, then I can find-- now I'm basically writing out the whole proof, but I can find capital An-- sorry-- capital Na so that if little n is bigger than capital Na, then you have that a n minus a is less than--

**[49:24]** I don't quite use that epsilon. And I don't quite use epsilon over 2, but I take absolute value. I multiply it like this because I don't want to have something where if b was was zero, then it really didn't make any sense what I wrote. So now there's no problem. It definitely makes sense even if b is 0. Likewise since bn converges to b, then there exists--

**[50:17]** so again, you gave me an epsilon. So there exists an nb such that if little n is bigger than nb, then actually you have that bn minus b is less than epsilon again over 2. And this is not quite what I use because I don't want to be in trouble that c-- c is already non-negative because it's bigger than this absolute value. But I'm just adding one for the same reason. And so now you see that if little n-- so therefore, if little n is bigger than the maximum of these two,

**[51:04]** then both of these inequalities hold. Right. Both of them hold. And so this means that you now have that cn minus a times b, this thing here. So we had it here. This is less than c. And then this difference here was now assumed to be epsilon over 2, 1 plus c. And likewise, this thing here is bounded by this number here times-- and then this thing here, so epsilon

**[51:53]** over 2 absolute value of b plus 1. OK. But now you see that this thing here, that c divided by 1 plus c, that's bounded by 1. Right. So this thing here is bounded by epsilon over 2. And this thing here, same reason is that this thing here is bounded by epsilon over 2. And so the whole thing was bounded by epsilon when little n was bigger than the maximum of these two. So in the end, I wrote out the whole proof. I already posted the lecture notes.

**[52:38]** In the lecture notes, I didn't write out the whole proof but I gave the idea. So I stopped once we were here and somewhere here after this one somewhere anyway. But you see. OK. Right. So the next thing I want to talk about is that if you-- No, no, I still need property four. And that's also useful. Sorry. So let's go through that and then we'll come to subsequences.

**[53:24]** So I want to prove that if you take a sequence of real numbers none of them is zero. They converge and the limit is not 0, then 1 over the sequence is another convergence sequence. But again, just the main takeaway. The main takeaway, I think, from property, this third property was that this little idea about inserting something that was halfway between the two things you were comparing because they weren't

**[54:10]** very easy to compare directly. And that's like a little trick that is useful in various places. It comes up almost the same thing. One place it comes up is what's called Leibniz rule that if you take two functions, and you take the product of these two functions, and you try to prove that one is the derivative of the product, it's exactly the same trick. And it comes up various other-- more fancy ways. So now let's look at-- let's prove property four. So property four. Proof of property four.

**[54:56]** So we have this. So cn is 1 over n. And we know that a n are not equal to 0. And we know that a is not equal to 0. This here makes sense. And also 1 over a makes sense. So we want to compare this here with 1 over a. And so this thing here is 1 over a n minus 1 over n And now I can put it on a common denominator. So this is a minus a n divided by a n times a so like that. You can write it like this.

**[55:42]** Now already the denominator looks very promising because we know that this goes to 0. Right. But now I need to bound this. So I need to bound-- Right. So I need to bound. We need to bound. So we want to bound this here by epsilon when little n is sufficiently large. The top, the [? nominator ?] here looks great. The denominator maybe we're a little bit worried about. But the thing is that-- so we need to bound a n times a, this here from below.

**[56:33]** But we want to bound it from below because then when you're looking at 1 over it, then that's an upper bound. And really, because a here is just a fixed number that is not 0, then it's equivalent to proving. So this is equivalent to bound the norm of a n from below. Remember, we don't need to bound it from below for all a n. But we need to bounded from below for n sufficiently large.

**[57:20]** And so now, you make the trivial observation. So that a n, you can write a n as a n minus a plus a. And so therefore, therefore, the norm of a n is bounded by the norm of a n minus a plus the norm of a. Sorry, this was not the-- this was not how I wanted to write it. I'm going to write it slightly differently. I'm going to write a. I'm going to do the symmetric thing.

**[58:05]** But I'm doing it-- so I'm writing a in as a minus-- so in writing a as a minus a n plus a n. And then, if I do that, then I can just take the absolute value of a is bounded by the absolute value of this difference plus the absolute value of a n. And now I can move this here over on the other side. So this here implies that norm of a minus the norm of a minus a n is less or equal to this here.

**[58:56]** And now, you see that this thing here is-- so now we're going to use that this here was not equal to 0. So this here is bounded away from 0. And so now we can take, say, a here over 2. So we can use this here. We can use norm of a over 2. This is a positive number because a was not 0. And we can use this in the definition of that a n-- so use this in the definition of that a n converges to a, right?

**[59:50]** So this means that if you are-- this means that there exists a capital N. Let's call it capital N1. It's not the final N that we want to use. But there exists a capital N1 so that if little n is bigger than this capital N1, then, actually, we have that a n-- a minus a n is less than this thing here. But now, you see that-- this means that when you're looking at-- when you go up here, and you're looking at--

**[1:00:36]** when you go up to that line before-- so this is the line from before. Sorry. This is minus this here-- this and this. When you're looking at this line here, well, this thing here-- this here is at most half of this. So this thing here is bigger than this thing here over 2. And so now you see that we have bounded these guys from below. And so now we go back up to-- so now we go back up to-- we're looking at C minus-- oh, sorry.

**[1:01:22]** We're looking at Cn minus 1 over a. This is this up here. I'm just transferring that equation down to this board here. So this here is a n, a, minus a n, divided by-- and I can just take the absolute value separately of the denominator-- and the denominator, a n times a. OK. So now you see that this thing here, as long as-- so when

**[1:02:08]** n here, little n, is bigger than N1, well, then we have that this thing here is at the very least the absolute value of a over 2. So this means that this thing here, we can now bound from above, like this. This is as long as you have this inequality here. And this thing here-- this is just a norm of a. This here will give you another norm of a over 2. So the 2 jumps up. So it's like this thing here. And now you see that--

**[1:02:53]** now you see that this a is just like a constant. So this means that I may have to go even further out than N1. But if I go even further out, then I can make this thing here smaller than a given epsilon, OK? All right. So this was like the outline, if you will. But that's not-- at this point, that's not very much to fill in. OK. So now I want to talk about subsequences.

**[1:03:38]** And then I want to-- then I want to prove a little theorem about subsequences. So I have a sequence. And so I have a sequence and then a subsequence. So I'll give you first some examples. And then I will explain. Then I will give you the proper definition of what a subsequence is. So I'll start with this sequence from before.

**[1:04:28]** So this was the sequence where a1 was minus 1, a2 was 1, a3 was minus 1. It was alternating between minus 1 and 1. And so, in this case here-- in this case here, if you take the sequence-- let's call it-- let's call it b. Let's call it-- let's use a different index. Let's call it bk. So k here plays the same role as n before. But I want to use a different symbol to not somehow confuse with the n over here. So if I take--

**[1:05:15]** so I could take a sequence that was like 1 all the time, this here, for all k. This here would be a subsequence. This would correspond to that you took all the even ones, that you just take all the even ones. So this is like a subsequence. You could also have another example. So this is example 1. Another example is where you took all the odd ones. So this here is also a subsequence. And you could do something more elaborate, where you take-- say, first, you take the first two odd,

**[1:06:05]** and then you take the next two even. So you could have a sequence that was like b1 is equal to minus 1. b2 is equal to minus 1. b3-- now it becomes the next two even ones. And then you go back to the next two odd ones, et cetera. That would be another subsequence. Let me look at a few more examples. So, for instance, if your sequence,

**[1:06:53]** your original sequence-- so here's another example. If your original sequence was just that a n was equal to n, then you could take a sequence. So then the sequence where you just take the odd numbers, this here is a subsequence. And likewise, if you take just the even numbers, this is also a sequence, a subsequence. But if you're looking at--

**[1:07:40]** if you look at, say, something like this, where you're taking-- so if you define a sequence where it was 1, 1-- 1, 1, 2, even like this-- this here is not a subsequence. This is not a subsequence, because you have-- what you have done here is that you have taken the same number several times. And it doesn't appear several times. The value doesn't appear several times in the original one. So that's not allowed. It's also not allowed to do something like this.

**[1:08:28]** This here is also not a-- so not a subsequence, another thing that's not a subsequence-- when you take things out of order. So if this here was the original sequence, if you're now looking at a sequence that was 3, 2, and then 4, 5, this here is-- et cetera-- this here is not a subsequence either, because things are taken out of order. So now, what is the formal definition of a subsequence? So here is a formal definition.

**[1:09:30]** So you have a sequence, a n. A subsequence of a n is where you have a map, g, from N into N. This is an increasing map. This is strictly increasing. And then, if you're thinking about this thing here, you think about this as a function, f, then you now could think about the composition of these two

**[1:10:15]** functions, so this thing here. And maybe I will use a different notation like this, a different index like this. This thing here, bk, this here is a subsequence. So you see that this here, when you pick-- if you have a sequence like this, the first one could be anything in the original one. But once you have fixed the first one, you can't look back, or you can't go to this. You have to-- the next element have to be somewhat further out in the sequence. And that continues.

**[1:11:01]** And this here is often just to indicate that it's a subsequence of this sequence. Then the standard notation is a n and then another subscript. So anyway, so of course, hopefully, there's not too many subsequences of sequences, because each time, it's supposed to be another subscript. Now, there's a little theorem that we can just prove here at the end. And that is that if you-- and it's-- yeah, it's sometimes-- it's a very simple fact. But it is sometimes a useful fact. And that is that if you take a sequence--

**[1:11:48]** so a sequence-- so theorem, that-- so a sequence, a n, is convergent to a if and only if all subsequences of a n converge to a.

**[1:12:37]** OK. Now, to prove this, there's two things we need to prove, because it's an "if and only if" statement. So we need to prove that if it is convergent, then all subsequences are also convergent. And then we need to prove that if all subsequences are convergent, then the original sequence is convergent. But one of the two implications is trivial. So one of the two implications is trivial. And that is that, namely, since--

**[1:13:25]** so the map-- remember that the map to define a subsequence has to be strictly increasing. So remember that a sequence was a function like this. That was a sequence. And a subsequence-- there, you have another map that is strictly increasing. And then you're looking at the composition. But if you take this other map to be the identity, that the other map is like g of k is equal to k, of course, this is strictly increasing. And if you did-- if this here map was the identity, then the subsequence would just be the original sequence.

**[1:14:14]** So one of the two implications here is trivial, since a n itself is admittedly trivial. But it is a subsequence. So if all subsequences converge to a, well, then the original sequence, since it is a subsequence, certainly, it will converge. So that was trivial. OK, so we just need to prove that if a n converged to a, then any subsequence. But this is not much more difficult, because you see,

**[1:15:02]** if you're-- so given an epsilon-- so now, given epsilon-- so now we have-- so we now have that a n converges to a. And we're looking at a subsequence, ank. And we want to show that ank also converges to a. So given epsilon, given epsilon greater than 0, there exists a capital N so that if little n is bigger

**[1:15:51]** than capital N, then a n minus a is less than epsilon. But now you see that if k is bigger than capital N, then what corresponds to-- this here is-- this here, how to think about it-- this here, nk, you should really think about that this thing here is the value of this strictly increasing function. But this thing here is-- because it's strictly increasing, it's bigger than k. So you see that if this thing here is bigger than this, then means that this index here is further out than,

**[1:16:38]** in particular, the capital N. And so this means that if you have this here, then ank, this is some element like this. But it's further out than capital N. So this thing here surely will also be less than epsilon because it's falling under here. So that implication wasn't too much harder. And that's sometimes useful, that-- so if-- yeah, it's sometimes useful that you're looking at a sequence, and you see that if it is converging, then--

**[1:17:28]** you're looking at a sequence, and you see that there's a subsequence that is not converging, or you have that there are two different subsequences of a given sequence that converge to different limits. Then the original sequence wasn't converging either. Yeah? AUDIENCE: Can you not have a finite subsequence of-- a convergent subsequence that doesn't get to n, so it hasn't arrived at the point of convergence? TOBIAS COLDING: So convergence is always something about the tail, about the end, right? It never cares about what happened in the beginning. So there might be finitely many n's initially where things are crazy, but then from there on out.

**[1:18:13]** AUDIENCE: OK. The subsequences that we care about in this case are those subsequences that also-- TOBIAS COLDING: Yeah, yeah. So all sequences, including subsequences, are infinite things, right? Yeah. So like-- that's right, because the thing is that you had to have this map. Maybe I erased it. But g here had to be a map from all the natural numbers N to N. So it means that for each element here, you get something. So there's really infinitely many of them. Yeah.

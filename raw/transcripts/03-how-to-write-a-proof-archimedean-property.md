---
title: Lecture 3: How to Write a Proof; Archimedean Property
lecture: 3
video: https://www.youtube.com/watch?v=QJ96fO8Eef4
source: edited transcript (copy-edited from the OCW captions; verbatim original in original/)
---

# Lecture 3: How to Write a Proof; Archimedean Property — transcript

This is a light copy-edit of the OCW captions (sound tags, filler and false starts removed; audience speech marked as the captions label it). The verbatim captions are at [original/03-how-to-write-a-proof-archimedean-property.md](original/03-how-to-write-a-proof-archimedean-property.md); the lecture notes are at [../notes/03-how-to-write-a-proof-archimedean-property.md](../notes/03-how-to-write-a-proof-archimedean-property.md). Timestamps mark the start of each paragraph.

Terms restored (checked against the notes) and editor marks:

- "I bounded from above" restored to "it is bounded from above" (8:12).
- "for all A in A, A here is strictly less than 1" restored to "for all a in A, a here" and "looking A as a subset" to "looking at A" (12:21).
- "H" restored to "h" in "the h here" (1:02:16).
- *[Ed: …]* marks: 6:39 ("less than a"; the notes have less than or equal to), 30:17 ("alpha is less than 1", unclear; he goes on to show alpha less than or equal to 2), 35:51 ("nominator" for numerator), 46:07 ("alpha 0" for alpha 1, throughout the paragraph), 58:08 ("alpha squared" for alpha 2 squared), 1:00:42 ("denominator" for numerator), 1:02:16 (garbled formula for h), 1:10:49 ("sup of A" for the sup of the set of natural numbers), 1:15:06 ("1 as a limit" garbled), 1:18:20 (digits read out as "2, 1, 4, 1" unclear).
- The captions label student speech as "AUDIENCE:" (first at 14:08, then 19:42, 26:51, 49:16, 50:50, 51:35 and 1:06:09); Colding is "TOBIAS COLDING:" throughout. Several audience remarks are inaudible.

**[0:00]** TOBIAS COLDING: So one of the things I want to focus on today, and we'll get to this in just a minute, is how to write a proof. So this is going to be how to write a mathematical proof. So how do you write a proof, as opposed to, how do you think about why something should be true?

**[0:49]** And so this is one of the important topics for this course. So overall, there's a lot of important concepts that we will talk about. But some of the general things that we will learn is how to prove something, but also how to write a proper mathematical proof. And those things are a little bit different. And we'll talk about this in a minute. I also want to say that on the course information, the last page of the course-- several people were asking about this. On the last page of course information, there are the notes for the class that I write.

**[1:35]** And I typically try to write them in advance, a couple of days in advance. And then I try to go over it the day, also, to make sure to find typos and things like that, so that it's more readable. So if I were you, I would first read the lecture notes that I post after the lectures. And then there's also, on the last page of the course information-- and I try to do this in advance. But it's a little bit difficult to do it in advance. So it says the date. And it says some key words from the lecture on that date. So over the weekend, I posted it for the two lectures for this week.

**[2:22]** But then I will try to go back. So I actually went back this morning and changed some of it from the second lecture so that it fits more. I give references there to the book. And initially, I was thinking of giving both references to Rudin and to the main textbook. I think it's probably smarter just to give it from the main textbook. And Rudin is a great book. This was a book that was created here a long time ago.

**[3:09]** And it is a classic in the subject. It's a great book. It's more formal than the other book. So the other book is a little bit more accessible. And so that's why we're using that. But actually, Rudin is a fantastic book. If it was just myself, I think Rudin is hard to beat. But the other one is more accessible. And so it might actually be better the first time you learn it. So I think, from here on out, I deleted the references I had to Rudin. I think I will just give references to the main textbook.

**[3:55]** But I certainly encourage you to look at Rudin also. I also encourage you to look at chapters that we will skip. But there's also things that we initially skip, and then we come back to. But again, when I list the things that we will cover in the lecture in advance, it's only a sort of approximation. So once I write the lecture, it might be slightly different. OK. So last time, we talked about the theorem-- we didn't prove it-- that the reals is a complete ordered field.

**[4:48]** And so, in particular, it was an ordered set that was also a field. And it was complete. And so, again, "complete" meant-- so if you had a subset A here, which was a subset of R, then A is bounded from above if there exists M in R such that for all a in A, a here is less than or equal to M.

**[5:43]** And then, if that's the case, then we say that an M here is said to be an upper bound for A. Likewise, if A here is a subset of R, then we say that A is bounded from below

**[6:39]** if there exists little m in R such that m here is less than a for all a *[Ed: the notes have less than or equal to]*. So this is upper and lower bounds, OK? And several people ask-- on Piazza, they ask-- they were a little unclear about, where does this M, capital M, where does this have to be?

**[7:26]** In what set does it have to be? And likewise for this little m, right? And so let me try to give you some example. And I tried to do that on Piazza. But because several people were asking about it, let me just say again. So this capital M, when you have it like this, this capital M does not need to be in the set, right? A is bounded. So here's an example. If you're looking at the set, 0, 1-- so this is the interval. But it does not contain 0. And it does not contain 1. But it contains everything in between 0 and 1.

**[8:12]** This one here is bounded. So if this has A, and we think about A here as a subset of R, then A is bounded. And so one usually says it's bounded if it's both from above and below. So if one just says that it's bounded, then one means that it's bounded from above and below. And so, because it is bounded from above--

**[9:01]** above, because you have that if x here is in this interval, then, of course, x is less than or equal to 1, right? In fact, it's strictly less than 1, right? But you see, this set here, there is no element in this set that is an upper bound for this set, right? The upper bound is outside the set. But it is in all of R. And that's fine. An upper bound will typically just be in the larger set. And the same with lower bound. Now, everything on this board except this theorem--

**[9:48]** but this is in terms of ordered sets. It has nothing to do-- it's just much more general than R. So if S here is an ordered set, and A here is a subset-- so it's an ordered set. So it's a set with an ordering. And if A here is a subset of S, then, again, we can say that A is bounded from above if there exists M--

**[10:45]** again, M does not have to be in A. But it can be just in a larger set, such that for all a in A, it's less or equal to M. So this is like the definition in general, being bounded above, if you have a ordered set, and you have a subset. And now, just to illustrate it. So typically, we're going to think about where the set is R with the usual ordering. And you have a subset of it. And you talk about whether it's bounded from above or below.

**[11:32]** But of course, you could also do it in a more general setting like this. And so here's an example, which maybe is counterintuitive. If S here is the half line, so it's all the real numbers between, say, 0 and infinity. And then you'll have A here. It's a subset, 0 to 1.

**[12:21]** Now, A here, and the ordering-- so this is, of course, a subset of R. But you should forget about R. I mean, you know the ordering from R. But forget about it, because this is now what you think about the set S, right? And so, if you're looking at A as a subset of this, then A is bounded from above. Why? This is just because, for all a in A, you have that a here is strictly less than 1. So 1 here is an upper bound for A, right?

**[13:10]** But now, think about, does this set here have a lower bound? Well, a lower bound has to be inside this set, S, because we're thinking about this here as a subset of this ordered set. We don't think about it as a subset of the real line. But if you think about it as a subset of this set here, then there is no lower bound, because 0 is not in this set, and no negative numbers in this set. So this seems maybe a little bit counterintuitive. But A is not bounded from below as a subset of S. Obviously,

**[14:08]** it is bounded from below if you were thinking about it as a subset of a real line. But if you think about it as a subset of S, it's not bounded from below. OK. So another person was asking the infinite and minus infinity. Those are not real numbers, OK? Yeah? AUDIENCE: So on the homework, should we consider all of the things as subsets of R? TOBIAS COLDING: Sorry? AUDIENCE: For question 3 on the homework *[inaudible]* they're all subsets of R. TOBIAS COLDING: If it's not directly stated that--

**[14:56]** if it's not directly stated that there's a set, S, and then it has to be a subset of that set, then it would be assumed that it's a-- yeah. Of course, you are welcome to ask on Piazza. I don't have the homework here. But I would say that you're safe-- if it's not stated directly what the larger set is, then you can assume it's R, because we're going to concentrate mostly on R. This is another distinction between Rudin and this book that is the main textbook. Rudin is more abstract than the main textbook we are using. In particular, the main textbook here,

**[15:42]** and I'll do the same in my lectures, is that a lot of things are motivated from R. And then you abstract afterwards, whereas Rudin starts with the abstraction, and then it specializes to R. And of course, there's an argument for maybe starting with the familiar and then abstract, instead of doing the other way around. And so whether it's just an ordered set-- just in general, remember that completeness-- so this is when you have an ordered set.

**[16:28]** So if you have an ordered set, and A here is a subset of S that is bounded from above, then it is complete if S is complete. So if S is complete, then any subset that is bounded from above has a least upper bound. Then A has a least upper bound.

**[17:24]** And that least upper bound is denoted by the sup of A, right? So this thing here, it has the property that a is less than or equal to M for all a in A. And also, if M1 is another upper bound for A, then M is less than or equal to M1.

**[18:11]** So that's a least upper bound. And the same thing is-- so, similarly, when we have an ordered set, and we have a set, if it's complete, and if A here is bounded from below, then inf of A

**[18:56]** is the least upper-- is the largest, the greatest, lower bound for A. So this, again, means that this number here, little m-- so m here is less or equal to a for all a in A. And if m1 here is another lower bound,

**[19:42]** then m1 here is less or equal to m. So this is a symmetric property. And so, again, R, the reals, is complete. So whenever you take a bounded subset of the real-- so if it's bounded, that means that it's bounded from above and below-- then it has a least upper bound and a greatest lower bound. And those are denoted by sup and inf. And in general, sup and inf are not in the set itself, in the set A. I mean, they could be. But in general, they wouldn't be. AUDIENCE: The example that we talked about earlier

**[20:29]** *[inaudible]* open set *[inaudible]* but that is not complete *[inaudible]*. TOBIAS COLDING: That's right. So no. So if you're looking at this set here, so suppose that this here is the set S. And if you take A here is a subset of S, and A here is bounded from-- let's say that A here is bounded from below.

**[21:16]** If it's bounded from below, then it couldn't be-- this set here is not bounded from below. So it means that if it's bounded from below, then A here could not have numbers that was approaching 0. And so actually, if it is bounded from below, if it's a subset of this, and it's bounded from below, then actually, it would have a least lower bound-- a greatest lower bound, right? Yeah. So I'm not going to prove anything is complete or not complete. But it's pretty convincing that it is actually complete,

**[22:07]** in this sense. There's another sense that is not complete. But anyway, in this sense, it is complete. Yeah. No, it can be confusing. Later on, we'll talk about maybe some other notion of completeness. And then it's not complete. But in this notion, it is complete. OK, so the next thing I want to get to is this with how to write a mathematical proof. And again, that's a super important thing to learn in this class. And it's not just a--

**[22:52]** it's not just a formal thing. It may seem like a formal thing. Why bother with that? But it's really, really useful. And the more complicated things become, the more useful it is. And so I want to illustrate this with how to write a mathematical proof. So we will illustrate it by proving again--

**[23:41]** by writing a formal proof of why square root of 2 is a real number. So last time, we talked about that square root of 2 was a real number. But when we proved it, it was more like we talked about the idea. And so then the question is-- imagine you have a piece of scrap paper. What we did last time was what you would

**[24:27]** be writing on the scrap paper. So I want to talk about, if you were handing it in or showing it to somebody, then you wouldn't do that. You would do what we do now. But a formal proof doesn't necessarily make for a great lecture, because it's kind of formal. So let me try to explain how you should write this. And again, this is a very simple example. But hopefully, it will give you an idea of what to do. And again, this is a really important part of this class that you're bound to use in many other classes later on.

**[25:18]** OK, so let's first talk about what was square root of 2. So square root of 2 was a number. And it was given by that it has a property-- that it's positive, and when you square it, then you get 2. That was what square root of 2 was. Now, so we want to prove-- so this is the theorem. So theorem-- square root of 2 is a real number. So maybe I should write it more formally.

**[26:03]** There exists alpha greater than 0-- this is alpha in R with alpha greater than 0 and alpha squared is equal to 2. Now, we look at the set A. The set A is the numbers-- it's the x, such that x is positive,

**[26:51]** and x squared is less than or equal to 2. AUDIENCE: *[inaudible]* see what x is, like where-- TOBIAS COLDING: Yeah. So x here-- so now I will specialize to the real numbers. So that was why I didn't actually write it. But you're right. It certainly can't hurt. OK, so that's the theorem. And so now we try to write a formal proof. Observe first that A here is nonempty,

**[27:43]** since 1 is in A, right? 1 is positive. And when you square 1, you get 1. So this is definitely less than or equal to 2. So A here is nonempty. Next, observe that A here is bounded from above. In general, by the way, when you write a proof, then you really only try to establish the properties

**[28:28]** that you need, because otherwise, it's confusing. If you establish all kinds of other properties that is not needed, that just makes it confusing. So it's bounded from above. And this is just because 2 is an upper bound for A. Now, the next thing is-- so now we have a non-empty bounded subset. So set alpha equal to the sup of A.

**[29:18]** And we want to show that alpha is positive, and alpha squared is equal to 2. Well-- all right. By definition, the way we defined A, all the elements in A were positive. So by definition, 0 is a lower bound.

**[30:17]** So you for sure have that 0 here is less or equal to-- well, I mean, even 1 is a lower bound. So you can also just say that since 1 is a lower bound-- since 1 here is in A, you also have that this alpha here must be bigger or equal to 1, because it was supposed to be an upper bound for A, so in particular. Now-- and so we have that alpha is less than 1 *[Ed: unclear; the bound he goes on to show is that alpha is less than or equal to 2]*. And it's the least upper bound. And 2 was an upper bound. So you have this, since--

**[31:02]** maybe I should write it with this thing. Since 1 is in A, we have that 1 here, less than or equal to alpha. And since alpha is the least upper bound, and 2 is an upper bound, we have that alpha

**[31:49]** is less than or equal to 2. Now, remember, we were going to do it exactly like we did last time. But we're just going to write it down in a proper way as a proof. So remember that last time, we then divided the proof into two steps. The first step was-- so part 1-- so now, all we need to prove, to show, is that alpha squared is equal to 2, because we already have it as positive now, because it's bigger than 1.

**[32:36]** And so there was two parts to this, step 1 and step 2, or part 1 and part 2. The first part was-- so part 1, we will show that alpha squared is less than or equal to 2. And so we prove this-- so assume not. We will show that that leads--

**[33:29]** that this leads to a contradiction to that alpha is the least upper bound for A. I'm writing everything out here, just to illustrate it. As you get more and more familiar with this, then the structure is the same. But some of these steps will seem almost too trivial.

**[34:16]** And that's probably fine. But of course, it's always good to err on more details than fewer details. So this is what we want to do. So we assume not. So assume that alpha squared is strictly bigger than 2. Then-- and this is where it deviates more from how we did it last time. And that's why what we did last time is really what you want to have on the scrap paper.

**[35:02]** What we did last time was like the idea. And then, once you see the idea, then you try to write it as a formal proof, like what we do now. And so, assume not. Set h equal to-- so I'm going to set h equal to alpha squared minus 2 over 4 alpha. Obviously, if this was the first time you would do it, you wouldn't just come up with this sort of thing, right? This is coming from the scrap paper that you had. So you're setting h equal to that. And then you observe--

**[35:51]** you observe that since alpha here is bigger than 1, and alpha squared is bigger than 2, then the nominator *[Ed: numerator is meant]* here is positive. And the denominator is positive. So h here is positive. You also have that h is-- right. You also have automatically that h is-- maybe we don't need that.

**[36:37]** Let's see if we need that. So OK. So now you set alpha 1 equal to alpha minus h. And what I want to prove is-- so we want to show that alpha 1 is an upper bound for A. So I want to prove that this is an upper bound for A.

**[37:25]** The first thing I want to do-- if it's an upper bound, it does need to be positive. So let's check that. So since we already have that h was positive-- so this here was h was positive, alpha squared minus 2 over 4 alpha. This thing here is less or equal to-- I can even forget about the 2. So I can write it as alpha squared over 4 alpha. And so I can just divide by alpha. So I get alpha over 4. So since we have that h here is less than alpha over 4,

**[38:14]** then alpha 1 is bigger or equal to 3/4 of alpha, because I'm subtracting at most alpha over 4. And so there's still 3/4 of alpha left, right? So in particular, this thing here. It's actually bigger than 3 over 4. But I just need it to be positive. So alpha 1 is positive. Now I'm looking at alpha 1 squared, right?

**[39:04]** And so alpha 1 squared is equal to alpha minus h squared. So this here is equal to alpha squared plus h squared minus 2 alpha h. And this thing here is less or equal to alpha squared. Here, h is-- so now I'd like to say that h is less or equal to 1. Actually, I'm going to use that it's less than 1/2.

**[39:51]** And why is that the case? It's actually, alpha itself-- we already know that alpha was less than 2. So you have that this thing here is less or equal to 2 over 4. So this is equal to 1/2, right? So now I have that this thing here is less than plus-- here, I just use that it's less than this thing here.

**[40:36]** I think it's fine to just use h here. I could use h over 2. Maybe I'll use h over 2. So one of the h, I just replaced by 1/2. That is an upper bound. And the other one, I just keep, right? So I have that and then minus 2 alpha h. But if you multiply alpha by h, then it's disappeared in the denominator. So you're getting minus 2. And then you're getting alpha squared minus 2 over 4.

**[41:22]** And so here, this here becomes alpha squared plus-- and here, I'm just writing in. And I think at the moment, we're overkilling it here. And so I can replace this one here. So let me just write it in-- alpha squared minus 2 over 2 times 4 times alpha. And this thing here is alpha squared minus 2 over 2. This 2 cancels with one of those 2. So this is what I have. And so now I get that this thing here is--

**[42:14]** so I get that this thing here is-- we're adding it here. So this thing here is alpha squared. So let me just bring these two together. Maybe I'll just combine all of these. I don't think I need it this well. Right. So if I combine these two here, I think I'm fine with just having a 2 here-- a 4, sorry, instead of the 2.

**[43:00]** So if I do that, then I get alpha squared. Maybe I should just bring it on the common denominator. So this here, this alpha, sorry, I'm getting rid of. I'm bounding this from above by alpha squared plus-- and I'm going to just make it easier for myself. I think it's fine to just use that alpha is bounded by 1. And then you can just bound it by alpha squared minus 2 over 4. And this thing here is alpha squared minus 2 over 2, right?

**[43:49]** Here, again, I'm just using that alpha was bigger or equal to 1, and-- right. And then I just actually ignore this 2, right? So this is definitely an upper bound. And so now you see that this thing here is equal to alpha squared. You can write this thing here, if you will, as alpha squared, plus alpha squared minus 2 over 4, minus 2 alpha squared, minus 2 over 4. And so what you get is that it's alpha squared,

**[44:36]** minus alpha squared, minus 2 over 4. And this thing here is now positive, because alpha squared was strictly bigger than 2. This is positive. So this is strictly less than alpha squared. And so this here would also-- which is still-- so this thing here is also an upper bound. I'm sorry. I need to-- no, sorry. OK. So I have this.

**[45:21]** No, no, sorry about that. OK, so-- yeah, no, I-- sorry. OK, let's just go over this again. Sorry. So what am I trying to prove here? I'm trying to write down the formal-- that's the problem, that it got so formal that I was now in-- so what I'm trying to prove here is that I want to say-- this part 1 is that alpha squared is less or equal to 1. This is what-- less or equal to 2. That's what I want to prove. This is part 1. And so I assume not.

**[46:07]** So I assume that alpha squared was strictly bigger than 2. If alpha squared was strictly bigger than 2, here, you have 0. Here, you have alpha. And now we define this alpha 0 *[Ed: alpha 1 is meant, here and in each later mention of alpha 0 in this paragraph]*. Alpha 0 was to the left, so to speak, of alpha, because it was subtracting a little bit. And what I want to show is that this alpha 0-- I want to show that this alpha 0 is also an upper bound. So I want to prove that this square here is also bigger than 2. That's what I want to prove. So I want to find a lower bound.

**[46:54]** And that lower bound should be true. So this is not exactly what I wanted to do. So let's just go through it here. Sorry. So this here was correct. And this here is really for the second part. OK. So we define it like this. And now I say that this thing here is bigger or equal to-- I want to bound it from below. And so then I can ignore the h squared. So it's bigger than alpha squared minus 2 alpha h, because that's positive. And this thing here is--

**[47:41]** so this is equal to alpha squared minus 2 alpha. I fill in what h was. This here was h. And then you see that this here cancels with that. And you're getting alpha squared-- this is this alpha squared minus alpha squared minus 2 over 2. And this thing here is equal to alpha squared over 2. This is subtracting that.

**[48:28]** And then you're adding, right? You're adding 1. So this is what it is. We have already proven that alpha here was bigger or equal to 1. So this here is bigger or equal to-- I claim that this here is bigger or equal to 2 using that alpha is bigger or equal to 1. And so you see that alpha 1, that is a smaller number, because you're subtracting a positive number from alpha. That is also an upper bound. So this contradicts.

**[49:16]** And then one often writes this symbol here. This is a standard symbol that means this is a contradiction. Yeah? AUDIENCE: Did you say using that alpha is greater than or equal to 1? TOBIAS COLDING: Yeah. AUDIENCE: What if alpha is 1? TOBIAS COLDING: Yeah, then you get 2. But that's fine. All I needed to do was I needed to prove that-- so you see that I'm assuming that this thing here is strictly positive. And then I define alpha 1. But alpha 1 is strictly less than alpha.

**[50:02]** And then I have that alpha 1 squared is bigger or equal to 2. This here means that alpha 1 is also an upper bound. This is strictly less than alpha. This was supposed to be the least upper bound. That's a contradiction, right? And so, you see, I fell into the trap. I was doing it so formally that I lost track of what I was doing. So I was actually in the process of proving the-- that's a danger with-- but the formal proof is much easier to read afterwards. And so, you see, the difference here with the formal proof was, last time, we did a little calculation. And then we tried to figure out, what should this h be?

**[50:50]** And then it came at the end. But when you write down the formal proof, then you would, up front, you would already have done that little calculation. And you would, up front, say what h was supposed to be. And then you run through the argument. Yeah? AUDIENCE: Should it say that alpha-- oh, I was looking *[inaudible]*. TOBIAS COLDING: Sorry? AUDIENCE: I was just confused because I thought that alpha was *[inaudible]*. TOBIAS COLDING: Here? So of course, alpha is much bigger than 1. But we already-- I only need here that alpha is bigger or equal to 1

**[51:35]** to say that this thing here is bigger or equal to 2. AUDIENCE: If you get greater than 2, right? TOBIAS COLDING: Sorry? AUDIENCE: *[inaudible]* AUDIENCE: I think *[inaudible]*. TOBIAS COLDING: This is-- right. This is alpha. So the inequality here is that alpha 1 squared is bigger or equal to 2. And I'm using that alpha at this stage here to conclude this inequality. I'm using-- sorry. No, no, you're right. Yeah, sorry about that. You're right. I'm using that alpha-- no, I'm not using that. I'm using that alpha squared is bigger or equal to 2. Yeah, sorry. That was what you meant. Yeah? Thank you. OK, so that was a formal proof of part 1.

**[52:21]** And then there's part 2, so the other inequality. So how do we do that? And when you write this, it's always good to try to explain what you're going to do, and in this case, what is going to be the contradiction. So let's try to prove part 2. And hopefully, we get it straight this time. So part 2, so I want to show that-- so part 1 was establishing that alpha

**[53:09]** squared was less or equal to 2. Now we want to prove-- so part 2, we want to show that alpha squared is bigger or equal to 2. And so, again, we will show this by contradiction. So assume that alpha squared is strictly less than 2.

**[54:06]** And now I think it's helpful. You don't necessarily have to do it. But I think it's helpful if you say-- maybe it's too long. But it's at least helpful to think about, where is the contradiction coming from? So if alpha squared is less than 2-- so I will say it. You don't necessarily have to write it. But indeed, we will show that if this is the case, then

**[54:56]** there exist some numbers, alpha 2, bigger than alpha, such that alpha 2 squared is also less than 2, contradicting that alpha is an upper bound for the set A

**[55:49]** we defined. That's what we will prove. And so we want to find a real number that is larger than this. But still, the square is still less than 2, OK? And so, in this case, the structure is going to be the same. We had this little scrap paper where we outlined the argument and figure out what h had to be.

**[56:34]** And so I'm going to use this h. So we're going to, again-- maybe I'll just erase this here so we don't get confused with the first part and the second part. OK, so I'm going to set h again.

**[57:21]** I'm going to define it very similar to what I did before. But now I have to remember that I'm assuming that alpha squared is less than 2. So I define h to be 2 minus alpha squared over 4 alpha. This is how I define it. And then what I'm interested in is-- so I have here 0. I have this that is supposed to be the upper bound. But I want to prove that that really isn't an upper bound. That's an element in my set A. And so this is this alpha 2. So I'm setting--

**[58:08]** set this and alpha 2 equal to alpha plus h. This here was just to illustrate. You don't necessarily have to include that. And I want to show-- I think it's a good idea to write what you want to show. In particular, if I really had written that before, then I wouldn't have been in trouble, because I was trying to prove something else. So you want to prove that alpha squared here is also less than 2 *[Ed: alpha 2 squared is meant]*. So we already have that alpha here is positive.

**[59:10]** It's bigger than 1. So this number here, we already know, is bigger than alpha. And so, if I can prove that the square is less than 2, then alpha here, sorry, would not be an upper bound. There's another element in the set A that is bigger. So I want to prove that. So now I'm looking at alpha 2 squared. So that is alpha plus h, right? That's how I define alpha 2.

**[59:55]** And I square it. And if I do that, then I get alpha squared plus h squared plus 2 h alpha. And now I want an upper bound. And so we already have that alpha is this one here. You see that h is, in this case here, equal to 2 minus alpha squared over 4 alpha. Alpha is bigger or equal to 1.

**[1:00:42]** This here, the denominator, is bounded by 2 *[Ed: numerator is meant]*. So again, it's 2 over 4. So this is bounded by 1/2. So we have that h is positive and h is less than 1/2, right? And so now, I can bound this trivially by just using that h is bounded by 1. So I get this plus h plus 2. And then h times alpha, again, or 2h alpha, when we multiply this by 2 alpha, then the alpha

**[1:01:27]** cancel out. And the 2 cancel with one of these-- 2 and this 4. So you're getting 2 minus alpha squared over 2. And so now I get that this thing here is bounded by-- so a very rough bound for h is using-- sorry-- so I have that, and now using that h here is equal to alpha 2 minus alpha squared

**[1:02:16]** over 2 over 4 alpha *[Ed: h equal to 2 minus alpha squared over 4 alpha is meant; the captions are garbled here]*, which is less than 2 minus alpha squared over 2, since alpha here is bigger than 1, right? So I have that. So using that, we have that alpha 2 squared is less or equal to-- let me just write that line. I'm just now filling in. Alpha squared, the h here-- I'm using this inequality here-- 2 minus alpha squared over 2. And then I have the same thing again.

**[1:03:03]** And so you see that this here, it's this here times 2. So this is just alpha squared minus 2 plus 2 minus alpha squared. And this inequality here, one of these inequalities, I should have replaced by a strict inequality. This is because h is positive and is strictly less than 1. So this here is actually a strict inequality. But now you see that this thing here, the alpha cancel out. And you're getting 2. So you have that alpha 2 squared is strictly less than 2.

**[1:03:50]** That's what we wanted to prove. And this gives that alpha 2 is also in A. And yet, alpha 2 was bigger than alpha. And this is the desired contradiction. So again, we already did this last time. But the point here is that, how do you write down a formal proof? And a formal proof, in this case,

**[1:04:36]** is that you try-- very clearly, in this case, it was divided into two steps. So you try to divide it into the two steps. And then maybe you have a last line to say that part 1-- part 1 and part 2 together show that alpha squared is equal to 2, completing the proof. And again, the point here was that we already knew how to prove this.

**[1:05:21]** But how do you write down a formal proof? And so, for this proof, it was divided into these two steps. So you try to write each step separately. Both of the two steps was proven by contradiction. And so you would say up front that you're going to prove it by contradiction. And then, of course, there would be the statement that you want to prove-- since you're proving it by contradiction, you would assume the negation. And then I think, if you can, and it doesn't feel too much, I think it's very helpful to write what you are trying, how you are trying to get the contradiction, right? That's what I tried here.

**[1:06:09]** And then, you see, then the big difference from when we were trying to figure out how to prove it is that you now go ahead, and you just define those things. You define h and alpha 2, right? That seems to come out of nowhere. And then you establish the property that you want to prove that leads to the contradiction. That's the structure. Are there any questions to this? Yeah? AUDIENCE: *[inaudible]* property of the real numbers *[inaudible]* least upper bound *[inaudible]*? TOBIAS COLDING: Right. So we're using a few things.

**[1:06:55]** We're using that it's ordered. We're also using something about that it's an ordered field. And why? Because we're using something about multiplication to at all define square root. And also, we're using something about that 1 is bigger than 0. And then we're also using, of course, completeness in order to define this least upper bound. So we're using a bunch of these things.

**[1:07:41]** But of course, if you're asking when-- and that's not really, at this stage, very, very soon, in one of the next few lectures, things will be in the real numbers. We're not going to work on general fields. General fields-- this is not part of this topic. But of course, it's interesting to ask. And I think that's your point, is like, when can you define something like a square root of 2 in a field? Or something like that. And there's a lot of things. You're absolutely right that there's a lot of these things that was just general property.

**[1:08:27]** But maybe we shouldn't get too much into that. So there's a few more things I was hoping to do. So I also wanted to just talk about the Archimedean property again. And so I wanted to just outline how to write a formal proof. And the reason, of course, why I'm illustrating how to write a formal proof is an important part of this class. And I'm obviously using the things that we already proved last time, just so

**[1:09:15]** that you can focus on how-- not to prove-- not the statements, why the statements should be true, but just how to write it. And so let's talk about the Archimedean property. And so the Archimedean property, just saying that-- so this is the theorem that the natural numbers is not bounded from above. That's one way of formulating it.

**[1:10:01]** You could also say, like we did last time, that whenever you take a real, there's a larger natural number than that real. But that's the same. OK. So now, how do we prove this? So again, here, we're thinking about things as being subset of R. When we don't really mention it, then we always think about it as being subset of R. And so we will show this by contradiction.

**[1:10:49]** So suppose alpha is an upper bound for the natural numbers. Well, we can assume, after replacing alpha by sup of A *[Ed: the sup of the set of natural numbers is meant]*, we can assume that alpha is the least upper bound.

**[1:11:43]** And now I think it's nice, again, to write where the contradiction is coming from. So we will get the desired contradiction by showing

**[1:12:33]** that alpha minus 1 is also an upper bound, contradicting that alpha was the least upper bound. And so this is what we want to prove. Since alpha is an upper bound for all natural numbers,

**[1:13:32]** if you add 1 to the natural number, this here is also a natural number, right? n plus 1 is also a natural number. So n plus 1 must be less or equal to this upper bound. But this implies that n-- subtracting 1 on both sides implies that n is less or equal to alpha minus 1, which holds for all n, all natural numbers.

**[1:14:20]** So alpha minus 1 is also an upper bound. OK. And this proof gives you the desired contradiction. So that's how you would write that. Let me talk a little bit about sequences. So this will be a big topic. So sequences.

**[1:15:06]** Well, first-- so we talked about that a little bit. So how do we think about square root 2 on the real line? So the way to think about square root of 2 is what we did here-- that is, this positive thing so that the square is 2. But if you want to place square root of 2 on the real line, then you could think about it as 1 as a limit *[Ed: the 1 here is a stray word; as a limit is meant]* of a sequence. If you take 1, and then the 1 is less than 1.4, which is less than 1.41, which is less than 1.414, et cetera.

**[1:16:02]** And so this here is a sequence. I'll make that precise in just a minute, but an increasing sequence of numbers. And the limit is square root of 2. So if you plug square root of 2 in on the calculator, it will bring out a lot of digits. And these are the first digits. And it will continue on. And that's how you think about square root of 2 if you want to think about it on the real line. And so square root of 2 is going to be the limit of these. And we need to make this precise. And we also need to make precise what, really, a sequence is.

**[1:16:48]** So a sequence of real numbers-- this is a map. It's a function from the natural numbers into R. So for each natural number, you get a real number. And so a function--

**[1:17:35]** a function is defined by the value at different points. But if you want to think about it as a sequence, then it's common to denote this here like that. So this is how one typically writes a sequence, where, instead of what the argument is, inside a bracket, you write it as a subscript. So this is a sequence. And so, in the case over there, if you're thinking about a1, say, to be equal to 1,

**[1:18:20]** a2 to be equal to 1.4, a3-- and now I'm thinking about the sequence here. As I'm thinking about square root of 2, and I take the number of the subscript here, I'm just taking the number of digits in square root of 2. So now I need three digits. Here, I need a 2, 1, 4, 1 *[Ed: unclear; the digits as captioned do not match the sequence 1.41 for the third term]*. a4 is 1.414, et cetera. And so then a n here is a sequence of real numbers.

**[1:19:05]** And it's actually increasing-- that the sequence a n is less than a n plus 1. We have this property. And we want to talk about-- next time, we want to talk about, what does a limit mean? What is a limit? And so square root of 2, indeed, will be the limit of this sequence. And the limit, you write like this, sometimes, as n goes to infinity of a n. But we'll talk about this next time.

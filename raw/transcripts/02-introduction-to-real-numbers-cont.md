---
title: Lecture 2: Introduction to Real Numbers (cont.)
lecture: 2
video: https://www.youtube.com/watch?v=6i6sV8WIzLc
source: edited transcript (copy-edited from the OCW captions; verbatim original in original/)
---

# Lecture 2: Introduction to Real Numbers (cont.) — transcript

This is a light copy-edit of the OCW captions (sound tags, filler and false starts removed; audience speech marked as the captions label it). The verbatim captions are at [original/02-introduction-to-real-numbers-cont.md](original/02-introduction-to-real-numbers-cont.md); the lecture notes are at [../notes/02-introduction-to-real-numbers-cont.md](../notes/02-introduction-to-real-numbers-cont.md). Timestamps mark the start of each paragraph.

Terms restored (checked against the notes) and editor marks:

- "c" restored to "z" in the transitivity axiom, as in the notes (4:57).
- "the squared is equal to 2" restored to "x squared is equal to 2" (11:49).
- "1.4.1" restored to "1.41", the notes' sequence (17:40).
- "s that is what it means" restored to "So that is what it means" (24:44; stray letter).
- "And is a subset of S" restored to "A is a subset of S" (25:35).
- "for a if M is an upper bound" restored to "for A" (26:36).
- "at least upper bound" restored to "a least upper bound" (35:07).
- "The squared is non-negative" restored to "h squared is non-negative" (39:53).
- "2 minus a x squared" restored to "2 minus x squared" (51:35).
- "in the set a" restored to "in the set A" (52:20).
- "Archimedean problem" restored to "Archimedean property" (1:01:41).
- *[Ed: …]* marks: 1:38 (garbled), 6:33 (garbled), 14:13 ("2 m1 squared" for the square of 2 m1), 21:35 ("bigger or equal to A" for each element of A), 41:23 ("minus h" for x minus h), 52:20 ("some x" for h; and "we immediately get of this" garbled), 57:17 ("actually equal to x" unclear), 58:09 ("replace by the least upper bound property" garbled), 59:57 ("also not a natural number" for also a natural number), 1:02:34 ("less than 1" for less than y), 1:05:52 ("x times m" for x times n; "x times n, this is an integer", "definition m" and "let's denote n and choose the largest one" unclear), 1:07:26 ("denominator" for numerator), 1:08:14 ("n minus 1/n" for m minus 1 over n; "this m" for m/n).
- The captions label student speech as "STUDENT:" in the closing question period (from about 1:09:46); no other audience speech is marked.

**[0:00]** PROFESSOR: OK. So just to remind you, last time we had the motivating example that we had a graph. We had a function f defined on some interval from a to b. And it was going inside the real numbers. And it started off negative here. This is f of a. This is negative. And it ended up positive, f of b.

**[0:47]** And this was a continuous function. And we wanted to say that there was some c. So we wanted to show that there's a c between a and b so that the value at c is equal to 0. So this was the intermediate value theorem. And so this here was a motivating example

**[1:38]** for trying to understand, what property of R do we need? So what property of R do we need to make this rigorous? So that was the motivating example. And so in order to make this rigorous, well, then we need to concept of that R *[Ed: garbled in the captions]*--

**[2:27]** we need to understand the following statement, that R is a complete ordered field. And a field here, just briefly, was a set with two operations, a plus and what we called multiplication.

**[3:16]** So each of these two operations have a 5 property. And then there's an 11th property that chain them together. And the last one is usually referred to as the distributive law. So that was one of the two important concepts

**[4:05]** that we talked about last time. The other concept that we talked about was what's called an ordered set. So that's a set with an ordering. And the ordering has actually two properties. The first one is that whenever you take an element x and an element y in the set, then

**[4:57]** you should be able to relate these two by the ordering. So either x is equal to y or x is smaller than y or y is smaller than x. And the second property is what's called transitive, that if x and y and z are elements in the set and x is less than y and y is less than z, then x should be less than z.

**[5:42]** So this is the transitive property. So the first property, again, is that you can compare any two elements. And the second one is this transitive law. So that was the two concepts we talked about last time. And then we talked about what is meant to be an ordered field. And then ordered fields is, you have a field that is also an ordered set. And then the relationship, that one being less than

**[6:33]** the other one-- to interact. have So this is these two things *[Ed: garbled in the captions]* that, if you take x is less than y and you're adding any elements on both sides, then it still preserve the order. So this is one thing. And the second is that if you take x that's bigger than 0 and y that's bigger than 0, then the product of x and y should be bigger than 0. And so an ordered field, again, is a field that has a set, also has an ordering. And then the ordering together with the operation of the field

**[7:22]** should be chained together by these two rules. So we're getting close to understanding this. So this question is, in order for all of this to make sense, we need to understand what it means that the real numbers is a complete ordered field. And so we have now this part of it, that it's an ordered field. We understand that. This here, we need to understand what this means. OK. So now before I get into that, let's just talk about-- so what is the difference

**[8:15]** between the real numbers and the rational numbers? Remember, the rational numbers are numbers of this form here, where this is an integer and this is a natural number. So what is the difference between these two? Well, one difference is that square root of 2 is a real number but not a rational number.

**[9:13]** Now let me try to explain first why it's not a rational number. So what is square root of 2? The square root of 2, you can think about it as a number, x. And it has to have the property that if you multiply it by itself-- so x times x or, if you will, x squared-- this here should be equal to 2. It also should be positive. Now I claim that square root of 2

**[10:04]** is not a rational number. So by that, I want to claim the following. There does not exist a rational number x equal to m/n, where-- again, this is an integer. This is a natural number-- so that x squared is equal to 2.

**[10:53]** So I claim that you don't have a rational number that is square root of 2. OK. Now let's try to prove that. So suppose there was such a number. So we want to prove it. So we prove by contradiction. So assume that there exists x that is a rational number.

**[11:49]** So it can be written in this form here, where m is an integer, and n is a natural number. So assume that there exists an x that is a rational number and so that x squared is equal to 2. Well, if that's the case, then m/n-- so this here squared is supposed to be equal to 2. So this implies that m squared over n squared is equal to 2. And this, just multiplying over, implies that m squared is equal

**[12:36]** to 2n squared. Now, when we write x as a rational number-- of course, we know that there are many ways of writing it as rational number. Because if you have one, then you can just multiply the numerator and denominator by a natural number, and then you get another representation. But we may assume that m and n does not have a common factor.

**[13:27]** Because otherwise, we could just reduce it. So we could reduce it until they don't have a common factor. OK. So we will assume that m and n do not have a common factor. We have now that m squared is equal to this. But this means that m here must be even. So we have that since m squared is equal to 2n squared-- so it means that 2 is a factor in m squared.

**[14:13]** So it must actually be a factor in m. So it means that 2 here is a factor in m. In other words, m is even. So you can write m here as 2 times another integer here. But this means that m squared is equal to 2 m1 squared *[Ed: the square of 2 m1 is meant, which is why it equals 4 m1 squared]*, which is equal to 4 m1 squared. And we already know that that is equal to 2n squared.

**[14:59]** So this means dividing by 2 on both sides. It means that 2 m1 squared is equal to n. But this means that-- sorry, is equal to n squared. So this means that 2 here must be a factor of n. So this means here that 2 is also a factor in n. But now you see that this is a contradiction. So this is a contradiction. Because now what we have is that 2 is a factor in m and 2 is a factor on n. So they have a common factor.

**[15:44]** But we assumed they didn't have a common factor. So we argue by contradiction-- we assumed there was a rational number so that the square of it was equal to 2. And we get a contradiction. So there could not be a rational number that has a property that the square is equal to 2. So square root of 2 is definitely not a rational number. So now, how do we think about square root of 2? So how do we fit square root of 2 into the number system?

**[16:47]** Well, square root of 2 is-- if you think about it as a decimal number, then it starts with 1.4142136. And then it continue like this. So we'll come back to this at some later lecture. One way of thinking about square root of 2

**[17:40]** is as a limit of a sequence of number. And that brings us to another really important concept that we will talk much more about later, is sequences and limits. And so if we want to think about it as a limit of a sequence, we think about maybe the number 1 first. And then we think about 1.4. And then we think 1.41, and then 1.414, and then 1.4142,

**[18:30]** et cetera. And so you see that this here is a sequence of numbers. And so this is an increasing sequence of numbers. And square root of 2 is the limit of the sequence. So again, we'll talk much more about sequences and limits later. But this is just something to keep in mind

**[19:16]** as also motivating why we need to understand sequences and their limits. So we now know-- maybe not super surprisingly, but we know and see there was a very simple proof why the real numbers is larger than the rational numbers. It contain a particular square root of 2 that the rational numbers does not contain. We still need to-- and this is related to the completeness of R and why the rational numbers is not complete.

**[20:02]** And this is, again, what we're now working towards. So we're working towards what it means for a field to be complete. So let me just write that, and I'll explain it more. But this here is what we are aiming towards, completeness, which is-- and I'll explain that--

**[20:48]** at the least upper bound property. OK. So suppose S is an ordered set. And the ordering-- as usual, we're ordering, we denote by this. So suppose S is an ordered set.

**[21:35]** And suppose that A here is a subset of S. Then we say that M is an upper bound for the subset for A if, for all elements in A, M here is bigger or equal to A *[Ed: "bigger or equal to each element of A" is meant, as in the notes]*. So an upper bound for a subset is something that has to be bigger than all

**[22:22]** the elements in the subset, bigger or equal to. It could be equal to one of the elements. So that's a upper bound. And so, of course, a couple of examples here. Let's say S is the natural numbers here. And the subset here is 1, 2, 3.

**[23:10]** So then the element 4 here is an upper bound for A. So 4 is an upper bound for A, whereas 2 is not. Obviously, 3 is bigger than 2. So 2 is not an upper bound. Another example is if you take--

**[23:58]** let's say S is the rational numbers, and A here is the natural numbers. Then A here does not have an upper bound. And I'll return to this second example in just a minute.

**[24:44]** So that is what it means to be an upper bound. So now there's another concept. And that is a least upper bound. So there's another concept of the least upper bound. So again, we have S is an ordered set.

**[25:35]** We have A here is a subset of S. Maybe let me just point out that it's bounded. So A is a subset of S that is bounded. Then we say that capital M is a least upper bound

**[26:36]** for A if M is an upper bound-- so it has to be an upper bound-- and if, for any other upper bound-- we have to have that for any other upper bound, say, M1, we have that M1 has to be bigger or equal to M.

**[27:25]** So a bounded set has a least upper bound if there is an element that is the smallest, so to speak, of the upper bound. OK. And so now we are ready to state what it means to be a complete ordered field. So a complete ordered field is an ordered field

**[28:35]** so that any bounded subset has a least upper bound. OK. So that's a complete ordered field. And so we have the following theorem that we're not going to prove because that really takes us off field.

**[29:21]** So we'll just take it for granted. So theorem-- so there exists a smallest complete ordered field that contains the rational numbers.

**[30:11]** OK. So this is a theorem. Again, we won't prove it because it's really outside the scope of this class. It's not really what we want to focus on here. But you can prove this. And so that field is what we call R, is R. It's the real numbers. OK. So now I want to see that if we work with that field instead

**[30:58]** of the rational numbers, then actually, we have in particular that the square root of 2 is in that field. So we want to show that a square root of 2 is in the reals.

**[31:45]** So now I'm going to look at the set A, which is the element in R such that x here is bigger than 0 and x squared is less than 2. So I'm going to look at this set. Now, of course, this set A here is bounded. We'll say first, it's not empty. It's not empty since 1 here is in A. 1 is positive.

**[32:38]** And 1 squared here is, of course, 1, which is less than 2. So it's non-empty. And A here is also bounded. Because any element-- so for all x in A, you have that x squared, x is positive and is less than 2. So this means that x here must be itself less than 2. Because 2, of course, when you square it, you're getting 4.

**[33:25]** So A here is a bounded subset of the reals. So now the real has the least upper bound property. So this means that I can now define square root of 2 to be the least upper bound of A. A

**[34:20]** was a nonempty bounded subset. So because we are in the reals, if you grant this theorem, then there is a least upper bound. So let me denote this number by x. I'm going to denoted by x instead of square root of 2. Because if I denote it by square root of 2, then it's going to be confusing. And it's like you will automatically

**[35:07]** use what you think square root 2 should satisfy. So let's call it x. So it's clear that since x here is a least upper bound for A and, in particular, 1 is in A, then it means that 1 here has to be less than or equal to x. And 1, of course, is positive.

**[35:54]** So it means that x here is definitely positive. Now we need to show that x squared is equal to 2. That's what we need to prove in order to prove that x is really the square root of 2. So I'm going to divide it up.

**[36:41]** So we divide the proof into two steps. The first one, step 1, we're going to show that x squared is less than or equal to 2. So this is what we would show in the first step. And then the second step would be the reverse inequality. And of course, together, this would be the proof.

**[37:28]** So again, just like we argued before, in this case, we will also argue by contradiction. You may get the feeling that we're always going to argue by contradiction in this class. And we won't. And it's generally thought of that it's better style to prove things directly. But sometimes it's a much more logical and easier in a way-- at least, easier the first time-- to prove it by contradiction. And there's nothing wrong with proving it by contradiction. So we will show this by contradiction.

**[38:20]** OK. So we show this by contradiction. And so we assume not. So assume that x squared is not less than or equal to 2.

**[39:05]** So we assume not. So assume that x squared is strictly bigger than 2. Now I will look at x minus some small number. I'm going to prove now that if this here was strictly bigger than 2, then I can find some small number so that this here would also be an upper bound. So h would be positive.

**[39:53]** This here would be a number strictly less than x. And I would show that this here is also an upper bound. That's what I want to do. So I take x minus h, and I square it. If I do that, then I get that this is x squared minus 2xh plus h squared. h squared is non-negative. So this here is definitely bigger or equal to x squared minus 2xh. And so you see that--

**[40:38]** right. So we have that x squared is bigger than 2. So this means that x squared minus 2 is positive. I'm just subtracting a 2 from both sides. So we're assuming that this here is positive. And so now if I just make sure that--

**[41:23]** So now I want to get the contradiction by finding a h bigger than 0 so that minus h is also an upper bound for A *[Ed: x minus h is meant, as the next paragraph confirms]*.

**[42:11]** Because this here is clearly smaller than x, right? And this would then contradict that x was the smallest upper bound. So that's what I want to do. And so now, how do I do that? So using this little calculation here, I want to find h positive so that when I square, when I subtract h from x and I square it, then I still get something bigger than 2.

**[42:59]** So I want to find h positive so that this thing here is bigger than 2. And all I need to do is show that I can find h such that x squared minus 2xh, that this thing here is bigger than 2. And so you see, now I just move over

**[43:44]** on the other side to say that this here is bigger than 2. It's the same as saying I can just move this 2 over on that side. And I can move this here over on the other side. So I just need to find h with this property. But that, of course, is equivalent to saying that h has to be less than x squared minus 2 over 2x. x is positive. This thing here is strictly positive. So I can certainly find a positive number. This here is something strictly positive. So I can certainly find some small h

**[44:30]** so that it's less than this strictly positive number. So this is step one. This is just showing that x squared was less than or equal to 2. Now I want to argue similarly to prove the other direction.

**[45:15]** In this case, there's not really any difference. You see in a minute that the one inequality is not any easier than the other. I have a colleague here. He's retired now. And he collaborated with some other guy and made a lot of famous work. And the other guy maybe become even more famous. And he used to say that when you do mathematics-- so it doesn't really apply here because the two inequality is just as easy. But he used to say that when you do mathematics, there's three things you do. You locate a problem. You prove one of the two inequality, whichever one is easier. And you ask Raghu-- Raghu was his collaborator-- to prove the other inequality.

**[46:03]** *[laughter]* OK. So step two is that x squared is bigger or equal to 2. And we will again prove this. So again, we'll show this by contradiction. So I assume not.

**[46:50]** So assume that x squared here is strictly smaller than 2. Now what we want to prove is-- so then we want to get the contradiction. We want to get the contradiction by showing that x is not

**[47:36]** an upper bound for A. x was supposed to be the least upper bound, so in particular an upper bound. So how do we do that? Well, we're going to add just a little bit to x. So this is similar to how we argued before. So I'm going to add-- h, again, is being positive.

**[48:24]** So h is positive. And I'm going to add just a little bit to x. I want to prove that if h is small enough, then x plus h is in A, contradicting that x was an upper bound. And so h is going to be chosen small. So in particular, it's going to be between 0 and 1. And I'm looking at x plus h.

**[49:13]** And I'm squaring it. So this thing here is x squared plus h squared plus 2hx. Now h is less than 1. So this means that h squared-- since h is positive and is less than 1, then you have that h squared is less than actual h. And so this thing here is less than x squared plus h plus 2hx

**[50:00]** And I want to show that this x plus h, this is still in A. So I want to show that we can find such a h so that this here squared is still less than 2. So all I need to do is, because of this inequality, I just need to find an h so that this thing here is less than 2.

**[50:47]** So I want to find h such that this thing here is less than 2. Right now, again, we're just moving over on the other side. In this case, we're moving this x squared over here. So we have h plus 2hx is less than--

**[51:35]** this is what we want to find, an h such that this thing here is less than 2 minus x squared. This thing here is now-- because x squared is strictly less than 2. This is positive. Here, you can just factor out an h. So if you factor out an h, then you have this thing here is less than 2 minus x squared. And this is just saying that you want to find an h so that this thing here is strictly less than 2 minus x squared over 1 plus

**[52:20]** 2x. x is positive. So this thing here is positive. So this and this here is also positive. So this here is a positive number. So you can definitely find some x with this property *[Ed: h is meant; the h chosen small enough is what is being found]*. And then you see that-- so this means that this x plus h would also be in the set A, contradicting that x was an upper bound. OK. So now, accordingly, we immediately get of this *[Ed: garbled in the captions]* is that the rationals is not complete.

**[53:07]** So we get the following corollarys. The rational number is not complete. And this is just because-- so the proof of that is that we have already-- so if we're looking at a field that is complete and contains a rational, then we know that square root of 2 is in that field. So we just proven that if f is a complete field containing

**[54:08]** the rationals, then square root of 2 is in that field. But we have also shown that square root of 2 is not a rational number. So the rational in itself is not complete.

**[54:54]** OK. Now the next thing I want to do is prove what's called the Archimedean property, the Archimedean property. And so this is actually something that was sort of used here, sort of used it a little bit already. But let me just prove it rigorously. So the Archimedean property--

**[55:41]** so this is the following, that for all real numbers, every time you take a real number, then there exists an integer-- actually, even a natural number n such that n here is bigger than x.

**[56:28]** OK. This seems like a kind of trivial fact. But let me try to actually prove it in a rigorous way. So this is what's called the Archimedean property. And so, again, we prove this by contradiction. So suppose not-- so if there existed an x so that you did not have this, well then-- so suppose not, then--

**[57:17]** so the negation of that statement is that then there exists an x such that for all natural numbers, for all, you have that n here is less than or equal to x. Yeah, it's actually equal to x *[Ed: unclear; the negation just stated is "less than or equal to x"]*. Because this is the negation of that. But this means that x here is an upper bound.

**[58:09]** And so then you could take-- so you could replace by the least upper bound property *[Ed: garbled in the captions]*. So it's upper bound. So in particular, the natural number is a bounded subset of the reals. And then we let, let's say, y be the least upper bound of the natural numbers.

**[59:10]** If the natural numbers was really bounded, because it's a subset of the reals, we could now take the least upper bound. OK. So now we have that for any natural number-- so for all, we have that n here is less than or equal to y. But whenever you take a natural number, then add 1 to that natural number-- so we would also have that-- so y is not just an upper bound for n, but it actually--

**[59:57]** because n plus 1 is also not a natural number *[Ed: "also a natural number" is meant; the notes say "Since n + 1 is also a natural number"]*. So y here would have to be bigger or equal to n plus 1 also. And this now holds for all n. So this means that-- just moving the 1 over on the other side-- so hence, n here is less than y minus 1. But this here say that-- so this means that y minus 1 is also an upper bound and that this is a contradiction.

**[1:00:49]** So this contradicts that y was the least upper bound. And that's the Archimedean property. OK. Now I want to give one application of this. And so this is the following.

**[1:01:41]** So I now want to prove the following corollary of the Archimedean property. And the corollary is that whenever you have two real numbers, x and y-- so these are real numbers. And x here is less than y. Then the claim is that then there exists a rational number m/n with the property that is between these two

**[1:02:34]** so that x is less than m/n and less than 1 *[Ed: less than y is meant, as the construction below shows]*. that's what I want to prove using the Archimedean property. And so to prove that, I look at beta. Say beta is y minus x. And I'm looking at-- so y minus x. Because y is bigger than x, this here is positive.

**[1:03:19]** And I can now look at 1 over beta. So 1 over beta is some positive real number. And now the Archimedean property say that-- so by the Archimedean property, there exists a n, a natural number such that n is

**[1:04:05]** bigger than 1 over beta. That's the Archimedean property. It gives us this n. But now, of course, if that's the case, this implies you can just take 1 over it on both sides, and that reverses the inequality. This implies that 1/n is smaller than beta. So we get that. And so now define the step size to some extent.

**[1:04:54]** So we have here x, and we have here y. And beta is really this distance here. This here is beta, the distance between the two. And n here is-- we've now seen that there's an n so that when you're looking at 1/n, then-- so 1/n here is smaller than beta. It's something positive and smaller than beta. So now you're looking at the m. So now look at the integers so that m minus 1

**[1:05:52]** is less than x times m *[Ed: x times n is meant; the notes have m minus 1 at most x times n]*. So suppose you're looking at this thing here. If you take x times n, this is an integer *[Ed: unclear in the captions]*. So there's definition m with this property *[Ed: unclear in the captions]*. And you can find the biggest-- so look at m with this property. And let's denote n and choose the largest one, the largest such m *[Ed: unclear in the captions]*.

**[1:06:38]** So if you choose the largest such m, then you see that-- so this inequality here, this will just tell you that m minus 1 over n, that this is smaller than x. But you would also have that because it was the largest such m-- since m was the largest such m, then

**[1:07:26]** you would have that if you had m itself in the denominator *[Ed: numerator is meant, since the fraction is m over n]*, then it wouldn't be smaller than x. It would actually be larger or equal to x. And I just want to now prove that this-- so this here is bigger than x. That's part of what I needed to prove. I also wanted to show that it's smaller than y. But now the step size. So when you have here-- here, you have x. Here, you have y. 1/n was smaller than this distance.

**[1:08:14]** So if you are at some point here-- this is where you are when you are at n minus 1/n *[Ed: m minus 1 over n is meant]*. Then you can't go further to the right. You go 1/n to the right. But that can't take you all the way past y. So that's why, if you're looking at this number here, this m must be smaller than y *[Ed: m/n is meant]*. And if I had just chosen m so that this here was smaller or equal to that, then I would get this *[inaudible]*. OK. So that's a corollary of the Archimedean property. I think there would be something along these lines

**[1:08:59]** on the homework. And again, I'm just waiting for the office hour. I know that the office hour, there will at least be four office hours next week. On Mondays and Wednesday, there would be office hours from 5:00 to 6:00 on Monday and Wednesday. And the other days, it would be 1:15 to 2:15. But you can check-- the time is actually already posted. The room number, I hope to have that today. Once I have that, then I will also assign the homework, probably today, or maybe more likely, tomorrow, the homework. But it won't be due next week, just the following week.

**[1:09:46]** Any questions? And, of course, I very much encourage you to go to the office hours. And yeah. Yeah? STUDENT: Are you upper bounding-- PROFESSOR: Sorry. STUDENT: Oh, sorry. PROFESSOR: Oh. STUDENT: So we defined plus in the solution. So how do we define minus 1, for example? PROFESSOR: So remember that the minus 1 was this element that you had when you had-- remember that a field had the two operation, plus and multiplication. And for each of these that had 5 property, they were almost the same property.

**[1:10:32]** There was one exception, that 0 didn't have a inverse for multiplication. But minus 1 is the-- so you have 1, but 1 is the neutral element for multiplication. Why? That was how 1 was defined, right? And we proved that there was a unique 0. That same argument would prove that there's a unique 1. So there's just one 1. So it's a well-defined notion. And then you can look at the inverse element of that with respect to addition. That's minus 1. Yeah. STUDENT: Why did we define an upper bound and not a lower bound? PROFESSOR: Yeah, and that's a good question.

**[1:11:17]** And I will come back to that next time. And it would seem more logical to define both upper and lower bound. But you can look at the complement. And so if you take a set and you're looking at the complement, then the upper bound for that is the same as the lower bound. So that's a kind of sneaky way-- that's the reason why we did it. I might have done it the other way around, but then it was a little bit overkill. But I agree, it seemed more logical to define both things. But it actually is contained in this. Any other questions? Yeah? STUDENT: I was a little confused because I was thinking-- I wonder if you could please speak about the completeness

**[1:12:05]** of *[inaudible]*? Like you make the statement *[inaudible]* say a bounded subset of rational numbers would not have this upper bound. PROFESSOR: So again, we saw that square root of 2 is not a rational number. And if we're looking at all rational numbers, all rational numbers so that the square is less than or equal to 2, that set, it has an upper bound in the rational number, but it doesn't have a least upper bound.

**[1:12:51]** And that's because we first prove that there wasn't a rational number so that it multiplied itself was equal to 2. We proved that-- STUDENT: But does the least *[inaudible]* also have to belong to the-- PROFESSOR: Yeah, that's right. That's right. That's right. STUDENT: --*[inaudible]*? PROFESSOR: That's right. That's right. That's right. That's right. So it's this. A field is complete means that whenever you take a subset of that field that is bounded, then that subset has to have a least upper bound. But any bound, including the least upper bound, that always have to be in the fields. OK. Any other questions? Yeah? STUDENT: Well, when we tried to define it, and *[inaudible]* did we also prove the result 2 minus x

**[1:13:42]** squared over 1 plus 2x is smaller than 1 because you have assumed for *[inaudible]* smaller than 1 so that we can do the-- PROFESSOR: So you're saying-- so I just want to make sure I understand. So in the step two, we added something. And we wanted to prove that you could add something, and this is still less than 2. And so I was looking for h between 0 and 1. And so then I got some equation somewhere that is probably erased now. But it just require that--

**[1:14:31]** h had to be positive, but it was less than something. And that was positive. STUDENT: Yeah, but that's something-- should the left something smaller than 1? PROFESSOR: Right. OK. So I don't remember what I got here. So yeah, you're right. I guess I can reconstruct it. STUDENT: Over 1 plus 2x. PROFESSOR: Yeah. So what you are saying is that-- actually, so this thing here is positive. And so you want to choose h so that it's smaller than this but also this here. So you don't. But if this is 500, well, I'm not

**[1:15:17]** going to choose 500 because it was supposed to be less than 1. But I just choose it so that it's less than 1 and also less than this positive number. Yeah.

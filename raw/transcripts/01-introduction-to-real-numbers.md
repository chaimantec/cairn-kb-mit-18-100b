---
title: Lecture 1: Introduction to Real Numbers
lecture: 1
video: https://www.youtube.com/watch?v=BWvjy0a1Ffg
source: edited transcript (copy-edited from the OCW captions; verbatim original in original/)
---

# Lecture 1: Introduction to Real Numbers — transcript

This is a light copy-edit of the OCW captions (sound tags, filler and false starts removed; audience speech marked). The verbatim captions are at [original/01-introduction-to-real-numbers.md](original/01-introduction-to-real-numbers.md); the lecture notes are at [../notes/01-introduction-to-real-numbers.md](../notes/01-introduction-to-real-numbers.md). Timestamps mark the start of each paragraph.

Terms restored (checked against the notes) and editor marks:

- "2 set" restored to "Z set" (the integers, 15:21).
- "integral from a to b" restored to "interval from a to b" (13:39).
- "contains irrational numbers" restored to "contains rational numbers" (13:39).
- "n2 times N2 is equal to N2 times n1" restored to "m1 times n2 is equal to m2 times n1" (17:47).
- "p1 comma q1" restored to "p1/q1" (25:46).
- "m2 times p2, m2 times q2" restored to "m2 times p2 divided by n2 times q2" (28:59).
- "reputation" restored to "representation" (28:59).
- "O1" / "O2" for the two zero elements restored to "0₁" / "0₂", as in the notes (45:55 to 47:33).
- "serial elements" restored to "zero element" (49:04).
- "c" restored to "z" where the notes use z (55:01, 59:09).
- *[Ed: …]* marks: 19:21 and 21:37 ("denominator" said where "numerator" is meant), 27:26 (garbled equation), 28:59 (denominator "into q2"), 50:37 ("proof regression"), 51:29 ("slides"), 1:02:19 ("the same as x").
- The captions carry no audience labels, and no audience speech was found that could be marked with confidence.

**[0:00]** TOBIAS COLDING: So this here is just to make sure that you are in the right place, which is 18.100B or 18.1002. And my name is Toby, so Toby Colding. And by the way, so we will be recorded. And the video from the lecture will be posted online.

**[0:46]** And I will also write lecture notes. I hope you appreciate it because I wrote the first one. It actually took me quite a long time. I don't typically type the lecture notes, but I will do this for this class. And I also wanted to just give you an idea of the structure. First of all, this is one of the most important math classes at MIT. And I'll tell you in a minute why it is important. And of course, I think that, being one of the most important math classes, it's one of the most important classes, period. But just to give you an idea of what will be expected from the class--

**[1:32]** so there will be 10 weekly homework. And the first one, it won't be due next week. It will probably be due the week after next week. And in part, it will just allow you to get settled in a bit. But also, I'm waiting for somebody else to assign the TA and the grader. So I think it will be at least one graduate TA, and there will be some undergraduate TAs. And then there will also probably be some graders. And most of these, including myself,

**[2:18]** will have office hours or so. So it'll be 10 weekly homework. There will be a midterm, so one midterm and one final. And the midterm is on March 20. And the final is-- I don't know when it is. I'm not the one that is deciding the date. And it will be a while before we know what date that will be. And in terms of the grade, the homework will count for 50% of your grade, midterm will count for 20%, and the final for 30%.

**[3:06]** And you can see all this information about this in-- there's a syllabus and a course information posted on the Canvas. So make sure to check out the Canvas site for the class. And there's also the information about the book. And also, the lecture notes will be posted on the Canvas site. The lecture notes, I think, will probably be posted on the files.

**[3:54]** And one other thing is that I have activated what's called pset partners. So you are encouraged to work with other people on the psets, but everybody have to hand in their own psets. And pset partners is a way of finding other people to work with. Of course, you can do it another way. But this is a tool that is used in a lot of classes. OK. I think this covered the basic information. And so the class here is-- so the two key topics for this class is--

**[4:44]** so key topics, one is you will learn how to write a mathematical proof. So what does it mean to write something so that is mathematically rigorous? And the second thing that you will learn is how to prove theorems. And so here's an example of this.

**[5:29]** Let's suppose you have a function. So suppose you have some interval. So a and b are real numbers. And you have a function f defined on this interval. And you take real values. And so here, you have the interval here, a. Here's b. And let's say that the value at a is negative, and the value at the other endpoint, b, is positive. So if you were drawing the graph, here, you have a, maybe. Here, you have b. And then the function initially is negative, and it end up being positive.

**[6:15]** So this is f of a. Here, you have f of b. And then this function here is continuous. So the function looks maybe like this. So f is continuous. So the intermediate value theorem's saying-- so the intermediate value theorem.

**[7:09]** It's saying the following, that if you have a continuous function on an interval, then it takes all values in between. So the intermediate value theorem says in particular that there exists a c. And the c here is between a and b so that the value of the function at c is 0. Because the function starts off negative, and it end positive. So there must be somewhere in between where it hits 0. That's the intermediate value theorem. But now the question is then, how do we make this into--

**[7:55]** and it's kind of obvious. It's sort of intuitively obvious that if you take a function, continuous means something like that if you were drawing the graph, and you'd have this piece of chalk here, then as you're drawing the graph, the chalk is not allowed to leave your table. It can't have a function like this here that jumps, so go like this, and then jumps like this. That's not continuous. So continuous function is that you have to, when you draw it, it's in one motion.

**[8:40]** The chalk doesn't leave the blackboard. And so it seems obvious that there should be some point in between where you're crossing this axis here. But how do we make this into a rigorous proof? And what is the property? So how do we make this intuition into a proof? And this is not just a semantic question.

**[9:29]** It's not just a crazy question. Maybe in this case, it seemed clear. But very quickly, if your foundation is not totally rigorous, then you get into something where it seems to be the case, but it might not be the case. And you also quickly arrive to that you don't even know whether it should be the case or not. And so it's really important to build things up, step to step, where each step is totally rigorous. And you write it because it's not only you know for sure that things are right, but it also makes it much easier to predict what should be true.

**[10:18]** And so in order to understand why there should be some c between a and b where the value is 0, immediately, the first question that arises-- what are you using? What property do we need to make this into a proof? What property do we need of the real numbers? So this is the first question that arises.

**[11:12]** And so, in fact, what is the real numbers? So what are the real numbers? And so the thing is that, in particular, what is square root of 2? And is that a real number?

**[11:58]** Is square root of 2 a real number? So those are some of the questions that you immediately get to. And so now, the answer to, what are the properties that you're using of the real numbers? So the answer to this question is the following.

**[12:45]** So what are the properties of the real numbers that you're using? So the answer to that is the following, that the real numbers-- so R is a complete ordered field that contains the rational numbers,

**[13:39]** Q. I denote the rational numbers by Q and the real numbers by capital R. So in order to make this the intermediate value theorem, this property that if you have an interval from a to b, you have a continuous function on that interval. And it starts off negative, and it ends positive-- that then there is some value in between, where 0 is achieved. In order to make that rigorous, what you're using about the real numbers is that it's complete ordered field that contains rational numbers. So we need to understand what this here means. And in this lecture here, I will not explain complete.

**[14:27]** I will do that at a later lecture. But we will understand the rest of what are these properties that we're using. So just first, some notation-- so the natural numbers here, this here is 1, 2, 3, 4, 5, et cetera. So these are the natural numbers.

**[15:21]** The integers-- so Z set here, these are the integers. And the integers are simply the natural numbers. But then it also allows them to be negative, and it also includes 0. So this is 0 plus or minus 1, plus or minus 2, plus or minus 3, et cetera. These are the integers. The rational numbers are then-- so the rational numbers, Q, so these are numbers of the form m/n,

**[16:10]** where m here is an integer and n here is a natural number. That's a rational number. And so now what are the properties? So we're building up to trying to understand what property of the real numbers is. But let's try to somehow understand it a bit better. What are the properties that we really have about the rational numbers? So for rational numbers, we have-- so we write a rational number as a quotient, like that.

**[16:56]** But of course, there are many ways that you can write a quotient. So properties of the rational numbers-- we write it as a quotient, like this. But this is not uniquely defined. If you take a quotient, like this, you think that this here is equal to another quotient, right? Again, m1 and m2 are integers, and n1 and n2

**[17:47]** are natural numbers. Two quotients are the same if and only if that if you multiply this over here and this over there, then those numbers are the same. So m1 times n2 is equal to m2 times n1. Those two rational numbers are the same if and only if those two natural numbers are the same-- or integers, because m could be negative. So again, a rational number, it has a representative like this.

**[18:33]** But you could think about it as always, you can write this quotient. And two quotients are the same if and only if this here is the case. So this is what it means to be a rational number. But then there are some operations. If you have two rational numbers, then you can add two rational numbers together. And that's really important, that you have some operations on the rational numbers. So if you take-- this here is one rational number.

**[19:21]** And if you now take another rational number, m2/n2-- then how do you add two rational numbers together? Well, of course, you know that you put it on the common denominator. So this here is m1 times n2 plus m2 times n1 divided by n1 times n2. This here is an integer in the denominator *[Ed: "numerator" is meant; m1 n2 + m2 n1 is the numerator]*. And this is a natural number in the denominator. And so that's representative of a rational number. So that's an operation.

**[20:06]** Now, in order to really know that this is-- so the idea here is that if you take one rational number, like this, and you take another rational number, like that, then you can add them. And that gives you another rational number. That's this operation that we know so well and its addition. In order for this really to make sense, you should check that this rational number you get is independent on the representation.

**[20:52]** If you have another representation for the same rational number and another representation for the same rational number, then when you add them, you should get another representation for the same rational number. And we will check one of these things in just a minute. The other thing is that-- so that was one operation. When you have the rational number, then addition is one operation. Another operation is, of course, multiplication.

**[21:37]** So another operation is multiplication. And so if you take one rational number, like this, and you take another rational number, like that, then if you multiply them together-- so what does it mean to multiply two rational number together? Well, of course, you know this very well. It's just multiplying the denominator *[Ed: "numerator" is meant; the product of the numerators is the integer]*. So that gives you an integer. And then multiplying the denominator, that gives you a natural number. So this here is a rational number.

**[22:25]** And then there's another thing. So this was addition. This is multiplication. But there's another important property that you have for the rational number. And that is an ordering. Again, we're trying to understand this question up there. But we want to try to understand, how do we make the intermediate value theorem-- how do we make this rigorous? And so we need to understand what property of the real numbers we need. And so this is explained in this. And we were working towards trying to understand the different concepts in this. What is a field?

**[23:10]** That's what we're trying to understand. And so we have addition in the rational numbers. We have multiplication. But we have another operation on it, which is an ordering. So if you take a rational number here, then you can say that this rational number is less than another rational number. When is it less than another rational number, this is equivalent to saying-- remember that these here are natural numbers. So they're positive. So that this rational number is less than that just means that m1 times n2 is less than m2 times n1.

**[24:01]** Here, I am just multiplying over here over here. And I'm using, of course, that these numbers here are positive. OK. So this is an ordering. So in the rational numbers, there is actually ordering. So that's really important also. So we have these two operations, and then we have an ordering. So let me just check. So I said that when we talked about addition, then there was something, really, you had to check, that this even made any sense. And for this to make any sense means

**[24:49]** that this rational number you get from adding these two is independent on how you write this rational number and how you write that rational number-- and the same for multiplication. So let us check that. So this here is checking that multiplication is a well-defined operation, i.e, it is independent.

**[25:46]** It is independent of the representative. So we are multiplying-- we take this rational number. Sorry, let me write a little bit bigger-- this rational number. So this is one rational number. And we multiply this rational number by another rational number. Let's call it p1/q1.

**[26:33]** And then we take another representative for the same rational number. And let's call this m2/n2. And for this rational number, we take another representative. And we want to prove that this number here is the same as that number here. So how do we do that? So we have that this here and this here is the same-- it's two different representation of the same rational number. So we have that m1/n1 is equal to m2/n2.

**[27:26]** So remember that this just meant that when you multiply over here, like that, then you get the same integers-- so this here, n2, plus m2 times n1 *[Ed: unclear — caption is garbled here; by the notes this should be m1 times n2 equals m2 times n1]*. That's what it meant, that these here were the same. And likewise, you have the two rational numbers here. This is one. This is equal to that p2 divided by q2. This just meant that when you multiply over, p1 q2 is equal to p2 q1. So this just meant that these two represent

**[28:12]** the same rational number. And now what we need to prove is that the product here is independent of these representations. So the product here is-- this product here, this is just m1 times p1 divided by n1 times q1. And this is what we want to show, that this thing here

**[28:59]** is the same if we took this other representation and multiply it by the other representation of this. So this is m2 times p2 divided by n2 times q2. That's what we want to prove, that those two are same. And so we need to show that m1 p1 times this denominator here into q2 *[Ed: unclear — caption wording kept; by the notes this is presumably n2 q2]*-- we need to show that this thing here

**[29:50]** is equal to m2 p2 n1 q1. That's what we need to prove. But now let's see. So we know that if we take m1 together with n2, this is the same as-- so this here is the same as m2 n1. This is what this here say.

**[30:35]** And it also says that if you take p1 together with q2, then you may as well write this thing here. So you may as well write p2 q1. So this thing here is equal to that. But now you see that here, you have m2. Here, you have n1. Here, you have p2. Here, you have q1. So those two are the same. So this proves that this operation of multiplication is well defined in the rational number-- and similarly for addition. The reason, of course, why I chose multiplication is that it looks a little simpler on the blackboard. It's a little more messy if you did addition.

**[31:22]** But it's just exactly the same. OK. So this is also supposed to illustrate how detailed a proof is. So when we have a concept like this, we want to make sure that it really makes sense. And in this case, it makes sense that it's well defined. It's independent under representation. And so the proof here, this here would be the proof. OK. So the takeaway here at the moment

**[32:08]** is, we're building towards this. We're understanding a field. We want to understand the real numbers. But the takeaway at the moment is that on the rational numbers, there is a way of adding two rational numbers and multiplying two rational numbers. And there's also an ordering. And so this leads us to the following definition. And so this is the definition of a field. So a field-- and I will use F here, capital F for a field--

**[33:05]** is the following. So it's a set with two operations. And the operations we are denoting suggestively by a plus and a multiplication, like a dot. But this is just abstract.

**[33:52]** So we have a set, and we have these two operations. What property do these two operations need to have? Each of them have five properties. So that means that there are 10 properties. And then there's 11 properties that chain those two operations together. So let's start with addition. So properties of addition-- so the first property is that addition make any sense. So if you take a element in the field and you take another element in the field,

**[34:40]** then addition gives you a third element. So when you add these together, this is just a third element in the field. So this is the first property, that it really is an operation that when you take two elements of the field, then you get another element in the field. So this is one. The second is that if you add two elements together-- so x and y are in the field. If you add two elements together, then the ordering that you're adding is irrelevant. So this here is the same as y plus x.

**[35:28]** Then the next one is-- this is sometimes called abelian or commutative, this property here. Then there's a third property, which is that if you add two elements together and then you add a third element to the sum of these two, then this here is the same as that you can add the last two first and then add the first one to the sum of the other two.

**[36:17]** And so the fourth property is that there is what is sometimes referred to as a neutral element. So there exists an element that we denote by 0. But it's just to make it kind of easier to understand, that we denote by 0. And it has the property that if you take this 0 element

**[37:07]** and you add it to any other element, then it just gives you back that other element. So it's kind of neutral for the operation. And then there's supposed to be a fifth property. And the fifth property is that for any element x, there exist another element. And again, we write this suggestively by minus x with a bracket around, like this.

**[37:52]** So there is another element with the property that if you take x and you're adding this other element, then you get 0. So those are the five properties that addition has to have. And then multiplication have to have five properties also. And these are similar to this with a little twist. And so for multiplication, you need to have the following properties.

**[38:41]** So again, it's five properties. The first one is the similar property to the property 1 up there, namely that if you take two elements, x and y, in the field, then when you multiply them together, that should give you another element in the field. The second one is similar to 2 up there, is that x times y should be the same as y times x. So again, that's often referred to that it is abelian or commutative.

**[39:30]** The third property, it's similar to the third property up there-- is that if you take x times y and then you multiply it by a third element, then you could as well have first multiplied the two last elements and then multiply by the first element, like that. And then the fourth property is similar to that property 4 up there, is that there exists an element denoted suggestively

**[40:22]** by 1 here, with a property that 1 times any element x just give you back that element, x. And then the fifth is similar, except there is a slight twist. And so the fifth property is that-- it's very similar to that fifth over there. The fifth property here is that for any x in the field except 0--

**[41:12]** you have to disregard 0. For any other elements, there exist an element-- and, again, suggestively denoted by 1/x with the property that x times 1/x is equal to 1. OK. So those are the five properties for addition, five properties for multiplication.

**[41:57]** And you see that the one for multiplication is like a mirror of the one for addition, except the fifth one has that you have to look away from the 0 element. And so, again, 1 is just that it is an operation. 2 is usually called the abelian property or commutative property. This is called the associative property. This, it's often also referred to as a neutral element. And this here, that exists this element-- in this case, minus x is sometimes

**[42:43]** called the inverse element-- and likewise for multiplication. And then there is, again, an 11th property. And that's a property because you see that those-- at the moment, there's basically no interaction between these two operations. The only way that you see some interaction, but this is very little, is that the fifth property over here refer to the neutral element for addition. But they don't really chain the two operations together. And that is the last property that is often referred to as the distributive law. So this is an axiom chaining addition--

**[43:32]** write it like this, addition together with multiplication. And that's if you take x and you multiply it by y plus z-- you take the sum here, and then you multiply it by x. That is supposed to be the same as where you first multiply x with y and then you multiply x by z.

**[44:19]** So this is often called the distributive law. And that's a law, again, or axiom that is chaining these two operations together. OK. So now let me just establish one little property of a field. And you see that when we talk about the axioms for addition, I just said that there had to exist one element that we call the 0 element, and it had to have some property. But maybe there are many elements. And so this is the first little theorem.

**[45:10]** For any field-- I just write it as capital Field. But you don't really have to. For any field F, there exist only one zero element. OK. Let's try to prove this. And again, there's all kind of important concepts in this class.

**[45:55]** But there's also another thing that is important to learn. And you have to be a little bit patient because it will take you a little bit of time to learn it-- is how to write a mathematical proof. And so this here just gives you just a little bit of idea of it. So we want to prove that there exists only one zero element. So assume that 0₁ and 0₂ are both zero element.

**[46:45]** So that it's a zero element just means that if you take 0₁ and you add anything to it-- x could be anything in the field-- then you get x back. That is that 0₁ is a zero element. That 0₂ is a zero element just means the same thing-- that if you take anything in x, then you get x back. And now we want to prove that 0₁ is equal to 0₂. So I just write 0₁ plus 0₂. But now I'm just thinking about this 0₂ as my x. So I'm adding 0₁ to this x. So I know that I'm just getting this here back.

**[47:33]** Is because 0₁ is a 0 element. But I could do the same with 0₂ that I take. The ordering I know already is irrelevant, whether it's 0₁ plus 0₂ or 0₂ plus 0₁. That's the same. So I can think about this 0₁ here as my x. And so I'm adding the 0₂ to it. But then I know that I'm getting this here back. So this here must also be equal to 0₁. And so you see that 0₁ is equal to 0₂. And of course, in the notes that are post,

**[48:18]** things are written slightly more rigorous. There's a little bit more meat to it. Here, I write it a little bit shorter on the board. So look also at the notes. OK. So now we know what a field is. So a field, again, it has these two operations, additions and multiplication. Each of those operations have five properties. And then there's 11 properties that chain those two operations together. And so the examples of a fields is--

**[49:04]** so we already have an example. So the rational numbers here is a field. It has these two operations and with all the 11 properties. The natural numbers is not a field. It fails even the most basic thing. It fails many of the properties it needs, but it fails that even the zero element is not in it.

**[49:52]** And the integers here also is not a field. That is slightly closer to being a field, but it's still not. And why is this not a field? It's for multiplication, right? If you think about 2, then the neutral element for multiplication, that's the usual 1. But if you take, say, the element 2, then there should be an element like the inverse. There should be an element with the property that if you take 2

**[50:37]** and you multiply with that element, then you should get 1. That should be the inverse element, 1 over it. But this is like a half. But you're missing a half in the integers. So that's why this here is not a field. OK. So the next concept is-- again, we're working our way towards trying to understand what property of the real numbers that we need in order to make the intermediate value theorem, the proof regression *[Ed: unclear — "proof regression" is the caption's wording, probably "proof rigorous"]*. And so we now know what a field is.

**[51:29]** The next few slides *[Ed: as spoken; there are no slides, and the notes defer completeness to a later lecture]*, I'll talk about complete, what that means. But we also have this ordering. So what does it mean that a field is ordered? So let's start with an ordered set. So an ordered set-- so this is a set denoted by capital S. And it has the property that whenever you have two elements in the set, then it should either be-- and the ordering, by the way-- so an ordered set with an ordering--

**[52:23]** and I denote the ordering, again, suggestively by this. I could have used any other symbol, but I'm just suggestively using this symbol, just to make it easier to remember the property. It's like this property that you know so well. So an ordered set is a set with an ordering-- and, again, denoted by this-- so that if you take any two elements in the set, then one of the three properties should hold. The following three properties should hold.

**[53:26]** One is that either x should be equal to y. 2, the other possibility, is that x is smaller than y. Or 3, y is smaller than x. So basically, if you have an ordered set, whenever you take two elements, you should be able to compare these two elements. Of course. These two elements could be the same elements. But if they're not the same element, then one should be smaller than the other. So that's the idea. OK. And so now the next concept is an ordered field.

**[54:15]** So now we have a field, and we have an ordered set. So an ordered field is a field that is also an ordered set. And then the operations from the fields and the ordering, they should speak to each other. So there should be an interaction between these two

**[55:01]** operations. So it has to have the following two properties, that if x is less than y and you're adding a z to both-- so this here implies that for any z in the field, if you add this z to both sides--

**[55:47]** so x plus z is less than y plus z. So you should be able to add something to both sides and it's still less than, like that. So this here is, how does the ordering interact with addition? And the other thing is, how does it interact with multiplication? And there, the property is that if you take a x that is positive and y is positive-- so you have both x and y that are positive.

**[56:33]** Then the product of these two should also be positive. And so this is how the ordering interact with multiplication. This is how it interacts with addition. This is how it interacts with multiplication. And so now-- well, the first thing you observe is that, again, you already know an example of this. So the rational numbers--

**[57:24]** so Q here is an ordered field. We have already seen that it is a field, has those 11 properties. It has addition, multiplication. Each of those have 5 property. It has the 11 that chain the two together. And we also discussed the ordering. If you take two rational numbers, what does it mean that one is less than the other? It has the property of an ordering, that you can compare any two elements, any two rational numbers, that either they are the same or, if you have two, one is less than the other.

**[58:14]** And it also has this, the additive property. And also, the ordering interact with addition in this way. And it interacts with multiplication in this way. So the rational number is indeed an ordered field. Now let me just establish one last property. And that is that if I take-- well, let me try to prove a little theorem here. So here's the theorem.

**[59:09]** So F here is supposed to be an ordered field. And then we have that x here is less than y. And z here, this is positive. So I assume I have this. And now I claim that from these properties that our ordered field have, I get automatically then x times z is less than y times z. So I claim I get this property here

**[59:55]** that you know these properties over here. So let's try to prove that. So what I want to do is-- so we want to show that x times z is less than y times z. This is what we want to show. Now, to say this here--

**[1:00:42]** this here is equivalent to showing that-- because this here, if you add minus y times z-- sorry. If you take this thing here and to both sides-- so you take x times z and then you plus minus x times z, then this here is the same as--

**[1:01:31]** to say that this is less than that is equivalent to saying this thing here. Why is that equivalent? This is this law here that is chaining the ordering together with addition. And this here, this element here, this is just the inverse element of this product here. But now you see that these two things together, that just gives you 0.

**[1:02:19]** This thing here, this here is the same as x *[Ed: as spoken; by the board argument, x z plus minus x z is 0]*. So maybe we need to show this. But this here, it's not hard to believe that this here is the same as y times z minus x times z. So this here is now-- you can factor out. So this is this law, the 11th law that allow you to factor this one out. So this is the same as y minus x times z. This was the distributive law and was the 11th law.

**[1:03:04]** But now you see that because y was bigger than x-- since y here was bigger than x, this is equivalent to saying that y is bigger than x-- if you subtract x on both sides, this is equivalent to saying that y minus x is bigger than 0. This is, again, using the first axiom over here. And so you see that now we have that. So we want to prove that this thing here, this

**[1:03:49]** here is all equivalent to proving that this thing here is bigger than 0. So the claim up there is equivalent to proving that this thing here is bigger than 0. But the difference here, this difference here is positive. This is assumed to be positive. The second law that is chaining the ordering together with multiplication say that if you have something positive and you multiply it by something positive, you're getting something positive. And so in order to prove this here, it was the same as proving that this thing here is actually positive. And we have now just reduced it to this second axiom.

**[1:04:35]** OK. Is that clear? OK. So we go just a little bit easier here in the first lecture. This is what I have for the first lecture. But there's a bunch of different concepts. And again, feel free, of course, to ask any questions. On the class, I typically just linger around for a few minutes afterwards if anybody has any questions after the class. And we will also have office hours. I'm just waiting for the assignment of the TAs. So that will be put all on online.

**[1:05:20]** Yeah. OK. Let me know how it goes. And one more thing is that this-- again, I mentioned before. So my experience is that it takes people a little bit of time to get a hang of this with writing proofs. So don't be discouraged. A few weeks or months into the class, things will really turn around, and it will all make sense. And then it will be more fun also. OK.

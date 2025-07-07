What is Mathematics at its core?
- Manipulation of numbers and variables
- Extending logic to its limits (and sometimes beyond...)
- Abstract representation of the real world
- Search/discovery (invention?) of Universal Absolute Truths
Small history lesson:
YBC 7289: <img src="https://github.com/AlexKontorovich/2025EuclideanGeometryCourse/blob/main/LectureNotes/Pasted%20image%2020250707124606.png?raw=true" width="300">
Meaning: 
![[Pasted image 20250707124624.png]]Mystery: You find this ball of clay in the ground, dated to ~2000 BCE. What is it, what does it mean? 
Babylonians / Mesopotamians used base 60. 
$1 + 24/60 + 51 / 3600 + 10 / 60^3 \approx 1.414212$
This is $\sqrt 2 \approx 1.414213$ to VERY many decimal places. This accuracy is within one part in a million. Way more than necessary for ANY engineering / economic application. 

This to me distinguishes this object as being mathematics as opposed to engineering. Has no practical application.

Why $\sqrt 2$? Well the picture shows they hypotenuse of a square, so if we use the side of the square as a unit, then by the Pythagorean (~500 BCE) Theorem, the diagonal is $\sqrt 2$.

Another ancient objects (also from ~2000BCE): Plimpton 322 ![[Pasted image 20250707125548.png]]This contains huge integer solutions to the Pythagorean equation $x^2 + y^2 =z^2$. 

What these ancient objects are "missing" to be Mathematics (as we now understand it) is : PROOF

There came a time when people no longer accepted mere "Fact" as the Truth, they wanted a pair (Truth, Proof).

Earliest (known today) proof is by Thales ~600BCE:
Thales's Theorem: Take a circle, draw its diameter, and put any other point on the circle. ![[Pasted image 20250707130029.png]]Question: How does the angle $\angle BCD$ depend on $C$? How does it change as $C$ moves around? We check: and every time we measure it, the angle is $90\degree$ 
If we were Babylonians, just stating that fact might be satisfactory. 
But of course today that seems deficient for UNDERSTANDING.

How can we actually PROVE This theorem?

IDEA: Try drawing a line from the center $A$ to $C$ .
![[Pasted image 20250707130716.png]]
Another idea: Suppose that we know that the sum of interior angles in a triangle add up to 180.
IDEA : $\angle ADC = \angle ACD=x$ (Why? Because $AD$ and $AC$ are both radii of the circle, and hence equal. So triangle $ADC$ is isosceles, and hence base angles are equal.) Same for $ABC$, that is, $\angle ACB=\angle ABC=y$. 
But : $\angle D + \angle B + (\angle DCA + \angle ACB) = 180\degree = x + y + (x+y)=2(x+y)$. Therefore $\angle C=x+y=90\degree$. 
QED

Here's a problem: If every fact is proved using other facts, why are those facts true? And so on FOREVER. You get an infinite recursion of facts, and then how do you know you're not proving nonsense. 

E.g. Suppose in proving a fact, we used another fact, namely that $0=1$. (That's false. That's a contradiction.)
Let's prove the Riemann Hypothesis: Proof. Assume it's not true. $0=1$ gives a contradiction. Therefore RH is true. QED. 

Our whole house of cards can come tumbling down if it turns out that we used facts that depend on other facts that depend on other facts that depend on $0=1$. (How do we tell that we haven't hidden a false statement in this infinite recursion?)

We have to START with something that we Declare to be True. Those are called the Axioms.
We actually need a triplet: (Axioms on which to build a theory, Fact to prove, Proof).

What document is the ancient epitome of this ideal? Euclid's Elements.

http://aleph0.clarku.edu/~djoyce/java/elements/elements.html

**[Definition 1](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/defI1.html).**

A _point_ is that which has no part.

**[Definition 2](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/defI2.html).**

A _line_ is breadthless length. [ By line, he means "curve" ]

**[Definition 4](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/defI4.html).**

A _straight line_ is a line which lies evenly with the points on itself.

**[Definition 15](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/defI15.html).**

A _circle_ is a plane figure contained by one line such that all the straight lines falling upon it from one point among those lying within the figure equal one another.

**[Definition 23](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/defI23.html)**

_Parallel_ straight lines are straight lines which, being in the same plane and being produced indefinitely in both directions, do not meet one another in either direction.

**[Postulate 1](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post1.html).**

To draw a straight line from any point to any point.

**[Postulate 2](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post2.html).**

To produce a finite straight line continuously in a straight line. [ I.e. if you've drawn a finite segment, you can always extend it a little further ]

**[Postulate 3](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post3.html).**

To describe a circle with any center and radius. [compass!]

**[Postulate 4](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post4.html).**

That all right angles equal one another.

**[Definition 10](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/defI10.html).**

When a straight line standing on a straight line makes the adjacent angles equal to one another, each of the equal angles is _right,_ and the straight line standing on the other is called a _perpendicular_ to that on which it stands.

**[Postulate 5](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post5.html).**

That, if a straight line falling on two straight lines makes the interior angles on the same side less than two right angles, the two straight lines, if produced indefinitely, meet on that side on which are the angles less than the two right angles.

Homework: Prove 
**[Proposition 1.](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/propI1.html)**

To construct an equilateral triangle on a given finite straight line.

You may want to use: https://www.geogebra.org/classic?lang=en to help you "see" things, but your solution should be an argument on paper.

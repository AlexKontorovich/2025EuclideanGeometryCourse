
Homework: Assume that the angles in a triangle always add up to less than 180 degrees.
Prove: That a pair of triangles with same angles are congruent!!! 

Set up: 

Goal : to prove that AAA implies not similarity but congruence!!! That is, that AB=DE etc

Fact (to be proved later): In any geometry (including Euclidean / hyperbolic etc), you can move lengths, and you can move angles.

| Moves                                                                                            | Rationale                                     |
| ------------------------------------------------------------------------------------------------ | --------------------------------------------- |
| 1. Given triangles ABC, DEF with $\angle A=\angle D$ etc                                         | Given                                         |
| 2. Underlying Postulate 5': Sum of angles in a triangle is $<180\degree$                         | Given                                         |
| 3. Therefore the sum of angles in a quadrilateral is also $<360\degree$                          | quad splits into two triangle, and angles add |
| 4. Assume by contradiction that $DE \ne AB$ hence one of them is longer, say $DE > AB$.          | Argue by contradiction                        |
| 5. Draw point G so that GD = AB.                                                                 | using compass tool                            |
| 6. Move the angle $\angle B$ over to $G$, and let $H$ be the point of intersection of GH with DF | There's a theorem that we can                 |
| 7. Triangles ABC and DGH are congruent                                                           | ASA                                           |
| 8. Therefore the angle DHG = $\angle C = \angle F$                                               | By congruence of triangles ABC and DGH        |
| 9. $\angle HGE = 180 - \angle G = 180 - \angle E$                                                | straight angles = 180                         |
| 10. $\angle GHF = 180 - \angle DHG = 180 - \angle F$                                             | straight angles = 180                         |
| 11. Sum of angles in quad $GHFE$ is $(180-E)+E+F +(180-F)=360$                                   | angles add                                    |
| 12. CONTRADICTION!!!                                                                             | contradicts step 3                            |
QED

![[Pasted image 20250709125922.png]]
--



In 1899, Hilbert rewrites all of Euclid.

Look back at Prop I.1 (constructing an equilateral triangle from its side length)

Instead: we'll do a straightedge and compass construction.

| Moves                                           | Rationale                          |
| ----------------------------------------------- | ---------------------------------- |
| 1. Given points A and B                         | By assumption                      |
| 2. Construct line segment between A and B       | Postulate 1                        |
| 3. Construct Circle with center A and radius AB | Postulate 3                        |
| 4. Construct Circle with center B and radius BA | Postulate 3                        |
| 5. Get point C where circles intersect          | GLARING GAP!!!                     |
| 6. Draw line segment from A to C                | P1                                 |
| 7. Draw line segment from B to C                | P1                                 |
| 8. AB = AC                                      | Both radii of Circle centered at A |
| 9. AB = BC                                      | Both radii of Circle centered at B |
| 10. BC = AC                                     | Common Notion 1 (transitivity)     |
QED
THERE IS A GLARING GAP IN THIS ARGUMENT!!!

[![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/79/Hilbert.jpg/250px-Hilbert.jpg)](https://en.wikipedia.org/wiki/File:Hilbert.jpg)
Hilbert says: We have to do mathematics purely formally if we don't want to make these kinds of mistakes.
Another major error in what Euclid sets up.
How does Euclid rule out "straight" lines being curved from some other viewpoint? Look back at the definition: 
The definitions are meaningless!! What does it mean to have a part or not? To be breadthless or not?

Just like we have to stop infinite recursion of logic, and start with unjustified axioms, and justify everything thereafter, we must also start with UNDEFINED terms and build on top of those.

We will not prejudice our minds with what "point" or "line" or "plane" or "circle" literally means, we will only say what you can logically *do* with those objects.

Famously, Hilbert said: take my entire reworking of Euclid's geometry, and replace every instance of "point" "line" and "plane" with "table", "chair", "beer bottle", and all the LOGIC should remain solid. 

Now we can start the course.

```
structure EuclideanPlane where
  Pt : Type -- undefined object
  Line : Type -- undefined!!!
  Circ : Type -- undefined
  Pt_on_Line : Pt -> Line -> Prop
  Line_of_Pts : forall a b : Pt, exists L : Line, (Pt_on_Line a L) and 
	  (Pt_on_Line b L) -- Postule 1
  -- Postulate 2 is not needed, all our "Lines" are already infinite
  Pt_on_Circ : Pt -> Circ -> Prop 
  Center_of_Circ : Pt -> Circ -> Prop 
  Circ_of_Pts : forall a b : Pt, exists alpha : Circ, (Center_of_Circ a alpha) 
	  and (Pt_on_Circ b alpha) -- Postulate 3
  

```

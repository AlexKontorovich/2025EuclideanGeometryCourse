Claim: We can now prove the Riemann Hypothesis! Or 1=2. The reason is: we (very subtly) let slip into our axioms a contradiction!!! And if you have a contradiction, you can prove anything!
```
theorem WhateverWeWant : 1 = 2 := by
	exfalso
	sorry
```
Step 1: use `exfalso` to convert whatever to `false`. The problem is that our version of Postulate 3 allows us to construct a circle with radius 0, but `Pts_of_Circ` implies (as we proved last time) that all radii are positive! 
we write:
```
have := Circ_of_Pts a a
obtain ⟨α, a_cent_α, a_on_α⟩ := this
```
to get a circle `α` of radius zero!!
```
theorem WhateverWeWant : 1 = 2 := by
exfalso
obtain ⟨a, _⟩ := Pt_Exists
have := Circ_of_Pts a a
obtain ⟨α, a_cent_α, a_on_α⟩ := this
have distPos := radius_pos a a α a_cent_α a_on_α
have distZero := dist_self a
-- new tactic: `rw` (rewrite)
-- I will write: `rw [distZero] at distPos`
-- this will look at `distPos` and try to find the LHS of `distZero`
-- namely, `dist a a`. If the tactic works (it finds LHS), then
-- it will replace it with the RHS.
rw [distZero] at distPos
exact (lt_self_iff_false 0).1 distPos
```
Obviously this is BAD
So we fix Postulate 3 to require a not equal to b
Let's go back to the proof of `in_Circ_of_center`


On to Prop I.2
Given a point A and a line segment BC. Goal: Draw at A a line segment of length BC.
With modern compasses, you just put the spike at B, and the pencil at C, tighten the compass and pick it up and move it to A. Or in GeoGebra, there's a tool called "Compass" that lets you do this:
![[Pasted image 20250723132447.png]]
But Euclid does not allow this!! His compass is "collapsing" -- it only works when it's first put down on paper. 
Question: Why can't you just use a ruler??? Euclid's geometry is *straightedge* and compass, not ruler! You don't have an axiom that allows you to mark your straightedge! 
Two pieces of homework:
1. State Prop I.2 formally
2. Solve this problem in natural language (star for formal solution!)
Go to: https://codespaces.new/leanprover-community/mathlib4

Make a free Github account, click "Create Codespace", wait 5 minutes until you see "ReadME"

Make a new file called "YourFave.lean"

```
import Mathlib -- importing the math library of Lean4  

class EuclideanPlane where
  Pt : Type -- undefined object
  Line : Type -- undefined!!!
  Circ : Type -- undefined
  Pt_on_Line : Pt → Line → Prop
  -- Postule 1: (Note: "∀" = "for all", "∃" = "there exists", "∧" = "and")
  Line_of_Pts : ∀ a b : Pt, ∃ L : Line, (Pt_on_Line a L) ∧ (Pt_on_Line b L)
  -- Postulate 2 is not needed, all our "Lines" are already infinite
  Pt_on_Circ : Pt → Circ → Prop
  Center_of_Circ : Pt → Circ → Prop
  -- Postulate 3:
  Circ_of_Pts : ∀ a b : Pt, ∃ α : Circ, (Center_of_Circ a α) ∧ (Pt_on_Circ b α)
  dist : Pt → Pt → ℝ
  -- `Circs_inter` "means:" generic, not tangential intersection
  Circs_inter : Circ → Circ → Prop 
  Pts_of_Circs_inter : ∀ α β : Circ, Circs_inter α β → ∃ a b : Pt,
	Pt_on_Circ a α ∧ Pt_on_Circ b α ∧ Pt_on_Circ a β ∧ Pt_on_Circ b β ∧ a ≠ b

--- homework : what are the actual conditions under which two circles intersect???

variable [EuclideanPlane]

namespace EuclideanPlane
```

lets try to state and prove Proposition I.1
first we need to define what it means for a triangle to be equilateral
Def: Given three points `a`, `b`, and `c`, they are the corners of an equilateral triangle
if: dist from `a` to `b` = dist from `b` to `c` AND dist from `a` to `b` = dist `a` to `c`
```
def IsEquilateralTriangle (a b c : Pt) : Prop := (dist a b = dist b c) ∧ (dist a b = dist a c)
```
  
  Statement of Prop I.1: Given two points `a` and `b`, there exists a point `c` so that 
   `a`, `b`, and `c` form an equilateral triangle

```
theorem PropIp1 (a b : Pt) : ∃ (c : Pt), IsEquilateralTriangle a b c := by
-- " := by " that's the beginning of the proof
/-
What is the current goal state?? (" ⊢ " = "goal")
a b : Pt
⊢ ∃ (c : Pt), IsEquilateralTriangle a b c
-/
-- Step 1: Create a circle centered at `a` with `b` on the circle (using Postulate 3)
-- Let's have the fact that `Circ_of_Pts`:
have := Circ_of_Pts a b
/-
Goal state:
a b : Pt
this : ∃ α, Center_of_Circ a α ∧ Pt_on_Circ b α
⊢ ∃ c, IsEquilateralTriangle a b c
-/
-- need to obtain the circle and two properties
obtain ⟨α, a_center_of_α, b_on_α⟩ := this
/-
New goal state:
a b : Pt
α : Circ
a_center_of_α : Center_of_Circ a α
b_on_α : Pt_on_Circ b α
⊢ ∃ c, IsEquilateralTriangle a b c
-/
-- Step 2: Draw circle with center `b` passing through `a`
have Vaibhav := Circ_of_Pts b a
obtain ⟨β, b_center_of_β, a_on_β⟩ := Vaibhav
```

![[Pasted image 20250710152356.png]]
![[Pasted image 20250710152426.png]]
Homework : what are the actual conditions under which two circles intersect???
Recall:
**[Postulate 1](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post1.html).**
To draw a straight line from any point to any point.

**[Postulate 2](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post2.html).**
To produce a finite straight line continuously in a straight line.

**[Postulate 3](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post3.html).**
To describe a circle with any center and radius.

**[Postulate 4](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post4.html).**
That all right angles equal one another.

**[Postulate 5](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/post5.html).**
That, if a straight line falling on two straight lines makes the interior angles on the same side less than two right angles, the two straight lines, if produced indefinitely, meet on that side on which are the angles less than the two right angles.

**[Proposition 1.](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/propI1.html)**
To construct an equilateral triangle on a given finite straight line.

More formally: we are given points A and B. Goal: construct an equilateral triangle. 
If we just use the GeoGebra built-in tool to construct regular $n$-gons, that's cheating because there's no $n$-gon Tool Postulate!

Instead: we'll do a straightedge and compass construction.

| Moves                                           | Rationale                          |
| ----------------------------------------------- | ---------------------------------- |
| 1. Given points A and B                         | By assumption                      |
| 2. Construct line segment between A and B       | Postulate 1                        |
| 3. Construct Circle with center A and radius AB | Postulate 3                        |
| 4. Construct Circle with center B and radius BA | Postulate 3                        |
| 5. Get point C where circles intersect          |                                    |
| 6. Draw line segment from A to C                | P1                                 |
| 7. Draw line segment from B to C                | P1                                 |
| 8. AB = AC                                      | Both radii of Circle centered at A |
| 9. AB = BC                                      | Both radii of Circle centered at B |
| 10. BC = AC                                     | Common Notion 1 (transitivity)     |
QED

Fast forward 2000 years:
People were very bothered by the 5th postulate. It's way longer than the others. Not so "self-evident". Felt more like a "Theorem" (a fact to be proven from more basic facts)

In the 19th century (Gauss, Lobichevsky, Bolyai ,... , Riemann , Poincare) people tried to assume that the 5th postulate is False, and prove a cascade of consequences, hoping to find a contradiction!
They did not manage to come up with a definitive contradiction. But proved all kinds of crazy sounding stuff like: 

Homework: Assume that the angles in a triangle always add up to less than 180 degrees.
Prove: That a pair of triangles with same angles are congruent!!! 

So....???

Slight detour:
# "Platonic solids"
3-D shape that mimics the "perfect" symmetry of a regular $n$-gon
- all sides (faces) are the same 
- all edges are the same
- all angles are the same ($\Longrightarrow$ faces are all regular $n$-gons, and the same ones)
Case 1: Bring 3 equilateral triangles together at one corner ("Tetra - hedron" 4-sided)
[![Tetrahedron - 3d geometric solid - Polyhedr.com](https://polyhedr.com/images/polyhedra/001/Tetrahedron350x350.jpg)![Tetrahedron - 3d geometric solid - Polyhedr.com](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR5sxhKU5ot3bIedX6XBVNqoHflrfy_VGD2BA&s)](https://www.google.com/url?sa=i&url=https%3A%2F%2Fpolyhedr.com%2Ftetrahedron.html&psig=AOvVaw2j-0tQ5c_IS5wjjLKCSvKN&ust=1752080101554000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCPjpwpLdrY4DFQAAAAAdAAAAABAE)

Case 2 : bring 4 equilateral triangles together (square pyramid), double it, get Octahedron:
[![Octahedron - 3d geometric solid - Polyhedr.com](https://polyhedr.com/images/polyhedra/002/Octahedron350x350.jpg)![Octahedron - 3d geometric solid - Polyhedr.com](https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcSlinx-NljLhur2S3bjvSD-vk4J17F0aJz7hKuWZOKGBs0UrAHVpQRVexzCCyt5NvUFwPHWXQ)](https://www.google.com/url?sa=i&url=https%3A%2F%2Fpolyhedr.com%2Foctahedron2.html&psig=AOvVaw3xsHIqSi6g-k2e7jNRJIEZ&ust=1752080231899000&source=images&cd=vfe&opi=89978449&ved=0CBAQjRxqFwoTCJDlgdHdrY4DFQAAAAAdAAAAABAE)
Case 3: bring 5 equilateral triangles together : Icosahedron (20-gon)

![[Pasted image 20250708130034.png]]

-Case 4:-  bring 6 equilateral triangles together: 

Each triangle has 60 degrees at its corner, so 6 of them meeting at a corner make a total of 360 degrees, so you get a tiling of the plane by equilateral triangles
[![Triangular tiling - Wikipedia](https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Tiling_3_simple.svg/330px-Tiling_3_simple.svg.png)![Triangular tiling - Wikipedia](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqi2N3AqSg6qf_dBSG4BG1Ycp7M5bYwEVFwg&s)](https://www.google.com/url?sa=i&url=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FTriangular_tiling&psig=AOvVaw39837H4y9f6W__FM9z9oHJ&ust=1752080572410000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCPCW9fLerY4DFQAAAAAdAAAAABAE)

Aside: 7 equilateral triangles together at a corner tile the "hyperbolic plane" 
[![Crocheted Hyperbolic Planes | Visions in Math](https://mathvis.academic.wlu.edu/files/2016/05/IMG_4718.jpg)![Crocheted Hyperbolic Planes | Visions in Math](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbYDMej4IxzZes9dhk5eEJ4j4rSY4A2GE4Xg&s)](https://www.google.com/url?sa=i&url=https%3A%2F%2Fmathvis.academic.wlu.edu%2F2016%2F06%2F15%2Fcrocheted-hyperbolic-planes%2F&psig=AOvVaw3e6JLl8pBwTX05jYX6vPp6&ust=1752080701768000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCMiYoLDfrY4DFQAAAAAdAAAAABAL)

We're run out of room with triangles

Case 4: squares. 3 squares at a corner (vertex) : CUBE !

-Case 5 :-  4 squares meeting at a corner NO GOOD!! $90\times 4=360$ This tiles the plane

Done with squares

Case 5: Regular Pentagons. A pentagon can be broken into 3 triangles, so has a total angle sum of 540. And $540\div 5 = 108$. Can put 3 together at a corner.  Get a dodecahedron (12 sides)
![[Pasted image 20250708131353.png]]Done with pentagons

-Case 6:- hexagons (regular). How big is each angle? Hexagons are broken in 4 triangles. Each triangle gives 180 degrees. So total angle sum is $180\times 4 = 720$. Each vertex gets the same amount, and $720\div 6 = 120$. (Ofcourse : hexagon is 6 equilateral triangles, two coming together at each corner. ) So 3 hexagons tile the plane! 

All larger $n$-gons can't even fit 3 in a corner without going hyperbolic.

We have completely classified the "Platonic" solids.
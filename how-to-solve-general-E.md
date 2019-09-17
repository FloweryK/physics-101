# How to calculate E-flux of a surface S, when E is not uniform?

## Introduction
General definition of E-flux is like this:

$$
\Phi_E = \int_S \vec{E} \cdot d\vec{A}
$$

where E is the electric field, dA is the infinitesimal area vector.

In order to calculate the flux in actual situation, I recommend you to remind the following order:
#### 1. First, think about what dA vector is.
<b>REMEMBER</b>, dA vector is a VECTOR, not just an scalar value. dA vector has its size, and is perpendicular to the surface. Therefore, I recommend you to first separate them into two parts:

$$
d\vec{A} = |d\vec{A}| \,\, \hat{n}
$$
Well, the first part of dA vector is just its absolute value, |dA|, and later part, n-hat, is the normal vector that is parallel to dA vector.
(You may wonder what is the odd triangular shape above 'n' character. It's called 'hat' sign, which represent that the vector is an unit vector. You might heard of k-hat which represent an unit vector for z-direction.)

#### 2. Second, choose your coordinate system.
Now, you should choose which coordinate you will use: It will give you specified format for your |dA| and n-hat vector. Before you choose the coordinate, you should carefully see how your problem describes (1) E-field (2) and the integral surface. In many cases, you might follow the coordinate they use. Here are some examples you might encounter frequently:

- Cartesian coordinate: |dA| = dx dy
- Polar coordinate: |dA| = r dr dθ

Your choice of the coordinate will dramatically change the difficulty of your problem. If you choose a good coordinate, it will give you short, easy answer. If not, well, you have a long, long way to go.

#### 3. Finally, calculate the integral.
There's any further tips left for this part. There are only mathematical things left. So be prepared.

$$
\Phi_E
= \int_S \vec{E} \cdot d\vec{A}
= \int_S (\vec{E} \cdot \hat{n}) |d\vec{A}|
$$

## Now, let's solve an actual example
<b>Question</b>
(Prob. 21.45 in your textbook) An electric field is given as below. Find the flux through the square in the x-y plane bounded by the points (0,0), (0,a), (a,a), (a,0).

$$
\vec{E} = E_0 \, (y/a) \, \hat{k}
\\ where \, E_0, \, a \,\, are \,\, constants.
$$

<b>Answer</b>
1. First: choose your coordinate. You might consider using cartesian coordinate because (1) E-field is described in Cartesian (2) and the surface is flat on x-y plane. Then your dA vector is:
$$
d\vec{A} = |d\vec{A}| \, \hat{n} = (dx \, dy) \, \hat{n}
$$
Here, normal vector n is perpendicular to x-y plane. It means that n-hat is just an z-directional unit vector, k-hat. Therefore:
$$
d\vec{A}
= (dx \, dy) \, \hat{n}
= (dx \, dy) \, \hat{k}
$$

2. Second: there's no second. Just do the calculation.
$$
\Phi_E
= \int_{x=0}^{x=a} \int_{y=0}^{y=a}(\vec{E}(y) \cdot \hat{k}) \, dx \, dy
\\
= \int_{x=0}^{x=a} \int_{y=0}^{y=a}(E_0 \frac{y}{a} \, \hat{k} \cdot \hat{k}) \, dx \, dy
\\
= \frac{E_0}{a}\int_{x=0}^{x=a} \int_{y=0}^{y=a}(y \, \hat{k} \cdot \hat{k}) \, dx \, dy
\\
= \frac{E_0}{a} \int_{x=0}^{x=a} \int_{y=0}^{y=a} y \, dx \, dy
\\
= \frac{E_0}{a} \int_{x=0}^{x=a} [\frac{y^2}{2}]_{y=0}^{y=a} \, dx
\\
= \frac{E_0}{a} \frac{a^2}{2} \int_{x=0}^{x=a} \, dx
\\
= \frac{E_0}{a} \frac{a^2}{2} \cdot a
\\
= \frac{E_0}{2} \cdot a^2
$$
Done.

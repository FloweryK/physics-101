# From Potential Energy to Electric Dipole

## 1. The concept of potential energy

### 1.1 Where does potential energy comes from?

Before we start, let's think about the relationship between Work and Kinetic energy.

```bash
When we push something, it gains speed.
Here:
- work: the action of pushing the thing
- kinetic energy: a value that is related to the speed
```
or, we can just write an equation equivalent to the above:
```bash
Work (me->the thing) = (change of) kinetic energy of the thing
```

or even simpler, we can say:
$$
W = \Delta K
$$

You might remember that work can be represented as integral form as:
$$
W = \int_{initial}^{final} \vec{F} \cdot d\vec{s}
$$

At this point, let's care more about the "indefinite integral" in above equation. Let's say:
$$
U \equiv - \int \vec{F} \cdot d\vec{s} + C
$$

where C is an arbitrary scalar value.

Well, this U does not have any name... yet. I know you're eager to call it as 'potential energy', but let's act like we know nothing here. For now, it's just a simple "minus - indefinite integral" now.

Then we finally have:
$$
-(U(final)-U(initial)) = K(final) - K(initial)
$$

or, more intuitive equation is:
$$
K(initial) + U(initial) = K(final) + U(final)
$$

Well, it seems that U function is working as a 'potential' kinetic energy. So let's name it as 'potential energy'. Then we might say: "Hey, the total 'ENERGY' is conserved!".

(Or we might call K as 'potential' potential energy. Who knows?)

So the answer is: <b>The concept of potential energy comes from the energy conservation law.</b>

### 1.2 What should we do about C?

OK, some would be uncomfortable with the constant C that suddenly appeared when defining U. It's an purely mathematical value that comes from indefinite integrals. Then how can we handle it?

As we have total freedom of choosing C, we conventionally choose C as zero. This makes many problems a lot easier. Of course, there are few that requires non-zero C. But trust me, you will intuitively know the value you should choose when solving the problem. So don't worry.

So the answer is: <b>Conventionally, we choose C as zero.</b>

### 1.3 Is there an alternative way of understanding U?

From the previous sections, we accepted the concept of potential energy from the concept of work and kinetic energy. One of many beautiful things in physics, however, is that we can understand one concept in many ways. This section introduces more short but deep way of understanding nature in 'field' way.

When we have a vector function v, we can always find a corresponding scalar function A that satisfies the following equation:

$$
\vec{v} = \nabla A
$$

As you may see here, the scalar field has a freedom of adding an arbitrary constant scalar value:

$$
A \rightarrow A + \lambda \, (constant)
\\
\nabla(A+\lambda) = \nabla A
$$

as a derivative of a scalar value is always zero.

Now, we have a vector field, which we call 'Force'. Then there should be always a corresponding scalar field for the force vector. Well, we already know the answer as:

$$
\vec{F} = \nabla (-U) = -\nabla U
$$

Of course, we have the freedom of choosing U as well:

$$
U \rightarrow U + \lambda \, (constant)
\\
-\nabla (U+\lambda) = -\nabla U
$$

This way of understanding the potential energy is somewhat opposite to what we think about the nature with force. What we know as 'force' is actually the minus-gradient of some scalar field, what we call 'potential energy'. Moreover, now we can explain the meaning of F=-∇U: "Every motion prefers low potential energy."

So the answer is: <b>Yes, there are tremendous ways of understanding nature.</b>

### 1.4 TIPS

#### TIP 1: Does nature always prefers low energy?
Maybe there's someone who wants to argue that the statement is wrong: "NOT everything prefers low energy!". Well, some is right, and the other is wrong. There are many quantities you should consider in real situations, like entropy, enthalpy, free energy, etc. But in my experience, at least in our level of mechanics, you might only think about the 'low-potential-law'.

#### TIP 2: Do we actually need the concept of energy?
If you deal with some exercises in your textbook, you might realize how hard it is to solve problems without energy. Every moment you should calculate the speed of everything only with differential equations (Newton's law). Instead, if we do accept the concept of energy, you can just use the energy conservation law. That all. Therefore, YES, we need the concept of energy.

#### TIP 3: Do I have to always care about every plus or minus sign of integrals?
In actual calculations (when doing homework or taking exams), the sign of integrals will always blow your mind. I saw many students who got troubles with plus or minus signs, especially when they have to consider dot products of F (force) and ds (infinitesimal parameter).

It would be nice if we can carefully calculate every sign and get the right result, like a master of physics and mathematics. But sometimes, reality hits you hard. Your signs go wrong somewhere, and we think about what we have got wrong from the beginning. A total nightmare. In such cases, be free to think about the actual phenomenon. This is what PHYSICS is all about!

There's only one thing you should remind: 'nature prefers low energy.'

As an example, let's calculate the potential energy of gravity. But here, <b>I will intentionally put wrong signs so that we can fix it at the end of the calculation</b>:

$$
U(r)
= -\int_{\infty}^{\vec{r}}  \vec{F}_{gravity} \cdot d\vec{s}
= \int_{\infty}^{r} -\frac{GMm}{s^2}ds
= [\frac{GMm}{s}]_{\infty}^{r} = \frac{GMm}{r}
$$

Is the result good? Well, in order to check you did right or not, let's see what's actually happening with the result: It seems that the potential energy increases when we get close to the source of gravity (r->0). We remember that the nature prefers low energy position. Therefore, what our equation is saying is that source 'somehow' pushes the things around it.

Oops... is this really THE gravity we know? Pushing everything, instead of pulling? I think not. There should be something wrong. It seems that the problem comes from somewhere in the signs. So let's just flip the sign and pretend we have calculated everything right from the start :)

$$
U(r) = - \frac{GMm}{r}
$$

Now, the potential decreases when we go to the source of gravity. As everything prefers low energy position, things will move towards the source. This is seems OK with the gravity we know.

(You may notice that U(r) is actually ΔU from infinity to r. If we set U(∞) = 0, however, ΔU = U(r) - U(∞) = 0.)

## 2. Potential energy of an eletric dipole

### 2.1 How can we calculate an electric dipole's potential energy?

#### Before we start
Let's assume that the motion is in xy plane and E field is parallel to x axis.

Now, let's see how potential difference are represented in torque way:

$$
ΔU = U(\theta_f)-U(\theta_i) = - \int_{\vec{\theta_i}}^{\vec{\theta_f}} \vec{\tau} \cdot d\vec{\theta}
$$

You may see that the integral is related to torques and angles. We have two elements in a single dipole: a positive charge and negative charge. We have to be very careful about the choice of coordinate, as torques and angles may change depending on the coordinates. In many cases, good coordinate choice makes a problem a lot easier. To see the difference, let's see the bad choice first and good choices later.

#### Bad choice: general coordinate
Unfortunately, we cannot say that the ranges of dθ for positive charge and negative charge are the same. therefore, we should do the integral in two parts: one for the positive charge, and the other for the negative charge.

$$
\Delta U_p = - \int_{\vec{\theta_{p,i}}}^{\vec{\theta_{p,f}}} \vec{\tau_p} \cdot d\vec{\theta} = - \int_{\vec{\theta_{p,i}}}^{\vec{\theta_{p,f}}} (\vec{r_p}(\theta) \times q\vec{E}) \cdot d\vec{\theta}
\\
\Delta U_n = - \int_{\vec{\theta_{n,i}}}^{\vec{\theta_{n,f}}} \vec{\tau_n} \cdot d\vec{\theta} = - \int_{\vec{\theta_{n,i}}}^{\vec{\theta_{n,f}}} (\vec{r_n}(\theta) \times (-q)\vec{E}) \cdot d\vec{\theta}
$$

(Here, p is for positive and n is for negative.)

Some might eager to merge those two potentials to one as:

$$
\Delta U = \Delta U_p + \Delta U_n = - \int (\vec{r_p}-\vec{r_n}) \times q\vec{E}) \cdot d\vec{\theta} \,\,\, (Wrong!)
$$

This is wrong. Generally, we cannot say that [θ(p,i), θ(p,f)] and [θ(n,i),θ(n,f)] are equal. Moreover, position vector is now a function of θ. Therefore we cannot simply merge them.

Q1. What should I do then?
A1. Analyzing all the relationships between angles and positions.
Q2. Will I do that?
A2. No. It's too complicated. I give up :(


#### Good choice: coordinate origin at the center of dipole
Fortunately, now we can say the the ranges of dθ for the positive and the negative charge are somewhat related: if the positive one has [θ(i),θ(f)], then the negative one has [π+θ(i),π+θ(f)]. What's more, now r_p and r_n have the same size with opposite directions. These will allow us to merge the two integrals.

$$
\Delta U_p
= - \int_{\vec{\theta_{i}}}^{\vec{\theta_{f}}} (\vec{r_p} \times q\vec{E}) \cdot d\vec{\theta}
= -\int_{\theta_i}^{\theta_f} q \, r_p \, E \, (-sin\theta)d\theta
\\
\Delta U_n
= -\int_{\vec{\pi}+\vec{\theta_{i}}}^{\vec{\pi}+\vec{\theta_{f}}} (\vec{r_n} \times (-q)\vec{E}) \cdot d\vec{\theta}
=-\int_{\pi+\theta_i}^{\pi+\theta_f} (-q) \, r_n \, E \, sin\theta \, d\theta
$$

(※ About the signs of cross products:
  - The cross product in the positive charge has minus sign, as the rotation from r_p to E is clockwise.
  - The cross product in the negative charge has plus sign, as the rotation from r_n to E is anti-clockwise.)

Thanks to our choice of the coordinate, the length of r_n is equal to r_p. In order to merge the integrals, we may handle a little bit about the negative charge term:

$$
\theta \equiv \pi+\theta'
\\
d\theta = d(\pi+\theta')=d\theta'
\\
then \,\, \theta' \in \,[\theta_i, \theta_f]
$$

so that the negative charge term become:

$$
\Delta U_n
= -\int_{\pi+\theta_i}^{\pi+\theta_f} (-q) \, r_n \, E \, sin\theta \, d\theta
= \int_{\theta_i}^{\theta_f} q \, r_p \, E \, sin(\theta'-\pi) \, d\theta'
= \int_{\theta_i}^{\theta_f} q \, r_p \, E \, sin\theta \, d\theta
$$

As you may see, this is exactly the same as the positive term. Therefore, we can now express the potential difference from θ_i to θ_f as:

$$
\Delta U = \Delta U_p + \Delta U_n
= \int_{\theta_i}^{\theta_f} 2 \, q\, r_p \, E \, sin\theta \, d\theta
= - 2q \, r_p \, E \, (cos \, \theta_f - cos \, \theta_i)
= -|\vec{p}||\vec{E}|(cos \, \theta_f - cos \, \theta_i)
$$

Well, you should always remember that this is the potential DIFFERENCE. Then what about the potential itself? As you may see from the very above section, it depends on your choice. You may generally write the potential energy of dipole as:

$$
U(\theta)
= -|\vec{p}||\vec{E}| cos\theta + C
= -\vec{p} \cdot \vec{E} + C
\\
so \,\, that \,\, \Delta U = U(\theta_f)-U(\theta_i)
$$

where C represents an arbitrary scalar value. The conventions for dipole moment is setting C as zero. Therefore, we have:

$$
U(\theta)
= -\vec{p} \cdot \vec{E}
$$

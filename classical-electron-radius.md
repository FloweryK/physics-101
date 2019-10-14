# 전자의 반지름을 고전적인 방식으로 유추하기


$$
\rho = \frac{e}{\frac{4\pi R^3}{3}} = \frac{3e}{4 \pi R^3}
$$

$$
dU = \frac{k \, q(r)}{r}dq
$$

$$
q(r) = \rho \frac{4\pi r^3}{3}
\\
dq = \rho \, 4\pi r^2 \, dr
$$

$$
dU
= \frac{k}{r} \cdot \rho \frac{4\pi r^3}{3} \cdot \rho \, 4\pi r^2 \, dr
\\
= \frac{k}{r} \cdot \rho \frac{4\pi r^3}{3} \cdot \rho \, 4\pi r^2 \, dr
\\
= \frac{16 \pi^2}{3} k \rho^2 \, r^4 dr
$$

$$
U(R)
= \int_{0}^{R} \frac{16 \pi^2}{3} k \rho^2 \, r^4 dr
\\\\
= \frac{16 \pi^2}{3} k \rho^2 \, \frac{R^5}{5}
\\
= \frac{16 \pi^2}{3} \cdot k \cdot \frac{9e^2}{16 \pi^2 R^6} \, \frac{R^5}{5}
\\
= \frac{3}{5} \frac{ke^2}{R}
$$

$$
U(R) = m_e c^2
\\
R = \frac{3}{5} \frac{ke^2}{m_e c^2} \sim 10^{-15}m
$$

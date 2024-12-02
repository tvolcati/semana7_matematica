# Resolução da Atividade – Ondas Eletromagnéticas e Derivada Direcional

---

## ITEM 1 – Vetor de Poynting

### a) Expressão Geral para o Vetor de Poynting

A fórmula do vetor de Poynting é:

```math
\vec{S} = \frac{1}{\mu_0} \vec{E} \times \vec{B}
```

Substituímos as expressões de \(\vec{E}(x, y, z)\) e \(\vec{B}(x, y, z)\):

```math
\vec{E}(x, y, z) = (3x, y^2, z - x)
\quad
\vec{B}(x, y, z) = (2y, x - z, z^2) \cdot 10^{-6}
```

O produto vetorial é calculado como o determinante:

```math
\vec{E} \times \vec{B} =
\begin{vmatrix}
\hat{i} & \hat{j} & \hat{k} \\
3x & y^2 & z - x \\
2y & x - z & z^2 \cdot 10^{-6}
\end{vmatrix}
```

Expandimos o determinante por cofactores:

1. **Componente \( \hat{i} \):**
```math
\hat{i} \cdot \left( (y^2)(z^2 \cdot 10^{-6}) - (z - x)(x - z) \right)
```

2. **Componente \( \hat{j} \):**
```math
-\hat{j} \cdot \left( (3x)(z^2 \cdot 10^{-6}) - (z - x)(2y) \right)
```

3. **Componente \( \hat{k} \):**
```math
\hat{k} \cdot \left( (3x)(x - z) - (2y)(y^2 \cdot 10^{-6}) \right)
```

Substituímos para obter a expressão geral:

```math
\vec{E} \times \vec{B} = 
\hat{i} \cdot \left( y^2 z^2 \cdot 10^{-6} - (z - x)(x - z) \right) -
\hat{j} \cdot \left( 3x z^2 \cdot 10^{-6} - (z - x)(2y) \right) +
\hat{k} \cdot \left( 3x(x - z) - 2y y^2 \cdot 10^{-6} \right)
```

---

### b) Intensidade no ponto (1, 2, 1)

Substituímos \(x = 1\), \(y = 2\), \(z = 1\) nas funções de \(\vec{E}\) e \(\vec{B}\):

```math
\vec{E}(1, 2, 1) = (3, 4, 0)
\quad
\vec{B}(1, 2, 1) = (4, 0, 1) \cdot 10^{-6}
```

Calculamos o produto vetorial:

```math
\vec{E} \times \vec{B} =
\begin{vmatrix}
\hat{i} & \hat{j} & \hat{k} \\
3 & 4 & 0 \\
4 & 0 & 1 \cdot 10^{-6}
\end{vmatrix}
```

Expandimos:

1. **Componente \( \hat{i} \):**
```math
\hat{i} \cdot \left( (4)(1 \cdot 10^{-6}) - (0)(0) \right)
= \hat{i} \cdot 4 \cdot 10^{-6}
```

2. **Componente \( \hat{j} \):**
```math
-\hat{j} \cdot \left( (3)(1 \cdot 10^{-6}) - (0)(4) \right)
= -\hat{j} \cdot 3 \cdot 10^{-6}
```

3. **Componente \( \hat{k} \):**
```math
\hat{k} \cdot \left( (3)(0) - (4)(4) \right)
= \hat{k} \cdot -16
```

O resultado do produto vetorial:

```math
\vec{E} \times \vec{B} = (4 \cdot 10^{-6}) \hat{i} - (3 \cdot 10^{-6}) \hat{j} - 16 \hat{k}
```

Intensidade do vetor de Poynting:

```math
|\vec{S}| = \frac{1}{\mu_0} |\vec{E} \times \vec{B}|
```

Substituímos 
```math
( \mu_0 = 4\pi \cdot 10^{-7} \, \mathrm{H/m} ).
```
---

## ITEM 2 – Derivada Direcional

### a) Derivada direcional no ponto (1, 2, 1)

A função é:

```math
I(x, y, z) = 0.796(y^2z^2 + 2xyz + 3x^2)
```

Calculamos o gradiente no ponto \((1, 2, 1)\):

1. Derivada parcial em relação a \(x\):
```math
\frac{\partial I}{\partial x} = 0.796(2yz + 6x)
```
Substituímos \(x = 1, y = 2, z = 1\):
```math
\frac{\partial I}{\partial x} = 0.796(2(2)(1) + 6(1)) = 0.796(4 + 6) = 7.96
```

2. Derivada parcial em relação a \(y\):
```math
\frac{\partial I}{\partial y} = 0.796(2y z^2 + 2xz)
```
Substituímos \(x = 1, y = 2, z = 1\):
```math
\frac{\partial I}{\partial y} = 0.796(2(2)(1^2) + 2(1)(1)) = 0.796(4 + 2) = 4.78
```

3. Derivada parcial em relação a \(z\):
```math
\frac{\partial I}{\partial z} = 0.796(2y^2 z + 2xy)
```
Substituímos \(x = 1, y = 2, z = 1\):
```math
\frac{\partial I}{\partial z} = 0.796(2(2)^2(1) + 2(1)(2)) = 0.796(8 + 4) = 9.55
```

O gradiente é:

```math
\nabla I = (7.96, 4.78, 9.55)
```

Direção do vetor \(\vec{u} = (2, 3, 1)\):

1. Norma do vetor:
```math
\|\vec{u}\| = \sqrt{2^2 + 3^2 + 1^2} = \sqrt{4 + 9 + 1} = \sqrt{14}
```

2. Versor do vetor:
```math
\hat{u} = \left(\frac{2}{\sqrt{14}}, \frac{3}{\sqrt{14}}, \frac{1}{\sqrt{14}}\right)
```

Produto escalar para derivada direcional:

```math
D_u I = \nabla I \cdot \hat{u}
```

---

### b) Versor da máxima taxa de variação

O versor da máxima taxa de variação é a direção do gradiente normalizada:

1. Norma do gradiente:
```math
\|\nabla I\| = \sqrt{(7.96)^2 + (4.78)^2 + (9.55)^2} \approx 13.32
```

2. Versor:
```math
\hat{v} = \frac{\nabla I}{\|\nabla I\|} = \left(\frac{7.96}{13.32}, \frac{4.78}{13.32}, \frac{9.55}{13.32}\right)
```

```math
\hat{v} \approx (0.598, 0.359, 0.717)
```

---


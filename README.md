# The Vector Space Rules
## Group 1️⃣: Rules that make addition behave sensibly (5 rules)

These ensure **vector addition behaves like normal addition**.

### 1. Closure under addition

If **${v}$** and **${w}$** are in the space, then **${v + w}$** is also in the space

📌 Without this: adding vectors could throw you outside the universe.

---

### 2. Commutativity

$$
{v + w = w + v}
$$

📌 Direction shouldn’t depend on order.

---

### 3. Associativity

$$
{(v + w) + u = v + (w + u)}
$$

📌 Grouping shouldn’t change meaning.

---

### 4. Additive identity (zero vector)

$$
{v + 0 = v}
$$

📌 There must be a “do nothing” vector.

---

### 5. Additive inverse

$$
{v + (−v) = 0}
$$

📌 Every move must be undoable.

---

## Group 2️⃣: Rules that make scaling behave sensibly (4 rules)

These ensure **scalars interact cleanly with vectors**.

### 6. Closure under scalar multiplication

${αv}$ is in the space for any scalar ${α}$

📌 Otherwise scaling could destroy structure.

---

### 7. Distributivity over vector addition

$$
{α(v + w) = αv + αw}
$$

📌 Scaling a sum should match summing scaled parts.

---

### 8. Distributivity over scalar addition

$$
{(α + β)v = αv + βv}
$$

📌 Multiple scalings should combine logically.

---

### 9. Associativity of scalar multiplication

$$
{α(βv) = (αβ)v}
$$

📌 Scaling order must not matter.

---

## Group 3️⃣: Rule that links vectors to numbers (1 rule)

### 🔟 Scalar identity

$$
{1 · v = v}
$$

📌 Multiplying by “one” should change nothing.



---

$$
{\color{yellow}\text{***************************************************************************************************}}
$$


# Linear Transformation Rules


## 1️⃣ Rule 1: Additivity (preserve addition)

$$
\boxed{T(v + w) = T(v) + T(w)}
$$

Meaning:

Transforming ${a}$ sum = summing the transforms

---

##  2️⃣ Rule 2: Homogeneity (preserve scaling)

$$
\boxed{T(\alpha v) = \alpha T(v)}
$$

Meaning:

Scaling first or transforming first gives the same result

---

$$
{\color{yellow}\text{***************************************************************************************************}}
$$

# EigenValues & Eigenvectors 

${\Rightarrow}$ An **eigenvector** is a **non-zero vector whose direction does not change** under a linear transformation — only its length may change.

If direction changes → **not** an eigenvector.

---

## 2️⃣ The defining equation (this is the ONLY starting point)

For a matrix ${A}$:

$$
{\boxed{A\mathbf{v} = \lambda \mathbf{v}}}
$$

Where:

* ${\mathbf{v} \neq 0}$ → eigenvector
* ${\lambda}$ → eigenvalue (scaling factor)

This equation **defines** eigenvalues & eigenvectors.
Everything else comes from this.

---

## 3️⃣ Why this equation makes sense (intuition)

* ${A\mathbf{v}}$ → apply transformation
* ${\lambda\mathbf{v}}$ → same direction, scaled

So:

* Same direction ✔
* Possibly stretched or flipped ✔

---

## 4️⃣ Turning the definition into a solvable formula

Start from:

$$
{A\mathbf{v} = \lambda \mathbf{v}}
$$

Move everything to one side:

$$
{A\mathbf{v} - \lambda \mathbf{v} = 0}
$$

Factor out (\mathbf{v}):

$$
{(A - \lambda I)\mathbf{v} = 0}
$$

This is the **core equation**.

---

## 5️⃣ The NON-TRIVIAL condition (very important)

The equation:

$$
{(A - \lambda I)\mathbf{v} = 0}
$$

has:

* trivial solution ${\mathbf{v}=0}$ → useless ❌
* non-zero solution → eigenvector ✔

A non-zero solution exists **only if**:

$$
{\boxed{\det(A - \lambda I) = 0}}
$$

👉 **THIS is the eigenvalue rule**

---

## 6️⃣ Step-by-step RULES to find eigenvalues

### RULE 1: Form ${A - \lambda I}$

Subtract ${\lambda}$ from the diagonal of ${A}$.

---

### RULE 2: Take determinant

$$
{\det(A - \lambda I)}
$$

---

### RULE 3: Set determinant = 0

$$
{\det(A - \lambda I) = 0}
$$

This gives the **characteristic equation**.

---

### RULE 4: Solve for ${\lambda}$

Solutions are the **eigenvalues**.

---

## 7️⃣ Full worked example (ℝ², no shortcuts)

Let:

$$
{A = \begin{bmatrix}
2 & 1 \\
1 & 2
\end{bmatrix}}
$$

---

### Step 1: Compute ${A - \lambda I}$

$$
{\begin{bmatrix}
2-\lambda & 1 \\
1 & 2-\lambda
\end{bmatrix}}
$$

---

### Step 2: Determinant

$$
{(2-\lambda)^2 - 1}
$$

---

### Step 3: Set equal to zero

$$
{(2-\lambda)^2 - 1 = 0}
$$

---

### Step 4: Solve

$$
{(2-\lambda)^2 = 1}
$$

$$
{2-\lambda = \pm 1}
$$

$$
{\lambda = 1, \\, 3}
$$

✅ **Eigenvalues found**

---

## 8️⃣ RULES to find eigenvectors (for each eigenvalue)

For **each** eigenvalue (\lambda):

---

### RULE 5: Plug (\lambda) back into

$$
{(A - \lambda I)\mathbf{v} = 0}
$$

---

### RULE 6: Solve the linear system

This gives eigenvectors.

---

## 9️⃣ Eigenvector example (complete)

### For ${\lambda = 3}$

$$
{
A - 3I =
\begin{bmatrix}
-1 & 1 \\
1 & -1
\end{bmatrix}
}
$$

Solve:

$$
{
-x + y = 0 \Rightarrow y = x
}
$$

Eigenvectors:

$$
{
\mathbf{v} =
\begin{bmatrix}
1 \\
1
\end{bmatrix} \,
\begin{bmatrix}
2 \\
2
\end{bmatrix} \,
\text{etc.}
}
$$

(Any non-zero multiple)

---

### For ${\lambda = 1}$

$$
{
A - I =
\begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}
}
$$

Solve:

$$
{
x + y = 0
\Rightarrow y = -x
}
$$

Eigenvectors:

$$
{
\begin{bmatrix}
1 \\
-1
\end{bmatrix}
}
$$


---

## 🔟 Important rules people forget (memorize)

### Rule A: Eigenvectors are NEVER unique

If ${\mathbf{v}}$ is one → ${c\mathbf{v}}$ also is.

---

### Rule B: Zero vector is NEVER an eigenvector

By definition.

---

### Rule C: Number of eigenvalues ≤ matrix size

* 2×2 → max 2
* 3×3 → max 3

(Counting multiplicity)

---

### Rule D: No eigenvectors? Possible.

Example:

* Rotation by 90° in ℝ² → **no real eigenvectors**

---

## 1️⃣1️⃣ Quick failure examples (to sharpen intuition)

### ❌ Nonlinear transformation

Eigenvalues are defined **only for linear transformations**.

---

### ❌ Translation

$$
{T(x)=Ax+b}
$$

No eigenvectors unless (${b}$=0).

---

## 1️⃣2️⃣ Why eigenvalues matter (intuition)


* PCA → eigenvectors = principal directions
* Stability → eigenvalues control explosion/decay
* Differential equations → long-term behavior
* NN → gradient flow & conditioning

---

## FINAL LOCK-IN (this ends confusion)

### Eigenvalue rule

$$
{\boxed{\det(A - \lambda I) = 0}}
$$

### Eigenvector rule

$$
{\boxed{(A - \lambda I)\mathbf{v} = 0,;\mathbf{v}\neq0}}
$$

---

## One-sentence intuition 🔒

**Eigenvectors are directions a transformation cannot bend — it can only stretch or flip them.**

---

$$
{\color{yellow}\text{***************************************************************************************************}}
$$

<br>

# Normal distribution/Gaussian distribution probability density function (PDF):


$$
{
f(x) = \frac{1}{\sigma \sqrt{2\pi}} \\, e^{-\frac{(x - \mu)^2}{2\sigma^2}}
}
$$

### Meaning of the symbols

* $${x}$$: the random variable (or a list of numbers)
* $${\mu}$$: the **mean** (center of the distribution)
* $${\sigma}$$: the **standard deviation** (spread of the distribution)
* $${\pi}$$: the mathematical constant pi
* $${e}$$: Euler’s number (${e \approx 2.718}$)



---

$$
{\color{yellow}\text{***************************************************************************************************}}
$$

<br>

# Standard differentiation rules

## 1. Constant Rule

$$
{
\frac{d}{dx}(c) = 0
}
$$

where (${c}$) is a constant.

---

## 2. Constant Multiple Rule

$$
{
\frac{d}{dx}(c f) = c\\,\frac{df}{dx}
}
$$

---

## 3. Power Rule

$$
{
\frac{d}{dx}\left(x^n\right) = n x^{n-1}
}
$$

(for any real number (${n}$))

More generally:

$$
{
\frac{d}{dx}\left(f^n\right) = n f^{\\,n-1}\frac{df}{dx}
}
$$

---

## 4. Sum Rule

$$
{
\frac{d}{dx}(f + g) = \frac{df}{dx} + \frac{dg}{dx}
}
$$

---

## 5. Difference Rule

$$
{
\frac{d}{dx}(f - g) = \frac{df}{dx} - \frac{dg}{dx}
}
$$

---

## 6. Product Rule

$$
{
\frac{d}{dx}(f g) = f\\,\frac{dg}{dx} + g\\,\frac{df}{dx}
}
$$

---

## 7. Quotient Rule

$$
{
\frac{d}{dx}\left(\frac{f}{g}\right) = \frac{g \frac{df}{dx} - f \frac{dg}{dx}}{g^2} \quad (g \neq 0)
}
$$

---

## 8. Chain Rule

If (${y = f(g(x))}$)\\, then:

$$
{
\frac{dy}{dx} = \frac{df}{dg}\\,\frac{dg}{dx}
}
$$

---

## 9. Exponential Rules

$$
{
\frac{d}{dx}(e^x) = e^x
}
$$

$$
{
\frac{d}{dx}(a^x) = a^x\\, \ln(a)
}
$$

---

## 10. Logarithmic Rules

$$
{
\frac{d}{dx}(\ln\\, x) = \frac{1}{x}
}
$$

$$
{
\frac{d}{dx}(\log_a\\, x) = \frac{1}{x\ln\\, a}
}
$$

---

## 11. Trigonometric Rules

$$
{
\frac{d}{dx}(\sin x) = \cos\\, x
}
$$

$$
{
\frac{d}{dx}(\cos x) = -\sin\\, x
}
$$

$$
{
\frac{d}{dx}(\tan x) = \sec^2\\, x
}
$$

$$
{
\frac{d}{dx}(\csc x) = -\csc\\, x\\, \cot\\, x
}
$$

$$
{
\frac{d}{dx}(\sec x) = \sec\\, x\\, \tan\\, x
}
$$

$$
{
\frac{d}{dx}(\cot x) = -\csc^2\\,x
}
$$

---

## 12. Implicit Differentiation (rule form)

If an equation involves (${x}$) and (${y}$):

$$
{
\frac{d}{dx}(y) = \frac{dy}{dx}
}
$$




$$
{End\,of\,files} 
$$

---
topic:
  - "[[Propositional Logic]]"
---
# Propositional Logic — Inference Rules

## 1. Basic Rules

**Modus Ponens (MP)**  
$$  
\frac{P,\quad P\to Q}{\therefore Q}  
$$

**Modus Tollens (MT)**  
$$  
\frac{P\to Q,\quad \neg Q}{\therefore \neg P}  
$$

**Hypothetical Syllogism (HS)**  
$$  
\frac{P\to Q,\quad Q\to R}{\therefore P\to R}  
$$

**Disjunctive Syllogism (DS)**  
$$  
\frac{P\lor Q,\quad \neg P}{\therefore Q}  
$$

## 2. Conjunction and Disjunction

**Simplification (Simp)**  
$$  
\frac{P\land Q}{\therefore P}  
$$

**Conjunction (Conj)**  
$$  
\frac{P,\quad Q}{\therefore P\land Q}  
$$

**Addition (Add)**  
$$  
\frac{P}{\therefore P\lor Q}  
$$

## 3. Other Useful Rules

**Resolution (Res)**  
$$  
\frac{P\lor Q,\quad \neg P\lor R}  
{\therefore Q\lor R}  
$$

**Constructive Dilemma (CD)**  
$$  
\frac{P\to R,\quad Q\to S,\quad P\lor Q}  
{\therefore R\lor S}  
$$

---

**Notation:**

- Premises appear above the line.
    
- The conclusion appears below the line.
    
- (\therefore) means “therefore.”
    

**Important:** Inference rules derive conclusions from premises; equivalence laws transform a formula into a logically equivalent formula.
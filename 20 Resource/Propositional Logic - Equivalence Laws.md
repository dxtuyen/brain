---
topic:
  - "[[Propositional Logic]]"
  - "[[Discrete Math]]"
aliases:
  - Luật tương đương
---
# Propositional Logic — Equivalence Laws

## 1. Elimination

**Implication Elimination**  
$$  
P \to Q \equiv \neg P \lor Q  
$$

**Biconditional Elimination**  
$$  
P \leftrightarrow Q  
\equiv (P \to Q)\land(Q \to P)  
$$

**Contrapositive**  
$$  
P \to Q \equiv \neg Q \to \neg P  
$$

## 2. Negation

**Double Negation**  
$$  
\neg\neg P \equiv P  
$$

**De Morgan's Laws**  
$$  
\neg(P\land Q)\equiv\neg P\lor\neg Q  
$$

$$  
\neg(P\lor Q)\equiv\neg P\land\neg Q  
$$

**Negated Implication**  
$$  
\neg(P\to Q)\equiv P\land\neg Q  
$$

## 3. Distribution and Factoring

**Distributive Laws**  
$$  
P\land(Q\lor R)  
\equiv(P\land Q)\lor(P\land R)  
$$

$$  
P\lor(Q\land R)  
\equiv(P\lor Q)\land(P\lor R)  
$$

## 4. Simplification

**Absorption**  
$$  
P\lor(P\land Q)\equiv P  
$$

$$  
P\land(P\lor Q)\equiv P  
$$

**Complement**  
$$  
P\lor\neg P\equiv T  
$$

$$  
P\land\neg P\equiv F  
$$

**Identity**  
$$  
P\land T\equiv P  
\qquad  
P\lor F\equiv P  
$$

**Domination**  
$$  
P\lor T\equiv T  
\qquad  
P\land F\equiv F  
$$

## 5. Rearrangement

**Commutative Laws**  
$$  
P\land Q\equiv Q\land P  
$$

$$  
P\lor Q\equiv Q\lor P  
$$

**Associative Laws**  
$$  
(P\land Q)\land R  
\equiv P\land(Q\land R)  
$$

$$  
(P\lor Q)\lor R  
\equiv P\lor(Q\lor R)  
$$

---

**Notation:**

- (T): True
    
- (F): False
    
- (\equiv): logically equivalent
    

**Typical workflow:** Eliminate implications → apply De Morgan's laws → distribute or factor → simplify.
---
title: "EST011 — Aula 2"
author: ""
date: "2024-03-08"
format:
  html:
    toc: true
  pdf: default
---

# Vetores Aleatórios

Seja $X = (X_1, \ldots, X_p)'$, $p \in \mathbb{N}$, onde cada $X_i$ é uma v.a. (unidimensional), $i=1,\ldots,p$. Então $X$ é um **vetor aleatório** de dimensão $p$.

- $C_X$ : conjunto de valores possíveis (não necessariamente discreto)

## Esperança e Variância

Seja $X = (X_1, \ldots, X_p)'$ um vetor aleatório com

$$
\mathbb{E}(X) = (\mu_1, \ldots, \mu_p)' = \mu
$$

com $(X_1, X_j) \mapsto f_{ij}$, $i,j = 1,\ldots,p$.

### Matriz de covariância

$$
\Sigma = \text{Cov}(X) =
\begin{bmatrix}
\sigma_{11} & \cdots & \sigma_{1p} \\
\vdots & \ddots & \vdots \\
\sigma_{p1} & \cdots & \sigma_{pp}
\end{bmatrix}
$$

## Propriedades

1. $$\Sigma = \mathbb{E}[(X-\mu)(X-\mu)']$$

2. $$\Sigma \text{ é simétrica e semidefinida positiva}$$

3. $$\Sigma \text{ é uma matriz semidefinida}$$

Se $\sigma_{ij} = 0$, então $X_i$ e $X_j$ são não correlacionadas.

4. Existe uma matriz $V$ tal que

$$
\Sigma = V^{1/2} V^{1/2}
$$

com $V$ diagonal:

$$
V = \text{diag}(\lambda_1, \ldots, \lambda_p)
$$

Logo,

$$
\Sigma^{1/2} = P V^{1/2} P'
$$

onde $P$ é ortogonal.

5. $$\Sigma = V^{1/2} P V^{1/2}$$

---

## Proposição

Sejam $X$ e $Y$ vetores aleatórios de dimensão $p$ com médias $\mu_X$ e $\mu_Y$ e matrizes de covariância $\Sigma_X$ e $\Sigma_Y$.

1. $$\mathbb{E}(aX + bY) = a\mathbb{E}(X) + b\mathbb{E}(Y)$$

2. $$\text{Cov}(AX) = A \Sigma_X A'$$

**Prova (esboço):**

$$
\text{Cov}(AX) = \mathbb{E}[(AX - A\mathbb{E}(X))(AX - A\mathbb{E}(X))']
$$

$$
= A\mathbb{E}[(X - \mathbb{E}(X))(X - \mathbb{E}(X))']A'
$$

$$
= A \Sigma_X A'
$$


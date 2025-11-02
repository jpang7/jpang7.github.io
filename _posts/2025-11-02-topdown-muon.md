---
layout: post
title: "[Top Down] Muon"
date: 2025-11-02
---

Learning about the Muon optimizer from the top down.

Top Down series is about learning stuff at a painfully, unreadably high level,
feeling like I know all about the subject, and maybe filling in gaps later.

Muon: SGD + Momentum, but at every step, replace the weight matrix with the
nearest orthogonal matrix.

Why orthogonal? Well what is an orthogonal matrix? An orthogonal matrix doesn't
scale the vector.

Ok, so what? Well, a matrix that scales a lot in one or few directions (called
"ill-conditioned") slows down training and has funky behavior. I guess in an LLM
it'll be really good at a few things and bad at others? It slows down training
because gradient updates can get fixated on a specific direction, and it might
ignore other good directions.

Wait but the gradient is computed based on the loss function, why does an
ill-conditioned weight matrix affect the loss function? Answer-- it does because
of the math.

Also do you really want a perfectly orthogonal weight matrix? Isn't scaling
important? Well apparently Muon doesn't make it perfectly orthogonal. Supposedly
that would be expensive too. A full orthogonalization is done with Gram-Schmidt
but we're using Newton-Schulz which apparently is just a few matrix
multiplications? Is that actually fast enough? What if it's a huge matrix?

Also apparently making a matrix orthogonal assumes the matrix is linearly
independent? Do we know that the weight matrix is L.I.? Answer-- with high
probability becauses the dimensions are large.

Apparently the ideal weight matrix is conditioned but in the right directions,
because conditioning equals compression in a sense? Maybe it's like a person who
knows what's important and invests their focus on a few important things?

### Follow Ups

Take a small LLM and do SVD on it, tweak a few singular values, recompute the
weight matrix, and talk to it again. See if it behaves differently. I don't know
how to measure change in chatbot behavior but for intuition.

Follow the derivation behind how the condition of the weight matrix affects the
Jacobian of the loss function.

What is Gram-Schmidt, what is Newton-Schulz, what are their complexities? If NS
takes you "near-orthogonal", how near is it? Why aren't we worried about NS
killing all the scaling? I learned this before in CS 4220.

Why are matrices in high dimensions linearly independent with high probability?
If they even are. This is a CS 4850 flavored question and I probably learned
this before.

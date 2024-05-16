---
layout: post
title: The nominal amount of debt increases over time
date: 2024-05-08 14_12_00 +0200
tags: mathjax
categories: mathjax
---
# The nominal amount of debt increases over time

Our modern financial system is based on credit money. This money does not gain its value through being backed against a standard, e.g., gold. Rather, certain entities (banks, the government) are allowed to create money out of nothing --- they issue money. The money gains it value either by the government's promise to accept the money for paying taxes or fees or by the banks' threat to sell securities once money is not paid back. 

In such a financial system, money is created by contracts about a credit between an entity that is allowed to issue money - the debitor - and any other legal person - the debtor. With \\(g_i(t)\\) we will denote the amount of money that is added to the debotor's accounts at time \\(t\\) in process of contract $i$. Here, we do not consider loan contracts, where money is lent out. We consider credits, where \\(g_i(t)\\) is newly created (issued) by the creditor. The total amount of money that \\(G_i\\) that the debtor receives can then be written as

$$G_i = \int_{-\infty}^{\infty} g_i(t) dt$$.

In most cases, there is only one timepoint \\(t_0\\) at which the whole money is transfered. Hence, without loss of generality, we write \\(g_i(t) = G_i\delta(t_0)\\) with the Delta-Distribution \\(\delta\\).

While the debtor receives money at one timepoint $t_0$, he is also required to pay money out of his account back to the debitor. With \\(s_i(t)\\), we describe the timepoints at which the debtor has to make these payments. Again, the total amount of money that debtor has to pay back, can be written as

$$S_i = \int_{-\infty}^{\infty} s_i(t) dt$$.

Most of the time, we have \\(S_i > G_i\\) which resembles positive interest rates. We define \\(K_i = S_i - G_i\\) as the cost of the credit. With positiv interest rates, the cost \\(K_i\\) is also positive.

For every contract, we also have the identity

$$\int_t^\infty s_i(\tau) d\tau > \int_t^\infty g_i(\tau) d\tau$$.

There is another observation. The total amount of money in all accounts available - the money in circulation - can be written as

$$M(t) = \sum_i\int_{-\infty}^t g_i(\tau) - s_i(\tau) d\tau$$.

It is the money spend into existence up to now (\\(t\\)) minus the money that had to be paid back up to now. As money should be in circulation, we demand \\(M(t) > 0\\).

For contracts that have been finalized (all the money is paid back and no more payments are outstanding), we can write

$$K_i = -\int_{-\infty}^t g_i(\tau) - s_i(\tau) d\tau$$.

Let \\(F\\) denote all the contracts that have been finalized and \\(O\\)) its complement---the still open contracts. We can rewrite

$$M(t) = -\sum_{i\in F} K_i + \sum_{i\in O}\int_{-\infty}^t g_i(\tau) - s_i(\tau) d\tau > 0$$.

By reordering we get

$$\sum_{i\in F} K_i < \sum_{i\in O}\int_{-\infty}^t g_i(\tau) - s_i(\tau) d\tau$$.

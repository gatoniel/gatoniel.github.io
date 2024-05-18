---
layout: post
title: The nominal amount of debt increases over time
date: 2024-05-08 14_12_00 +0200
tags: money mmt debt loan credit
categories: money
---
# The nominal amount of debt increases over time

Our modern financial system is based on credit money. This money does not gain its value through being backed against a standard, e.g., gold. Rather, certain entities (banks, the government---#MMT) are allowed to create money out of nothing---they issue money. Actually, they create money out of nothing only under certain conditions: in the case of banks, for example, a debtor agrees to either pay back the money or to loose her deposited securities. In general, to create money, two otherwise independent entities must come together to sign a contract. The money gains its value either by the government's promise to accept the money for paying taxes or fees or by the banks' threat to sell securities once money is not paid back. 

In the following, we will derive that the total amount of all outstanding debt (private + governmental sector) is monotonically increasing in times of positive interest rate.

As mentioned, money is created by contracts about a credit between an entity that is allowed to issue money---the debitor---and any other legal person---the debtor. With \\(g_i(t)\\) we will denote the amount of money that is added to the debotor's accounts at time \\(t\\) in process of contract \\(i\\). Here, we do not consider loan contracts, where money is lent out. We consider credits, where \\(g_i(t)\\) is newly created (issued) by the creditor. The total amount of newly issued money \\(G_i\\) that the debtor receives can then be written as

$$
\begin{equation}
G_i = \int_{-\infty}^{\infty} g_i(t) dt
\end{equation}
$$.

In most cases, there is only one timepoint \\(t_0\\) at which the whole money is transfered. Hence, without loss of generality, we write \\(g_i(t) = G_i\delta(t_0)\\) with the Delta-Distribution \\(\delta\\).

While the debtor receives money at one timepoint \\(t_0\\), he is also required to pay money out of his account back to the debitor. With \\(s_i(t)\\), we describe the timepoints at which the debtor has to make these payments. Again, the total amount of money the debtor has to pay back, can be written as

$$
\begin{equation}
S_i = \int_{-\infty}^{\infty} s_i(t) dt
\end{equation}
$$.

Most of the time, we have \\(S_i > G_i\\) which resembles positive interest rates. We define \\(K_i = S_i - G_i\\) as the cost of the credit. With positiv interest rates, the cost \\(K_i\\) is also positive. Under positive interest rates, for every contract \\(i\\) and all times \\(t\\), we have the identity

$$
\begin{equation}\tag{I}
\int_t^\infty s_i(\tau) d\tau > \int_t^\infty g_i(\tau) d\tau.
\end{equation}
$$

There is another observation. The total amount of money \\(M(t)\\) in all accounts available---the money in circulation---can be written as

$$
\begin{equation}
M(t) := \sum_i\int_{-\infty}^t g_i(\tau) - s_i(\tau) d\tau
\end{equation}
$$.

It is the money spend into existence up to now ('now' is depicted by \\(t\\)) minus the money that had to be paid back up to now. As money should be in circulation, we demand \\(M(t) \ge 0\\). Actually, it is not about money in circulation that we demand \\(M(t) \ge 0\\). If \\(M(t) < 0\\), more money has left all bank accounts than has ever entered them. This should not be possible as we could not trust our monetary system anymore.

For contracts that have already ended at timepoint \\(t\\) (all the money is paid back and no more payments to the debitor are outstanding), we can write

$$
\begin{equation}
K_i = \int_{-\infty}^t s_i(\tau) - g_i(\tau) d\tau
\end{equation}
$$.

Let \\(F\\) denote all the contracts that have already ended and \\(O\\) its complement---the still open contracts. We can rewrite

$$
\begin{equation}
M(t) = -\sum_{i\in F} K_i + \sum_{i\in O}\int_{-\infty}^t g_i(\tau) - s_i(\tau) d\tau \ge 0
\end{equation}
$$.

By reordering and defining \\(K=\sum_{i\in F}K_i\\) we get

$$
\begin{equation}\tag{II}
\sum_{i\in O} \int_{\hat{t}}^t g_i(\tau)d\tau \ge K + \sum_{i\in O}\int_\hat{t}^t s_i(\tau)d\tau
\end{equation}
$$,

where \\(\hat{t}\\) is the timepoint the earliest contract in \\(O\\) starts.

Now we define the total amount of currently outstanding debt \\(S(t)\\) and find

$$
\begin{eqnarray}
S(t) := \sum_{i\in O} \int_t^\infty s_i(\tau) d\tau &= \sum_{i\in O} \int_\hat{t}^\infty s_i(\tau)d\tau - \int_\hat{t}^t s_i(\tau)d\tau \\\\
&\overset{\text{I}}{\ge} \sum_{i\in O} \int_\hat{t}^\infty g_i(\tau)d\tau - \int_\hat{t}^t s_i(\tau)d\tau \\\\
&\ge \sum_{i\in O} \int_\hat{t}^t g_i(\tau)d\tau - \int_\hat{t}^t s_i(\tau)d\tau \\\\
&\overset{\text{II}}{\ge} K .
\end{eqnarray}
$$

In the second estimate, we have used \\(g_i(t)\ge 0\\). We find that the sum of the outstanding debt across all debtors must be bigger than the sum of fincancing costs of all contracts that have been finished up to now. As \((K\)) increases with time due to positive interest rates, we see that \((S(t)\)) increases, too.

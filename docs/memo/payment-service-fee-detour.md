# Payment-Service Fee Detour

This note documents why adding a payment-service fee only to the budget constraints of banks and non-banks does not, by itself, close the model or deliver an independent downward-sloping reserve-demand curve.

## Setup

The detour considered the following payment-service structure. Non-banks need payment services to consume:

$$
z_t^N \ge C_t^N,
\qquad t=0,1.
$$

Banks supply these services and must hold reserves to settle them. If $z_t$ denotes payment services supplied per bank, then

$$
m_t \ge \theta P_t z_t.
$$

The fee $s_t$ is paid by non-banks and received by banks. In per-non-bank terms, the non-bank budget constraint includes

$$
P_t s_t z_t^N,
$$

while the bank budget constraint includes fee income

$$
P_t s_t z_t.
$$

This makes the payment-service fee an explicit transfer from non-banks to banks.

## Non-Bank Fixed Point

Let $\nu_t^N$ denote the current-value multiplier on the non-bank budget constraint and let $\xi_t$ denote the multiplier on the payment-services requirement. The first-order conditions for $C_t^N$ and $z_t^N$ are

$$
u'(C_t^N)=\nu_t^N P_t+\xi_t,
$$

and

$$
\nu_t^N P_t s_t=\xi_t.
$$

Combining them gives

$$
s_t=\frac{u'(C_t^N)}{\nu_t^N P_t}-1.
$$

At first glance, this looks like an inverse demand curve for payment services. However, the multiplier $\nu_t^N$ is itself determined by the same budget constraint that contains the fee $s_t$. From the two first-order conditions,

$$
u'(C_t^N)=\nu_t^N P_t(1+s_t),
$$

so

$$
\nu_t^N=\frac{u'(C_t^N)}{P_t(1+s_t)}.
$$

Substituting this back into the fee equation gives

$$
s_t
=
\frac{u'(C_t^N)}
{
\left[u'(C_t^N)/(P_t(1+s_t))\right]P_t
}
-1
=
s_t.
$$

Thus the equation is a fixed point, not a primitive inverse demand schedule. The apparent inverse demand only becomes meaningful if $\nu_t^N P_t$ is held fixed as a partial-equilibrium object.

## Why the Bank Side Does Not Close It

On the bank side, fee income raises resources by $P_t s_t z_t$. The reserve-settlement constraint creates a shadow value of reserves, $\lambda_t$, and the bank first-order conditions imply

$$
\frac{u'(C_t^A)}{P_t}
=
\lambda_t
+\beta(1+i_t^R)\mathbb{E}_t
\left[
\frac{u'(C_{t+1}^A)}{P_{t+1}}
\right],
$$

and

$$
\lambda_t
=
\frac{u'(C_t^A)}{P_t}\frac{s_t}{\theta}.
$$

This maps the service fee into the bank's reserve Euler equation. But it does not determine $s_t$ independently. The fee is still the price of an internal transfer from non-banks to banks. Without an independent valuation of payment services, the bank side only translates the fee into a reserve shadow value.

## Consolidated Interpretation

Because the service fee is paid by non-banks and received by banks, it cancels in the aggregate resource constraint. It redistributes resources across private agents but does not create or destroy goods. Therefore, a service fee that appears only in budget constraints is not enough to pin down aggregate real allocations or the price level path.

This is why the fee-only detour does not close the model. It adds an internal price, but the price is not anchored by a separate preference or technology margin.

## What Would Close the Model

To obtain a genuine downward-sloping reserve-demand curve, payment services need to enter the model as an independent margin. Two natural options are:

1. Put payment services directly in non-bank preferences:

$$
U(C_t^N,z_t^N),
\qquad U_z>0,\quad U_{zz}<0.
$$

Then the fee is pinned down by a true marginal rate of substitution:

$$
s_t
=
\frac{U_z(C_t^N,z_t^N)}{U_C(C_t^N,z_t^N)}.
$$

If $U_z/U_C$ declines with $z_t^N$, reserve demand is genuinely downward sloping.

2. Introduce a payment or liquidity technology, such as shopping-time costs or settlement-failure costs, so that payment services relax a real resource cost rather than only shifting resources across agents.

In either case, reserves acquire a convenience yield from an independent economic margin. Then the reduced-form term

$$
\frac{\chi_t \ell'(m_t/P_t)}{P_t}
$$

can be interpreted as the nominal counterpart of that genuine marginal liquidity value.

## Bank Cost of Payment Services

Another way to motivate a fee schedule is to assume that banks face a real resource cost of providing payment services. Let $z_t$ denote payment services supplied per bank and let the real cost be

$$
\Gamma(z_t),
\qquad
\Gamma'(z_t)>0.
$$

Then the bank's period-$t$ real net revenue from payment services is

$$
s_t z_t-\Gamma(z_t).
$$

In nominal terms, the bank budget receives

$$
P_t\left[s_t z_t-\Gamma(z_t)\right].
$$

Holding the bank's marginal value of nominal wealth fixed, the first-order condition for payment-service supply is

$$
s_t=\Gamma'(z_t).
$$

This closes the fee block in the narrow sense that the service fee is now pinned down by a technological cost schedule rather than by the non-bank budget multiplier. Combining the reserve-settlement requirement,

$$
m_t=\theta P_t z_t,
$$

with the marginal-cost condition gives

$$
s_t
=
\Gamma'\!\left(\frac{m_t}{\theta P_t}\right).
$$

Thus the service fee becomes a direct function of real reserves.

However, this is a supply-side schedule, not a downward-sloping reserve-demand curve. If payment-service costs are convex,

$$
\Gamma''(z_t)>0,
$$

then the fee is increasing in payment-service volume:

$$
\frac{\partial s_t}{\partial (m_t/P_t)}
=
\frac{1}{\theta}\Gamma''\!\left(\frac{m_t}{\theta P_t}\right)
>0.
$$

This means that providing more payment services becomes more costly at the margin. It can determine the price of payment services, but by itself it gives an upward-sloping supply curve rather than the declining marginal convenience yield needed for downward-sloping reserve demand.

To close the full market for payment services, the model still needs a demand side. For example, if non-banks value payment services directly through $U(C_t^N,z_t^N)$, then equilibrium combines

$$
s_t
=
\frac{U_z(C_t^N,z_t^N)}{U_C(C_t^N,z_t^N)}
$$

with the bank supply condition

$$
s_t=\Gamma'(z_t).
$$

Together, these equations determine the service fee and payment-service quantity. The bank cost function therefore helps close the model only when paired with an independent demand for payment services.

## Bottom Line

Adding $s_t z_t$ only as an expense for non-banks and income for banks does not create a true reserve-demand curve. It produces a fixed point because the fee and the non-bank marginal value of wealth are jointly determined by the same budget constraint. To close the model, payment services must enter preferences or technology directly, not only the budget constraints.

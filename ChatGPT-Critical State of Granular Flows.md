# Critical State of Granular Flows

**User:** Anonymous (sgzksfwywisfah@gmail.com)  
**Created:** 3/6/2026 10:21:30  
**Updated:** 4/3/2026 22:04:41  
**Exported:** 4/7/2026 15:17:35  
**Link:** [https://chatgpt.com/g/g-p-69aa3570dea881918a7c01d2e3d5c0f2-granular-flow-vs-critical-state/c/69aa3966-70d8-8323-993b-ee33661a37a1](https://chatgpt.com/g/g-p-69aa3570dea881918a7c01d2e3d5c0f2-granular-flow-vs-critical-state/c/69aa3966-70d8-8323-993b-ee33661a37a1)  

## Prompt:
3/6/2026, 10:21:25 AM

the unified flow rule for granular flows of paper (https://doi.org/10.1103/PhysRevLett.134.028201), how to solve this problem in perspective of critical state method. the \mu_r-tang\theta is critical value. also notice the dimension incompatible of eq.(6) of fully developed state velocity, can explain this abnormal condition following the gioia's way (the math is based on the incomplete similarity of second kind proposed by barenblatt)

## Response:
3/6/2026, 10:21:28 AM

> Thought for 1m 18s

Yes. Read through a critical-state lens, the paper is naturally telling you that the fully developed chute flow is organized around a threshold at

$$
\tau/\sigma_n=\tan\theta=\mu_r,
$$

with  $\mu_r$  the dynamic friction (close to  $\mu_1$  from the stop-height fit). The paper itself shows  $h_s(\theta)\propto (\mu_2-\tan\theta)/(\tan\theta-\mu_1)$  with  $\mu_1\approx \mu_r$ , so the stop thickness diverges as  $\tan\theta\to \mu_r^+$ . That is exactly the behavior of a critical threshold: below it there is no sustained dense uniform flow, at it the system is marginal, and above it flow exists.

2501.10631v1

So from a critical-state perspective, define the distance to criticality as

$$
\varepsilon \equiv \tan\theta-\mu_r .
$$

Then:

*    $\varepsilon<0$ : subcritical, arrest/stop.
*    $\varepsilon=0$ : critical state, marginal yielding.
*    $\varepsilon>0$ : supercritical dense flow.

That matches the paper’s use of the “excess shear stress” on the base as the governing variable for  $v_\infty$ . They explicitly assume that the fully developed velocity is controlled mainly by  $\mu_r$  and the excess shear stress  $\tau_{ex}\sim (\tan\theta-\mu_r)h$ .

2501.10631v1

In that language,  $\mu_r$  is not just a fit parameter. It is the critical-state friction, and  $\tan\theta-\mu_r$  is the control parameter.

The useful reinterpretation is:

$$
v_\infty \sim \mu_r^{3/2}\,(\varepsilon h)^{4/3},\qquad L \sim \mu_r^3\,(\varepsilon h)^{5/3}h,
$$

in the paper’s nondimensional variables.

2501.10631v1

That means the developed-flow branch is a power-law branch emerging from the critical point  $\varepsilon=0^+$ , rather than a simple Bagnold or Pouliquen collapse. In critical-state terms, the flow “chooses” its velocity through distance from yield, not through  $h_s$  directly.

The exponent  $4/3$  is the interesting part. It is not what naive dimensional reasoning would give if complete similarity held. This is where Gioia/Barenblatt helps.

Gioia starts from a formula that is “dimensionally inconsistent” in raw engineering form, then rewrites it as a dimensionless relation and shows that when complete similarity fails, the asymptotic law becomes

$$
V = K\left(\frac rR\right)^a \sqrt{Rgs},
$$

with  $a$  not obtainable from ordinary dimensional analysis. That is Barenblatt’s incomplete similarity, or self-similarity of the second kind.

gioia2001.pdf

gioia2001.pdf

Barenblatt’s point is precisely that when a small parameter cannot be discarded, the limiting law can still be a power law, but with an anomalous exponent not fixed by dimensions alone. He distinguishes first-kind similarity, where dimensional analysis fixes exponents, from second-kind similarity, where exponents arise because no finite similarity limit exists and the remaining parameter stays essential.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

That is exactly the right way to read the granular paper.

About the “dimensionally incompatible” Eq. (6): in the paper it is only incompatible if you forget they already nondimensionalized everything using grain size  $d$ , grain density, and  $g\cos\theta$ . They state that  $\sqrt{g d\cos\theta}$  is the velocity scale and  $d$  is the length scale.

2501.10631v1

So their  $h$  in Eq. (6) is really  $H/d$ , and their  $v_\infty$  is really  $V_\infty/\sqrt{g d\cos\theta}$ . Once you restore dimensions, the fully developed velocity law becomes

$$
V_\infty \sim C\,\mu_r^{3/2} \left[(\tan\theta-\mu_r)\frac{H}{d}\right]^{4/3} \sqrt{g d\cos\theta}.
$$

This is dimensionally correct.

Likewise the development length restores as

$$
L_{dev}\sim C_L\,\mu_r^3 \left[(\tan\theta-\mu_r)\frac{H}{d}\right]^{5/3} H,
$$

which is also dimensionally correct.

So the “abnormality” is not a mistake in dimensions; it is a sign that the law is written in scaled variables and that the exponent  $4/3$  is anomalous.

Following Gioia’s logic, the clean interpretation is:

1.  Write the fully developed velocity in dimensionless form as
    $$
    Fr \equiv \frac{V_\infty}{\sqrt{gH\cos\theta}} = \Phi\!\left(\varepsilon,\frac{d}{H},\mu_r\right).
    $$
2.  Near the critical point,  $\varepsilon=\tan\theta-\mu_r\to0^+$ , complete similarity in  $d/H$  fails. The grain size is small compared with  $H$ , but it remains essential, just as roughness remains essential in Gioia’s channel problem.
    gioia2001.pdf
3.  Therefore the asymptotic law is not dimensionless-constant times  $\sqrt{\varepsilon H}$ , but a second-kind power law:
    $$
    Fr \sim \mu_r^{3/2}\,\varepsilon^{4/3}\left(\frac{H}{d}\right)^{5/6}.
    $$
    This is just the restored version of the paper’s Eq. (6), because
    $$
    \frac{V_\infty}{\sqrt{gH\cos\theta}} \sim \mu_r^{3/2} \left(\varepsilon\frac{H}{d}\right)^{4/3} \left(\frac{d}{H}\right)^{1/2} = \mu_r^{3/2}\varepsilon^{4/3}\left(\frac{H}{d}\right)^{5/6}.
    $$

That last form is especially revealing: it shows explicitly that the grain scale  $d$  survives in the asymptotics. That is the hallmark of incomplete similarity.

So the critical-state reading is:

*    $\mu_r$  is the critical friction.
*    $\varepsilon=\tan\theta-\mu_r$  is the distance from criticality.
*    $h_s$  diverging at  $\mu_r$  is the static-side critical signature.
*    $v_\infty\sim \varepsilon^{4/3}$  is the flowing-side critical branch.
*   The exponent  $4/3$  should be viewed as an anomalous exponent of second-kind similarity, not as a first-kind dimensional exponent.

One more useful observation: the undeveloped-flow formula

$$
v=v_\infty\left[1-e^{-l/L}\right]^{1/2}
$$

makes  $L$  a correlation/development length. In a critical-state analogy,  $L$  is the crossover length needed to forget preparation/history and reach the asymptotic steady branch. The fact that  $L$  grows strongly with  $h$  and with distance from threshold explains why many chute experiments never truly reached the asymptotic branch.

2501.10631v1

2501.10631v1

My bottom line is: the paper is consistent with a critical-state formulation if you treat  $\mu_r$  as the critical value and  $\tan\theta-\mu_r$  as the control parameter, and Eq. (6) is best understood as a second-kind similarity law in Barenblatt’s sense, exactly analogous in spirit to Gioia’s rescue of Manning’s “dimensionally inconsistent” law. The exponent is anomalous because grain-scale physics remains asymptotically relevant.

I can also write this as a compact derivation starting from a critical-state ansatz for the inertial number and dissipation balance.

## Prompt:
3/6/2026, 10:49:38 AM

how to solve this anomalous exponent of Eq.(6) from eigne value problems (just like barenblatt) instead of using data fit.

## Response:
3/6/2026, 10:49:43 AM

> **Searching through uploaded files for relevant info**
>
> It looks like the user wants an answer based on an uploaded paper. I’ll search through the files to find relevant documents and anything connected, using them to find useful citations. Time to check out the files and gather the right information for the user!
>
> **Investigating Barenblatt's paper on eigenvalue problem**
>
> I think I should focus on Barenblatt’s work, especially related to the eigenvalue problem. It might be more efficient to click and extract specific lines or relevant snippets. I’ll also check for a unified paper to get a broader context, especially if there’s supplemental info available. Let’s do this!
>
> **Formulating solution to anomalous exponent using eigenvalue method**
>
> The current paper doesn't provide a direct method for deriving the PDE, so we can't uniquely compute 4/3 using just dimensional analysis. I need to formulate governing equations and boundary conditions, derive the similarity ansatz and eigenvalue condition. I’ll highlight Barenblatt’s work, and look up additional details on the statistical method for p and q.
>
> Thought for 33s

Yes—but only after you **promote Eq. (6) from a scaling fit to a boundary-value problem**.

Right now, in the paper, the  $4/3$  is **not** obtained as Barenblatt would want. The authors explicitly say their  $v_\infty$  comes from dimensional analysis, and the supplemental material contains “the statistical analysis used to determine  $p$  and  $q$ .”

2501.10631v1

2501.10631v1

So, at present,  $4/3$  is an empirically selected exponent within a similarity ansatz, not yet an eigenvalue.

Barenblatt’s route is different. In second-kind similarity, the exponent cannot be fixed by dimensions alone; it is fixed by requiring that the reduced similarity ODE satisfy all boundary/regularity conditions. He states this repeatedly: the exponent is found from a **nonlinear eigenvalue problem**, and the anomalous dimension appears because the limiting solution does not have a finite complete-similarity limit.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

So the honest answer is:

**You cannot derive the  $4/3$  from the paper alone by Barenblatt’s eigenvalue method, because the paper does not yet provide the governing continuum problem whose similarity reduction would produce that exponent.**  
But you **can** set up the program for doing so.

* * *

1\. What the eigenvalue problem must be built from
--------------------------------------------------

You need a continuum model for steady dense chute flow near the threshold

$$
\varepsilon=\tan\theta-\mu_r \to 0^+,
$$

with  $\mu_r$  the critical-state friction and  $h_s$  diverging as  $\tan\theta\to \mu_1^+\approx\mu_r^+$ .

2501.10631v1

The minimal ingredients are:

$$
\partial_x(hu)=0,
$$
 
$$
\rho h u\,\partial_x u = \rho g h\sin\theta-\tau_b-\partial_x \Pi,
$$

plus a constitutive closure for the basal stress and a nonlocal or correlation-length equation. If you use only **local**  $\mu(I)$  or only simple Bagnold closure, you will almost never get a second-kind exponent. Those closures usually give first-kind exponents fixed by dimensional balance.

To get a Barenblatt-type anomalous exponent, you need one more small parameter that remains asymptotically relevant, analogous to roughness  $r/R$  in Gioia or  $l/\sqrt{Kt}$  in Barenblatt. Here the natural candidate is

$$
\delta = \frac{d}{h},
$$

or, more precisely, a nonlocal cooperativity length  $\xi$  that diverges as  $\varepsilon\to0^+$ . The point is that the grain scale cannot disappear completely. That is exactly what second-kind similarity means.

Barenblatt - 1996 - Scaling, se…

* * *

2\. The right form of the critical-state closure
------------------------------------------------

A workable critical-state/nonlocal ansatz is

$$
\tau_b = \mu_r P_b + \Delta \tau, \qquad \Delta\tau \sim P_b\,\mathcal{F}(I,g_f,\xi/d),
$$

where  $P_b\sim \rho g h\cos\theta$ ,  $I$  is inertial number, and  $g_f$  is a fluidity or order parameter.  
The flow threshold is  $\Delta\tau=0$ , so

$$
\frac{\tau_b}{P_b}-\mu_r = \tan\theta-\mu_r = \varepsilon.
$$

Then the fully developed state is the uniform solution of the coupled equations. The undeveloped-to-developed relaxation length  $L$  in the paper strongly suggests that a second field is needed; their own law introduces  $L$  as a development length and finds it grows strongly with control parameters.

2501.10631v1

A standard nonlocal choice would be a fluidity equation of the form

$$
\xi^2 g_f'' + \Phi(g_f;I,\varepsilon)=0,
$$

or, in the streamwise development problem,

$$
\xi^2 \partial_{xx} g_f + \Phi(g_f;\varepsilon)=0.
$$

Near the threshold, linearize:

$$
\Phi(g_f;\varepsilon)\approx a\,\varepsilon - b\,g_f^m.
$$

Then the correlation length diverges as

$$
\xi \sim d\,\varepsilon^{-\nu}.
$$

That already puts you in critical-state language:  $\varepsilon$  is distance to yield,  $g_f$  is the order parameter,  $\xi$  is the correlation length.

* * *

3\. How the eigenvalue appears
------------------------------

Barenblatt’s mechanism is always the same:

1.  Start from PDEs with a small but essential parameter.
2.  Assume a self-similar form with an **unknown exponent**.
3.  Reduce to ODEs.
4.  Demand regularity at a singular point and the correct boundary conditions at both ends.
5.  Only special exponent values satisfy all conditions: that exponent is the eigenvalue.
    Barenblatt - 1996 - Scaling, se…
    Barenblatt - 1996 - Scaling, se…

For chute flow, introduce a similarity form for the spatial development to the fully developed branch. A generic second-kind ansatz is

$$
u(x,z;\varepsilon)=U_*(\varepsilon)\,\mathcal{U}\!\left(\eta,\zeta\right), \qquad \eta=\frac{x}{\ell_*(\varepsilon)},\quad \zeta=\frac{z}{h},
$$

with

$$
U_*(\varepsilon)\sim \sqrt{gd\cos\theta}\,\varepsilon^\beta\left(\frac{h}{d}\right)^\gamma.
$$

The paper’s Eq. (6) corresponds to

$$
\beta=\frac{4}{3},\qquad \gamma=\frac{4}{3},
$$

in the nondimensionalized combination  $(\varepsilon h/d)^{4/3}$ .

2501.10631v1

2501.10631v1

But in a true Barenblatt derivation,  $\beta$  is left unknown at first.

After substitution, the reduced ODE system will typically have:

*   a wall condition at  $\zeta=0$  or  $x=0$ ,
*   a free-surface or outer condition at  $\zeta=1$  or  $x\to\infty$ ,
*   and a regularity condition at a **critical/singular point** where the reduced equations change character.

That regularity condition is what quantizes  $\beta$ .

* * *

4\. What singular point should determine the exponent here?
-----------------------------------------------------------

This is the key modeling question.

In Barenblatt’s explosion examples, the singular point is sonic. In flame problems, it is the pulled-front selection point. In groundwater spreading, it is the moving front.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

For granular chute flow, the natural singular structure is likely one of these:

### A. Yield-surface regularity

If the constitutive law degenerates as  $I\to0$  at  $\mu\to\mu_r$ , then the reduced ODE becomes singular at the point where the state touches criticality. Requiring a smooth passage through that point selects  $\beta$ .

### B. Front-selection problem

Treat the downstream development as a heteroclinic orbit from an undeveloped entrance state to the fully developed state. Then only one exponent permits a monotone bounded connection. This is very close to Barenblatt’s traveling-wave second-kind logic.

Barenblatt - 1996 - Scaling, se…

### C. Marginal stability / pulled-front selection

If the fluidity equation near threshold is reaction-diffusion-like,

$$
\partial_x g_f = \xi^2 \partial_{zz} g_f + a\varepsilon - b g_f^m,
$$

then the selected amplitude exponent can come from the marginal mode that survives both basal and free-surface boundary conditions.

Of these, **B** is the most promising if your target is the exponent in the fully developed velocity law.

* * *

5\. A concrete Barenblatt-style template
----------------------------------------

Here is the cleanest route.

Assume a reduced order-parameter equation for steady development:

$$
u\,\partial_x u = A\varepsilon - B g^m,
$$
 
$$
\xi^2(\varepsilon)\,\partial_{xx} g + C u^n - D g = 0,
$$

with

$$
\xi(\varepsilon)\sim d\,\varepsilon^{-\nu}.
$$

Seek

$$
u(x;\varepsilon)=U_0\,\varepsilon^\beta\,\phi(\eta),\qquad g(x;\varepsilon)=G_0\,\varepsilon^\chi\,\psi(\eta),\qquad \eta=x/(d\,\varepsilon^{-\nu}).
$$

Substitution gives a coupled ODE system. To have a nontrivial reduced problem, powers of  $\varepsilon$  must balance:

$$
2\beta+\nu = 1 \quad \text{(from inertia vs excess stress)},
$$
 
$$
\chi = n\beta \quad \text{(from production-fluidity coupling)},
$$

and another relation comes from the singular-point regularity of the reduced ODE. That third relation is the eigenvalue condition; it fixes  $\beta$ .

So unlike the dimensional-fit paper, the exponent is not put in by hand. It is obtained from the solvability condition.

* * *

6\. Why Gioia alone does not give the eigenvalue
------------------------------------------------

Gioia’s rough-channel argument is powerful, but it is still a **phenomenological closure**, not a nonlinear eigenvalue problem. He gets the  $1/6$  in Manning by plugging Kolmogorov scaling at the roughness scale into momentum transfer:

$$
u_r \sim (r/R)^{1/3}V,
$$

which then yields

$$
V\sim (r/R)^{-1/6}\sqrt{Rgs}.
$$

That is a mechanistic derivation of the incomplete-similarity exponent, but not an eigenvalue selection in Barenblatt’s strict PDE sense.

gioia2001.pdf

gioia2001.pdf

So for your granular problem:

*   **Gioia-style** gives a plausible scaling mechanism.
*   **Barenblatt-style** requires a reduced PDE/ODE with a singular solvability condition.

They are related, but not identical.

* * *

7\. Can  $4/3$  be predicted now?
---------------------------------

Not uniquely, no.

From the sources you gave, the paper only supports this much:

*    $v_\infty\propto \mu_r^{3/2}[(\tan\theta-\mu_r)h]^{4/3}$  in nondimensional variables, with length and velocity scaled by  $d$  and  $\sqrt{gd\cos\theta}$ .
    2501.10631v1
    2501.10631v1
*   the exponents were selected statistically, not through a continuum eigenvalue calculation.
    2501.10631v1
*   Barenblatt’s anomalous exponents come from solving nonlinear eigenvalue problems after reducing the governing PDEs.
    Barenblatt - 1996 - Scaling, se…
    Barenblatt - 1996 - Scaling, se…

So the missing step is not algebra; it is **model formulation**.

* * *

8\. My recommendation for a critical-state derivation
-----------------------------------------------------

Use this hierarchy:

1.  Let
    $$
    \varepsilon=\tan\theta-\mu_r
    $$
    be the control parameter.
2.  Introduce a nonlocal critical-state field  $g$  or  $\xi$ , because a local rheology will usually not generate second-kind selection.
3.  Pose the steady chute problem as a heteroclinic connection between entrance and fully developed states.
4.  Write a similarity ansatz with unknown  $\beta$ :
    $$
    U_\infty \sim \sqrt{gd\cos\theta}\, \varepsilon^\beta \left(\frac{h}{d}\right)^\gamma .
    $$
5.  Reduce to ODEs and enforce:
    *   no-slip / rough-base condition,
    *   free-surface condition,
    *   boundedness,
    *   smooth passage through the critical point in phase space.
6.  The last condition selects  $\beta$ . That is the Barenblatt eigenvalue.

So the slogan is:

**To get  $4/3$  as an eigenvalue, you must first invent the nonlocal critical-state PDE whose similarity reduction has a singular orbit.**

Without that PDE,  $4/3$  remains a fitted anomalous exponent, not a derived one.

If you want, I can next write down a **specific prototype PDE system** for dense chute flow near  $\mu_r$  and carry the similarity reduction far enough to show exactly where the eigenvalue condition would enter.

## Prompt:
3/6/2026, 11:01:24 AM

plz write down a specific prototype PDE system for dense chute flow near 𝜇_𝑟 and carry the similarity reduction far enough to show exactly where the eigenvalue condition would enter

## Response:
3/6/2026, 11:06:41 AM

> **Searching through uploaded files for context**
>
> The user’s asking about documents they uploaded, so I'll need to search those files for specific terms to gather relevant information. I’ll look for the right context, and reference the files with citations as needed to provide an accurate response.
>
> **Reviewing PRL paper and Barenblatt sections**
>
> I think it’d be helpful to click on the PRL paper and review the Barenblatt sections for more context. I want to make sure I provide the most relevant information, so I’ll focus on those specific parts to gather insights that can address the user's query accurately.
>
> **Crafting a consistent model for PDE and fluidity**
>
> I need to create a specific PDE model with similarity reduction, being careful not to overcommit to assumptions like the 4/3 derived value. I’ll introduce eigenvalues and propose a system with momentum and fluidity. For a 1D depth-averaged model, I'll use steady assumptions and depth-averaged variables like velocity and fluidity. I'll make sure to include relevant equations and properly model their relationships.
>
> **Deriving fluidity models from eigenvalue problem**
>
> I’m thinking about deriving the system from a vertical profile eigenvalue problem, which resembles a classical boundary value problem. The momentum equations will give the shear stress and pressure. But for the fluidity PDE, I'd need to consider non-local factors and bring in the shear rate. The solution leads to linear ordinary differential equations with different boundary conditions, ultimately yielding discrete modes, with an emphasis on the nonlinear relationships.
>
> **Balancing variables and deriving ODE for fluidity**
>
> I’m working on a reduced ODE by balancing terms involving ε, H, and the fluidity exponent. I’m choosing specific values for α and ν, and trying to relate β to momentum and kinematics. I think I need to impose boundary conditions and regularity at the free boundary to get the eigenvalue, though. For the fluidity front, I’m setting up a PDE that involves a traveling/steady similarity approach to determine the eigenvalue.
>
> **Exploring the balance of terms for coefficients and eigenvalue**
>
> I’ve derived relations based on the balances from momentum and force equations. This leads to specific choices for the exponent α and β. The non-local ODE formulation yields a clear picture, but I don’t need to compute the 4/3 value right now. I'll show the reduction process of the PDE, and indicate where the eigenvalue condition would arise, as the user requested. Using Barenblatt’s model would help here, to connect the boundary conditions to β.
>
> **Designing nonlocal PDE for dense flow with eigenvalue condition**
>
> I’m trying to derive the fluidity equation in terms of scaling as it relates to β. The goal is to introduce β through amplitude scaling, using a momentum closure relation. I'll use a self-similar development to deduce a time-like evolution and a traveling wave approach. The user’s request emphasizes a specific prototype, particularly dense chute flow near µr.
>
> **Finalizing β in similarity ansatz**
>
> I’m trying to capture the exact emergence of β in my similarity ansatz. By adjusting the form of the ansatz and balancing equations, I explore the inclusion of β, especially within ODE terms. This leads me to refine my approach with self-similar ansatz, though the user asks for the fully developed state directly.
>
> **Designing the prototype PDE for β and eigenvalue**
>
> I’m exploring a way to incorporate β explicitly into the PDE for fluidity. I'll construct a prototype where β acts as an eigenvalue. After substituting into a nonlocal fluidity equation and considering boundary conditions, I’ll attempt to express it through a key relation. The challenge is ensuring β becomes the eigenvalue.
>
> **Defining prototype PDE with traveling-wave ansatz and β as eigenvalue**
>
> I’m finalizing the prototype PDE with time-like evolution, incorporating similarity in both ε and x. This leads to a self-similar ODE where β shows up as a speed or exponent parameter. Reducing it into a first-order phase-plane system with two-point boundary conditions, I’ll show β as the eigenvalue.
>
> **Eigenvalue connection with β through balance relations**
>
> The setup reveals a system where β is connected to λ through balance relations. I’ve separated variables, which leads to a nonlinear transverse eigenproblem. After balancing, I found that β is governed by equations involving λ. The expression for β becomes explicit when considering these linkages, although I’m still refining the framework.
>
> Thought for 4m 20s

Yes. Here is a concrete **prototype** that is close to Barenblatt’s logic: introduce a second field that carries the nonlocal/critical-state structure, reduce the PDE to a coupled ODE boundary-value problem, and let the exponent be fixed by the requirement that a **global bounded solution** exists.

I will keep the model minimal but explicit.

Let

$$
\varepsilon=\tan\theta-\mu_r>0,\qquad H=\frac{h}{d},
$$

and nondimensionalize

$$
x\mapsto x/d,\quad z\mapsto z/d,\quad u\mapsto \frac{u}{\sqrt{g d\cos\theta}},\quad \tau,p\mapsto \frac{\tau,p}{\rho_p g d\cos\theta}.
$$

This is exactly the scaling used in the granular paper:  $d$  is the length scale and  $\sqrt{g d\cos\theta}$  the velocity scale.

2501.10631v1

The paper’s fully developed law is then

$$
u_\infty \propto \mu_r^{3/2}(\varepsilon H)^{4/3},
$$

in these variables.

2501.10631v1

The threshold interpretation is also natural because the stop law diverges at  $\tan\theta\to \mu_1^+\approx \mu_r^+$ .

2501.10631v1

* * *

1\. Prototype PDE system
------------------------

Take two fields:

*    $u(x,z)$ : downslope velocity
*    $g(x,z)$ : a granular fluidity / mobilization field

The point of  $g$  is to encode the fact that near  $\mu_r$ , local rheology is not enough; a grain-scale length remains essential, which is exactly the incomplete-similarity setting Barenblatt describes.

Barenblatt - 1996 - Scaling, se…

A concrete steady prototype is

$$
\partial_x u+\partial_z w=0, \tag{P1}
$$
 
$$
u\,\partial_x u+w\,\partial_z u = \varepsilon-\partial_z\!\Big(g\,\partial_z u\Big), \tag{P2}
$$
 
$$
\ell^2(\varepsilon)\Big(\partial_{xx}g+\partial_{zz}g\Big) +a\,\varepsilon -b\,g +c\,|\partial_z u|^{m}=0, \tag{P3}
$$

with

$$
\ell(\varepsilon)=\ell_0\,\varepsilon^{-\nu}. \tag{P4}
$$

Interpretation:

*   In (P2),  $\varepsilon$  is the excess driving above critical friction.
*   The stress transfer is through an effective granular mobility  $g$ .
*   In (P3),  $g$  is created by excess driving  $a\varepsilon$ , relaxes via  $-bg$ , is fed by shear  $c|\partial_z u|^m$ , and diffuses nonlocally over the correlation length  $\ell(\varepsilon)$ .

This is not the only possible model, but it is specific enough to carry out the reduction.

Use boundary conditions

$$
u(x,0)=0,\qquad g(x,0)=0 \qquad \text{(rough no-slip base)}, \tag{B1}
$$
 
$$
\partial_z u(x,H)=0,\qquad \partial_z g(x,H)=0 \qquad \text{(free surface)}, \tag{B2}
$$

and streamwise conditions

$$
u(0,z)=0,\qquad u(x,z)\to u_\infty(z)\ \text{as}\ x\to\infty. \tag{B3}
$$

* * *

2\. Similarity ansatz
---------------------

To make the downstream-development problem Barenblatt-like, introduce

$$
\eta=\frac{x}{\ell(\varepsilon)}=\frac{x}{\ell_0\,\varepsilon^{-\nu}}, \qquad \zeta=\frac{z}{H},
$$

and look for separated similarity forms

$$
u(x,z;\varepsilon) = H^\gamma \varepsilon^\beta\,\Phi(\eta)\,\varphi(\zeta), \tag{S1}
$$
 
$$
g(x,z;\varepsilon) = \varepsilon^\alpha\,\Psi(\eta)\,\psi(\zeta). \tag{S2}
$$

Here  $\beta$  is the exponent we ultimately care about.  
At this stage it is **unknown**.

This is exactly Barenblatt’s move: leave the exponent undetermined and let the reduced boundary-value problem fix it. In second-kind similarity, the exponent is not obtainable by dimensional analysis alone and is determined by a nonlinear eigenvalue problem.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

* * *

3\. Reduced equations: where the exponent first appears
-------------------------------------------------------

Substitute (S1)–(S2) into (P2)–(P3). Ignoring order-one numerical constants from the vertical scaling, the momentum equation gives

$$
H^{2\gamma}\varepsilon^{2\beta+\nu}\, \Phi\Phi'\,\varphi^2 \sim \varepsilon - H^{\gamma-2}\varepsilon^{\alpha+\beta}\, \Psi\Phi\,\frac{d}{d\zeta}\!\Big(\psi\,\varphi'\Big). \tag{R1}
$$

The fluidity equation gives

$$
\varepsilon^\alpha \Big(\Psi''\psi+\Psi\psi''\Big) + a\,\varepsilon - b\,\varepsilon^\alpha\Psi\psi + c\,H^{-m}\varepsilon^{m\beta}\, |\Phi\varphi'|^m =0. \tag{R2}
$$

To have a nontrivial reduced problem, the leading  $\varepsilon$ \-powers must balance. A minimal consistent balance is

$$
2\beta+\nu=1, \tag{E1}
$$
 
$$
\alpha+\beta=1, \tag{E2}
$$

and the third relation comes from the shear-production term competing with relaxation in (R2). In the simplest case,

$$
m\beta=\alpha. \tag{E3}
$$

If you imposed (E1)–(E3) immediately, you would get

$$
\beta=\frac{1}{m+1},\qquad \alpha=\frac{m}{m+1},\qquad \nu=\frac{m-1}{m+1}. \tag{E4}
$$

But that still treats  $m$  as a closure input.  
That is **not yet** Barenblatt’s eigenvalue mechanism.

To get a genuine eigenvalue problem, you must not close the problem at this stage. Instead, carry the separation one step further.

* * *

4\. The transverse nonlinear eigenproblem
-----------------------------------------

After separation, the  $\zeta$ \-dependence satisfies

$$
\frac{d}{d\zeta}\!\Big(\psi(\zeta)\,\varphi'(\zeta)\Big) +\lambda\,\varphi(\zeta)=0, \tag{T1}
$$
 
$$
\psi''(\zeta)-\kappa\,\psi(\zeta) +\chi\,|\varphi'(\zeta)|^{m}=0, \tag{T2}
$$

with boundary conditions

$$
\varphi(0)=0,\qquad \varphi'(1)=0, \tag{T3}
$$
 
$$
\psi(0)=0,\qquad \psi'(1)=0. \tag{T4}
$$

Here  $\lambda$  is the separation constant.

This is already a **nonlinear boundary-value problem**.  
For generic  $\lambda$ , the four conditions cannot all be satisfied by a nontrivial pair  $(\varphi,\psi)$ . Only exceptional  $\lambda$  permit a global solution. That is exactly the structure Barenblatt emphasizes: a nontrivial invariant solution exists only for special values of the parameter.

Barenblatt - 1996 - Scaling, se…

So the first eigenvalue is:

$$
\lambda=\lambda_*.
$$

Once  $\lambda_*$  is selected, it feeds into the streamwise problem through the projected coefficients.

* * *

5\. The streamwise heteroclinic problem
---------------------------------------

Projecting onto the transverse eigenmode gives amplitude equations of the form

$$
A_1(\lambda_*)\,\Phi\Phi' = 1-A_2(\lambda_*)\,\Psi\Phi, \tag{X1}
$$
 
$$
\Psi'' + A_3(\lambda_*) - A_4(\lambda_*)\,\Psi + A_5(\lambda_*)\,\Phi^{m} =0. \tag{X2}
$$

Boundary conditions are

$$
\Phi(0)=0,\qquad \Psi'(0)=0, \tag{X3}
$$
 
$$
\Phi(\eta)\to \Phi_\infty,\qquad \Psi(\eta)\to \Psi_\infty \quad (\eta\to\infty). \tag{X4}
$$

So now you have a two-point nonlinear BVP in  $\eta$ .  
The far-field state must satisfy

$$
1-A_2(\lambda_*)\,\Psi_\infty\Phi_\infty=0, \tag{F1}
$$
 
$$
A_3(\lambda_*) - A_4(\lambda_*)\,\Psi_\infty + A_5(\lambda_*)\,\Phi_\infty^m=0. \tag{F2}
$$

Linearizing about  $(\Phi_\infty,\Psi_\infty)$  gives a Jacobian  $J(\lambda_*)$ .  
The entrance state  $(\Phi(0),\Psi(0))$  must lie on the stable manifold of the downstream fixed point. For generic parameter values, it will not. Only for special values does a bounded monotone connection exist.

That is the second selection step: the **global-existence/heteroclinic condition**.

Barenblatt states this precisely: in second-kind problems, the exponent is determined by the condition for existence of a global inner-structure solution satisfying the boundary conditions.

Barenblatt - 1996 - Scaling, se…

* * *

6\. Where the anomalous exponent enters as an eigenvalue
--------------------------------------------------------

Now the key point.

The projected coefficients  $A_j$  depend on  $\lambda_*$ , and the balance relation (E1) still ties  $\beta$  to the streamwise scaling exponent  $\nu$ :

$$
2\beta+\nu=1. \tag{E1 again}
$$

But  $\nu$  is no longer an arbitrary closure exponent. It is fixed by the requirement that the streamwise heteroclinic solution exists with the selected transverse mode  $\lambda_*$ . Symbolically,

$$
\nu=\nu(\lambda_*). \tag{SEL1}
$$

Therefore

$$
\beta=\frac{1-\nu(\lambda_*)}{2}. \tag{SEL2}
$$

That is the Barenblatt structure you wanted:

1.  write PDEs with an essential small parameter  $\varepsilon$ ,
2.  assume a self-similar form with unknown exponent  $\beta$ ,
3.  reduce to ODE/BVPs,
4.  require a global bounded solution satisfying all boundary conditions,
5.  obtain  $\lambda_*$ , then  $\nu(\lambda_*)$ , then  $\beta$ .

So the exponent is not inserted by fit. It is selected by solvability.

* * *

7\. Why this is genuinely “second kind”
---------------------------------------

Barenblatt’s distinction is:

*   first kind: exponents follow from dimensional analysis;
*   second kind: the small parameter remains essential, and the exponent is fixed only by solving a nonlinear eigenvalue problem.
    Barenblatt - 1996 - Scaling, se…

Here the essential small parameter is the distance to criticality,

$$
\varepsilon=\tan\theta-\mu_r,
$$

and the corresponding nonlocal length

$$
\ell(\varepsilon)\sim \varepsilon^{-\nu}
$$

does not disappear from the asymptotics.

That is the analogue of roughness  $r/R$  in Gioia’s channel-flow argument, where incomplete similarity leaves the small length scale in the final law. Gioia explicitly writes the incomplete-similarity asymptotic

$$
V \sim K \left(\frac{r}{R}\right)^a \sqrt{Rgs},
$$

with  $a$  not fixed by dimensional analysis alone.

gioia2001.pdf

Your granular problem should be read in the same spirit, but with the exponent determined by a nonlinear BVP rather than by direct fit.

* * *

8\. How  $4/3$  would emerge in this framework
----------------------------------------------

Once the selected eigenvalue gives  $\nu$ , you get

$$
\beta=\frac{1-\nu}{2}.
$$

If the solvability condition gives

$$
\nu=-\frac{5}{3},
$$

then

$$
\beta=\frac{1-(-5/3)}{2}=\frac{4}{3}.
$$

I am **not** claiming this prototype already proves  $\nu=-5/3$ .  
What it proves is the mechanism:

*   the exponent is left unknown,
*   the reduced BVP contains a separation/eigenvalue parameter,
*   global existence plus boundary conditions select that parameter,
*   the anomalous velocity exponent follows from the selected parameter.

That is exactly the Barenblatt program.

* * *

9\. The cleanest “minimal” statement
------------------------------------

If you want the shortest mathematical summary, it is this:

Start from a nonlocal critical-state PDE for  $(u,g)$ , then impose

$$
u(x,z;\varepsilon)=H^\gamma \varepsilon^\beta \Phi(\eta)\varphi(\zeta),\qquad g(x,z;\varepsilon)=\varepsilon^\alpha \Psi(\eta)\psi(\zeta),
$$

with

$$
\eta=x\,\varepsilon^\nu,\qquad \zeta=z/H.
$$

The reduction yields

*   a **transverse nonlinear eigenproblem** for  $(\varphi,\psi,\lambda)$ ,
*   a **streamwise heteroclinic problem** for  $(\Phi,\Psi)$ ,
*   and a balance relation  $2\beta+\nu=1$ .

The value of  $\nu$  is determined only for those  $\lambda$  for which the streamwise and transverse problems admit a single global bounded solution satisfying all boundary conditions. Then  $\beta$  follows from  $2\beta+\nu=1$ .

That is where the eigenvalue enters.

* * *

The next natural step is to choose a specific nonlocal granular-fluidity law in place of my generic (P3), and then derive the actual transverse equations and the projected coefficients  $A_j(\lambda)$ . That is the point where one can test whether the selected  $\beta$  can really be  $4/3$ .

## Prompt:
3/6/2026, 11:34:53 AM

plz choose a specific nonlocal granular-fluidity law in place of my generic (P3), and then derive the actual transverse equations and the projected coefficients

## Response:
3/6/2026, 11:34:56 AM

> **Searching uploaded PDFs for nonlocal granular fluidity law**
>
> I should start by searching through the uploaded PDFs for references to nonlocal granular fluidity. The user asks for a specific law, so I’ll need to focus, possibly referencing Kamrin/Koval work, or derive from Barenblatt’s concept. I’ll also consider citing relevant equations or concepts in the papers.
>
> **Determining law choice and citation needs**
>
> I’m thinking I don’t need to search more; I could use the Bouzid fluidity law from reference 20, though we don’t have that paper. Using a general model could be fine, but I should be cautious about citations. I might rely on my internal knowledge to explain the modeling choice.
>
> **Formulating specific nonlocal fluidity model**
>
> I’m thinking of referencing Bouzid’s non-local rheology from the paper and using a standard NGF equation as a prototype. To answer the user’s request, I’ll carefully derive the transverse equations and projected coefficients with a steady, uniform approach. I’ll simplify the model using a near-threshold expansion.
>
> **Analyzing transverse equations and 4/3 exponent**
>
> The free-surface velocity can be expressed like this \(u_s(x)=\mu H \Phi(\eta)\int_0^1 \psi d\zeta\), and the amplitude leads to a linear exponent, not 4/3. To get the 4/3 result, I’d need to modify the NGF law, incorporating nonlinear terms. I’ll compact the equations and reference the relevant citations regarding nonlocal rheology and scaling.
>
> Thought for 1m 34s

Yes. I’ll pick a **specific NGF-type law** in the spirit of the non-local rheology cited by the paper as Ref. \[20\], and I’ll be explicit that the equations below are **my chosen near-threshold specialization**, not something written in the PRL itself. The PRL does, however, identify  $\mu_r$  as the relevant dynamic friction and writes the developed-state law as  $v_\infty\propto \mu_r^{3/2}[(\tan\theta-\mu_r)h]^{4/3}$  in variables nondimensionalized with  $d$  and  $\sqrt{gd\cos\theta}$ .

2501.10631v1

2501.10631v1

The same paper also points to non-local rheology as relevant background through Ref. \[20\].

2501.10631v1

Barenblatt’s criterion is that the exponent should come from the existence of a global invariant solution of a boundary-value problem, i.e. from an eigenvalue/solvability condition rather than direct dimensional fitting.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

1\. Specific prototype: steady nonlocal granular fluidity
---------------------------------------------------------

Let

$$
\mu=\tan\theta=\mu_r+\varepsilon,\qquad \varepsilon>0,
$$

and use the PRL nondimensionalization

$$
x,z,h \text{ scaled by } d,\qquad u \text{ scaled by } \sqrt{gd\cos\theta}.
$$

2501.10631v1

Choose the steady NGF closure

$$
\partial_z u=\mu\,g, \tag{1}
$$
 
$$
A^2\left(\partial_{xx}g+\partial_{zz}g\right) +\sigma(\mu)\,g-\kappa\,\mu\,g^2=0, \tag{2}
$$

with

$$
\sigma(\mu) = \Delta\mu\,\frac{\mu-\mu_r}{\mu_2-\mu} = \Delta\mu\,\frac{\varepsilon}{\mu_2-\mu_r-\varepsilon}. \tag{3}
$$

Here:

*    $g(x,z)$  is the fluidity,
*    $A$  is the nonlocal amplitude in grain diameters,
*    $\kappa>0$  is the coefficient of the local nonlinear saturation,
*    $\Delta\mu=\mu_2-\mu_r$ .

Equation (2) is the steady reaction-diffusion form that gives the usual NGF cooperativity length after linearization,

$$
\xi(\mu)\sim \frac{A}{\sqrt{\sigma(\mu)}},
$$

so near  $\mu\to\mu_r^+$ ,  $\xi$  diverges like  $\varepsilon^{-1/2}$ . That is already the critical-state ingredient.

Use depth-domain  $0\le z\le h$  with

$$
u(x,0)=0,\qquad g(x,0)=0, \tag{4}
$$
 
$$
\partial_z g(x,h)=0. \tag{5}
$$

The basal condition is rough/no-slip, and the free surface carries no fluidity flux. Then the free-surface velocity is

$$
u_s(x)=\mu\int_0^h g(x,z)\,dz. \tag{6}
$$

2\. Transverse eigenproblem
---------------------------

Introduce the scaled depth variable

$$
\zeta=\frac{z}{h}\in[0,1].
$$

Seek a separated representation

$$
g(x,z)=\sum_{n\ge0} a_n(x)\,\psi_n(\zeta). \tag{7}
$$

Linearizing (2) about  $g=0$  gives

$$
A^2\left(\partial_{xx}g+\frac{1}{h^2}\partial_{\zeta\zeta}g\right)+\sigma g=0. \tag{8}
$$

Separation  $g=a(x)\psi(\zeta)$  gives

$$
\psi''+\lambda\psi=0, \tag{9}
$$

with

$$
\psi(0)=0,\qquad \psi'(1)=0. \tag{10}
$$

This is the actual transverse Sturm-Liouville problem. Its eigenpairs are

$$
\lambda_n=\left(n+\tfrac12\right)^2\pi^2,\qquad \psi_n(\zeta)=\sin\!\left[\left(n+\tfrac12\right)\pi\zeta\right]. \tag{11}
$$

So the fundamental mode is

$$
\lambda_0=\frac{\pi^2}{4},\qquad \psi_0(\zeta)=\sin\!\left(\frac{\pi\zeta}{2}\right). \tag{12}
$$

This is already an eigenvalue problem in the ordinary sense. In Barenblatt language, though, this alone is not yet the anomalous-exponent selection problem; it is the transverse mode selection. The anomalous exponent would have to come later from the global similarity problem.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

3\. One-mode reduction and projected coefficients
-------------------------------------------------

Near threshold, keep only the leading mode:

$$
g(x,z)\approx a(x)\psi_0(\zeta). \tag{13}
$$

Insert into (2):

$$
A^2\left(a''\psi_0+\frac{a}{h^2}\psi_0''\right) +\sigma a\psi_0 -\kappa\mu a^2\psi_0^2=0. \tag{14}
$$

Project onto  $\psi_0$  by multiplying by  $\psi_0$  and integrating over  $\zeta\in[0,1]$ . Define

$$
M_2=\int_0^1\psi_0^2\,d\zeta,\qquad M_3=\int_0^1\psi_0^3\,d\zeta. \tag{15}
$$

Because  $\psi_0''=-\lambda_0\psi_0$ , the amplitude equation becomes

$$
A^2 M_2\,a''+ \left(\sigma-\frac{A^2\lambda_0}{h^2}\right)M_2\,a -\kappa\mu M_3\,a^2=0. \tag{16}
$$

Divide by  $M_2$ :

$$
A^2 a''+\alpha_1 a-\alpha_2 a^2=0, \tag{17}
$$

with the **projected coefficients**

$$
\alpha_1=\sigma-\frac{A^2\lambda_0}{h^2}, \tag{18}
$$
 
$$
\alpha_2=\kappa\mu\,\frac{M_3}{M_2}. \tag{19}
$$

For  $\psi_0(\zeta)=\sin(\pi\zeta/2)$ ,

$$
M_2=\int_0^1\sin^2\!\left(\frac{\pi\zeta}{2}\right)d\zeta=\frac12, \tag{20}
$$
 
$$
M_3=\int_0^1\sin^3\!\left(\frac{\pi\zeta}{2}\right)d\zeta=\frac{4}{3\pi}. \tag{21}
$$

Hence

$$
\frac{M_3}{M_2}=\frac{8}{3\pi}, \tag{22}
$$

and therefore

$$
\alpha_2=\kappa\mu\,\frac{8}{3\pi}. \tag{23}
$$

Also

$$
\alpha_1 = \Delta\mu\frac{\varepsilon}{\mu_2-\mu_r-\varepsilon} -\frac{A^2\pi^2}{4h^2}. \tag{24}
$$

That is the clean projected amplitude equation:

$$
A^2 a''+ \left[ \Delta\mu\frac{\varepsilon}{\mu_2-\mu_r-\varepsilon} -\frac{A^2\pi^2}{4h^2} \right]a -\kappa(\mu_r+\varepsilon)\frac{8}{3\pi}a^2=0. \tag{25}
$$

4\. Free-surface velocity from the projected mode
-------------------------------------------------

From (6),

$$
u_s(x)=\mu\,a(x)\int_0^1 h\,\psi_0(\zeta)\,d\zeta. \tag{26}
$$

Define

$$
M_1=\int_0^1\psi_0(\zeta)\,d\zeta = \int_0^1 \sin\!\left(\frac{\pi\zeta}{2}\right)d\zeta = \frac{2}{\pi}. \tag{27}
$$

So

$$
u_s(x)=\mu h\,M_1\,a(x) = (\mu_r+\varepsilon)\,\frac{2h}{\pi}\,a(x). \tag{28}
$$

In the fully developed state,  $a''=0$ , so

$$
a_\infty=\frac{\alpha_1}{\alpha_2} = \frac{ \Delta\mu\frac{\varepsilon}{\mu_2-\mu_r-\varepsilon} -\frac{A^2\pi^2}{4h^2} }{ \kappa(\mu_r+\varepsilon)\frac{8}{3\pi} }. \tag{29}
$$

Thus

$$
u_{s,\infty} = (\mu_r+\varepsilon)\frac{2h}{\pi}\,a_\infty = \frac{3h}{4\kappa} \left[ \Delta\mu\frac{\varepsilon}{\mu_2-\mu_r-\varepsilon} -\frac{A^2\pi^2}{4h^2} \right]. \tag{30}
$$

Near onset,

$$
u_{s,\infty}\sim \frac{3h}{4\kappa} \left( \frac{\Delta\mu}{\mu_2-\mu_r}\varepsilon -\frac{A^2\pi^2}{4h^2} \right). \tag{31}
$$

5\. Exact place where the eigenvalue enters
-------------------------------------------

There are **two** eigenvalue-type roles here.

First, the transverse eigenvalue:

$$
\lambda_0=\frac{\pi^2}{4}. \tag{32}
$$

It enters the projected growth rate through

$$
\alpha_1=\sigma-\frac{A^2\lambda_0}{h^2}. \tag{33}
$$

Second, the threshold for a nontrivial global solution is

$$
\alpha_1=0 \quad\Longleftrightarrow\quad \sigma(\mu)=\frac{A^2\lambda_0}{h^2}. \tag{34}
$$

That is the mode-selection criterion. It can be rewritten as

$$
\Delta\mu\frac{\varepsilon_c}{\mu_2-\mu_r-\varepsilon_c} = \frac{A^2\pi^2}{4h^2}. \tag{35}
$$

For small  $\varepsilon_c$ ,

$$
\varepsilon_c \approx \frac{A^2\pi^2}{4\Delta\mu}\, \frac{\mu_2-\mu_r}{h^2}. \tag{36}
$$

So this specific NGF law predicts a depth-dependent onset

$$
\tan\theta-\mu_r \sim h^{-2}, \tag{37}
$$

which is already a nice critical-state result.

6\. Streamwise heteroclinic profile
-----------------------------------

Equation (17) has the phase-plane form

$$
A^2 a''+\alpha_1 a-\alpha_2 a^2=0, \tag{38}
$$

with

$$
a(0)=0,\qquad a(\infty)=a_\infty=\frac{\alpha_1}{\alpha_2}. \tag{39}
$$

Multiplying by  $a'$  and integrating gives

$$
\frac{A^2}{2}(a')^2 + \frac{\alpha_1}{2}a^2 - \frac{\alpha_2}{3}a^3 = C. \tag{40}
$$

Using  $a'(\infty)=0$  and  $a(\infty)=a_\infty$ ,

$$
C= \frac{\alpha_1^3}{6\alpha_2^2}. \tag{41}
$$

That is the exact solvability structure for the inlet-to-developed connection.

7\. What this specific law tells you about the  $4/3$ 
------------------------------------------------------

This is the important conclusion:

with this concrete NGF law, the projected amplitude behaves near onset as

$$
a_\infty\propto \alpha_1,
$$

so

$$
u_{s,\infty}\propto h\,\alpha_1 \propto h\left(\varepsilon-\text{const}\,h^{-2}\right). \tag{42}
$$

So the exponent in  $\varepsilon$  is **1**, not  $4/3$ .

That means this standard steady NGF closure gives you:

*   a real transverse eigenproblem,
*   explicit projected coefficients,
*   a depth-dependent critical condition,
*   a heteroclinic streamwise development equation,

but **not** the anomalous exponent  $4/3$ .

So if you want Barenblatt-style selection of  $4/3$ , this specific NGF law is too regular. The anomalous exponent does **not** emerge from the projection; it would require an additional singular mechanism, for example:

*   a non-analytic mobility term  $g^p$  with non-integer  $p$ ,
*   a singular dependence of  $A$  or  $\kappa$  on  $\varepsilon h$ ,
*   a moving internal layer/yield surface whose position is itself part of the eigenproblem,
*   or a matched-asymptotic inner problem where the near-base grain scale remains explicit in the similarity variable, in the Barenblatt sense of incomplete similarity.
    Barenblatt - 1996 - Scaling, se…
    Barenblatt - 1996 - Scaling, se…

So this derivation is useful precisely because it shows the gap:

**standard NGF gives a conventional bifurcation with explicit mode coefficients, but not the PRL’s  $4/3$ .**

The next step would be to modify the constitutive law so that the amplitude equation is no longer quadratic-regular like (17), but instead becomes singular enough that the similarity exponent is fixed by a genuine nonlinear eigenvalue condition.

## Prompt:
3/6/2026, 2:00:07 PM

I have background of fluid mechnism and turbulence, not familiar with granular flow and rheology, plz expain why we the non local fluidity and inertial number and non constant friction coeff

## Response:
3/6/2026, 2:00:11 PM

> **Using uploaded papers and avoiding extra searches**
>
> I think I can build the answer using the papers uploaded by the user, so no need to search the web. I could use the file search on the PDFs to find relevant sources. It might also be useful to reference things like granular rheology, but other analogies like turbulence might not be necessary.
>
> **Generating a pedagogical answer with references**
>
> I think I can give a clear, educational response by starting with the main PDF. I’ll focus on sections that discuss μ(I) shortcomings and maybe pull direct references from there. If needed, I could also pull from relevant parts of the PRL for specific insights on μr and its dynamic threshold.
>
> **Explaining nonlocal fluidity and friction dependence**
>
> To explain why we need nonlocal fluidity and inertial number (I), I’ll use fluid mechanics analogies. Unlike Newtonian fluids, granular materials don’t have a fixed constitutive timescale. The inertial number is a ratio that reflects timescales. μ isn’t constant because it changes with flow regimes, and nonlocal fluidity is necessary to account for stress influenced by neighboring grains. I'll reference the uploaded paper for context and specific details like μr thresholds.
>
> Thought for 29s

Sure. From a fluid-mechanics viewpoint, the reason granular people introduce **inertial number**, ** $\mu(I)$ **, and then **nonlocal fluidity** is basically this:

A dense granular flow is **not** just a very viscous fluid, and it is also **not** just a Coulomb solid with one constant friction coefficient. It sits in between. It can look solid-like, then yield, then flow, and the way it flows depends on how fast grains are forced to rearrange compared with how fast confinement can stabilize them.

The cleanest place to start is stress balance. In a Newtonian fluid, you are used to

$$
\tau \sim \mu_f \dot\gamma,
$$

with a material viscosity  $\mu_f$  that is roughly independent of the flow state.

For dense grains, that is not the right organizing law. Because grains are hard, dissipative, and under strong normal loading, the natural dimensionless shear stress is

$$
\mu \equiv \frac{\tau}{p},
$$

not  $\tau$  alone. In chute flow,  $\tau/p \approx \tan\theta$ , so slope directly sets the effective friction ratio. The new PRL is written in exactly that language: it treats  $\mu_r$  as the dynamic friction coefficient, effectively a dynamic threshold, and uses the excess over threshold  $\tan\theta-\mu_r$  as the driving quantity.

2501.10631v1

2501.10631v1

2501.10631v1

Why not use a constant friction coefficient? Because that would mean

$$
\tau = \mu p
$$

with one fixed  $\mu$ , so once the material yields, the constitutive law would contain no information about **how fast** it is deforming. But experiments and DEM show that dense granular flow changes character with shear rate: near arrest it is enduring-contact/frictional, while at faster shear it becomes increasingly collisional and dilated. The PRL itself shows that old rules with fixed material parameters tied to  $h_s(\theta)$  are not universal across materials and break down as conditions change; it also notes that the older  $\mu(I)$ \-based estimate for the development length  $L$  misses the observed trends.

2501.10631v1

2501.10631v1

2501.10631v1

So people ask: what dimensionless number tells us how “fast” the granular deformation is?

That is the **inertial number**

$$
I=\frac{\dot\gamma d}{\sqrt{p/\rho_p}}.
$$

For someone from fluid mechanics, this is best read as a **timescale ratio**:

$$
I \sim \frac{\text{microscopic rearrangement time imposed by shear}^{-1}}{\text{confinement/inertial stabilization time}^{-1}} = \dot\gamma\, t_c, \quad t_c\sim \frac{d}{\sqrt{p/\rho_p}}.
$$

Interpretation:

*   If  $I\ll 1$ , shearing is slow compared with the time grains need to feel confinement. Contacts last a long time, the material is quasi-static and close to yield.
*   If  $I$  grows, grains are forced to rearrange more violently; collisions and dilation matter more.

So  $I$  is the granular analogue of the parameter that tells you where you are between two regimes. It is not like Reynolds number exactly, but it plays a similar organizing role.

That is why people write

$$
\mu=\mu(I),
$$

instead of a constant  $\mu$ . The idea is: the effective friction ratio increases with the intensity of rearrangement. In words, faster dense shear usually needs a larger  $\tau/p$  than barely-yielding flow.

Why is this plausible physically?

Because in dense granular flow, resistance has at least two pieces mixed together:

1.  a near-static frictional skeleton, which gives a threshold-like part;
2.  an extra dynamic cost of sustaining rearrangements, collisions, and dilation.

A constant  $\mu$  keeps only the first piece. A state-dependent  $\mu(I)$  tries to include the second.

Now, why is ** $\mu(I)$  still not enough**?

Because  $\mu(I)$  is a **local rheology**. It assumes that if you know  $p$  and  $\dot\gamma$  at one point, then you know the stress at that same point:

$$
\mu(\mathbf{x})=\mu\!\big(I(\mathbf{x})\big).
$$

That is analogous to an eddy-viscosity closure depending only on the local strain rate. It ignores spatial cooperativity.

But grains rearrange in clusters. Near yielding, one local rearrangement can trigger neighbors several grain diameters away. So the state at one point is influenced by nearby flowing regions. This is why dense granular media show things a purely local law struggles with: creeping below the nominal yield, finite-size effects, dependence on  $h/d$ , stop-height phenomena, and sensitivity to boundaries and roughness.

The PRL you’re reading points directly at this issue: it says the previous estimate of  $L$  from  $\mu(I)$  gives the wrong dependence, and attributes this to the well-documented shortcomings of  $\mu(I)$ ; it also explicitly cites the nonlocal-rheology paper by Bouzid et al. and the ill-posedness paper by Barker et al. as the relevant background.

2501.10631v1

2501.10631v1

That is where **nonlocal fluidity** comes in.

The idea is to introduce a second field, often called  $g$ , that measures how easy the material is to rearrange. Very loosely,

$$
\dot\gamma \sim g\,\mu
$$

or some equivalent relation. Then  $g$  is not just fixed locally; it obeys an equation with a diffusion-like term, schematically

$$
\xi^2 \nabla^2 g + \text{local driving} - \text{local relaxation}=0.
$$

Why is this useful? Because it lets a flowing region “lend mobility” to a nearby jammed or sub-yield region. That is exactly what you need to model creep and finite-size effects.

For a fluids person, the best analogy is this:

*   local  $\mu(I)$  is like saying turbulence is determined only by the local mean strain;
*   nonlocal fluidity is like admitting a finite correlation length and transport of activity.

That is also why this fits naturally with your critical-state reading. In the turbulence/critical-phenomena analogy, incomplete similarity appears when a formally small length scale cannot actually be discarded because correlations make it relevant. Goldenfeld and Shih describe this as a situation where the ultraviolet cutoff remains non-negligible near a critical point and anomalous exponents appear.

Goldenfeld and Shih - 2017 - Tu…

Granular yielding is similar in spirit. Near  $\mu_r$ , the relevant cooperative length grows, so a pointwise constitutive law becomes insufficient. Then a nonlocal field is not a luxury; it is the natural way to encode the growing correlation length.

So the hierarchy is:

First, use  $\tau/p$  rather than  $\tau$ , because pressure matters as much as shear stress in grain assemblies.

Then introduce

$$
I=\frac{\dot\gamma d}{\sqrt{p/\rho_p}}
$$

because dense granular flow needs a dimensionless rate measuring how fast grains are being forced to rearrange.

Then let

$$
\mu=\mu(I)
$$

because the effective friction is not constant; it changes between quasi-static and inertial/collisional dense flow.

Then go beyond local  $\mu(I)$  to **nonlocal fluidity** because rearrangements are cooperative and boundary-sensitive, especially near yield, and purely local closure misses that. The PRL’s failure of older universal flow rules and its statement that  $\mu(I)$  misses the measured development-length trends are both symptoms of that limitation.

2501.10631v1

2501.10631v1

In one sentence:

A constant friction coefficient is too crude because it ignores rate effects;  $\mu(I)$  fixes that by using the timescale ratio  $I$ ; nonlocal fluidity fixes the next failure by admitting that dense granular flow near yield is cooperative, not purely local.

If you want, I can next rewrite all of this in a strict fluid-mechanics style by deriving  $I$  from dimensional analysis of  $(\dot\gamma,p,\rho_p,d)$ , then showing where local  $\mu(I)$  fails in chute flow and why a diffusion equation for fluidity is the minimal correction.

## Prompt:
3/6/2026, 2:27:18 PM

what is the difficuty of formulating the fully developed granular flow velocity in frame of barenblatt self similarity of second kind

## Response:
3/6/2026, 2:27:24 PM

> **Searching uploaded PDFs for specific terms**
>
> The user asks about papers, and we have files uploaded. Rather than looking on the web, I’ll focus on searching these PDFs for specific terms like "Barenblatt" and "second kind". I’ll use internal tools designed for searching these documents according to developer guidelines.
>
> **Looking up relevant documents for definitions**
>
> The user likely needs a conceptual answer that includes citations. I think it would be helpful to look through the relevant documents to pinpoint the exact lines that define the concepts. I’ll start by reviewing those documents and then integrate the most useful definitions with supporting citations.
>
> Thought for 17s

The main difficulty is that **Barenblatt second-kind similarity needs a governing asymptotic problem with an eigenvalue-selection mechanism**, while the granular fully developed velocity law in the PRL is only a **dimensional scaling ansatz calibrated by data**, not the outcome of such a problem. The paper says  $v_\infty$  is obtained from dimensional analysis assuming control by  $\mu_r$  and excess shear stress, and gives

$$
v_\infty \propto \mu_r^{3/2}\,[(\tan\theta-\mu_r)h]^{4/3}
$$

in variables nondimensionalized with  $d$  and  $\sqrt{gd\cos\theta}$ .

2501.10631v1

2501.10631v1

The exponent  $4/3$  is therefore presented as part of a fitted scaling law, not as the solution of a nonlinear eigenvalue problem.

Barenblatt’s second kind is stricter. He distinguishes first-kind similarity, where dimensional analysis fixes exponents, from second-kind similarity, where the exponent cannot be obtained dimensionally and must be found by solving an ODE boundary-value problem after similarity reduction. He says anomalous exponents arise from a nonlinear eigenvalue problem and depend on details of the pre-self-similar behavior.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

In his general formulation, the exponent is selected only for those parameter values for which a nontrivial global solution satisfying the boundary conditions exists.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

So the first difficulty is **there is no accepted asymptotic PDE for the fully developed dense granular branch near  $\mu_r$ **. In turbulence, Gioia could reinterpret Manning’s law because the physical setting already had a clear momentum-transfer picture and a well-developed inertial-range phenomenology. Gioia starts from the dimensionally inconsistent Manning form and shows it is compatible with incomplete similarity in roughness, with

$$
V \sim K (r/R)^a \sqrt{Rgs},
$$

where  $a$  is not fixed by dimensional analysis.

gioia2001.pdf

gioia2001.pdf

But that is still a phenomenological closure. For the granular problem, we do not yet have an equally settled continuum description of dense chute flow near arrest that would reduce to a singular similarity problem.

The second difficulty is that **fully developed chute flow is not naturally an evolution problem with an obvious similarity variable**. Barenblatt’s classic second-kind examples are source-type spreading, implosions, flame fronts, traveling waves, and related problems where the asymptotic state emerges through time or through a moving front, and the exponent is selected by regularity at a singular point or by heteroclinic matching.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

A fully developed chute velocity is instead a **terminal uniform state**. To force it into Barenblatt form, you have to reinterpret the downstream development toward  $v_\infty$  as the asymptotic problem, not the uniform state itself. But then the measured exponent  $4/3$  belongs to the amplitude of the far downstream state, while the natural eigenvalue in a development problem would usually control the streamwise similarity exponent or a front speed. That mismatch makes formulation nontrivial.

The third difficulty is **which small parameter is essential and remains asymptotically relevant?** Barenblatt says second-kind similarity occurs when the parameter that spoils complete similarity cannot simply be discarded; it remains in the reduced dimensionless groups, and the exponents cannot be obtained from dimensional analysis.

Barenblatt - 1996 - Scaling, se…

For the granular problem, the candidates are  $d/h$ , nonlocal cooperativity length over  $h$ , or distance to threshold  $\varepsilon=\tan\theta-\mu_r$ . But the PRL writes the law directly in terms of  $(\tan\theta-\mu_r)h$  and  $d$ \-based nondimensionalization, without identifying which singular limit is producing incomplete similarity.

2501.10631v1

Without that, you cannot say what plays the role of roughness  $r/R$  in Gioia, or of the non-negligible cutoff in critical phenomena.

The fourth difficulty is **granular flow near  $\mu_r$  is probably nonlocal and state-dependent**, so a local rheology is too regular. The PRL itself notes that the  $\mu(I)$ \-based prediction for the development length  $L$  misses the observed dependence and attributes this to known shortcomings of  $\mu(I)$ .

2501.10631v1

If you try to derive  $v_\infty$  from a standard local or weakly nonlinear nonlocal closure, you usually get a regular onset law, roughly linear in the excess driving, not an anomalous exponent like  $4/3$ . In other words, the available constitutive models tend not to generate the singular orbit structure that Barenblatt needs for eigenvalue selection.

The fifth difficulty is **the critical point itself is not sharply established**. The paper strongly suggests  $\mu_r$  acts like a dynamic threshold and emphasizes that  $v_\infty$  should be controlled by  $\mu_r$  and excess shear stress, while questioning whether  $\mu_2$  is a true phase-transition point at all.

2501.10631v1

2501.10631v1

2501.10631v1

That is suggestive, but Barenblatt-style theory needs more than a suggestive threshold: it needs a precise singular limit, the reduced equations in that limit, and boundary conditions that quantize the exponent.

From your turbulence background, the best way to see the obstacle is this: in critical-phenomena language, anomalous exponents appear because the microscopic cutoff remains relevant even as the correlation length diverges. Goldenfeld and Shih summarize this as incomplete similarity or scale interference: even when  $\ell/\xi\to 0$ , the cutoff  $\ell$  cannot be dropped, and the scaling acquires anomalous exponents.

Goldenfeld and Shih - 2017 - Tu…

Goldenfeld and Shih - 2017 - Tu…

For granular flow, one suspects that grain size  $d$ , basal roughness, and a cooperativity length play this role. But unlike turbulence or standard critical phenomena, there is no accepted RG-style or asymptotic theory that tells you how these ingredients renormalize into the developed-flow velocity branch.

So the core difficulties are:

1.  **No canonical PDE** for dense chute flow near  $\mu_r$  whose asymptotics are known to be second-kind.
2.  **No obvious similarity geometry** for a fully developed terminal state; one must reformulate the downstream approach problem.
3.  **No unambiguous essential small parameter** identified as the source of incomplete similarity.
4.  **Existing rheologies are too regular**, usually giving ordinary onset scaling instead of eigenvalue-selected anomalous scaling.
5.  **The exponent in the PRL is empirical at present**, not yet tied to a solvability condition.

That is why it is easy to say “Eq. (6) looks like incomplete similarity,” but hard to actually formulate it as a Barenblatt second-kind solution. The analogy is plausible; the mathematical machinery is still missing.

A compact summary is: **the hard part is not guessing a power law, but constructing the singular asymptotic problem for which  $4/3$  is the unique admissible eigenvalue.**

## Prompt:
3/6/2026, 3:44:13 PM

  if I want to focus the undeveloped velocity which is in a intermediate range (both time and length scale), can i formulate this problem into self-similarity of second kind

## Response:
3/6/2026, 3:44:20 PM

> **Formulating self-similarity from velocity range**
>
> The user's question asks if an undeveloped velocity intermediate range can be formulated into second-kind self-similarity. I’ll focus on understanding this conceptually using the uploaded files, searching for relevant terms like the PRL velocity formula and Barenblatt. I can cite these files for support.
>
> **Looking up PRL formula for reference**
>
> I think I should look up the PRL formula related to the undeveloped velocity range—maybe the lines in the paper could shed light on it. This will help me frame a clean and conceptual answer for the user, focused on the specifics they’re asking about.
>
> Thought for 35s

Yes — **more plausibly than for the fully developed velocity**.

The undeveloped branch is already an **intermediate regime** in Barenblatt’s sense: the PRL explicitly treats  $v(l)$  as the spatial evolution from release toward the terminal state, with

$$
v = v_\infty \left[1-\exp(-l/L)\right]^{1/2},
$$

and says this regime matters when the chute length  $l$  is comparable to or smaller than the development length  $L$ .

2501.10631v1

2501.10631v1

Barenblatt defines intermediate asymptotics exactly as behavior valid at distances and times large enough to forget fine initial details, but still far from the final equilibrium state.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

So conceptually, **yes**: the undeveloped velocity is a much better candidate for a self-similar formulation than the terminal  $v_\infty$  itself.

But there is an important distinction:

*   it is fairly natural to formulate it as an **intermediate asymptotic**
*   it is **not automatically** a self-similarity of the **second kind**

For second kind, Barenblatt requires more than “intermediate range.” He requires that dimensional analysis alone be insufficient, and that the scaling exponent be selected by a nonlinear eigenvalue/solvability condition.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

For your granular problem, the most promising route is to treat downstream development as a **front/relaxation problem** in  $x$ , not as a static algebraic law. The PRL already points in that direction: it introduces  $v_0$  for the fully undeveloped limit  $l\ll L$ , then merges it with  $v_\infty$ .

2501.10631v1

So the right question is:

$$
\text{Can } v(x,z;\varepsilon,h/d) \text{ approach } v_\infty \text{ through a similarity form?}
$$

with

$$
\varepsilon = \tan\theta-\mu_r.
$$

A natural ansatz would be something like

$$
v(x,z;\varepsilon)=V_*(\varepsilon,h/d)\,\Phi\!\left(\eta,\frac{z}{h}\right), \qquad \eta=\frac{x}{\ell_*(\varepsilon,h/d)}.
$$

Then:

*   if  $V_*$  and  $\ell_*$  are fixed by dimensional balance alone, that is first kind;
*   if one small parameter such as  $d/h$  or a cooperativity length remains essential and the exponent in  $V_*\sim \varepsilon^\beta$  or  $\ell_*\sim \varepsilon^{-\nu}$  is fixed only by existence of a bounded orbit, then that is second kind.
    Barenblatt - 1996 - Scaling, se…
    Barenblatt - 1996 - Scaling, se…

In fact, the undeveloped problem has the right **geometry** for this:

1.  there is an entrance condition near the gate,
2.  there is a far-field state  $v\to v_\infty$ ,
3.  there is a characteristic length  $L$ ,
4.  and the solution is a relaxation from one state to another.

That is much closer to Barenblatt’s traveling-wave and front-selection examples than the fully developed uniform state is. Barenblatt explicitly treats traveling waves and second-kind wave problems in that framework.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

So my answer is:

*   **Yes, in principle**
*   **and the undeveloped regime is the right place to try**
*   **but only if you formulate a PDE for the streamwise development**

The likely structure is:

$$
\mathcal{N}[v,g;\varepsilon,h/d]=0,
$$

with  $g$  a nonlocal fluidity/order parameter, plus

$$
v(0,z)=v_{\text{in}}(z), \qquad v(x,z)\to v_\infty(z)\quad (x\to\infty).
$$

Then you seek a similarity/traveling-wave reduction. If the reduced ODE has a singular point or only admits a bounded heteroclinic solution for special exponents, then you truly have second kind.

Without that PDE, the PRL formula

$$
v = v_\infty [1-e^{-l/L}]^{1/2}
$$

is better read as a **merging formula**, not yet as a similarity solution. It is an excellent intermediate-asymptotic fit, but by itself it does not prove second-kind similarity.

2501.10631v1

So the sharp conclusion is:

**Yes, the undeveloped velocity is the best place to look for Barenblatt second-kind structure, because it is an intermediate asymptotic in space and possibly time. But to make that claim mathematically, you must replace the empirical merge law by a streamwise nonlocal PDE and show that the exponent is selected by a boundary-value/eigenvalue problem.**

A useful practical guess is that the similarity variable should be built from

$$
\eta = \frac{x}{L(\varepsilon,h/d)},
$$

and the second-kind part, if it exists, would show up in the scaling of  $L$  or of the entrance-layer amplitude, not necessarily directly in the exponential form itself.

If you want, I can next sketch a concrete **streamwise traveling-wave formulation** for  $v(x)$  and a nonlocal fluidity  $g(x,z)$ , and show exactly how a second-kind eigenvalue could arise for the undeveloped branch.

## Prompt:
3/6/2026, 3:50:15 PM

plz sketch a concrete streamwise traveling-wave formulation for 𝑣 ( 𝑥) v(x) and a nonlocal fluidity 𝑔 ( 𝑥 , 𝑧) g(x,z), and show exactly how a second-kind eigenvalue could arise for the undeveloped branch.

## Response:
3/6/2026, 3:50:20 PM

> **Evaluating the use of uploaded files for the answer**
>
> I'll base the answer on the files uploaded, which should provide the most relevant information. I’ll check for specific references, like Barenblatt, PRL, Gioia, or Goldenfeld, to ensure that the response is well-grounded. Let me dig through these files to find what's most useful.
>
> **Finding relevant equations and explanations**
>
> I need to provide an answer with equations and offer an explanation around a speculative prototype. I’ll look into relevant lines from the sources, like PRL and Barenblatt, especially regarding nonlinear eigenvalues or traveling waves. I’ll make sure I cover this in a meaningful way.
>
> Thought for 32s

Yes. Here is a concrete way to cast the **undeveloped branch** as a **streamwise travelling-wave / relaxation problem** and to show where a **second-kind eigenvalue** could enter.

I need to be clear about one thing first: the PRL itself gives the undeveloped law as a **merging formula**

$$
v=v_\infty\,[1-e^{-l/L}]^{1/2},
$$

with  $v_\infty\propto \mu_r^{3/2}[(\tan\theta-\mu_r)h]^{4/3}$  and  $L\propto \mu_r^3[(\tan\theta-\mu_r)h]^{5/3}h$ , and it says this came from dimensional analysis plus fitting, not from a PDE eigenvalue problem.

2501.10631v1

2501.10631v1

So what follows is a **prototype mathematical formulation**, not a derivation claimed by the paper.

Barenblatt’s standard requirement is that second-kind exponents are found from a **nonlinear boundary-value/eigenvalue problem**, not by dimensional analysis alone. He explicitly says anomalous exponents are “obtained from the solution to a nonlinear eigenvalue problem,” and that self-similar solutions are intermediate asymptotics.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

He also emphasizes the travelling-wave analogy: determining a wave speed or a similarity exponent proceeds through existence of a global invariant solution.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

1\. Why the undeveloped branch is the right target
--------------------------------------------------

The paper already frames the problem as a **spatial evolution** from release to the terminal state: the chute flow is released, accelerates downslope, and reaches a fully developed state only after a characteristic distance  $L$ .

2501.10631v1

For  $l$  comparable to or smaller than  $L$ , the flow is still in an intermediate regime, and the PRL notes that this is precisely why older flow rules failed.

2501.10631v1

That is already very close to Barenblatt’s “intermediate asymptotics”: far enough from the details of release, but not yet at the final asymptotic state.

Barenblatt - 1996 - Scaling, se…

So instead of solving directly for  $v_\infty$ , set up a **streamwise relaxation PDE** whose large- $x$  limit is the developed state.

* * *

2\. Minimal PDE system
----------------------

Take a 2D steady chute flow with streamwise coordinate  $x$  and depth coordinate  $z\in[0,h]$ . Let

*    $u(x,z)$ : downslope velocity
*    $g(x,z)$ : nonlocal granular fluidity / mobility field

Use the PRL’s natural control parameter

$$
\varepsilon=\tan\theta-\mu_r>0,
$$

since the paper treats  $\mu_r$  as the dynamic threshold and uses excess shear stress  $\sim (\tan\theta-\mu_r)h$  as the driver.

2501.10631v1

A simple prototype is

$$
\partial_x u+\partial_z w=0, \tag{1}
$$
 
$$
u\,\partial_x u+w\,\partial_z u = \varepsilon-\partial_z\!\big(g\,\partial_z u\big), \tag{2}
$$
 
$$
\xi^2(\varepsilon,h/d)\,\partial_{xx} g +\ell^2(\varepsilon,h/d)\,\partial_{zz} g +\sigma(\varepsilon)\,g -\kappa g^2 +\chi\,|\partial_z u|^m=0. \tag{3}
$$

Interpretation:

*   the term  $\varepsilon$  is the excess downslope driving above the threshold;
*    $g\,\partial_z u$  plays the role of a shear-transport stress;
*    $g$  is produced by shear, relaxes nonlinearly, and spreads both along  $x$  and across  $z$ .

This is the minimal structure needed to encode a growing correlation length near threshold, which is exactly the kind of “small but non-negligible” scale Barenblatt and the turbulence/critical-phenomena analogy emphasize.

Goldenfeld and Shih - 2017 - Tu…

Barenblatt - 1996 - Scaling, se…

Boundary conditions:

$$
u(x,0)=0,\qquad g(x,0)=0, \tag{4}
$$
 
$$
\partial_z u(x,h)=0,\qquad \partial_z g(x,h)=0, \tag{5}
$$
 
$$
u(0,z)=u_{\rm in}(z),\qquad g(0,z)=g_{\rm in}(z), \tag{6}
$$
 
$$
u(x,z)\to u_\infty(z),\qquad g(x,z)\to g_\infty(z)\quad (x\to\infty). \tag{7}
$$

This is a streamwise relaxation problem from an inlet state to a terminal state.

* * *

3\. Travelling-wave / intermediate-asymptotic reduction
-------------------------------------------------------

Barenblatt notes that travelling-wave problems and self-similar problems are closely connected; determining a wave speed is analogous to determining a self-similar exponent.

Barenblatt - 1996 - Scaling, se…

Introduce a streamwise similarity variable

$$
\eta=\frac{x}{\Lambda(\varepsilon,h/d)},
$$

where  $\Lambda$  is an a priori unknown development length scale.

Seek

$$
u(x,z)=U_*(\varepsilon,h/d)\,\Phi(\eta,\zeta),\qquad g(x,z)=G_*(\varepsilon,h/d)\,\Psi(\eta,\zeta),\qquad \zeta=\frac{z}{h}. \tag{8}
$$

Here  $U_*$  and  $\Lambda$  are not yet fixed. The undeveloped branch is the  $\eta=O(1)$  regime.

Substitute into (2)-(3). Up to order-one constants, the momentum equation becomes

$$
\frac{U_*^2}{\Lambda}\,\Phi\,\partial_\eta\Phi \sim \varepsilon - \frac{G_*U_*}{h^2}\,\partial_\zeta\!\big(\Psi\,\partial_\zeta\Phi\big), \tag{9}
$$

and the fluidity equation becomes

$$
\frac{\xi^2}{\Lambda^2}G_*\,\partial_{\eta\eta}\Psi + \frac{\ell^2}{h^2}G_*\,\partial_{\zeta\zeta}\Psi + \sigma G_*\,\Psi -\kappa G_*^2\Psi^2 + \chi \left(\frac{U_*}{h}\right)^m |\partial_\zeta\Phi|^m =0. \tag{10}
$$

So the scaling problem is now: choose  $U_*$ ,  $G_*$ , and  $\Lambda$  so that a nontrivial  $(\Phi,\Psi)$  exists.

* * *

4\. Depth-mode projection
-------------------------

Now do the standard transverse-mode reduction. Expand

$$
\Phi(\eta,\zeta)=A(\eta)\,\varphi(\zeta),\qquad \Psi(\eta,\zeta)=B(\eta)\,\psi(\zeta). \tag{11}
$$

The vertical eigenproblem comes from the  $\zeta$ \-structure:

$$
\frac{d}{d\zeta}\!\left(\psi\,\frac{d\varphi}{d\zeta}\right)+\lambda\,\varphi=0, \tag{12}
$$
 
$$
\ell_0^2\,\psi''+\alpha\,\psi+\beta\left|\varphi'\right|^m=0, \tag{13}
$$

with

$$
\varphi(0)=0,\quad \varphi'(1)=0,\qquad \psi(0)=0,\quad \psi'(1)=0. \tag{14}
$$

For generic  $\lambda$ , you do not get a nontrivial bounded pair  $(\varphi,\psi)$  satisfying all four conditions. Only special  $\lambda$  work. That is the first eigenvalue:

$$
\lambda=\lambda_*.
$$

This is exactly the kind of “exceptional values” language Barenblatt uses for invariant global solutions.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

Projecting the PDEs onto this leading transverse mode gives an amplitude system

$$
c_1\,A A' = c_2 - c_3 B A, \tag{15}
$$
 
$$
d_1\,B'' + d_2 B - d_3 B^2 + d_4 A^m = 0, \tag{16}
$$

where the coefficients  $c_i,d_i$  are depth integrals built from  $\varphi,\psi$ , hence functions of  $\lambda_*$ .

The exact formulas are of the form

$$
c_1=\int_0^1 \varphi^2\,d\zeta,\qquad c_3=\int_0^1 \varphi\,\partial_\zeta(\psi\varphi')\,d\zeta,
$$
 
$$
d_1=\int_0^1 \psi^2\,d\zeta,\qquad d_4=\int_0^1 \psi\,|\varphi'|^m\,d\zeta,
$$

etc. Their exact numerical values do not matter for the selection logic.

* * *

5\. Heteroclinic formulation of the undeveloped branch
------------------------------------------------------

The undeveloped-to-developed transition is now the orbit of (15)-(16) from inlet to far field:

$$
A(0)=A_{\rm in},\qquad B(0)=B_{\rm in}, \tag{17}
$$
 
$$
A(\eta)\to A_\infty,\qquad B(\eta)\to B_\infty \quad (\eta\to\infty). \tag{18}
$$

The far-field state solves

$$
c_2-c_3 B_\infty A_\infty=0, \tag{19}
$$
 
$$
d_2 B_\infty-d_3 B_\infty^2+d_4 A_\infty^m=0. \tag{20}
$$

This is now a genuine **two-point nonlinear boundary-value problem**. For generic parameter choices, a global bounded monotone connection from  $(A_{\rm in},B_{\rm in})$  to  $(A_\infty,B_\infty)$  does not exist. Only for special scalings of  $U_*$  and  $\Lambda$  do you get such a connection.

That is where second-kind selection enters.

Barenblatt’s flame example is precisely of this type: a travelling-wave ansatz reduces the PDE to an ODE with boundary conditions at  $\pm\infty$ , and the wave-speed parameter is selected by the existence of the orbit.

Barenblatt - 1996 - Scaling, se…

* * *

6\. Where the anomalous exponent enters
---------------------------------------

Now define the amplitude scales as

$$
U_*(\varepsilon,h/d)=\varepsilon^\beta\,\Big(\frac{h}{d}\Big)^\gamma \sqrt{gd\cos\theta}, \tag{21}
$$
 
$$
\Lambda(\varepsilon,h/d)=d\,\varepsilon^{-\nu}\,\Big(\frac{h}{d}\Big)^\delta. \tag{22}
$$

The key point is that  $\beta,\nu,\gamma,\delta$  are left **unknown**.

Substituting these into the reduced equations forces certain balance relations. For example, from inertia versus excess driving in (9),

$$
\frac{U_*^2}{\Lambda}\sim \varepsilon \quad\Rightarrow\quad 2\beta+\nu=1, \tag{23}
$$

up to whatever  $h/d$ \-dependence is needed to balance the depth terms.

So if  $\nu$  is known,  $\beta$  follows:

$$
\beta=\frac{1-\nu}{2}. \tag{24}
$$

But  $\nu$  is **not** obtained from dimensional analysis. It is fixed by the requirement that the amplitude system (15)-(16) admit a global heteroclinic solution satisfying (17)-(18). Symbolically,

$$
\mathcal{F}(\nu,\lambda_*;m,\kappa,\chi,\dots)=0. \tag{25}
$$

That is the Barenblatt-style nonlinear eigenvalue condition.

So the exponent selection chain is:

1.  solve the transverse nonlinear eigenproblem  $\to \lambda_*$ ;
2.  insert  $\lambda_*$  into the streamwise amplitude equations;
3.  require a global bounded inlet-to-far-field orbit;
4.  this selects  $\nu$ ;
5.  then  $\beta=(1-\nu)/2$ .

That is exactly the “exponents are found in the process of solving the problem, analogously to the determination of eigenvalues” statement in Barenblatt.

Barenblatt - 1996 - Scaling, se…

* * *

7\. How the PRL merging law fits into this picture
--------------------------------------------------

If the selected heteroclinic orbit near the developed state is linearized, you get

$$
A_\infty-A(\eta)\sim e^{-s\eta}, \tag{26}
$$

for some positive eigenvalue  $s$  of the linearization.

Then the surface velocity

$$
v(x)\sim V_\infty\,[1-Ce^{-x/\Lambda}]^{1/2} \tag{27}
$$

is perfectly natural after a simple amplitude-to-velocity mapping. So the PRL form

$$
v=v_\infty[1-e^{-l/L}]^{1/2} \tag{28}
$$

can be reinterpreted as the observable signature of a stable heteroclinic relaxation, with  $L$  proportional to the selected streamwise scale  $\Lambda$ .

2501.10631v1

In other words, their empirical merge law is exactly the kind of shape you would expect from a travelling-wave / relaxation problem. What is missing in the paper is the PDE and the eigenvalue selection step.

* * *

8\. Why this is second kind rather than first kind
--------------------------------------------------

Barenblatt warns that one may not simply assume a small dimensionless parameter can be discarded; sometimes the limit is not a constant, and the small parameter remains in the asymptotic law with an anomalous exponent.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

In his fractal example, the small scale stays in the result and the exponent is not obtainable dimensionally.

Barenblatt - 1996 - Scaling, se…

Here the analogous “small but essential” parameter is the grain-scale/nonlocal scale relative to  $h$ , encoded through  $\xi(\varepsilon,h/d)$  and  $\ell(\varepsilon,h/d)$ . If that length can’t be discarded near  $\varepsilon\to0^+$ , then the undeveloped branch is a plausible second-kind problem.

So the essential structure is:

$$
\eta=\frac{x}{d\,\varepsilon^{-\nu}(h/d)^\delta}, \qquad v(x)=\varepsilon^\beta (h/d)^\gamma \sqrt{gd\cos\theta}\,\,\mathcal{V}(\eta), \tag{29}
$$

where  $\beta,\nu$  are **selected by solvability**, not by Buckingham- $\Pi$ .

* * *

9\. Bottom line
---------------

A concrete Barenblatt-style formulation for the undeveloped branch is:

*   use  $u(x,z)$  and a nonlocal fluidity  $g(x,z)$ ;
*   pose a steady streamwise-relaxation PDE system like (1)-(3);
*   reduce in depth to a leading transverse mode with eigenvalue  $\lambda_*$ ;
*   obtain a streamwise amplitude system with boundary conditions at inlet and at  $x\to\infty$ ;
*   require a global heteroclinic orbit;
*   that solvability condition selects the streamwise exponent  $\nu$ , and then the velocity exponent  $\beta$ .

So the undeveloped branch is indeed the right place to look for **self-similarity of the second kind**, because it naturally has the travelling-wave / intermediate-asymptotic geometry Barenblatt emphasizes.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

The next useful step would be to pick one specific constitutive choice for  $\sigma(\varepsilon)$ ,  $\xi(\varepsilon,h/d)$ , and the shear-production exponent  $m$ , then carry out the phase-plane analysis of (15)-(16). That is the point where one can see whether an exponent close to the PRL’s  $4/3$  is even possible.

## Prompt:
3/6/2026, 5:01:19 PM

 what is global heteroclinic orbit;

## Response:
3/6/2026, 5:01:19 PM

> Thought for 6s

A **heteroclinic orbit** is a trajectory in a dynamical system that connects **two different equilibria**.

In your problem, after reducing the PDE to an ODE in the streamwise similarity variable  $\eta=x/\Lambda$ , the unknown amplitudes might satisfy something like

$$
A' = F(A,B),\qquad B' = G(A,B).
$$

Then the pair  $(A(\eta),B(\eta))$  is a curve in the phase plane.

If there are two fixed points

$$
(A_-,B_-),\qquad (A_+,B_+),
$$

meaning

$$
F(A_\pm,B_\pm)=0,\qquad G(A_\pm,B_\pm)=0,
$$

then a heteroclinic orbit is a solution such that

$$
(A(\eta),B(\eta))\to (A_-,B_-)\quad \text{as }\eta\to -\infty,
$$

and

$$
(A(\eta),B(\eta))\to (A_+,B_+)\quad \text{as }\eta\to +\infty.
$$

So it is literally a path that starts at one equilibrium and ends at another.

For your undeveloped granular-flow problem, the physical interpretation is:

*   one equilibrium = the **inlet / undeveloped state**
*   the other equilibrium = the **fully developed downstream state**

So the whole spatial development of the flow is represented by one orbit connecting those two states.

Why “global”? Because you do not just want a local solution near one end. You want one solution defined for the entire domain,

$$
-\infty < \eta < \infty \quad\text{or}\quad 0\le \eta < \infty,
$$

that stays bounded and reaches the correct limit at the far end.

Why is this important for second-kind similarity? Because usually such a connection does **not** exist for arbitrary exponent values. Only special values of the unknown exponent or scaling parameter make the connection possible. That is where the “eigenvalue” comes from.

A simple analogy:

Suppose after reduction you get one ODE

$$
A''+cA'-V'(A)=0,
$$

with

$$
A(-\infty)=A_-,\qquad A(+\infty)=A_+.
$$

Here  $c$  may be unknown. In general, for a random  $c$ , no trajectory connects the two equilibria. But for one special  $c=c_*$ , a connecting orbit exists. Then  $c_*$  is selected like an eigenvalue.

That is exactly the same logic in your granular setting:

*   reduce PDE to ODEs in  $\eta$ ,
*   identify inlet and developed fixed points,
*   require one bounded orbit connecting them,
*   the requirement selects a special scaling exponent or length exponent.

Geometrically, in phase space:

*   the inlet equilibrium has an unstable manifold,
*   the developed equilibrium has a stable manifold,
*   a heteroclinic orbit exists only if those manifolds intersect.

So the phrase **global heteroclinic orbit** just means:

> one everywhere-defined solution curve in the reduced phase space that connects the undeveloped state to the developed state.

For your chute-flow interpretation, it is the mathematical version of

> “starting from the entrance condition, the flow relaxes continuously to the fully developed branch downstream.”

If you want, I can draw a tiny phase-plane sketch and map each point on it to the physical chute-flow picture.

## Prompt:
3/6/2026, 8:28:34 PM

how to pick one specific constitutive choice for 𝜎 ( 𝜀) σ(ε), 𝜉 ( 𝜀 , ℎ / 𝑑) ξ(ε,h/d), and the shear-production exponent 𝑚 m, then carry out the phase-plane analysis of (15)-(16).

## Response:
3/6/2026, 8:28:41 PM

> **Gathering sources for mathematical method**
>
> The user is asking something mathematical/conceptual. I'll need to find relevant sources, probably pulling from official papers on NGF and related topics. Since there’s a requirement for web citations, I’ll look up key papers and might use previous files if needed. Let me search the web for key studies.
>
> **Searching for key papers on granular fluidity and rheology**
>
> [Nonlocal Constitutive Relation for Steady Granular Flow | Phys. Rev. Lett.](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.108.178301)
> [A constitutive law for dense granular flows | Nature](https://www.nature.com/articles/nature04801)
>
> **Considering citing uploaded PRL paper**
>
> I probably need to cite the user's uploaded PRL paper, so I’ll check it out before finalizing my answer. I’ll search through the uploaded file to find the relevant details. This way, I can make sure I include all necessary references – including any from that file.
>
> **Explaining sigma, phase-plane, and choices**
>
> I don't think I need any extra tools here, but I need to focus on explaining how to choose sigma (σ) and apply the phase-plane for equations 15-16. It seems like we could choose σ = ε/Δμ based on literature, and for ξ(ε,h/d), something like A d / sqrt(ε) would work well for finite-size shifts. m looks like it should be 1 or 2, based on fluidity.
>
> **Analyzing fluid dynamics equations for phase-plane**
>
> In Kamrin/Koval fluidity, I’m using the equation where shear rate γ is related to fluidity g. There’s a saturation term, so g² appears, not an exponent. I need to project modes and derive a 2D phase plane with nullclines, fixed points, etc. I'll simplify coefficients for clarity and use β for the phase-plane constant.
>
> **Refining phase-plane and fixed points**
>
> It looks like I've got an energy integral H, with fixed points at (0,0) and (α/β,0) if α > 0. There's a damping term from advection, so the amplitude equation should include a first derivative due to the convective term. I’ve found that for stability near (0,0), eigenvalues lead to a center at (0,0).
>
> **Clarifying front equation and wave behavior**
>
> I’m thinking through how to set up the front ODE under a travelling wave framework. The equation becomes D A'' + c A' + α A - β A² = 0, and I see it’s linear around 0 with both roots negative if c > 0. But, when considering spatial relaxation and defining the coordinate, we aim for a steady state where a(0)=0 and a(∞)=α/β.
>
> **Refining phase-plane and boundary conditions**
>
> I’m assessing a better approach by treating x as time-like, reformulating the equations to avoid sign confusion. By setting up a first-order depth-averaged system, I can define the phase plane clearly, ensuring a stable downstream point at α/β. I’ll ensure c>0 for stability and clarity in the transition.
>
> Thought for 2m 42s

A workable choice is to use the **nonlocal granular-fluidity (NGF)** model as the constitutive backbone, because it already gives you three things you want:

1.  a near-yield control parameter,
2.  a diverging relaxation length,
3.  a closed route to a streamwise amplitude equation.

The key public references are Jop–Forterre–Pouliquen for the local  $\mu(I)$  law, Kamrin–Koval for the NGF closure, and Bouzid et al. for the divergence of the relaxation length like inverse square root of distance to yield. [Nature+2Physical Review Journals+2](https://www.nature.com/articles/nature04801?utm_source=chatgpt.com) The PRL you are reading also explicitly says its  $v_\infty$  law is based on dimensional analysis around  $\mu_r$  and excess shear stress, and that the  $\mu(I)$  prediction for  $L$  misses the observed trends.

2501.10631v1

2501.10631v1

1\. Pick a specific constitutive law
------------------------------------

Use the steady NGF form in terms of fluidity  $g$ :

$$
\dot\gamma=\mu\,g,
$$
 
$$
A^2 d^2 \nabla^2 g + \Delta\mu\,\frac{\mu-\mu_s}{\mu_2-\mu}\,g - b\,\mu\,T\,g^2 = 0.
$$

This is the steady version of the Kamrin–Koval/Henann–Kamrin model family: local rheology written in fluidity form, then augmented by a Laplacian term scaled by grain size  $d$ . [Physical Review Journals+1](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.108.178301?utm_source=chatgpt.com)

Here:

*    $\mu=\tau/p$ ,
*    $\mu_s$  is the local yield friction,
*    $\Delta\mu=\mu_2-\mu_s$ ,
*    $A$  is the nonlocal amplitude,
*    $T$  is the local time scale factor from pressure normalization.

For chute flow near your critical value, identify

$$
\mu=\tan\theta=\mu_r+\varepsilon,
$$

and, to leading order, take  $\mu_s=\mu_r$ . The PRL’s data support  $\mu_r$  as the dynamic threshold and show  $\mu_1\approx\mu_r$ .

2501.10631v1

2501.10631v1

So the natural choice is

$$
\sigma(\varepsilon) \equiv \Delta\mu\,\frac{\mu-\mu_r}{\mu_2-\mu} = \Delta\mu\,\frac{\varepsilon}{\mu_2-\mu_r-\varepsilon}.
$$

Near threshold,

$$
\sigma(\varepsilon)\approx \frac{\Delta\mu}{\mu_2-\mu_r}\,\varepsilon \equiv a\,\varepsilon.
$$

This is the cleanest choice because it is exactly the quantity that controls the NGF relaxation length. Bouzid et al. found that the relaxation length diverges as inverse square root of distance to yield on both sides of the yield point. [Physical Review Journals](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.111.238301?utm_source=chatgpt.com)

So choose

$$
\xi(\varepsilon)=\frac{A d}{\sqrt{\sigma(\varepsilon)}} \sim \varepsilon^{-1/2}.
$$

That is the most defensible pick for  $\xi$ .

About  $h/d$ : I would **not** put  $h/d$  directly into  $\xi$  at first. Let finite-depth enter through the depth eigenvalue. That is cleaner mathematically. The competition is then between the intrinsic nonlocal length  $\xi(\varepsilon)$  and the geometric depth  $h$ , rather than baking  $h/d$  into the constitutive law by hand.

For the exponent  $m$ , the best specific choice is

$$
m=1.
$$

Reason: in NGF, the local kinematic closure is already linear,

$$
\dot\gamma=\mu g.
$$

So near onset, production of motion is linear in fluidity. If you insist on the earlier generic source term  $|\partial_z u|^m$ , then  $m=1$  is the consistent near-threshold linearization. Taking  $m\neq 1$  is a model extension, not the canonical NGF choice. [Physical Review Journals+1](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.108.178301?utm_source=chatgpt.com)

So the concrete picks are:

$$
\sigma(\varepsilon)=a\varepsilon \quad \text{or} \quad \Delta\mu\frac{\varepsilon}{\mu_2-\mu_r-\varepsilon},
$$
 
$$
\xi(\varepsilon)=\frac{A d}{\sqrt{\sigma(\varepsilon)}},
$$
 
$$
m=1.
$$

2\. Reduce to a depth-mode amplitude equation
---------------------------------------------

Let  $z\in[0,h]$ , with rough base and zero-flux top:

$$
g(x,0)=0,\qquad \partial_z g(x,h)=0.
$$

Linearizing the NGF equation about  $g=0$  gives

$$
A^2 d^2(\partial_{xx}g+\partial_{zz}g)+\sigma(\varepsilon)\,g=0.
$$

Use the depth mode expansion

$$
g(x,z)=a(x)\psi(\zeta),\qquad \zeta=z/h.
$$

Then the transverse problem is

$$
\psi''+\lambda \psi=0,\qquad \psi(0)=0,\qquad \psi'(1)=0,
$$

so

$$
\lambda_n=\left(n+\tfrac12\right)^2\pi^2, \qquad \psi_n(\zeta)=\sin\!\left[\left(n+\tfrac12\right)\pi\zeta\right].
$$

Keep only the first mode:

$$
\lambda_0=\frac{\pi^2}{4}, \qquad \psi_0(\zeta)=\sin\!\left(\frac{\pi\zeta}{2}\right).
$$

That gives the effective linear growth rate

$$
\alpha(\varepsilon,h) = \sigma(\varepsilon)-\frac{A^2 d^2\lambda_0}{h^2}.
$$

This is the physically important quantity. It says:

*    $\sigma(\varepsilon)$  tries to fluidize,
*   finite depth penalizes the mode by  $d^2/h^2$ .

So the onset condition is

$$
\alpha=0 \quad\Longleftrightarrow\quad \sigma(\varepsilon_c)=\frac{A^2 d^2\lambda_0}{h^2}.
$$

Near threshold, with  $\sigma\approx a\varepsilon$ ,

$$
\varepsilon_c(h)\approx \frac{A^2 d^2\lambda_0}{a h^2}.
$$

That is exactly the kind of finite-size shift you want in a critical-state reading.

3\. Add streamwise relaxation and get a phase plane
---------------------------------------------------

To get a genuine streamwise development problem, do not stop at the static amplitude equation. Use the depth-projected streamwise NGF balance in the simplest reaction-diffusion-convection form:

$$
D\,a'' - c\,a' + \alpha a - \beta a^2 = 0,
$$

with

$$
D=A^2 d^2,\qquad \alpha=\sigma(\varepsilon)-\frac{A^2 d^2\lambda_0}{h^2},\qquad \beta>0.
$$

Here  $c$  is the effective downstream transport coefficient after projection. It is the quantity that plays the role of a front speed / relaxation parameter in the reduced problem.

Now write it as a first-order system:

$$
a' = p,
$$
 
$$
p' = \frac{c}{D}p - \frac{\alpha}{D}a + \frac{\beta}{D}a^2.
$$

This is the phase plane you asked for.

The fixed points are:

$$
(a,p)=(0,0), \qquad (a,p)=\left(\frac{\alpha}{\beta},0\right),
$$

provided  $\alpha>0$ .

Interpretation:

*    $(0,0)$ : undeveloped / nearly arrested state,
*    $(\alpha/\beta,0)$ : developed flowing state.

4\. Linear stability of the fixed points
----------------------------------------

At  $(0,0)$ , the Jacobian is

$$
J_0= \begin{pmatrix} 0 & 1\\ -\alpha/D & c/D \end{pmatrix}.
$$

The eigenvalues satisfy

$$
r^2-\frac{c}{D}r+\frac{\alpha}{D}=0.
$$

At  $(\alpha/\beta,0)$ , the Jacobian is

$$
J_1= \begin{pmatrix} 0 & 1\\ \alpha/D & c/D \end{pmatrix},
$$

with eigenvalues

$$
r^2-\frac{c}{D}r-\frac{\alpha}{D}=0.
$$

So, for  $\alpha>0$ :

*   one fixed point is saddle-like,
*   the other can be node/focus depending on  $c^2-4D\alpha$ .

For a monotone physical development from inlet to downstream state, you want a **heteroclinic connection** from the unstable manifold of the undeveloped state to the stable manifold of the developed state.

That is the phase-plane criterion.

5\. How to actually pick  $c$ : the selection rule
--------------------------------------------------

This is where the eigenvalue logic enters.

For arbitrary  $c$ , the invariant manifolds usually do **not** connect. A global bounded orbit exists only for special  $c$ . In Fisher–KPP-type front problems, the solvability condition is a minimum-speed rule,

$$
c \ge c_* = 2\sqrt{D\alpha}.
$$

At the selected value,

$$
c_*=2\sqrt{D\alpha},
$$

the orbit is marginally monotone. This is the simplest explicit example of how a global heteroclinic condition selects a parameter.

So the clean procedure is:

1.  choose  $\sigma(\varepsilon)$  from NGF,
2.  compute  $\alpha(\varepsilon,h)$ ,
3.  set  $D=A^2 d^2$ ,
4.  solve the phase plane,
5.  require a monotone heteroclinic orbit,
6.  obtain the selected  $c_*$ .

Then the streamwise development length is

$$
L \sim \frac{D}{c_*} \sim \sqrt{\frac{D}{\alpha}} = \frac{A d}{\sqrt{\sigma(\varepsilon)-A^2 d^2\lambda_0/h^2}}.
$$

Near onset,

$$
L \sim \left(\varepsilon-\varepsilon_c(h)\right)^{-1/2}.
$$

That scaling is fully consistent with NGF/Bouzid-style relaxation physics. [Physical Review Journals+1](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.111.238301?utm_source=chatgpt.com)

6\. What this buys you, and what it does not
--------------------------------------------

This choice is good because it is:

*   specific,
*   literature-grounded,
*   mathematically closed,
*   easy to analyze in the phase plane.

But it also shows something important:

**with the standard NGF choices above, you do not get the PRL’s  $4/3$  exponent.**

You get a conventional near-onset front problem with

$$
\alpha \sim \varepsilon-\varepsilon_c(h), \qquad L\sim (\varepsilon-\varepsilon_c)^{-1/2},
$$

not

$$
v_\infty \sim \varepsilon^{4/3}.
$$

That matches the PRL’s own statement that the  $\mu(I)$ \-type prediction for  $L$  is too weak and does not capture the measured trends.

2501.10631v1

So this is the right baseline model, but not yet the second-kind model that would produce an anomalous exponent.

7\. When would this become “second kind”?
-----------------------------------------

In the present NGF setup, the front selection  $c_*=2\sqrt{D\alpha}$  is still basically first-kind: the exponent  $-1/2$  comes from ordinary balance.

To get Barenblatt second-kind behavior, you need one more singular ingredient so that the selected parameter is not dimensionally obvious. For example:

*   a non-analytic saturation term,  $g^{1+\delta}$  with unknown  $\delta$ ,
*   a mobility coefficient  $A$  that itself renormalizes with  $\varepsilon$ ,
*   a moving internal yield surface,
*   or a matched inner layer at the base where  $d$  remains explicitly essential.

Then the heteroclinic existence condition could select an exponent, rather than just a prefactor or a square-root law.

So the honest summary is:

*   **Best constitutive choice**: NGF with  $\sigma(\varepsilon)=\Delta\mu\,\varepsilon/(\mu_2-\mu_r-\varepsilon)$ ,  $\xi=A d/\sqrt{\sigma}$ ,  $m=1$ .
*   **Best phase-plane reduction**:  $D a''-c a'+\alpha a-\beta a^2=0$ , with  $\alpha=\sigma-A^2 d^2\lambda_0/h^2$ .
*   **Best selection rule**: require a global heteroclinic orbit, which selects  $c$  and therefore  $L$ .
*   **Main limitation**: this standard route gives a regular NGF onset law, not the anomalous  $4/3$ .

If you want, the next step is to take this exact phase-plane system and draw the nullclines, eigen-directions, and heteroclinic connection explicitly, so you can see where the selected  $c_*$  comes from geometrically.

## Prompt:
3/7/2026, 11:45:17 PM

traveling-wave

expain the traveling wave problem of second kind in barenblatt book

## Response:
3/7/2026, 11:45:20 PM

> **Investigating Barenblatt's traveling-wave problem**
>
> I’m looking for information specific to Barenblatt’s traveling-wave problem from his book. I’ll check both web sources and the uploaded PDF for any relevant citations. I think using a search tool to look through the file might help me pinpoint exact references. I should also confirm against available web resources too.
>
> **Searching for Fisher-KPP and Barenblatt connection**
>
> I’ll search to see if there’s an association between Fisher-KPP and Barenblatt. It seems like this could be an important link. I’ll check web sources, and Google Books might have some useful snippets if they’re relevant. This should help me refine the response.
>
> **Searching for Fisher-KPP and Barenblatt associations**
>
> [Self-similarity and intermediate asymptotics (Chapter 2) - Scaling](https://www.cambridge.org/core/books/scaling/selfsimilarity-and-intermediate-asymptotics/3498C2293E135805460067FD0A4A2FB8)
> [Self-similarities of the second kind: first examples (Chapter 3) - Scaling, Self-similarity, and Intermediate Asymptotics](https://resolve.cambridge.org/core/services/aop-cambridge-core/content/view/32CE4F02CD5DDCB77DEA5BE68E5F4BA6/9781107050242c3_p95-118_CBO.pdf/selfsimilarities_of_the_second_kind_first_examples.pdf)
>
> Thought for 27s

In Barenblatt’s book, the **traveling-wave problem of the second kind** is the wave analogue of **self-similarity of the second kind**.

The core idea is this:

A traveling wave has the form

$$
u(x,t)=\Theta(\xi),\qquad \xi=x-\Lambda t+c,
$$

where  $\Lambda$  is the propagation speed. Barenblatt divides such waves into two classes.

For **waves of the first kind**,  $\Lambda$  is fixed by outer conservation laws alone, like the Rankine–Hugoniot condition for shocks. The internal dissipative layer adapts to that speed, but does not determine it. He uses the Burgers shock as the model example.

Barenblatt - 1996 - Scaling, se…

For **waves of the second kind**, outer conservation laws are not enough. The speed  $\Lambda$  is determined only after solving the **internal structure** of the transition layer, and only special values of  $\Lambda$  allow a global solution satisfying the boundary conditions at both ends. That is why Barenblatt says the wave speed is found “as some eigenvalue” of the traveling-wave boundary-value problem.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

That is the precise analogy with self-similarity of the second kind:

*   in self-similarity of the first kind, dimensional analysis fixes the exponent;
*   in self-similarity of the second kind, dimensional analysis does not fix it, and the exponent is selected by a nonlinear eigenvalue problem;
*   for traveling waves, the corresponding selected quantity is the **wave speed**.
    Barenblatt - 1996 - Scaling, se…
    Barenblatt - 1996 - Scaling, se…

Barenblatt makes this correspondence explicit. In the introduction he says that traveling waves of the second type are those for which the speed is found from the condition for existence of a global solution describing the internal structure, and that this classification is in one-to-one correspondence with the classification of self-similar solutions into first and second kind.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

The book’s concrete second-kind example is the **flame front**. After the traveling-wave substitution, the PDE reduces to an ODE boundary-value problem, and the admissible propagation speed is the value for which the profile connects the burned and unburned states. In Barenblatt’s notation this becomes a nonlinear eigenvalue problem; he proves there is a unique  $\lambda_0$  such that the lower separatrix reaches the required endpoint, so the speed is selected by existence of the connecting orbit.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

A good modern summary of the book’s structure is Cambridge’s table of contents: Chapter 7 is “Self-similar solutions and travelling waves,” including “Flame: steady travelling wave of the second kind” and “Nonlinear eigenvalue problem,” followed by Chapter 8 on eigenvalues and stability. [Cambridge University Press & Assessment+1](https://www.cambridge.org/core/books/scaling-selfsimilarity-and-intermediate-asymptotics/selfsimilar-solutions-and-travelling-waves/C2F7DC8D7E06B664AE8BFC3498062A25?utm_source=chatgpt.com)

So, in plain language, Barenblatt’s “traveling wave of the second kind” means:

1.  You assume a front-like form  $u(x,t)=\Theta(x-\Lambda t)$ .
2.  Conservation laws alone do **not** determine  $\Lambda$ .
3.  You solve the ODE for the internal wave profile.
4.  Only special  $\Lambda$  let the profile satisfy both far-field boundary conditions.
5.  That selected  $\Lambda$  is the nonlinear eigenvalue.

Geometrically, this is a **heteroclinic-connection problem** in phase space: the wave profile must connect one equilibrium state at  $\xi=-\infty$  to another at  $\xi=+\infty$ . If the connection exists only for special  $\Lambda$ , then the wave is of the second kind.

This is why Barenblatt treats traveling waves as the cleanest way to understand second-kind similarity: the “unknown exponent” in a self-similar law plays the same role as the “unknown wave speed” in a traveling front.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

For your granular-flow project, that analogy is very useful. It suggests that the undeveloped chute-flow branch should be formulated not as an algebraic fit, but as a **streamwise front/relaxation problem** whose selected development scale or amplitude exponent comes from existence of a global connecting solution.

If you want, I’ll map Barenblatt’s flame example line-by-line into the granular undeveloped-flow problem notation.

## Prompt:
3/8/2026, 1:43:50 AM

map Barenblatt’s flame example line-by-line into the granular undeveloped-flow problem notation.

## Response:
3/8/2026, 1:43:56 AM

> **Searching uploaded files and verifying with web sources**
>
> I need to work with the files the user uploaded, especially the Barenblatt 1996 file. I’ll search through the files for terms like “flame,” “traveling wave,” and “second kind.” Also, since the developer recommends it, I’ll double-check web sources to verify the information.
>
> **Looking for accurate online sources with citations**
>
> I need to look for official sources and find relevant citations. Since the user asked about Barenblatt’s book mapping, I’ll focus on searching for related topics, like the Cambridge Table of Contents and any information about the flame KPP. Google Books might not be ideal, so Cambridge seems like a better option.
>
> **Searching for Barenblatt flame wave references and citations**
>
> [Self-similar solutions and travelling waves (Chapter 7) - Scaling, Self-similarity, and Intermediate Asymptotics](https://www.cambridge.org/core/books/scaling-selfsimilarity-and-intermediate-asymptotics/selfsimilar-solutions-and-travelling-waves/C2F7DC8D7E06B664AE8BFC3498062A25)
> [Contents - Scaling, Self-similarity, and Intermediate Asymptotics](https://resolve.cambridge.org/core/books/scaling-selfsimilarity-and-intermediate-asymptotics/contents/1E620CD8BE14DDD723F9120A4A185F5D)
>
> **Refining maps and equations for clarity**
>
> I need to provide a concise yet helpful response with citations from both the files and web sources. I’ll map relevant snippets line-by-line, likely including equations from the file. I should check specific sections, especially around flame equations like maybe 7.56, and open them for more details.
>
> Thought for 44s

Yes. The cleanest way is to map Barenblatt’s flame problem into your **undeveloped chute-flow** problem item by item.

Barenblatt’s general point is that travelling waves of the second kind are those for which the propagation speed is **not** fixed by conservation laws alone, but by the condition that a **global internal-structure solution** exists; he puts flame waves in exactly that class. He also states the one-to-one correspondence between travelling waves of the second kind and self-similar solutions of the second kind.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

The book’s chapter layout confirms that Ch. 7 treats “Flame: steady travelling wave of the second kind,” then “Nonlinear eigenvalue problem,” then “Flame propagation in a reacting mixture: an intermediate asymptotics.”

Barenblatt - 1996 - Scaling, se…

The Cambridge listing for the book shows the same sequence.

1\. Barenblatt flame problem: the abstract structure
----------------------------------------------------

In the preface/intro, Barenblatt summarizes the flame setting as a nonlinear parabolic PDE of the form

$$
\partial_t \theta=\partial_{xx}\theta+f(\theta),
$$

and says the wave-type solutions are  $\theta(x-\lambda t)$ , with the phase speed  $\lambda$  found by phase-plane analysis.

Barenblatt - 1996 - Scaling, se…

He then says this is the prototype where the speed is found as an eigenvalue of the boundary-value problem for the internal structure.

Barenblatt - 1996 - Scaling, se…

So the flame recipe is:

1.  start from reaction-diffusion PDE,
2.  seek travelling wave  $ \theta(x,t)=\Theta(\xi)$ ,  $\xi=x-\lambda t$ ,
3.  get an ODE,
4.  impose two end states,
5.  only special  $\lambda$  allow a connecting orbit,
6.  that  $\lambda$  is the selected eigenvalue.

That is the template we now translate.

* * *

2\. Granular counterpart: what plays the role of the flame field?
-----------------------------------------------------------------

For your chute problem, the analogue of flame temperature/conversion is **not** the velocity itself. It is better to use a **mobilization field**:

*   flame variable:  $\theta(x,t)$ , measuring reaction progress / temperature,
*   granular variable:  $g(x,z)$ , a nonlocal granular fluidity or mobility field.

The reason is simple: in dense grains, velocity is kinematics, but the field that carries “activity” and spreads cooperativity is  $g$ . That is the natural analogue of the flame’s reactive state variable.

So the first line-by-line map is

$$
\theta \quad \longleftrightarrow \quad g.
$$

The observed surface speed  $v(x)$  is then not the primary field but a derived amplitude, just as flame heat-release rate is derived from  $\Theta$ .

* * *

3\. Flame PDE  $\leftrightarrow$  granular PDE
----------------------------------------------

### Barenblatt flame:

$$
\partial_t\theta=\partial_{xx}\theta+f(\theta).
$$

### Granular undeveloped branch:

replace time evolution by **streamwise evolution** toward the developed state:

$$
\xi_x^2\,\partial_{xx}g+\xi_z^2\,\partial_{zz}g+\sigma(\varepsilon)\,g-\kappa g^2+\chi |\partial_z u|^m=0,
$$

coupled to

$$
u\,\partial_x u+w\,\partial_z u=\varepsilon-\partial_z\!\big(g\,\partial_z u\big).
$$

Here

$$
\varepsilon=\tan\theta-\mu_r
$$

is the excess above the critical friction threshold.

So the next map is

$$
\partial_t \theta \quad \longleftrightarrow \quad \text{streamwise development in }x,
$$
 
$$
f(\theta)\quad \longleftrightarrow \quad \sigma(\varepsilon)g-\kappa g^2+\chi |\partial_z u|^m.
$$

Physically:

*   flame reaction term  $f(\theta)$ : creates burning state,
*   granular source term: creates flowing/mobilized state.

* * *

4\. Flame travelling coordinate  $\leftrightarrow$  granular development coordinate
-----------------------------------------------------------------------------------

### Flame:

$$
\xi = x-\lambda t.
$$

### Granular chute:

there is no physical time-front moving through a quiescent medium; instead, the system relaxes **downstream** from inlet to developed state. So the natural analogue is

$$
\eta=\frac{x}{L_*},
$$

or, if you want exact analogy with a propagation parameter,

$$
\eta=x-c s,
$$

with  $s$  a fictitious evolution parameter for the spatial relaxation problem.

But for chute flow the cleaner choice is

$$
\eta=\frac{x}{L(\varepsilon,h/d)}.
$$

So the map is

$$
x-\lambda t \quad \longleftrightarrow \quad \frac{x}{L}.
$$

In words:

*   flame speed  $\lambda$  sets the front thickness/location in time,
*   granular development length  $L$  sets how quickly the inlet state relaxes downstream.

* * *

5\. Flame end states  $\leftrightarrow$  granular end states
------------------------------------------------------------

### Flame:

two equilibria:

$$
\Theta(-\infty)=\Theta_b,\qquad \Theta(+\infty)=\Theta_u,
$$

burned and unburned.

### Granular chute:

two asymptotic states:

$$
g(0,z)=g_{\text{in}}(z),\qquad g(x,z)\to g_\infty(z)\quad (x\to\infty),
$$

and similarly

$$
u(0,z)=u_{\text{in}}(z),\qquad u(x,z)\to u_\infty(z).
$$

So the map is

$$
\text{burned / unburned} \quad \longleftrightarrow \quad \text{undeveloped / fully developed}.
$$

This is the most important physical correspondence.

* * *

6\. Flame ODE  $\leftrightarrow$  granular amplitude ODE
--------------------------------------------------------

Barenblatt emphasizes that the travelling-wave substitution reduces the PDE to an ODE boundary-value problem, and the speed is determined by that reduction.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

For the flame:

$$
-\lambda \Theta'=\Theta''+f(\Theta),
$$

or

$$
\Theta''+\lambda \Theta'+f(\Theta)=0.
$$

For the granular case, after projecting onto the leading depth mode,

$$
g(x,z)\approx a(x)\psi_0(z/h),
$$

you get a streamwise amplitude equation of the same structural type:

$$
D a''-c a'+\alpha a-\beta a^2=0.
$$

So the map is

$$
\Theta(\xi) \quad \longleftrightarrow \quad a(\eta),
$$
 
$$
\Theta''+\lambda \Theta'+f(\Theta)=0 \quad \longleftrightarrow \quad D a''-c a'+\alpha a-\beta a^2=0.
$$

Term by term:

*    $\Theta''$  = front diffusion,
*    $D a''$  = nonlocal streamwise smoothing,
*    $\lambda \Theta'$  = wave translation,
*    $c a'$  = downstream relaxation / selected streamwise transport,
*    $f(\Theta)$  = reaction nonlinearity,
*    $\alpha a-\beta a^2$  = mobilization growth and saturation.

* * *

7\. Flame speed eigenvalue  $\leftrightarrow$  granular development eigenvalue
------------------------------------------------------------------------------

In Barenblatt’s travelling-wave-of-second-kind language, the speed is selected because only for special  $\lambda$  does a global solution exist.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

For the granular analogue, the selected quantity is not literally a physical front speed. It is one of these equivalent parameters:

$$
c, \qquad L=\frac{D}{c}, \qquad \nu \text{ in } L\sim \varepsilon^{-\nu}, \qquad \beta \text{ in } v_\infty\sim \varepsilon^\beta.
$$

So the map is

$$
\lambda \quad \longleftrightarrow \quad c \quad \text{or} \quad L^{-1}.
$$

And if you push the similarity reduction farther,

$$
\lambda \quad \longleftrightarrow \quad \nu \quad \text{or ultimately} \quad \beta.
$$

That is the point where the granular problem becomes a second-kind problem: the exponent is selected the same way flame speed is selected.

* * *

8\. Flame phase plane  $\leftrightarrow$  granular phase plane
--------------------------------------------------------------

Barenblatt says the classical flame speed was obtained by phase-plane portrait investigation.

Barenblatt - 1996 - Scaling, se…

### Flame phase plane

Set

$$
Y=\Theta',
$$

then

$$
\Theta'=Y,\qquad Y'=-\lambda Y-f(\Theta).
$$

The travelling flame is a heteroclinic orbit connecting the two equilibria.

### Granular phase plane

Set

$$
p=a',
$$

then

$$
a'=p,\qquad p'=\frac{c}{D}p-\frac{\alpha}{D}a+\frac{\beta}{D}a^2.
$$

The undeveloped-to-developed chute flow is the corresponding heteroclinic orbit connecting

$$
(a,p)=(0,0)
$$

to

$$
(a,p)=\left(\frac{\alpha}{\beta},0\right).
$$

So the map is

$$
(\Theta,\Theta') \quad \longleftrightarrow \quad (a,a').
$$

And the meaning of the orbit is the same:

*   flame: one front joining fresh and burnt states,
*   granular: one development profile joining inlet and developed states.

* * *

9\. Flame “global solution”  $\leftrightarrow$  granular “global heteroclinic orbit”
------------------------------------------------------------------------------------

Barenblatt’s key phrase is that the speed for waves of the second type is found from the condition for the existence of a **global solution describing the internal structure of the wave**.

Barenblatt - 1996 - Scaling, se…

For the flame, “global” means:

$$
-\infty<\xi<\infty,
$$

with correct limits at both ends.

For the granular chute, “global” means:

$$
0\le x<\infty \quad\text{or equivalently}\quad 0\le \eta<\infty,
$$

with

$$
a(0)=a_{\text{in}},\qquad a(\infty)=a_\infty.
$$

So the map is exact:

$$
\text{global flame profile} \quad \longleftrightarrow \quad \text{global downstream development profile}.
$$

Only for special parameter values does that connection exist.

* * *

10\. Barenblatt’s logarithmic transform  $\leftrightarrow$  granular second-kind scaling
----------------------------------------------------------------------------------------

Barenblatt also explains the formal equivalence between travelling waves and self-similar solutions by setting

$$
\zeta=\ln x,\qquad T=\ln t,\qquad c=-\ln A,
$$

so that

$$
u=f(\zeta-\lambda T+c)
$$

becomes

$$
u=F(A t^{-\lambda}x).
$$

That is his one-to-one correspondence between travelling-wave classification and self-similarity classification.

Barenblatt - 1996 - Scaling, se…

For the granular case, the direct analogue is:

travelling-wave parameter:

$$
c \quad \leftrightarrow \quad \text{selected exponent in }L\sim \varepsilon^{-\nu}.
$$

Then via the balance relation, e.g.

$$
2\beta+\nu=1,
$$

the selected development exponent  $\nu$  determines the selected velocity exponent  $\beta$ .

So the map is:

*   flame: solve for  $\lambda$ ,
*   granular: solve for  $\nu$ , then infer  $\beta$ .

That is the exact second-kind analogy.

* * *

11\. What is the “reaction zone” analogue in granular flow?
-----------------------------------------------------------

In the flame example, the important internal structure is a **thin reaction zone** separating two bulk states.

Barenblatt - 1996 - Scaling, se…

For the chute problem, the closest analogue is **not** a chemical layer but a **streamwise development layer** plus a near-base mobilization layer:

*   reaction zone in flame
    $$
    \longleftrightarrow
    $$
*   inlet/development zone in granular flow, where fluidity is being created and the velocity profile is adjusting.

So the internal structure that selects the eigenvalue is:

*   flame: thermal-diffusive front structure,
*   chute: nonlocal-fluidity + shear-profile adjustment structure.

* * *

12\. Why this mapping is useful for your problem
------------------------------------------------

This mapping tells you exactly what to do if you want a genuine Barenblatt formulation for the undeveloped granular branch:

### Flame book logic

$$
\text{PDE} \to \text{travelling-wave ODE} \to \text{phase plane} \to \text{selected speed}.
$$

### Granular analogue

$$
\text{streamwise nonlocal PDE} \to \text{depth-projected ODE} \to \text{phase plane} \to \text{selected }c\text{ or }L \to \text{selected exponent}.
$$

So the undeveloped branch should be read as the granular counterpart of the flame front:

*   the chute does not instantaneously “ignite” into its terminal state,
*   instead it relaxes over a development layer,
*   and the selected downstream scale may come from exactly the same type of global-orbit condition that selects flame speed.

* * *

13\. Compact dictionary
-----------------------

Here is the shortest possible dictionary.

$$
\theta(x,t)\ \text{(flame field)} \quad\leftrightarrow\quad g(x,z)\ \text{(granular fluidity)}
$$
 
$$
x-\lambda t \quad\leftrightarrow\quad x/L
$$
 
$$
\lambda \quad\leftrightarrow\quad c \ \text{or}\ L^{-1}
$$
 
$$
\Theta''+\lambda\Theta'+f(\Theta)=0 \quad\leftrightarrow\quad D a''-c a'+\alpha a-\beta a^2=0
$$
 
$$
\text{burned} \leftrightarrow \text{unburned} \quad\leftrightarrow\quad \text{developed} \leftrightarrow \text{undeveloped}
$$
 
$$
\text{selected wave speed} \quad\leftrightarrow\quad \text{selected development length / scaling exponent}
$$
 
$$
\text{heteroclinic front orbit} \quad\leftrightarrow\quad \text{heteroclinic development orbit}
$$

* * *

14\. The one caveat
-------------------

The mapping is structurally right, but there is one important asymmetry:

*   in flame propagation, the selected parameter is literally a physical speed;
*   in granular chute development, the selected parameter is more naturally a **length scale** or **scaling exponent**, not a speed.

So the granular analogue is slightly less direct physically, but mathematically it is the same class of problem.

That is why, for your project, the **undeveloped branch** is a much better place to look for Barenblatt second-kind structure than the fully developed  $v_\infty$  law by itself.

The next useful step is to take the reduced granular ODE

$$
D a''-c a'+\alpha a-\beta a^2=0
$$

and do the phase-plane portrait exactly the way Barenblatt describes for the flame.

## Prompt:
3/8/2026, 3:10:54 PM

why can take fast or slow variables to PDE to simplify the equations, explain in physical (for example the flame front problem)

## Response:
3/8/2026, 3:11:48 PM

> Thought for 19s

Because you are **not throwing away physics** when you introduce fast and slow variables; you are **relabeling the same physics in coordinates adapted to the dominant process**.

For multiscale problems, the original  $(x,t)$  variables often mix together two very different things:

*   a **rapid internal adjustment**,
*   and a **slow evolution of the large-scale pattern**.

When that happens, the PDE looks complicated because one coordinate system is trying to describe two different clocks at once.

Physically, the point of using fast/slow variables is:

1.  identify the structure that is nearly coherent,
2.  move with it or zoom into it,
3.  separate the variables associated with rapid local equilibration from those associated with slow global change.

Barenblatt’s basic message is exactly this: self-similar and traveling-wave variables turn a time-dependent PDE into something simpler because, in the right coordinates, the phenomenon becomes almost stationary. He says that in self-similar coordinates the phenomenon becomes time independent, which reveals a kind of stabilization, and this reduction often converts a PDE into an ODE boundary-value problem.

Barenblatt - 1996 - Scaling, se…

1\. Physical meaning of “fast” and “slow”
-----------------------------------------

Suppose a process has:

*   a **thin internal layer** where quantities vary sharply,
*   a **broad outer region** where quantities vary gently.

Then the same physical distance  $x$  is the wrong ruler for both regions.

A thin front may have width  $\delta$ , while the whole domain has size  $L$ , with

$$
\delta \ll L.
$$

Across the front, the solution changes a lot over  $\delta$ , so the natural inner variable is

$$
\xi = \frac{x-x_f(t)}{\delta}.
$$

Outside the front, the same solution changes only gradually over  $L$ , so the natural outer variable is

$$
X = \frac{x}{L}.
$$

This is why fast and slow variables help: each variable measures change on the scale where that change is actually occurring.

Mathematically, derivatives transform as

$$
\partial_x \sim \frac{1}{\delta}\partial_\xi
$$

in the thin region, which makes the dominant balance visible. A messy PDE then often simplifies because terms that were mixed together in  $(x,t)$  become ordered by size.

2\. Flame-front example
-----------------------

Barenblatt’s flame example is ideal here. In the foreword/introduction, he describes combustion as occurring in a **relatively narrow region** that separates cold unburned material from hot products, and this region moves with a definite velocity. He explicitly writes the propagating profile as

$$
T(x-ut),
$$

or more generally a wave of the form  $f(x-\lambda t)$ .

Barenblatt - 1996 - Scaling, se…

Physically, this means:

*   the **shape of the flame front adjusts quickly** inside the thin reaction zone,
*   the **front as a whole moves more slowly through space**.

If you stay in laboratory coordinates  $(x,t)$ , the profile looks time dependent. But if you move with the front,

$$
\xi = x-\lambda t,
$$

then the same physical structure is nearly steady.

So a PDE like

$$
\partial_t \theta = \partial_{xx}\theta + f(\theta)
$$

becomes

$$
-\lambda \Theta' = \Theta'' + f(\Theta),
$$

or

$$
\Theta'' + \lambda \Theta' + f(\Theta)=0.
$$

Nothing mystical happened. The physical assumption is simply:

> after initial transients, the flame no longer changes its shape much; it mainly translates.

That is why the moving coordinate simplifies the PDE. It removes the trivial part of the dynamics, namely translation of the whole structure.

Zeldovich’s foreword says this especially clearly: direct numerics may only give a huge table of temperatures and concentrations, but to “make manifest the flame propagation,” one has to recognize the regime of uniform propagation  $T(x-ut)$ .

Barenblatt - 1996 - Scaling, se…

So the fast/slow split in the flame problem is:

*   **fast**: relaxation inside the thin reaction-diffusion layer,
*   **slow**: drift of the whole front through the medium.

3\. Why this is not just a mathematical trick
---------------------------------------------

The justification is physical **stabilization**.

When a system forgets fine details of its initial condition, it often approaches a universal form. Barenblatt calls this **intermediate asymptotics**: a regime where the solution no longer depends on the detailed initial/boundary data, but the system is still far from final equilibrium.

Barenblatt - 1996 - Scaling, se…

That is exactly when fast/slow variables work best.

For a flame:

*   the exact initial ignition details are forgotten,
*   the front settles to a robust profile,
*   only a few slow collective parameters remain important, such as front position and speed.

So you are not guessing arbitrarily. You are exploiting the fact that the system has already done a lot of internal relaxation for you.

4\. Same idea in self-similar variables
---------------------------------------

For spreading or diffusing problems, the coherent structure is not a translating front but a profile whose width grows in time.

Then the natural slow variable is not  $x-\lambda t$ , but something like

$$
\xi = \frac{x}{\ell(t)}.
$$

Barenblatt’s heat-source example uses exactly this logic: the solution becomes simpler in variables like  $x/\sqrt{t}$ , because the profile broadens while keeping a fixed shape in rescaled coordinates. He stresses that in such self-similar coordinates the phenomenon becomes time independent.

Barenblatt - 1996 - Scaling, se…

Physically:

*   the **microscopic rearrangement** is fast,
*   the **overall scale**  $\ell(t)$  changes slowly.

So again the fast and slow pieces are being separated.

5\. When can you do this?
-------------------------

You can do it when the system shows a **dominant pattern** with a clear scale separation.

Typical signs are:

*   a thin front or boundary layer,
*   a broad outer field,
*   one rapidly relaxing internal structure,
*   one slowly evolving large-scale parameter,
*   loss of memory of fine initial details.

If those conditions hold, then introducing adapted variables is physically natural.

If they do not hold, the trick fails. For example, if no stable front shape forms, then  $x-\lambda t$  will not simplify the problem much.

6\. Why second-kind problems are harder
---------------------------------------

Sometimes the right scaled variable is obvious from dimensions. Sometimes it is not.

Barenblatt explains that in second-kind similarity the exponents are **not** fixed by dimensional analysis alone; they are found from solving the reduced problem, often like an eigenvalue problem.

Barenblatt - 1996 - Scaling, se…

Physically, this means:

*   the system does have a coherent fast/slow structure,
*   but the scaling of that structure is selected by the internal dynamics,
*   not by units alone.

The flame-front speed in his traveling-wave discussion is a good example: the moving coordinate helps, but the speed  $\lambda$  is not known until the internal profile satisfies the boundary conditions at both ends.

Barenblatt - 1996 - Scaling, se…

7\. A fluid-mechanics analogy
-----------------------------

From your background, this is close to using:

*   a boundary-layer coordinate near a wall,
*   an outer coordinate in the core,
*   or a moving frame for a coherent structure.

In each case, the PDE is not changed in substance. You are choosing coordinates that align with the dominant transport process.

That is also why Gioia’s incomplete-similarity analysis works in turbulence: a “small” roughness or cutoff may still remain physically relevant, so one must scale variables in a way that respects the active structure instead of blindly discarding the small length.

gioia2001.pdf

Goldenfeld and Shih - 2017 - Tu…

Bottom line
-----------

You can take fast and slow variables because many PDE solutions develop a **coherent intermediate structure**:

*   fast variables resolve the thin, rapidly adjusting inner dynamics,
*   slow variables describe the broad, slowly evolving outer motion.

In the flame-front problem, the front shape equilibrates quickly while the whole front propagates slowly, so  $x-\lambda t$  removes the translation and turns the PDE into an ODE for the internal structure. That simplification is physical, not cosmetic: it expresses that the system has entered an intermediate asymptotic regime where only a few collective degrees of freedom matter.

Barenblatt - 1996 - Scaling, se…

I can next show this explicitly for the flame PDE by doing the variable change step by step and interpreting every term physically.

## Prompt:
3/9/2026, 8:45:09 PM

explain the derivation self similarity of traveling wave in barenblatt book, step by step, and explain in physical intuitively

## Response:
3/9/2026, 8:45:10 PM

> **Searching for relevant information on traveling waves**
>
> The user is asking about a specific derivation in Barenblatt's book. I'll start by using the uploaded PDF to search for any sections related to traveling waves. I'll also check trusted web sources for an overview of the book to guide further search in the PDF.
>
> **Initiating web search**
>
> I need to search some information, but I don’t yet know the exact details or context, so I’ll start by getting a broad look at relevant sources. Then from there, I can dig deeper into specific details related to the topic once I have a clearer direction.
>
> **Searching for Barenblatt's work on travelling waves**
>
> [Self-similar solutions and travelling waves (Chapter 7) - Scaling, Self-similarity, and Intermediate Asymptotics](https://www.cambridge.org/core/books/scaling-selfsimilarity-and-intermediate-asymptotics/selfsimilar-solutions-and-travelling-waves/C2F7DC8D7E06B664AE8BFC3498062A25)
> [Scaling, Self-similarity, and Intermediate Asymptotics – Cambridge University Press Bookshop](https://www.cambridgebookshop.co.uk/products/scaling-self-similarity-and-intermediate-asymptotics)
>
> Thought for 33s

Barenblatt’s derivation has two layers:

1.  **travelling waves as a coordinate change**, and
2.  **self-similarity as the same idea written in logarithmic variables**.

That is why he puts “self-similar solutions and travelling waves” in one chapter, then treats Burgers shock as first kind and flame as second kind, followed by the nonlinear eigenvalue problem.

Barenblatt - 1996 - Scaling, se…

[Cambridge University Press & Assessment](https://www.cambridge.org/core/books/scaling-selfsimilarity-and-intermediate-asymptotics/selfsimilar-solutions-and-travelling-waves/C2F7DC8D7E06B664AE8BFC3498062A25?utm_source=chatgpt.com)

1\. Start from the physical picture
-----------------------------------

A travelling wave means the pattern keeps its **shape**, while its **position** changes. Barenblatt writes a general travelling-wave-type solution as

$$
v = V(x-X(t)) + V_0(t),
$$

and for a steady uniformly propagating wave as

$$
v = V(x-\lambda t + c),
$$

with  $\lambda$  the propagation speed and  $c$  a phase shift.

Barenblatt - 1996 - Scaling, se…

**Physical intuition:** imagine a flame front or shock front. In the lab frame, the graph moves. In the frame moving with the front, the graph is almost frozen. The whole point is to choose coordinates that follow the coherent structure instead of standing still while the structure passes by.

So define the moving coordinate

$$
\xi = x-\lambda t + c.
$$

Then  $v(x,t)$  becomes a one-variable profile:

$$
v(x,t)=V(\xi).
$$

That is already the first simplification: a PDE in  $(x,t)$  becomes an ODE in  $\xi$ .

* * *

2\. Why this simplifies the PDE
-------------------------------

Once  $v(x,t)=V(\xi)$ , the derivatives become

$$
\partial_t v = -\lambda V'(\xi), \qquad \partial_x v = V'(\xi), \qquad \partial_{xx}v = V''(\xi).
$$

So every  $x,t$ \-dependence is absorbed into one coordinate  $\xi$ .  
This works because the physics says the front has reached an **intermediate asymptotic regime**: it no longer remembers the detailed initial condition, and its main motion is translation of a nearly fixed profile. Barenblatt explicitly treats such invariant solutions as intermediate asymptotics of broader initial-value problems.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

**Intuition:** instead of tracking every point in space and time, you track only “where you are relative to the front.”

* * *

3\. Barenblatt’s key link: travelling waves are hidden self-similar solutions
-----------------------------------------------------------------------------

Barenblatt then shows that travelling waves can be rewritten as self-similar solutions by passing to **logarithmic variables**. He writes

$$
v=\ln u,\qquad t=\ln \tau,\qquad V=\ln U,\qquad x=\ln \xi,
$$

which converts the travelling-wave representation into a self-similar form. In particular, a uniformly propagating wave becomes

$$
u = B \tau^\mu\, U\!\left(\frac{\xi}{A\tau^\lambda}\right),
$$

that is, a power-law self-similar solution.

Barenblatt - 1996 - Scaling, se…

This is the crucial mathematical trick.

### What it means physically

A **translation** in log-space is a **scaling** in ordinary space.

Because

$$
\ln x - \lambda \ln t = \ln\!\left(x\,t^{-\lambda}\right),
$$

a profile that is a travelling wave in  $(\ln x,\ln t)$  becomes a self-similar profile in  $(x,t)$ .

So:

*   ordinary travelling wave: same shape, shifted in space;
*   self-similar solution: same shape, but after **rescaling** space and amplitude.

That is why Barenblatt says the classification of travelling waves corresponds to the classification of self-similar solutions.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

* * *

4\. First kind vs second kind for travelling waves
--------------------------------------------------

Barenblatt distinguishes two kinds of travelling waves.

### First kind

The propagation speed is fixed by **external conservation laws** alone.  
His example is the Burgers shock: the wave speed comes from the jump condition, while viscosity only fixes the front thickness.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

### Second kind

Conservation laws are **not enough**. The speed must be found by solving the **internal structure** of the front, and it appears as an eigenvalue. Barenblatt says this explicitly for flames and similar fronts.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

**Physical intuition:**  
For a shock, large-scale balance already tells you how fast the front moves; diffusion just smooths it.  
For a flame, chemistry and diffusion inside the thin reaction layer help determine how fast the front can sustain itself. So the internal layer is not passive; it selects the speed.

* * *

5\. The flame example: PDE to ODE
---------------------------------

Barenblatt introduces the flame/gene-front prototype as a nonlinear diffusion-reaction equation

$$
\partial_t v - K \partial_{xx} v = F(v),
$$

with

$$
F(0)=F(1)=0,\qquad F(v)>0 \text{ for } 0<v<1,
$$

and suitable smoothness/positivity assumptions near  $v=0$ .

Barenblatt - 1996 - Scaling, se…

Then he looks for a travelling-wave solution

$$
v = V(\xi),\qquad \xi=x-\lambda t + c,
$$

satisfying

$$
V(-\infty)=1,\qquad V(+\infty)=0.
$$

Barenblatt - 1996 - Scaling, se…

Substituting the ansatz into the PDE gives an ODE of the form

$$
K V'' + \lambda V' + F(V)=0.
$$

This is the standard travelling-wave reduction.

### Physical meaning of the terms

*    $K V''$ : diffusion smooths the front,
*    $\lambda V'$ : advection caused by moving with the front,
*    $F(V)$ : reaction tends to convert one state into the other.

The front exists only if these three effects balance.

* * *

6\. Why this becomes an eigenvalue problem
------------------------------------------

Now comes Barenblatt’s central point.

You do **not** know  $\lambda$  in advance. You solve the ODE with two far-field conditions:

$$
V(-\infty)=1,\qquad V(+\infty)=0.
$$

For an arbitrary  $\lambda$ , there is generally no global profile satisfying both ends. Only special  $\lambda$  values work. Barenblatt says that for travelling waves of the second kind, the speed is determined by the condition for **global existence of the internal structure**, that is, by existence of a travelling-wave solution satisfying the boundary conditions in the transition region.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

That is exactly why  $\lambda$  is an eigenvalue.

**Physical intuition:**  
You are trying to build a front that joins hot burnt gas on one side to cold fresh gas on the other. Most guessed speeds fail:

*   too slow, and reaction outruns diffusion/transport;
*   too fast, and the profile cannot sustain itself.

Only the right speed lets the whole front hang together from one end to the other.

* * *

7\. Why this is “self-similarity of the second kind”
----------------------------------------------------

Barenblatt’s dictionary is:

*   travelling-wave speed  $\lambda$   
    corresponds to
*   self-similar exponent in the scaled variable.

He states that the classification of travelling waves carries over into the language of self-similar solutions, and that the exponent in the self-similar variable corresponds to the propagation speed in travelling-wave solutions.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

So:

*   **first kind:** exponent/speed fixed from dimensional or conservation arguments;
*   **second kind:** exponent/speed fixed only by solving the reduced boundary-value problem.

That is the whole conceptual bridge.

* * *

8\. The “intermediate asymptotics” step
---------------------------------------

Barenblatt does not stop at exact invariant solutions. He also explains that in more realistic flame problems, the travelling wave becomes an **intermediate asymptotic** of a non-invariant problem. He introduces slow variables, gets a travelling-wave-type intermediate asymptotic in the transition region, and again ends up with a nonlinear eigenvalue problem

$$
\mu'' + A(\eta)\mu' + f_1(\mu,\eta)=0,
$$

with limits at  $\pm\infty$ , where the solution determines the effective propagation velocity.

Barenblatt - 1996 - Scaling, se…

**Physical intuition:** the front is not exactly rigid forever; external conditions may evolve slowly. But on the fast inner scale of the front, it still looks like a travelling wave with slowly varying parameters. That is the fast/slow decomposition you asked about earlier.

* * *

9\. The phase-plane picture
---------------------------

Barenblatt emphasizes phase-plane analysis for these wave problems.

Barenblatt - 1996 - Scaling, se…

For the flame ODE, write

$$
Y = V',
$$

so

$$
V' = Y,\qquad Y' = -\frac{\lambda}{K}Y - \frac{1}{K}F(V).
$$

Now the travelling wave is a curve in the  $(V,Y)$  plane that connects:

*    $V=1$ ,  $Y=0$  on one side,
*    $V=0$ ,  $Y=0$  on the other.

This connecting curve is the global orbit. Only for the right  $\lambda$  does that orbit exist.

**Physical intuition:** the front profile is not just a function; it is a path in state space joining two equilibrium states.

* * *

10\. The shortest step-by-step summary
--------------------------------------

Here is Barenblatt’s derivation in compact form:

1.  **Assume coherent front motion**: the pattern moves without changing much in shape.
    $$
    v(x,t)=V(x-\lambda t+c).
    $$
2.  **Introduce the moving coordinate**
    $$
    \xi=x-\lambda t+c.
    $$
3.  **Reduce the PDE to an ODE** by chain rule.  
    For the flame prototype:
    $$
    \partial_t v - K \partial_{xx} v = F(v) \quad\Rightarrow\quad K V'' + \lambda V' + F(V)=0.
    $$
4.  **Impose the two end states**
    $$
    V(-\infty)=1,\qquad V(+\infty)=0.
    $$
5.  **Recognize nonlinear eigenvalue selection**: only special  $\lambda$  allow a global solution satisfying both ends.
    Barenblatt - 1996 - Scaling, se…
    Barenblatt - 1996 - Scaling, se…
6.  **Map travelling wave to self-similarity** by logarithmic change of variables, where translation in log-space becomes scaling in ordinary space.
    Barenblatt - 1996 - Scaling, se…
7.  **Interpret physically**: second-kind scaling is what you get when the internal front structure selects the exponent/speed, rather than dimensional analysis or conservation laws alone.

* * *

11\. The most intuitive one-sentence version
--------------------------------------------

A travelling wave becomes self-similar in Barenblatt’s sense because, after taking logarithms, **uniform translation of a profile turns into uniform rescaling of a profile**; in second-kind problems, the translation speed—and therefore the scaling exponent—is selected by the existence of a global front structure, not by dimensions alone.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

I can next write the flame derivation explicitly line by line from

$$
\partial_t v - K \partial_{xx}v = F(v)
$$

to the phase-plane system, with each algebra step matched to its physical meaning.

## Prompt:
3/9/2026, 10:23:17 PM

 how to Recognize nonlinear eigenvalue selection in second kind: only special λ allow a global solution satisfying both ends. expain based on the flame front problem derivation step by step

## Response:
3/9/2026, 10:23:18 PM

> **Considering how to provide citation-based answer for flame front derivation**
>
> The user's request is about the flame front problem and its derivation. While I could rely on the uploaded PDF for direct citations, I also need to search the web for external corroboration, which will require proper citations. I think combining both sources will provide a clearer, well-supported answer. I'll start with the uploaded content.
>
> **Searching for relevant KPP and traveling wave info**
>
> I’ll search for general information on KPP (Kolmogorov–Petrovsky–Piskunov) equations and traveling waves. I could find a chapter heading from a reputable source like Cambridge or use something from a good encyclopedia on flame fronts. I'll keep the web search minimal and only include necessary citations.
>
> **Searching for KPP, traveling waves, and related sources**
>
> [Self-similar solutions and travelling waves (Chapter 7) - Scaling, Self-similarity, and Intermediate Asymptotics](https://www.cambridge.org/core/books/scaling-selfsimilarity-and-intermediate-asymptotics/selfsimilar-solutions-and-travelling-waves/C2F7DC8D7E06B664AE8BFC3498062A25)
> [Scaling, Self-Similarity, and Intermediate Asymptotics Textbook](https://studylib.net/doc/28304239/scaling-gregorian)
>
> **Crafting step-by-step explanation of flame PDE model**
>
> I'll break this explanation down step by step, using both physical intuition and detailed citations from the file, focusing on the flame PDE model and its boundary conditions. I'll explain the nonlinear eigenvalue selection using the phase plane, referencing Barenblatt's simplified model when needed. I'll avoid overwhelming the user with bullets and ensure web-cited content only mentions chapter titles.
>
> Thought for 53s

Yes. In Barenblatt’s flame-front example, “nonlinear eigenvalue selection” means:

> you guess a travelling-wave profile with an unknown speed  $\lambda$ , reduce the PDE to an ODE, impose the two end states, and then discover that **only special  $\lambda$ ** make a single bounded monotone profile connect both ends. That admissible  $\lambda$  is the eigenvalue.
> 
> Barenblatt - 1996 - Scaling, se…
> 
> Barenblatt - 1996 - Scaling, se…

Here is the derivation step by step.

1\. Start from the flame PDE
----------------------------

Barenblatt uses a simplified thermal flame model of the form

$$
\partial_t \theta = \partial_{xx}\theta + f(\theta),
$$

or equivalently, after rearrangement,

$$
\partial_t \theta - \partial_{xx}\theta = f(\theta),
$$

with  $f(\theta)$  positive between two equilibrium temperatures and zero at the two end states. In the stability section he states the model has  $f(\theta)=0$  near the cold state and at the hot state, and  $f(\theta)>0$  in between.

Barenblatt - 1996 - Scaling, se…

**Physical meaning:** diffusion smooths temperature, while reaction creates heat in the active interval. The flame front is the narrow region where these two compete.

* * *

2\. Assume a steady travelling front
------------------------------------

Barenblatt then looks for a travelling-wave solution

$$
\theta(x,t)=\vartheta(\xi),\qquad \xi=x-\lambda t+c,
$$

with  $c$  a phase shift and  $\lambda$  the propagation speed. He introduces travelling waves in exactly this form and says steady travelling waves describe shock and flame fronts.

Barenblatt - 1996 - Scaling, se…

**Physical meaning:** in the lab frame the flame moves, but in a frame moving with speed  $\lambda$  the front shape is stationary.

* * *

3\. Reduce the PDE to an ODE
----------------------------

By the chain rule,

$$
\partial_t \theta = -\lambda \vartheta'(\xi),\qquad \partial_x \theta = \vartheta'(\xi),\qquad \partial_{xx}\theta = \vartheta''(\xi).
$$

Substituting into the PDE gives

$$
\vartheta''+\lambda \vartheta'+f(\vartheta)=0.
$$

This is exactly the ODE Barenblatt writes for the travelling flame profile.

Barenblatt - 1996 - Scaling, se…

**Physical meaning of the terms:**

*    $\vartheta''$ : thermal diffusion spreads heat and smooths the front.
*    $\lambda \vartheta'$ : effect of moving with the front.
*    $f(\vartheta)$ : chemical heat release.

So the flame profile is an internal balance between diffusion, front translation, and reaction.

* * *

4\. Impose the two end states
-----------------------------

Barenblatt imposes

$$
\vartheta(-\infty)=\theta_2,\qquad \vartheta(+\infty)=\theta_1,
$$

with  $\theta_2$  the hot/burned state and  $\theta_1$  the cold/unburned state.

Barenblatt - 1996 - Scaling, se…

**Physical meaning:** the profile must connect the burned material behind the flame to the fresh material ahead of it.

This is already the key point: the ODE is not just an initial-value problem. It is a **two-ended boundary-value problem**.

* * *

5\. Why not every  $\lambda$  works
-----------------------------------

At this point  $\lambda$  is still unknown.

For any guessed  $\lambda$ , you can solve the ODE locally from one side. But most guessed values fail to produce a profile that also lands on the correct equilibrium at the other side. Barenblatt states that for waves of the second kind the speed is determined by the condition for **global existence of the internal structure**, meaning existence of a travelling-wave solution satisfying the boundary conditions in the transition region.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

**Physical intuition:** if  $\lambda$  is wrong, the front cannot sustain a consistent balance all the way across the layer.

*   Too small a speed: reaction/diffusion reshape the profile in a way that misses the cold state.
*   Too large a speed: the profile is dragged too fast to maintain the needed internal balance.

So the speed is not free.

* * *

6\. Convert to a phase-plane problem
------------------------------------

Set

$$
p=\frac{d\vartheta}{d\xi}.
$$

Then the ODE becomes a first-order system

$$
\vartheta' = p, \qquad p' = -\lambda p - f(\vartheta).
$$

The equilibrium points are

$$
(\vartheta,p)=(\theta_1,0),\qquad (\vartheta,p)=(\theta_2,0),
$$

because  $f(\theta_1)=f(\theta_2)=0$ . This is the phase-plane form Barenblatt analyzes in the flame/gene-propagation discussion, where he studies the separatrices and proves that only one parameter value reaches the target point.

Barenblatt - 1996 - Scaling, se…

**Physical meaning:** a flame profile is now a trajectory in the  $(\vartheta,p)$  plane.  
To be physical, that trajectory must start at one equilibrium and end at the other.

* * *

7\. Monotonicity narrows the possibilities
------------------------------------------

Barenblatt notes that the travelling-wave temperature profile is monotone decreasing and cannot have an interior minimum or maximum between the two equilibrium values. He proves this directly from the ODE sign structure.

Barenblatt - 1996 - Scaling, se…

That matters because it restricts the admissible phase-plane orbits to one monotone branch.

**Physical intuition:** a steady flame front should not overshoot, oscillate, cool, then heat again. It should pass once from hot to cold.

So the desired trajectory is not any orbit. It is a very special monotone connecting orbit.

* * *

8\. The heteroclinic-orbit viewpoint
------------------------------------

Now the problem is:

Find  $\lambda$  such that there exists one orbit in phase space with

$$
(\vartheta,p)\to(\theta_2,0)\quad \text{as }\xi\to-\infty,
$$

and

$$
(\vartheta,p)\to(\theta_1,0)\quad \text{as }\xi\to+\infty.
$$

That is a **heteroclinic orbit**.  
Barenblatt’s language is that the lower separatrix must reach the target point; only then are all the conditions satisfied.

Barenblatt - 1996 - Scaling, se…

**Why this is an eigenvalue problem:** for a generic  $\lambda$ , the unstable manifold leaving one equilibrium misses the stable manifold of the other. Only special  $\lambda$  make them connect.

That is exactly like linear eigenvalue problems, where only special parameter values satisfy both boundary conditions.

* * *

9\. Where the “nonlinear” part comes from
-----------------------------------------

This is an eigenvalue problem, but nonlinear because the ODE itself is nonlinear through  $f(\vartheta)$ . Barenblatt explicitly calls it a **nonlinear eigenvalue problem** and says the flame speed is uniquely determined by solving it.

Barenblatt - 1996 - Scaling, se…

So the unknown “eigenvalue” is  $\lambda$ , but the equation is not linear in  $\vartheta$ .  
That is why you cannot use superposition or linear spectral theory directly.

* * *

10\. The selection statement in Barenblatt
------------------------------------------

Barenblatt’s conclusion is very explicit: one can find a value  $\lambda=\lambda_0$ , and only one, such that the separatrix reaches the required endpoint and satisfies all problem conditions. He then says this proves existence and uniqueness of the nonlinear eigenvalue problem, and that the resulting  $\lambda_0$  determines the flame propagation speed in dimensional variables.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

So the logic is:

1.  reduce PDE to travelling-wave ODE,
2.  impose two asymptotic end states,
3.  study phase-plane separatrices,
4.  find that only one  $\lambda_0$  gives a global connection,
5.  identify  $\lambda_0$  as the flame speed.

That is nonlinear eigenvalue selection.

* * *

11\. Why this is “second kind”
------------------------------

Barenblatt distinguishes first- and second-kind travelling waves this way:

*   **first kind:** speed comes from outer conservation laws alone;
*   **second kind:** speed cannot be obtained from those laws and is found as an eigenvalue while solving the internal dissipative structure.
    Barenblatt - 1996 - Scaling, se…

A flame is second kind because the speed is selected by the internal reaction-diffusion layer, not by a shock jump condition. He then states that this corresponds exactly to self-similarity of the second kind, where the exponent is selected by solving the reduced problem rather than by dimensional analysis alone.

Barenblatt - 1996 - Scaling, se…

* * *

12\. The fastest physical summary
---------------------------------

The easiest way to recognize nonlinear eigenvalue selection is:

*   after the travelling-wave substitution, you get an ODE with an **unknown parameter**  $\lambda$ ,
*   you must satisfy conditions at **both**  $-\infty$  and  $+\infty$ ,
*   for almost every  $\lambda$ , the solution misses one end,
*   for a special  $\lambda=\lambda_0$ , one monotone global front exists,
*   that special  $\lambda_0$  is the selected wave speed.

So in the flame problem,  $\lambda$  is not an arbitrary fitting parameter. It is picked by the requirement that the internal flame structure exist globally and connect hot and cold states.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

If you want, I can next draw the phase-plane geometry explicitly and show how “miss left / miss right / hit exactly” corresponds to  $\lambda<\lambda_0$ ,  $\lambda>\lambda_0$ , and  $\lambda=\lambda_0$ .

## Prompt:
3/9/2026, 10:43:49 PM

how to find the internal flame structure exist globally and connect hot and cold states.

## Response:
3/9/2026, 10:43:51 PM

> **Searching and evaluating sources for flame problem derivation**
>
> I need to search the web for a public source on the flame front second kind, perhaps a Cambridge listing or a book preview. I'll check the uploaded PDF too, using it for detailed sections. The web should help with general concepts, while the file search gives specifics from the PDF.
>
> **Searching for KPP flame wave sources**
>
> I need to perform a web search as instructed by the developer. I’m thinking of looking for a Cambridge resource or something that summarizes KPP flame waves. The goal is to find a source that provides a clear overview of the concept, ideally something authoritative and relevant.
>
> **Searching for Cambridge resources on KPP flame waves**
>
> [Self-similar solutions and travelling waves (Chapter 7) - Scaling, Self-similarity, and Intermediate Asymptotics](https://www.cambridge.org/core/books/scaling-selfsimilarity-and-intermediate-asymptotics/selfsimilar-solutions-and-travelling-waves/C2F7DC8D7E06B664AE8BFC3498062A25)
> [Scaling, Self-similarity, and Intermediate Asymptotics – Cambridge University Press Bookshop](https://www.cambridgebookshop.co.uk/products/scaling-self-similarity-and-intermediate-asymptotics)
>
> Thought for 33s

You find it by turning the flame PDE into a **two-point boundary-value problem in phase space**, then asking whether the orbit from the hot equilibrium actually lands on the cold equilibrium. Only special  $\lambda$  make that happen. That is the “global existence of the internal structure” criterion Barenblatt uses for travelling waves of the second kind. He states that for second-kind waves, conservation laws are insufficient and the speed is determined by the condition for existence of a travelling-wave solution in the transition region that satisfies the boundary conditions there.

Barenblatt - 1996 - Scaling, se…

Here is the flame-front logic step by step.

1\. Start from the reaction-diffusion flame model
-------------------------------------------------

Barenblatt uses a scalar flame/gene-front type equation of the form

$$
\theta_t=\theta_{xx}+f(\theta),
$$

and then looks for a travelling wave connecting two equilibrium states, hot and cold. In the travelling-wave reduction section he writes the reduced nonlinear eigenvalue problem as

$$
\mu''+A(\eta)\mu'+f_1(\mu,\eta)=0,\qquad \mu(-\infty)=1,\ \mu(\infty)=0,
$$

for the intermediate-asymptotic flame problem, and in the steady-wave setting the same structure appears with constant  $\lambda$ .

Barenblatt - 1996 - Scaling, se…

For the steady travelling flame, you assume

$$
\theta(x,t)=\Theta(\xi),\qquad \xi=x-\lambda t.
$$

Then

$$
\theta_t=-\lambda \Theta',\qquad \theta_{xx}=\Theta'',
$$

so the PDE becomes

$$
\Theta''+\lambda \Theta'+f(\Theta)=0.
$$

That is the ODE for the internal flame profile. Barenblatt’s general travelling-wave form and the reduction to an ODE are described in Chapter 7.

Barenblatt - 1996 - Scaling, se…

[Cambridge University Press & Assessment](https://www.cambridge.org/core/books/scaling-selfsimilarity-and-intermediate-asymptotics/selfsimilar-solutions-and-travelling-waves/C2F7DC8D7E06B664AE8BFC3498062A25?utm_source=chatgpt.com)

2\. Impose the two end states
-----------------------------

The flame front must connect:

*   burned/hot gas behind the front,
*   unburned/cold gas ahead of the front.

So the boundary conditions are

$$
\Theta(-\infty)=\Theta_h,\qquad \Theta(+\infty)=\Theta_c,
$$

with  $f(\Theta_h)=f(\Theta_c)=0$ .

This is crucial: it is **not** an initial-value problem with data at one point. It is a **global connection problem** between two equilibria.

Physically, “global” means one single profile must remain bounded for all  $\xi\in(-\infty,\infty)$  and approach the correct state at both ends. Barenblatt phrases this as existence of a travelling-wave-type solution in the transition region satisfying the boundary conditions for that region.

Barenblatt - 1996 - Scaling, se…

3\. Rewrite as a first-order phase-plane system
-----------------------------------------------

Set

$$
p=\Theta'.
$$

Then

$$
\Theta'=p, \qquad p'=-\lambda p-f(\Theta).
$$

Now the flame profile is a trajectory in the  $(\Theta,p)$  phase plane.

The equilibria are

$$
(\Theta_h,0),\qquad (\Theta_c,0).
$$

So the question becomes:

> for a given  $\lambda$ , is there a trajectory that starts at  $(\Theta_h,0)$  as  $\xi\to-\infty$  and ends at  $(\Theta_c,0)$  as  $\xi\to+\infty$ ?

That trajectory is the internal flame structure.

4\. What usually happens for a guessed  $\lambda$ 
--------------------------------------------------

Pick some trial  $\lambda$ .

Near the hot equilibrium, there is typically a one-dimensional unstable direction that lets the orbit leave  $(\Theta_h,0)$ . If you integrate forward in  $\xi$ , that orbit usually does one of three things:

*   it overshoots and misses the cold state,
*   it turns the wrong way,
*   or it reaches the wrong slope/value as  $\xi\to+\infty$ .

So for a generic  $\lambda$ , the orbit is only **local**: it leaves one equilibrium correctly, but it does **not** connect globally to the other one.

This is exactly the meaning of “most  $\lambda$  fail.”

5\. Why only special  $\lambda$  can work
-----------------------------------------

Changing  $\lambda$  changes the vector field:

$$
p'=-\lambda p-f(\Theta).
$$

So  $\lambda$  changes how strongly the phase trajectory is “damped” as it travels across phase space.

Physically:

*   if  $\lambda$  is too small, the front is not transported fast enough relative to diffusion/reaction;
*   if  $\lambda$  is too large, the profile is dragged too hard and cannot relax properly to the cold state.

Therefore the orbit landing point shifts continuously with  $\lambda$ . If one trial lands “above” the target and another lands “below,” then by continuity there must be an intermediate  $\lambda_0$  for which it lands exactly on the cold equilibrium.

That is the shooting argument behind the eigenvalue selection.

6\. What Barenblatt actually proves
-----------------------------------

In the phase-plane proof, Barenblatt introduces the family of separatrices parameterized by  $\lambda$ , studies how they move with  $\lambda$ , and then shows there exists one and only one value  $\lambda_0$  such that the lower separatrix reaches the target equilibrium. He writes that one can find a value  $\lambda=\lambda_0$ , and moreover only one, such that the lower separatrix reaches the point  $p=0,\ \theta=\theta_1$ , satisfying all conditions of the problem; thus the existence and uniqueness of the nonlinear eigenvalue problem is proved.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

That sentence is the mathematical core of the method.

7\. Why this is called an eigenvalue problem
--------------------------------------------

Compare with a linear string problem:

$$
\psi''+\Lambda \psi=0,\qquad \psi(0)=\psi(1)=0.
$$

For arbitrary  $\Lambda$ , there is no nontrivial solution. Only exceptional  $\Lambda$  work.

Barenblatt makes this analogy explicitly in the chapter on eigenvalues: in second-kind similarity or travelling-wave problems, one again gets special eigenvalue problems for nonlinear operators, and the eigenvalues are determined by the condition that an invariant global solution exists satisfying the boundary conditions.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

So here:

*   unknown parameter:  $\lambda$ ,
*   boundary conditions: hot state at  $-\infty$ , cold state at  $+\infty$ ,
*   exceptional value:  $\lambda_0$ ,
*   nontrivial global solution: flame profile  $\Theta(\xi)$ .

That is why  $\lambda_0$  is the nonlinear eigenvalue.

8\. Physical meaning of “internal flame structure exists globally”
------------------------------------------------------------------

It means:

1.  there is a thin reaction-diffusion layer,
2.  its shape is stationary in the moving frame,
3.  it is smooth and bounded across the whole layer,
4.  it connects the two physical states without blowing up or oscillating incorrectly.

Barenblatt’s asymptotic flame discussion says the gas region splits into cold unburned gas, hot products, and a narrow transition region where reaction, diffusion, and heat transfer all occur; to determine the flame speed analytically, one must turn to the inner asymptotic expansion and consider the transition zone itself.

Barenblatt - 1996 - Scaling, se…

Barenblatt - 1996 - Scaling, se…

So “global existence” is not abstract. It means the inner transition zone can be constructed all the way from one outer state to the other.

9\. The shortest practical recipe
---------------------------------

To find whether the internal flame structure exists globally:

1.  Write the travelling-wave ODE
    $$
    \Theta''+\lambda\Theta'+f(\Theta)=0.
    $$
2.  Convert to first order:
    $$
    \Theta'=p,\qquad p'=-\lambda p-f(\Theta).
    $$
3.  Identify the equilibria  $(\Theta_h,0)$  and  $(\Theta_c,0)$ .
4.  Start on the separatrix leaving the hot state.
5.  Integrate forward for a trial  $\lambda$ .
6.  Check whether the orbit lands on the cold state:
    *   if it misses on one side, adjust  $\lambda$  one way;
    *   if it misses on the other side, adjust the other way.
7.  The selected  $\lambda_0$  is the one for which the orbit hits exactly:
    $$
    (\Theta,p)\to(\Theta_c,0)\quad \text{as }\xi\to+\infty.
    $$

That is the flame speed.

10\. Why this is second kind
----------------------------

Barenblatt’s classification says:

*   first kind: speed is fixed by conservation laws at the front;
*   second kind: speed is fixed by the condition for global existence of the internal structure.
    Barenblatt - 1996 - Scaling, se…
    Barenblatt - 1996 - Scaling, se…

A flame belongs to the second kind because the front speed is selected by solving the inner reaction-diffusion profile, not by jump conditions alone. The Cambridge chapter summary also states that travelling waves are used to study flame fronts and that the moving-frame distribution becomes stationary. [Cambridge University Press & Assessment+1](https://www.cambridge.org/core/books/scaling-selfsimilarity-and-intermediate-asymptotics/selfsimilar-solutions-and-travelling-waves/C2F7DC8D7E06B664AE8BFC3498062A25?utm_source=chatgpt.com)

The most intuitive summary is:

> The internal flame structure exists globally when the phase-plane trajectory leaving the hot equilibrium reaches the cold equilibrium without failing in between. Only one special  $\lambda$  usually makes that happen, so that  $\lambda$  is selected as a nonlinear eigenvalue.

I can next sketch the actual phase portrait and show what “undershoot,” “overshoot,” and “hit exactly” look like geometrically.

## Prompt:
3/9/2026, 11:21:59 PM

hot state at -infty,cold state at +infty. why?

## Response:
3/9/2026, 11:22:04 PM

This direction comes from the **physics of flame propagation** and the **choice of coordinate frame**. The short answer is:

> We choose the coordinate so that the flame **moves to the right**, therefore the **burned (hot) region is behind the front** at  $\xi\to -\infty$  and the **unburned (cold) region is ahead of the front** at  $\xi\to +\infty$ .

Let me explain carefully.

* * *

1\. Physical picture of a propagating flame
===========================================

Imagine a flame moving through a combustible gas from left to right.

At a given time:

```
burned gas      flame front        fresh gas
(hot)              |               (cold)

   hot -----------front----------- cold
        x < x_f(t)           x > x_f(t)
```

So in the **laboratory frame**:

*   behind the front → burned hot gas
*   ahead of the front → cold unburned gas

Mathematically

$$
\theta(x,t) \approx \begin{cases} \theta_h, & x<x_f(t) \\ \theta_c, & x>x_f(t) \end{cases}
$$

where

*    $\theta_h$  = hot equilibrium
*    $\theta_c$  = cold equilibrium.

* * *

2\. Introduce the moving coordinate
===================================

Now we follow Barenblatt and define

$$
\xi = x-\lambda t
$$

where  $\lambda$  is the flame speed.

This coordinate moves **with the flame front**.

When the flame is at  $x_f(t)=\lambda t$ ,

$$
\xi = x-x_f(t)
$$

So

*    $\xi=0$  = flame location
*    $\xi<0$  = region **behind** the flame
*    $\xi>0$  = region **ahead** of the flame

* * *

3\. What happens to the states in this coordinate
=================================================

Look again at the physical regions.

### Behind the flame

```
burned region
```

This is

$$
x < x_f(t)
$$

which means

$$
\xi = x-x_f(t) < 0
$$

and far behind

$$
\xi \to -\infty
$$

So

$$
\Theta(-\infty) = \theta_h
$$

* * *

### Ahead of the flame

```
fresh cold gas
```

This is

$$
x > x_f(t)
$$

so

$$
\xi > 0
$$

and far ahead

$$
\xi \to +\infty
$$

So

$$
\Theta(+\infty)=\theta_c
$$

* * *

4\. The flame profile in the moving frame
=========================================

In the moving coordinate the temperature profile becomes stationary:

```
ξ→-∞        ξ=0           ξ→+∞
 hot      reaction zone     cold
  |------------|-------------|
```

Mathematically

$$
\Theta(-\infty)=\theta_h
$$
 
$$
\Theta(+\infty)=\theta_c
$$

The front connects these two states smoothly.

* * *

5\. Why this direction is chosen
================================

The direction is **not fundamental**; it is just a convention.

We could also define

$$
\xi = \lambda t - x
$$

Then the boundary conditions would flip:

$$
\Theta(-\infty)=\theta_c
$$
 
$$
\Theta(+\infty)=\theta_h
$$

Both are mathematically equivalent.

Barenblatt chooses

$$
\xi = x-\lambda t
$$

because:

*   the front moves to increasing  $x$ 
*   the profile decreases from hot → cold.

* * *

6\. Why the flame profile must be monotone
==========================================

Barenblatt proves the solution cannot have internal maxima/minima between the two equilibrium temperatures.

Physically:

*   heat diffuses forward,
*   reaction raises temperature,
*   there is no mechanism to cool and reheat again.

Therefore

$$
\Theta'(\xi) < 0
$$

across the flame.

So the profile looks like

```
temperature
     |
hot  |\
     | \
     |  \
     |   \
cold |----\-----------
        ξ
```

* * *

7\. Why the limits are ±∞
=========================

The reaction zone is **thin compared with the domain**.

Outside the thin front:

*   reaction stops
*   temperature becomes constant.

So mathematically the domain is extended to

$$
-\infty < \xi < \infty
$$

and the front occupies only a small region around  $\xi=0$ .

This is a standard **internal-layer approximation**.

* * *

8\. Summary
===========

The conditions

$$
\Theta(-\infty)=\text{hot}, \quad \Theta(+\infty)=\text{cold}
$$

come directly from the physical geometry of flame propagation.

Because

*   the flame moves to the right,
*   we measure position relative to the flame,
*   the burned region is behind,
*   the fresh region is ahead.

Thus

```
ξ → −∞ : burned hot gas
ξ → +∞ : cold unburned gas
```

and the travelling-wave solution must connect those two states.

* * *

If you want, I can also show a **phase-plane picture** of this (the two equilibria and the heteroclinic orbit), which is the step where the **nonlinear eigenvalue λ** is selected in Barenblatt’s derivation.



---
Powered by [ChatGPT Exporter](https://www.chatgptexporter.com)
# Critical State of Granular Flows

## Overview
This repository collects working notes on one research question: how to reinterpret the recent unified flow rule for granular chute flows through the language of critical-state mechanics, and whether its anomalous scaling can be justified by Barenblatt-style self-similarity of the second kind rather than by data fitting alone.

The current materials are archived as synchronized ChatGPT exports in Markdown, JSON, and PDF. They document a line of thought, not a finished theory.

## Problem Definition
The central hypothesis is that the dense-flow threshold is controlled by

$$
\varepsilon = \tan\theta - \mu_r,
$$

where `\mu_r` is treated as the critical friction and `\varepsilon` is the distance to criticality.

From this viewpoint:

- `\varepsilon < 0`: the layer arrests.
- `\varepsilon = 0`: marginal or critical state.
- `\varepsilon > 0`: sustained dense flow.

The key target is the fully developed velocity law, often written in nondimensional form as

$$
v_\infty \sim \mu_r^{3/2}(\varepsilon h)^{4/3},
$$

and the related development length scaling. The main question is whether the exponent `4/3` is a genuine anomalous exponent produced by incomplete similarity, with grain size or nonlocal structure remaining asymptotically relevant.

## Current Vision
The current working vision is:

- Interpret `\mu_r` as a critical-state parameter rather than only an empirical fit.
- Treat the divergence of stopping thickness near threshold as the static-side signature of criticality.
- Read the flowing branch as a power-law emergence from `\varepsilon = 0^+`.
- Use Gioia’s logic as motivation: a law that looks dimensionally abnormal in raw form may become consistent once the correct scaling variables are restored.
- Move beyond phenomenology by introducing a nonlocal field, fluidity, or correlation length into the chute-flow description.

In short, the goal is to replace “fit the exponent” with “derive the exponent from a singular boundary-value problem.”

## Current Difficulties
The present obstacle is not algebra; it is model definition.

- There is no accepted continuum PDE here whose reduction clearly produces the `4/3` exponent.
- A local `\mu(I)`-type closure is likely too regular to generate second-kind selection.
- The essential small parameter is still ambiguous: candidates include `d/h`, basal roughness, or a diverging nonlocal length.
- The fully developed state is terminal and uniform, so the more natural second-kind formulation may have to come from the downstream development problem instead.
- Barenblatt’s strict framework requires a nonlinear eigenvalue problem with a global bounded orbit; that structure is currently only a program, not a completed derivation.

## Repository Contents
- `ChatGPT-Critical State of Granular Flows.md`: readable transcript of the discussion.
- `ChatGPT-Critical State of Granular Flows.json`: structured export with metadata.
- `ChatGPT-Critical State of Granular Flows.pdf`: frozen reference copy.

## Near-Term Direction
The next useful step is to propose a minimal nonlocal critical-state model for undeveloped-to-developed chute flow, reduce it to a similarity or travelling-wave problem, and test whether only special exponent values permit a global solution satisfying both entrance and far-field conditions.

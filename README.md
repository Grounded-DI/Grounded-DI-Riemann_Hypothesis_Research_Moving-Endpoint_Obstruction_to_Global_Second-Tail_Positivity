# RH-001H — Moving-Endpoint Obstruction

**MathWise / Grounded DI LLC**\
**Mark S. Weinstein**\
**Research checkpoint — October 4, 2026**

## Status

**ADVANCE — obstruction theorem.**

This checkpoint records an analytic existence argument showing that the actual-theta second tail is **negative at some endpoints at arbitrarily large real heights**.

It does **not** prove or disprove the Riemann Hypothesis.

It also does **not** invalidate the immediately preceding unbounded-height positive cone. The two results occupy different endpoint regions.

## Main result

Retain the RH-001H actual-theta definitions, including

\[
V_{2,t}(R)=\int_R^\infty (s-R)g_t(s)\,ds.
\]

The successor argument proves:

> For every \(H>0\), there exists a real
>
> \[
> t>\max\{H,448\pi\}
> \]
>
> such that, at
>
> \[
> R=\frac12\log\frac{t}{448\pi}>0,
> \]
>
> one has
>
> \[
> V_{2,t}(R)<0.
> \]

More precisely, with

\[
C_*=\frac{\pi^3}{2(2\pi)^{47/16}}>0,
\]

the constructed existence argument yields

\[
V_{2,t}(R)
<
-\frac{C_*}{100}\,
t^{63/16}e^{-\pi t/2}.
\]

This is an **existence theorem**. The package does not provide a directly evaluated negative pair \((t,R)\), a first negative height, or an effective first recurrence threshold.

## What changed

The preceding RH-001H V2 checkpoint proved the positive cone

\[
|t|\ge34,
\qquad
2\pi e^{2R}\ge\frac54|t|
\quad\Longrightarrow\quad
V_{2,t}(R)>0.
\]

That cone survives the present reconstruction.

The new negative endpoints satisfy

\[
2\pi e^{2R}=\frac{t}{224},
\]

which lies strictly below the positive cone. Their radial separation from the cone cutoff is

\[
\frac12\log 280.
\]

So there is no contradiction:

| Region | Current result |
|---|---|
| \(2\pi e^{2R}\ge5|t|/4,\ |t|\ge34\) | Positive cone survives reconstruction |
| \(2\pi e^{2R}=t/224\), at suitable arbitrarily large positive heights | \(V_{2,t}(R)<0\) exists |

The new theorem therefore blocks the stronger proposed route

\[
V_{2,t}(R)\ge0
\qquad
\text{for every real }t\text{ and every }R\ge0.
\]

Further positivity certification cannot establish a global statement that the successor argument proves is false.

## Why the obstruction appears

For fixed \(X>1\), define the moving endpoint

\[
R_X(t)=\frac12\log\frac{t}{2\pi X}
\]

and the finite divisor polynomial

\[
P_\sigma(t;X)
=
\sum_{1\le n<X}
n^{-\sigma}C_n(t)\log(X/n).
\]

The package derives the phase-uniform scaling law

\[
\frac{e^{\pi t/2}V_{2,t}(R_X(t))}
{C_*t^{63/16}}
=
P_{15/16}(t;X)+o(1)
\qquad(t\to+\infty),
\]

with an error bound independent of the changing divisor phases.

At \(X=224\), two exact-arithmetic implementations verify a strict negative finite witness

\[
D<-\frac3{100}
\]

together with the sensitivity bound

\[
B<156.
\]

The tight enclosure recorded for the finite witness is

\[
D\in
[-0.032763882323341271960959,\,
-0.032763882323341271960958].
\]

A continuous-time Fourier recurrence argument then shows that the required finite prime-phase neighborhood occurs at arbitrarily large real heights. The uniform asymptotic error transfers that strict finite sign to the actual second tail.

The result is analytic plus exact finite arithmetic. It is not based on a floating-point negative sample of \(V_2\).

## Relationship to RH

The source record's second-tail reformulation is

\[
\widehat H_x(t)
=
2xV_{2,t}(0)
+
4x^2\int_0^\infty
\sinh(2xr)V_{2,t}(r)\,dr.
\]

A negative value of \(V_{2,t}(R)\) at some positive endpoint does **not** determine the sign of this weighted aggregate.

Accordingly, this checkpoint:

- rules out blanket all-height/all-endpoint \(V_2\) positivity as a sufficient strategy;
- does **not** prove a negative aggregate transform;
- does **not** locate an off-critical-line zero;
- does **not** prove or disprove RH; and
- leaves the weaker aggregate-transform problem unresolved.

The remaining route must handle the signed compact contribution and the separate \(V_2(0)\) boundary term rather than assuming pointwise second-tail positivity everywhere.

## Related records

The [MathWise repository](https://github.com/Grounded-DI/MathWise) maintains the neighboring-zero certificate and replay record, including related RH certificate work. This repository remains the public record for the RH-001H moving-endpoint obstruction checkpoint. The records are related but distinct.

## Evidence package

Frozen review artifact (the PDF itself is labeled private review):

[RH_001H_Moving_Endpoint_Obstruction_2026-10-04.pdf](RH_001H_Moving_Endpoint_Obstruction_2026-10-04.pdf)

Frozen successor archive:

[RH_001H_Moving_Endpoint_Obstruction_2026-10-04.zip](RH_001H_Moving_Endpoint_Obstruction_2026-10-04.zip)

External SHA-256 sidecar:

[RH_001H_Moving_Endpoint_Obstruction_2026-10-04.zip.sha256.txt](RH_001H_Moving_Endpoint_Obstruction_2026-10-04.zip.sha256.txt)

Machine-readable final integrity record:

[RH_001H_Moving_Endpoint_Obstruction_FINAL_INTEGRITY.json](RH_001H_Moving_Endpoint_Obstruction_FINAL_INTEGRITY.json)

The successor contains the 15-page proof/review, LaTeX source, exact-sign implementations, replay commands and outputs, selected mutation/adversarial checks, dependency and provenance records, source snapshots, and a 75-file payload manifest.

It also contains selected byte-preserved material from the incoming positive-cone checkpoint plus its identity records. The full 72,771,333-byte predecessor ZIP is **not duplicated** inside this compact successor.

## Integrity

Successor ZIP SHA-256:

```text
0a395c36b61a0a8f7c791f4d3f1f0c78b999cb543a0cf8d2dfb3705dbba1cb0b
```

Successor ZIP size:

```text
923,899 bytes
```

Companion PDF SHA-256:

```text
e2825bbcb14e89aa51c5ee2d86d215838fa4683901e0244d664b75ca6f1fb69b
```

The final integrity record reports:

- ZIP CRC: **PASS**
- 75 payload files
- all payload hashes matching
- finite replay: **PASS**
- PDF inside ZIP byte-identical to the separately supplied PDF

The incoming positive-cone archive remains bound by:

```text
aa03fb1c204d622857f89804a05d5e5f4580d11bc291410dcff7dde332dc273c
```

**Byte integrity is not mathematical correctness, originality, authorship, peer review, or formal verification.**

## Replay

From the extracted successor root, ordinary Python 3 is sufficient for the finite checks.

Do **not** run Python with `-O`; assertions are part of verification.

```sh
python code/replay.py /path/to/a/new/replay-directory
```

The replay regenerates the exact finite certificate, performs the separate sign reconstruction, checks the reviewed cone constants, and checks finite phase algebra.

It does not machine-prove the universal analytic theorem and does not perform the unavailable Arb replay.

## Review limits

Preserved limitations include:

- no independent human mathematical review;
- no formal proof-assistant/kernel verification;
- no new Arb \(V_2\) evaluation;
- no full retrospective replay of the earlier \([33,34]\) numerical gate;
- no explicit first negative height or effective recurrence bound;
- no historical-priority claim; and
- no RH proof or disproof.

The two exact finite-check implementations use different computational paths but were written by the same assistant and share Python integer/rational arithmetic. They are not represented as independent human or independent-agent reviews.

## Predecessor checkpoint

The immediately preceding result remains a valid separate checkpoint in this research record:

**RH-001H V2 — Unbounded-Height Cone**

Its analytic cone was reconstructed in the successor review with no defect found. The new obstruction is inside the region that predecessor explicitly left unresolved.

For preservation purposes, the full predecessor archive may be retained separately as a release asset or archival artifact under its recorded SHA-256. It is not necessary to duplicate that 72.8 MB archive in this repository commit in order to publish the present successor checkpoint.

---

**Research classification:** bounded analytic obstruction theorem with exact finite witness  
**Date:** 2026-10-04  
**RH status:** unresolved

-Mark S. Weinstein, Grounded DI LLC

## Rights and Contact

Copyright © 2026 Grounded DI LLC for its original materials. Third-party sources retain their respective rights. No open-source license or additional reuse permission is granted by this README.

Commercial licensing, technical evaluation, and integration inquiries: [mark@groundeddi.com](mailto:mark@groundeddi.com).

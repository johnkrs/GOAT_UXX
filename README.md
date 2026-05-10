# GOAT Optimal Control for U_XX (2P1e)

Synthesising the single-step parity check gate U_XX (Üstün et al. 2024, Eq. 30) via GOAT (`qutip-qoc`).

**System:** 2 ³¹P nuclei + 1 electron ancilla (dim=8), hyperfine couplings A₁=95 MHz, A₂=9 MHz, B₀=1.33 T, T_gate=4 µs.

**Controls:** ESR (ω_e≈37 GHz) and NMR (ω_n≈23 MHz), each with I/Q quadratures → 4 rotating-frame channels.

**Ansatz:** Each channel is a sum of N sinusoids with optimisable amplitude, frequency, and phase. GOAT solves an augmented ODE for unitaries + gradients, optimised via L-BFGS-B.

**Strategy:** Multi-stage warm-start with progressively relaxed bounds and added frequency components.

**Verification:** Exact lab-frame propagation (DOP853, sub-Larmor steps) without RWA.

## Paper:
- G. Üstün, A. Morello, and S. Devitt, Single-step parity check gate set for quantum error correction, Quantum Sci. Technol. 10 (2024) 035037, doi:10.1088/2058-9565/ad473c. https://iopscience.iop.org/article/10.1088/2058-9565/ad473c

## QuTiP_QOC / GOAT:
- https://qutip-qoc.readthedocs.io/latest/
- https://github.com/qutip/qutip-qoc

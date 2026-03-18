# U_XX gate with GOAT

Goal: generate a high-fidelity `U_XX` gate with QuTiP GOAT.

Problem: a simple Fourier ansatz mainly learns a slow envelope and gets stuck at low fidelity, while the target pulse appears to need fast carrier structure.

Approach: use a carrier-informed GOAT ansatz and optimize slow envelopes instead of trying to learn the full fast pulse directly.
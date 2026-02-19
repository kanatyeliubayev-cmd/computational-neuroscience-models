# Computational Neuroscience Models

A portfolio of computational neuroscience models implemented from scratch in Python, 
developed as part of my preparation for PhD research in theoretical neuroscience.

The notebooks progress from single-neuron biophysics to network-level phenomena, 
with a focus on hippocampal oscillations relevant to memory consolidation.

---

## Notebooks

### 01 — Hodgkin-Huxley Neuron Model
[![Open in Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](01_hodgkin_huxley_model.ipynb)

Implementation of the full Hodgkin-Huxley model from scratch using NumPy and SciPy.

**Covers:**
- Voltage-gated Na⁺ and K⁺ channel dynamics (gating variables m, h, n)
- Simulation of single action potentials and decomposition into ionic currents
- F-I curve: firing rate as a function of injected current
- Phase plane analysis and limit cycle geometry
- Absolute and relative refractory periods

**Key result:** The threshold, refractory period, and firing rate all emerge naturally
from the biophysics of ion channels — no ad hoc assumptions required.

---

### 02 — Excitatory-Inhibitory Network Oscillations
[![Open in Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](02_ei_network_oscillations.ipynb)

Simulation of a 400E + 100I leaky integrate-and-fire network demonstrating
spontaneous gamma oscillations and sharp-wave ripple analogues.

**Covers:**
- PING mechanism (Pyramidal-Interneuron Network Gamma)
- Population raster plots and LFP proxy
- Power spectral density analysis
- E-I balance scan: how inhibitory strength controls oscillation frequency
- Sharp-wave ripple analogue: transient burst triggers synchronized fast oscillation

**Key result:** Gamma oscillations (~30 Hz) emerge purely from E→I→E feedback 
without any external oscillatory drive. Stronger inhibition shifts the frequency.
A transient excitatory input produces a burst-ripple structure qualitatively 
matching hippocampal sharp-wave ripples during sleep.

---

## Requirements

```bash
pip install numpy scipy matplotlib jupyter
```

Run any notebook with:
```bash
jupyter notebook 01_hodgkin_huxley_model.ipynb
```

---

## Scientific Context

These models are directly relevant to understanding hippocampal circuit dynamics,
particularly the CA3 network mechanisms underlying **sharp-wave ripples (SWRs)** —
brief synchronized bursts (80–140 Hz) that occur during sleep and quiet wakefulness
and are thought to drive **memory consolidation** through replay of prior experiences.

The Hodgkin-Huxley model provides the single-neuron biophysical foundation.
The E-I network demonstrates how populations of such neurons collectively generate
the oscillations and synchronized bursts observed in hippocampal recordings.

---

## References

- Hodgkin & Huxley (1952). A quantitative description of membrane current. *J. Physiology* 117.
- Buzsáki G. (2015). Hippocampal sharp wave-ripple. *Hippocampus* 25(10), 1073–1188.
- Brunel N. (2000). Dynamics of sparsely connected networks. *J. Comp. Neurosci.* 8, 183–208.
- Dayan & Abbott (2001). *Theoretical Neuroscience*. MIT Press.

---

*Yeliubayev Kanat | M.Sc. Neuroscience, Al-Farabi Kazakh National University*

# SIS 1 Neuron Models

A completed Jupyter notebook for **Modelling Biological and Artificial Neurons**.

[Open the notebook](SIS1_Neuro2026_completed.ipynb)

The notebook contains:

- A Leaky Integrate-and-Fire model with membrane leakage, input current, firing threshold, spike events, and reset behaviour.
- A perceptron with a weighted sum, bias, step activation, and an AND truth-table example.
- Two embedded figures, comments explaining the code, and a brief comparison of the models.
- Numerical checks against analytical LIF solutions and checks of the perceptron outputs.

## Run

Use Python 3.12 in a virtual environment:

```sh
python -m pip install -r requirements.txt
python -m notebook
```

Open `SIS1_Neuro2026_completed.ipynb`, then restart the kernel and run all cells.
No datasets or external files are required. The saved notebook already includes its outputs.

## Validation

All six code cells were executed successfully with Python 3.12.14, NumPy 2.3.5,
and Matplotlib 3.11.2. Both figures were visually checked.

- The pulse experiment produces seven spikes during the strong input.
- The maximum passive-decay and subthreshold errors are about 0.00922 mV.
- The simulated interspike interval is 27.7000 ms; the analytical value is 27.7259 ms.
- The perceptron correctly predicts all four AND inputs and handles the threshold boundary.

The LIF model uses forward Euler integration with a 0.1 ms time step. It represents
spikes as threshold events with immediate reset and does not include a refractory
period or an action-potential waveform. Perceptron weights are chosen directly;
no training is performed.

References are included in the notebook.

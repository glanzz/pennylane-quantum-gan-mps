# Quantum General Adversial Networks
The [notebook](./qgan.ipynb) implements QGAN compatible with following the code in Pennylane tutorial: https://pennylane.ai/qml/demos/tutorial_quantum_gans.
The code is tweaked to be compatible for training on Metal Performance Shaders (MPS) backend.
In addition, the following changes are done to achieve better results:
- Initial state is encoded using Rx gates instead of Ry gates used in tutorial
- The generator is updated once for every 3 gradient steps of the discriminator.
- The learning rate of discriminator is relative to generator's learning rate by factor of 0.01.


### Training results from tutorial:
<img width="80%" src="./tutorial_training.png">
<br/>
<br/>

### Training results from this notebook:
<img width="80%" src="./output.png">


### Installation
- Setup virtual environment
```python
python3 -m virtualenv venv
```
- Activate virtual environment
```python
source venv/bin/activate
```
- Install requirements.txt
```python
pip install requirements.txt
```





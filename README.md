# JijModeling-Transpiler-Quantum

`JijModeling-Transpiler-Quantum` is a transpiler from model written in [JijModeling]() to quantum optimization algorithms on variaous quantum platform.

## Installation

```bash
pip install jijmodeling-transpiler-quantum
```

## Qiskit

[Qiskit](https://qiskit.org/) is an open-source SDK for working with quantum computers at the level of circuits, algorithms, and application modules.

### Quantum Approximate Optimization Algorithm (QAOA)

```python
import jijmodeling as jm
import jijmodeling_transpiler as jmt
import jijmodeling_transpiler_quantum as jtq

# Create model
problem = jm.Problem("model")
...  # Modeling ...

# Compile
compiled_instance = jmt.compile_model(problem, instance_data, fixed_vars)

# Transpile to QAOA of qikit
qaoa_builder = jtq.qiskit.transpile_to_qaoa(compiled_instance)
```


## QURI-Parts



| ❌ Not supported yet.                         | 
|------------------------------------------|
| Currently, `quri-parts` is not supported. Please wait for the next release. |


[QURI Parts](https://quri-parts.qunasys.com/) is an open source library suite for creating and executing quantum algorithms on various quantum computers and simulators.

### Quantum Approximate Optimization Algorithm (QAOA)

```python
import jijmodeling as jm
import jijmodeling_transpiler as jmt
import jijmodeling_transpiler_quantum as jtq

# Create model
problem = jm.Problem("model")
...  # Modeling ...

# Compile
compiled_instance = jmt.compile_model(problem, instance_data, fixed_vars)

# Transpile to QAOA of qikit
qaoa_builder = jtq.quri.transpile_to_qaoa(compiled_instance)
```


## Contributing

### Setup

```bash
pip install poetry
poetry install
poetry shell
```

### Test

```bash
pytest tests
```




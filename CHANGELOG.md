# Release 0.12.0-dev

### New features since last release

### Breaking changes

### Improvements

### Documentation

### Bug fixes

### Contributors

This release contains contributions from (in alphabetical order):

---

# Release 0.11.0

### New features

* Made plugin device compatible with new PennyLane wire management.
  [(#37)](https://github.com/PennyLaneAI/pennylane-cirq/pull/37)
  [(#42)](https://github.com/PennyLaneAI/pennylane-cirq/pull/42)

  One can now specify any string or number as a custom wire label,
  and use these labels to address subsystems on the device:

  ```python
  dev = qml.device('cirq.simulator', wires=['q1', 'ancilla', 0, 1])

  def circuit():
    qml.Hadamard(wires='q1')
    qml.CNOT(wires=[1, 'ancilla'])
    ...
  ```

### Contributors

This release contains contributions from (in alphabetical order):

Josh Izaac, Nathan Killoran, Maria Schuld

---

# Release 0.9.1

### Improvements

### Contributors

This release contains contributions from (in alphabetical order):

---

# Release 0.9.0

### New features since last release

* Added a new mixedsimulator class to Cirq, which uses Cirq's
  DensityMatrixSimulator as a backend.
  [#27](https://github.com/XanaduAI/pennylane-cirq/pull/27)

### Documentation

* Redesigned the documentation to be consistent with other plugins.
  [#25](https://github.com/XanaduAI/pennylane-cirq/pull/25)

### Bug fixes

* Renamed probability to ``analytic_probability`` to support new
  changes in PennyLane.
  [#24](https://github.com/XanaduAI/pennylane-cirq/pull/24)

### Contributors

This release contains contributions from (in alphabetical order):

Theodor Isacsson, Nathan Killoran, Maria Schuld, Antal Száva

---

# Release 0.8.0

### Improvements

* Ported the `CirqDevice` class to use the new `QubitDevice` base class,
  enabling the use of tensor observables.
  [#19](https://github.com/XanaduAI/pennylane-cirq/pull/19)

* Added support for inverse operations by defining the `.inv()` method
  of the `CirqOperation` class which uses the `cirq.inverse` function.
  [#15](https://github.com/XanaduAI/pennylane-cirq/pull/15)

### Bug fixes

* Replaced depreceated Cirq commands.
  [#19](https://github.com/XanaduAI/pennylane-cirq/pull/19)

* Fix a minor bug introduced into the test suite by the release of Cirq 0.7.0.
  [#18](https://github.com/XanaduAI/pennylane-cirq/pull/18)

* Fix bugs introduced into the test suite by the release of Cirq 0.6.0.
  [#13](https://github.com/XanaduAI/pennylane-cirq/pull/13)

### Contributors

This release contains contributions from (in alphabetical order):

Johannes Jakob Meyer, Antal Száva

---

# Release 0.1.0

Initial public release.

### Contributors
This release contains contributions from:

Johannes Jakob Meyer

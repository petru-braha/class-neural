neural network driver

```
for epoch
  for batch
    for sample
      run neural network
  update weights
```

run neural network

```
feed forward
cost function
backpropagation
```

backpropagation

```
for layer in range(last to first):
  for neuron in layer:
    error = expected - activation
    w = gradient w.r.t. w
    b = gradient w.r.t. b
    expected_activation_prev_layer = // becomes `expected` in the next iteration
```

intuition for a specific neuron

```
- compare its activation with expected and determine error
- compute how weights and biases should update based on: error, activation of the previous layer neurons
- compute expected values for the previous layer neurons (the true propagation of the error)
  (want higher output? activations of previous layer associated with
   - positive weights - must increase
   - negative - must decrease ANALOG for smaller output)
```

### calculus

- how sensible is function g based on changes in f? partial derivate of g w.r.t. f

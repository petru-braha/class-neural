### algorithm

```
for example (training item)
  for state s
    feed s
    a = best action for s (based on Q(s, *))
    r = Q(s, a)
    s' = P(s, a)

    feed s'
    a' = best action for s'
    max = Q(s', a') * lr
    target = Q(s, *)
    target(s, a) = formula using r, max
    backpropagate target, a (NOT a')
```

- input = state
- output = Q(s, \*)
- weights = initial predictions

### course example

```
a = left
Q(s, a) = 330
r = -8

a' = right
max = 350 * 0.9 = 315
target = [315 - 8, 40, -430]

target = [307, 40, -430]
prediction = [330, 40, -430]
backpropagate target and a=left
```

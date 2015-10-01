INFOgain
========

MATLAB code for computing Information Gain (<https://en.wikipedia.org/wiki/Information_gain_in_decision_trees>).

See also <http://www.maxwell.vrac.puc-rio.br/7587/7587_4.PDF>

Works for both nominal and numeric attributes.

Useful for determining relevant attributes for classification problems.

Usage example:

```matlab
rng default;

x = unifrnd(1,10,20,1);
y = [repmat({'abc'}, 10, 1) ; repmat({'def'}, 10, 1)];
classe = [repmat({'class1'}, 10, 1) ; repmat({'class2'}, 10, 1)];

T = table(x, y, classe);

[gains, attorder] = computegains(T(:,[1 2]), T{:,3});
```


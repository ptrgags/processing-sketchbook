# Planar Curves

## 2021-07-11 Initial Experiments

This sketch is an experiment in learning about curvature of planar curves
in differential geometry. Starting with an initial point, orientation, and
a curvature function, this sketch computes the path, parameterized by
arc length.

The math for this can be found in [This paper](https://archive.bridgesmathart.org/2014/bridges2014-337.pdf)
about self-avoiding random walks (minus the self-avoiding part, that's beyond
the scope of this sketch).

```
theta(s) = integral(0, s, k(s), ds)
x(s) = integral(0, s, cos(theta(s)), ds)
y(s) = integral(0, s, sin(tehta(s)), ds)
```

When I first looked at these, I wasn't sure where the cos(theta) and sin(theta)
are, but these are just the components of the unit tangent vector:
`(cos(theta(s)), sin(theta(s)))`

I made an ensemble of curves with slightly varied parameters to make more
interesting designs. Like the [Hyperbolic Connections sketch](../HyperbolicConnections/),
I use palettes from https://coolors.co/, as the URLs are easy to parse.

Next Steps:
* Gather the parameters into a struct like I did with the seashell surfaces
* Experiment with more curvature functions such as:
  * square/saw/triangle waves?
  * normal curve or other impulse-like function?
  * Tap into the gamepad API to adjust the curvature in real-time?
  * Try the self-avoiding walk (perhaps in a separate sketch?)
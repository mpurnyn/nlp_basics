# Dividing Vector Spaces

In **normal hashing** you have a hashing function that groups data into "buckets".

**Locality Sensitive Hashing** technique that allows you to hash similar inputs into the same buckets with high probability. 

Instead of  typical buckets, you can think of clustering the points by deciding whether they are above or below a line. As you go into higher dimensions, you are start using planes instead of lines.

### Dot Prroducts importance

you can use the dot product to determin weather a vector is above or below a plane.

Assuming that the vector W is a normal vector to the plane, the dot product of a vector V on W can be either on the same side of the plane (positive) or negative.

This property is useful for clustiering in higher dimensions.

### Hashing in higher dimensions with multiple Planes

So given that you now know how to split up vectors with different planes.

You can hash a vector by calculating the sum of the "plane sign" for each plan multiplied by a power of 2.

$$ \sum^{PLANE_n}_{Plane_i} 2^{Plane_i}\times planesign_i  $$

or

$$ \sum^{H}_{i} 2^{i}\times h_i  $$
---

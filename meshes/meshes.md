# Meshes
Variations that generate meshes, three dimensional shapes made from connected triangles. These are all blur variations that ignore their inputs. They are most useful for solid renders, though they work for normal flames as well.

The mesh variations can perform subdivision surface smoothing. This can be helpful for some meshes to create a smoother surface. But it deforms meshes that aren't designed to be smoothed. For example, smoothing an icosahedron will make it a sphere. This is done by first subdividing each triangle into four triangles, then performing Taubin smoothing on each triangle. This process is repeated the number of times specified by subdiv_level (set it to 0 to disable smoothing).

For each subdivision level, each triangle in the mesh is subdivided into four triangles and Taubin smoothing is done on each resulting triangle. Taubin smoothing is done with multiple passes, with two smoothing steps done on each pass. The first step uses the lambda parameter to smooth the mesh, but this also shrinks it. The second step uses the mu parameter (which should be a negative value) to counteract the shrinking.


Note: I've deprecated this group, thinking the variations that were here work better in other groups. Keeping this file for now because of the subdivision smoothing description above.

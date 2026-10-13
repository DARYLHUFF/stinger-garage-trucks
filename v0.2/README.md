# v0.2: tractor library

- `tractors/*.glb`: single-part tractors (CC0 / CC-BY only), each with root node `Tractor_<id>` and empty `hitch_fifth_wheel`.
- `previews/*.png`: side views (red triangle = estimated fifth wheel, dotted lines = axles).
- `truck_roster_v0.2.json`: separate `tractors` and `trailers` lists (any tractor can pair with any trailer). v0.1 parts are referenced at their @v0.1 URLs, unchanged; the T880 entries stay disabled.
- Attribution: see `/ATTRIBUTION.md`.

Same conventions as v0.1: metres, Y-up, front -Z, tyres on y=0, fifth wheel at z=4.263, EXT_meshopt_compression + KHR_mesh_quantization (normals only).
All v0.2 tractors are `provisional`: scaled to standard 2.59 m width, hitch points estimated.

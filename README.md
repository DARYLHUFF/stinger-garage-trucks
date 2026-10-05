# stinger-garage-trucks

Tractor and trailer rigs for Stinger Garage's rig switcher. This library is separate from the car library ([stinger-garage-vehicles](https://github.com/DARYLHUFF/stinger-garage-vehicles)).
The models are derived from third-party ATS mods (T660/Cottrell lineage, the F3D Peterbilt 389 Auto Hauler v1.5, the CyrusTheVirus Cottrell trailer). Their licences are unverified; see the roster `source` fields.

Layout:
- `v0.1/glb/*.glb`: rig parts (`<rig_id>__tractor_v0.1.glb`, `<rig_id>__trailer_v0.1.glb`), each under 20 MB
- `v0.1/truck_roster_v0.1.json`: roster (ids, labels, default flag, CDN URLs, sha256, coupling and wheel positions, flags)

Served via jsDelivr:
`https://cdn.jsdelivr.net/gh/DARYLHUFF/stinger-garage-trucks@v0.1/v0.1/glb/<file>.glb`
`https://cdn.jsdelivr.net/gh/DARYLHUFF/stinger-garage-trucks@v0.1/v0.1/truck_roster_v0.1.json`

Conventions: metres, glTF Y-up, front = -Z, tyres on y = 0. Every rig is baked so its fifth wheel and kingpin sit at z = 4.263, the coupled pose of the default hauler. Files use EXT_meshopt_compression + KHR_mesh_quantization (normals only; positions stay float32), so three.js needs `GLTFLoader.setMeshoptDecoder(MeshoptDecoder)`.

| id | label | default | status |
|---|---|---|---|
| t660_cottrell_default | T660 daycab + Cottrell | yes | current baseline (30.4 hauler split into two parts, geometry identical) |
| p389_cottrell_cx09 | Peterbilt 389 + Cottrell headrack + CX09 LSFA | no | provisional box assembly from package 35 |
| t880_daycab_stinger | Kenworth T880 day cab + Cottrell | no | disabled: needs a Blender fitting pass |
| t880_madrina_rigid | Kenworth T880 Madrina (reference) | no | disabled: reference only |

Versioning: never overwrite a tag. New rigs or fixes go into `v0.2/` with tag `v0.2`.

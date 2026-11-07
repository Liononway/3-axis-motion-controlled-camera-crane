# 3-Axis Motion-Controlled Camera Crane (Pod-Type Universal Camera Mount)

An open-source, **purely mechanical** 3-axis camera crane / gimbal-style shooting rig. No electronics, no motors, no controllers — every axis is driven by hand through belts, worm drives and linear rails, which makes it quiet, reliable, cheap to build and easy to maintain.

![License](https://img.shields.io/badge/license-CERN--OHL--S--2.0-blue)
![Format](https://img.shields.io/badge/CAD-STEP%20AP214-informational)

## Overview

The rig is a pod-type universal camera mount built on a rigid extruded-aluminium table. It provides three orthogonal travel axes for the camera:

| Axis | Motion | Key hardware |
|------|--------|--------------|
| **X** | Left–right travel (ground rails) | 3030 aluminium extrusion + MSA15S linear rails (1650 mm) |
| **Y** | Vertical lift (twin lifting columns) | MSA20S linear rails (1200 mm) + synchronised belt drive |
| **Z** | Front–back travel | 6060 aluminium extrusion + MSA20S linear rails |

The lifting columns are synchronised through a belt-and-pulley system driven by a hex core shaft, and the folding/tensioning mechanism uses **limited-rotation worm gearboxes** so the structure can be folded flat for transport and locked securely in shooting position.

Everything on the frame folds: the front/rear supports, the lifting columns and the ground rails all fold down into a compact package.

## Highlights

- **Purely mechanical** — no wiring, no firmware, no batteries. Motion is fully operator-controlled.
- **Foldable design** — worm-driven folding joints (3× limited-rotation worm gear sets) let the whole rig fold flat.
- **Standard parts based** — built from commodity aluminium extrusions, Hiwin-style MSA linear rails, and off-the-shelf bearings; only small brackets, shafts and housings are custom (mostly 3D-printable).
- **Full BOM included** — 74 entries / 111 parts in a multi-level indented bill of materials.
- **STEP AP214 export** — the complete assembly opens in SolidWorks, Fusion 360, FreeCAD, Onshape, or any STEP-compatible CAD.

## Repository Structure

```
├── cad/
│   └── camera-crane-full-assembly.step   # Complete assembly (SolidWorks 2025 export, ~30 MB)
├── bom/
│   └── bom.xlsx                          # Full multi-level bill of materials (74 entries / 111 parts)
├── LICENSE                               # CERN-OHL-S-2.0 full text
└── README.md
```

## Bill of Materials (Summary)

The full indented BOM lives in [`bom/bom.xlsx`](bom/bom.xlsx). Main off-the-shelf components:

- Aluminium extrusions: LE-6-2040 (1650 mm), 6060 light, 6262, 4040, 3030
- Linear rails: MSA20S2R1200Z0CI+E2 ×3, MSA15S2R1650Z0CI+E2 ×2, with matching E2 slider blocks
- Deep-groove ball bearings 6300-2LS (GB/T 276-1994) ×10
- Limited-rotation worm gear sets ×3 (worm 57545K227 / gear 57545K211, McMaster-Carr reference)
- Synchronous belt pulleys and 6700ZZ bearings
- Custom 3D-printed parts: column spacers, rail end caps, hex-core isolators, crank handle, worm gearbox housings, etc.

> **Note:** The BOM lists part numbers and quantities; material specs are embedded in the part names. The STEP file contains the geometry of all custom parts.

## Usage

1. Download `cad/camera-crane-full-assembly.step` and open it in your CAD software to inspect the design, measure parts, or export STLs for the printed components.
2. Refer to `bom/bom.xlsx` for the complete parts list with assembly hierarchy (up to 5 levels deep).
3. Cut lists for aluminium extrusions can be derived directly from the assembly model.

## Contributing

Issues and pull requests are welcome — especially improvements to the 3D-printed brackets, assembly documentation, and photos/videos of builds.

## License

Copyright © 2026 Liononway

This project is licensed under the **CERN Open Hardware Licence Version 2 - Strongly Reciprocal** ([CERN-OHL-S-2.0](LICENSE)).

You are free to study, modify, manufacture, and commercialise this design, provided that you attribute the original author and share any modifications to the design under the same licence.

---

## 中文说明（Chinese Summary）

本项目是一套**纯机械结构**的三轴运动控制拍摄架（吊舱型万向拍摄架）：无电机、无电控，全部通过同步带、蜗轮蜗杆和直线导轨手动驱动三个正交轴（X 左右横移、Y 升降、Z 前后移动），并可通过三组限位回转蜗轮蜗杆机构整体折叠收纳。

- 完整装配模型：`cad/camera-crane-full-assembly.step`（STEP AP214，SolidWorks 2025 导出）
- 完整多级物料清单：`bom/bom.xlsx`（74 项 / 111 件）
- 开源许可证：CERN-OHL-S-2.0（允许商用与再制造，衍生设计须以相同协议开源并注明出处）

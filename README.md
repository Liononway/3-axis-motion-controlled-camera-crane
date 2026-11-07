# 3-Axis Motion-Controlled Camera Crane (Pod-Type Universal Camera Mount)

An open-source, **purely mechanical** 3-axis camera crane / gimbal-style shooting rig built from aluminium extrusions. No electricity, no motors, no controllers — all motion comes from a hand crank driving belts, worm drives and linear rails, which makes it silent, reliable, cheap to build and usable anywhere, indoor or outdoor.

**Key idea:** the camera can travel along three orthogonal axes (X / Y / Z), stop and hold at any position, and shoot from virtually any angle — overhead top-down shots, side shots, and everything in between. When you're done, the whole rig folds up into a slim package that tucks into a corner.

- **Folded footprint:** 1.8 m (H) × 2.2 m (L) × 30 cm (W) — slim enough to stand against a wall in the corner of a room
- **Power source:** one hand crank. That's it.

![License](https://img.shields.io/badge/license-CERN--OHL--S--2.0-blue)
![Format](https://img.shields.io/badge/CAD-STEP%20AP214-informational)

## Overview

The rig is a pod-type universal camera mount built on a rigid extruded-aluminium table. It provides three orthogonal travel axes for the camera:

| Axis | Motion | Key hardware |
|------|--------|--------------|
| **X** | Left–right travel (ground rails) | 3030 aluminium extrusion + MSA15S linear rails (1650 mm) |
| **Y** | Vertical lift (twin lifting columns) | MSA20S linear rails (1200 mm) + synchronised belt drive |
| **Z** | Front–back travel | 6060 aluminium extrusion + MSA20S linear rails |

The camera platform can therefore reach any point in a 3D working volume and hold position there without drift — enabling multi-angle shooting (top-down / overhead, side, and oblique) from a single setup.

The lifting columns are synchronised through a belt-and-pulley system driven by a hex core shaft, and the folding/tensioning mechanism uses **limited-rotation worm gearboxes** so the structure can be folded flat for transport and locked securely in shooting position.

Everything on the frame folds: the front/rear supports, the lifting columns and the ground rails all fold down into a compact package.

## Highlights

- **Zero power required** — no wiring, no firmware, no batteries. A single hand crank drives everything; works anywhere.
- **Any position, any angle** — the camera stops and holds at any point in the XYZ working volume for overhead, side and oblique shots.
- **Folds into a corner** — worm-driven folding joints (3× limited-rotation worm gear sets) collapse the rig to 1.8 × 2.2 × 0.3 m, slim enough to store against a wall.
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

本项目是一套用铝型材搭建的**纯机械**吊舱型万向拍摄架，可实现 **XYZ 三轴运动**：

- **完全不用电** —— 只靠一根手摇杆，通过同步带、蜗轮蜗杆和直线导轨驱动全部三轴；
- **任意位置停止** —— 相机可在三维工作空间内任意点定位悬停，实现**俯拍、侧拍等多角度拍摄**；
- **可整体折叠收纳** —— 收纳后尺寸 **高 1.8 米 × 长 2.2 米 × 宽 30 厘米**，薄薄一片，靠墙放在房间角落即可；
- 三组限位回转蜗轮蜗杆机构负责折叠锁定，双升降立柱由同步带保持两端同步。

- 完整装配模型：`cad/camera-crane-full-assembly.step`（STEP AP214，SolidWorks 2025 导出）
- 完整多级物料清单：`bom/bom.xlsx`（74 项 / 111 件）
- 开源许可证：CERN-OHL-S-2.0（允许商用与再制造，衍生设计须以相同协议开源并注明出处）

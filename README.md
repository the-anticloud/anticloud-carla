# CARLA

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-automotive-lightgrey)

> Anticloud-hardened packaging of the upstream project `CARLA` in category **AUTOMOTIVE**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** AUTOMOTIVE · **Upstream:** https://github.com/carla-simulator/carla · **Upstream pin:** `a7e2bf8912013d3e442d2aad54320ed8fac92c14` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

CARLA Simulator
===============

[![Documentation](https://readthedocs.org/projects/carla/badge/?version=latest)](https://carla-ue5.readthedocs.io)

[![carla.org](Docs/img/btn/web.png)](http://carla.org)
[![download](Docs/img/btn/download.png)](https://github.com/carla-simulator/carla/releases)
[![documentation](Docs/img/btn/docs.png)](https://carla-ue5.readthedocs.io)
[![forum](Docs/img/btn/forum.png)](https://github.com/carla-simulator/carla/discussions)
[![discord](Docs/img/btn/chat.png)](https://discord.gg/8kqACuC)

CARLA is an open-source simulator for autonomous driving research. CARLA has been developed from the ground up to support development, training, and
validation of autonomous driving systems. In addition to open-source code and protocols, CARLA provides open digital assets (urban layouts, buildings,
vehicles) that were created for this purpose and can be used freely. The simulation platform supports flexible specification of sensor suites and
environmental conditions.

[![CARLA Video](Docs/img/carla_ue5_readme_img.webp)](https://www.youtube.com/watch?v=q4V9GYjA1pE)

>[!NOTE]
> This is the development branch `ue5-dev` for the **Unreal Engine 5.5 version of CARLA**. This branch exists in parallel with the Unreal Engine 4.26 version of CARLA, in the `ue4-dev` branch. Please be sure that this version of CARLA is suitable for your needs as there are significant differences between the UE 5.5 and UE 4.26 versions of CARLA. 

### Recommended system

* Intel i7 gen 9th - 11th / Intel i9 gen 9th - 11th / AMD Ryzen 7 / AMD Ryzen 9
* +32 Gb RAM memory 
* NVIDIA RTX 3070/3080/3090 / NVIDIA RTX 4090 / NVIDIA RTX 5090 or better
* 16 Gb or more VRAM
* Ubuntu 22.04 or 24.04, or Windows 11

 >[!NOTE]
> You must use either Ubuntu 22.04 or 24.04, or Windows 11. The Unreal Engine 5.5 version of CARLA will not work on Ubuntu 20.04 or Windows 10 or lower.

## Documentation

The [CARLA documentation](https://carla-ue5.readthedocs.io/en/latest/) is hosted on ReadTheDocs. Please see the following key links:

- [Building on Linux](https://carla-ue5.readthedocs.io/en/latest/build_linux_ue5/)
- [Building on Windows](https://carla-ue5.readthedocs.io/en/latest/build_windows_ue5/)
- [First steps](https://carla-ue5.readthedocs.io/en/latest/tuto_first_steps/)
- [CARLA asset catalogue](https://carla-ue5.readthedocs.io/en/latest/catalogue/)
- [Python API reference](https://carla-ue5.readthedocs.io/en/latest/python_api/)
- [Blueprint library](https://carla-ue5.readthedocs.io/en/latest/bp_library/)

## CARLA Ecosystem
projects associated with the CARLA simulation platform:

* [**CARLA Autonomous Driving leaderboard**](https://leaderboard.carla.org/): Automatic platform to validate Autonomous Driving stacks
* [**Scenario_Runner**](https://github.com/carla-simulator/scenario_runner): Engine to execute traffic scenarios in CARLA 0.9.X
* [**ROS-bridge**](https://github.com/carla-simulator/ros-bridge): Interface to connect CARLA 0.9.X to ROS
* [**Driving-benchmarks**](https://github.com/carla-simulator/driving-benchmarks): Benchmark tools for Autonomous Driving tasks
* [**Conditional Imitation-Learning**](https://github.com/felipecode/coiltraine): Training and testing Conditional Imitation Learning models in CARLA
* [**AutoWare AV stack**](https://github.com/carla-simulator/carla-autoware): Bridge to connect AutoWare AV stack to CARLA
* [**Reinforcement-Learning**](https://github.com/carla-simulator/reinforcement-learning): Code for running Conditional Reinforcement Learning models in CARLA
* [**RoadRunner**](https://www.mathworks.com/products/roadrunner.html): MATLAB GUI based application to create road networks in OpenDrive format 
* [**Map Editor**](https://github.com/carla-simulator/carla-map-editor): Standalone GUI application to enhance RoadRunner maps with traffic lights and traffic signs information

**Like what you see? Star us on GitHub to support the project!**

Paper
-----

If you use CARLA, please cite our CoRL’17 paper.

_CARLA: An Open Urban Driving Simulator_<br>Alexey Dosovitskiy, German Ros,
Felipe Codevilla, Antonio Lopez, Vladlen Koltun; PMLR 78:1-16
[[PDF](http://proceedings.mlr.press/v78/dosovitskiy17a/dosovitskiy17a.pdf)]
[[talk](https://www.youtube.com/watch?v=xfyK03MEZ9Q&feature=youtu.be&t=2h44m30s)]

```
@inproceedings{Dosovitskiy17,
  title = {{CARLA}: {An} Open Urban Driving Simulator},
  author = {Alexey Dosovitskiy and German Ros and Felipe Codevilla and Antonio Lopez and Vladlen Koltun},
  booktitle = {Proceedings of the 1st Annual Conference on Robot Learning},
  pages = {1--16},
  year = {2017}
}
```

## Building CARLA with Unreal Engine 5.5
--------------

source this project locally from GitHub, specifying the *ue5-dev* branch:

```sh
git source -b ue5-dev https://github.com/carla-simulator/carla.git CarlaUE5
```

In order to build CARLA, you need access to the CARLA fork of Unreal Engine 5.5. In order to access this project, you must first link your GitHub account to Epic Games by following [this guide](https://www.unrealengine.com/en-US/ue-on-github). You then also need to use your git credentials to authorise the download of the Unreal Engine 5.5 project. 

__Building in Linux__:

Run the setup script from a terminal open in the CARLA root directory:

```sh
cd CarlaUE5
./CarlaSetup.sh --interactive
```

The setup script will prompt you for your sudo password, in order to install the prerequisites. It will then prompt you for your GitHub credentials in order to authorise the download of the Unreal Engine project. 

The setup script will install by default Python 3 using apt. If you want to target an existing Python installation, you should use the `--python-root=PATH_TO_PYTHON` argument with the relevant Python installation path. You can use whereis python3 in your chosen environment and strip the `/python3` suffix from the path.

__Building in Linux unattended__:

If you want to run the setup script unattended, your git credentials need to be stored in an envir

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python (requirements)** (manifests: requirements.txt; scanned in UPSTREAM_CLONE)
- Top-level source layout: `CMake/`, `Examples/`, `Import/`, `LibCarla/`, `PythonAPI/`, `Ros2Native/`, `Unreal/`, `Util/`, `carla-agentic-tools/`
- Snapshot size: **2688 files**, **324194 lines of code** (measured; see Benchmarks)
- Primary languages: `.h` (781), `.cpp` (476), `.py` (368), `.png` (262), `.jpg` (180), `.webp` (131)
- Upstream commit pinned for this packaging: `a7e2bf8912013d3e442d2aad54320ed8fac92c14`

---

## Installation

vehicles) that were created for this purpose and can be used freely. The simulation platform supports flexible specification of sensor suites and
environmental conditions.

[![CARLA Video](Docs/img/carla_ue5_readme_img.webp)](https://www.youtube.com/watch?v=q4V9GYjA1pE)

>[!NOTE]
> This is the development branch `ue5-dev` for the **Unreal Engine 5.5 version of CARLA**. This branch exists in parallel with the Unreal Engine 4.26 version of CARLA, in the `ue4-dev` branch. Please be sure that this version of CARLA is suitable for your needs as there are significant differences between the UE 5.5 and UE 4.26 versions of CARLA.

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

No usage section was found in the upstream readme. Entry points detected in this project directory:

```sh
python -m carla    # module entry point, when the package layout matches
```

Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

[![carla.org](Docs/img/btn/web.png)](http://carla.org)
[![download](Docs/img/btn/download.png)](https://github.com/carla-simulator/carla/releases)
[![documentation](Docs/img/btn/docs.png)](https://carla-ue5.readthedocs.io)
[![forum](Docs/img/btn/forum.png)](https://github.com/carla-simulator/carla/discussions)
[![discord](Docs/img/btn/chat.png)](https://discord.gg/8kqACuC)

CARLA is an open-source simulator for autonomous driving research. CARLA has been developed from the ground up to support development, training, and
validation of autonomous driving systems. In addition to open-source code and protocols, CARLA provides open digital assets (urban layouts, buildings,
vehicles) that were created for this purpose and can be used freely. The simulation platform supports flexible specification of sensor suites and
environmental conditions.

[![CARLA Video](Docs/img/carla_ue5_readme_img.webp)](https://www.youtube.com/watch?v=q4V9GYjA1pE)

>[!NOTE]
> This is the development branch `ue5-dev` for the **Unreal Engine 5.5 version of CARLA**. This branch exists in parallel with the Unreal Engine 4.26 version of CARLA, in the `ue4-dev` branch. Please be sure that this version of CARLA is suitable for your needs as there are significant differences between the UE 5.5 and UE 4.26 versions of CARLA.

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python (requirements) |
| Manifests detected | requirements.txt |
| Files in snapshot | 2688 |
| Lines of code | 324194 |
| Dependency references | 25 |
| Dependencies by ecosystem | native: 7, pypi: 18 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| native | LibXml2 | - | Util/DockerUtils/fbx/CMakeLists.txt |
| native | Python3 | - | PythonAPI/CMakeLists.txt |
| pypi | pygame | >=2.6 | PythonAPI/examples/nvidia/nurec/pyproject.toml |
| pypi | numpy | >=1.26 | PythonAPI/examples/nvidia/nurec/pyproject.toml |
| pypi | scipy | >=1.11 | PythonAPI/examples/nvidia/nurec/pyproject.toml |
| pypi | grpcio | >=1.66 | PythonAPI/examples/nvidia/nurec/pyproject.toml |
| pypi | protobuf | >=5.29 | PythonAPI/examples/nvidia/nurec/pyproject.toml |
| pypi | carla | >=0.10.0 | PythonAPI/examples/nvidia/nurec/pyproject.toml |
| pypi | pyyaml | - | PythonAPI/examples/nvidia/nurec/pyproject.toml |
| pypi | pillow | >=10 | PythonAPI/examples/nvidia/nurec/pyproject.toml |
| pypi | carla-cosmos | >=0.2.0 | PythonAPI/examples/nvidia/cosmos/server/pyproject.toml |
| pypi | carla-cosmos-workers | >=0.2.0 | PythonAPI/examples/nvidia/cosmos/server/pyproject.toml |
| pypi | fastapi | >=0.110 | PythonAPI/examples/nvidia/cosmos/server/pyproject.toml |
| pypi | uvicorn | >=0.29 | PythonAPI/examples/nvidia/cosmos/server/pyproject.toml |
| pypi | pydantic | >=2 | PythonAPI/examples/nvidia/cosmos/server/pyproject.toml |
| ... | (10 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

[![CARLA Video](Docs/img/carla_ue5_readme_img.webp)](https://www.youtube.com/watch?v=q4V9GYjA1pE)

>[!NOTE]
> This is the development branch `ue5-dev` for the **Unreal Engine 5.5 version of CARLA**. This branch exists in parallel with the Unreal Engine 4.26 version of CARLA, in the `ue4-dev` branch. Please be sure that this version of CARLA is suitable for your needs as there are significant differences between the UE 5.5 and UE 4.26 versions of CARLA.

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `CARLA` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
MIT License

Copyright (c) 2024 Computer Vision Center (CVC) at the Universitat Autonoma de
Barcelona (UAB).

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `CARLA` (category: AUTOMOTIVE)
- **Upstream URL:** https://github.com/carla-simulator/carla
- **Pinned commit (SHA):** `a7e2bf8912013d3e442d2aad54320ed8fac92c14`
- **Branch:** ue58-dev
- **Pin provenance:** GitHub API commits/ue58-dev. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`abf1bd4c6766b8384041fcac77f6042065730e4cf1160a7a58a8def1e8bedfe2`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.


> 源码范围：仅本模块 RTL、内部子模块及独立 TB；其他模块源码请进入对应工作台。`code/` 不收录联调包装、构建脚本、Makefile 或说明文件。

# TPU_CTRL Design Workbench

**[Open the TPU_CTRL Workbench](https://lin2513lp.github.io/TPU_CTRL_WORKBENCH/TPU_CTRL_WORKBENCH.html)**

Dataflow control and 16-lane input alignment between FIFO_IN and SA_TOP. The workbench runs in a browser and requires no installation.

## Workbench contents

- FIFO reads, zero padding, and skew alignment for 16 x 32-bit input lanes.
- Enable/start synchronization, input counting, and completion feedback from SA_TOP.
- Protocol-error detection, a three-bit error count, and AHB register-map access.
- Architecture reports, simulation captures, design notes, and source browsing.

## Source files

[`code/`](code/) contains only this module’s RTL, internal submodules and standalone HDL testbenches. There are **9 RTL/TB files**. Other modules are available from their respective workbenches. [`source-manifest.json`](source-manifest.json) lists the retained source hashes.


## Repository layout

| Path | Contents |
| --- | --- |
| [`TPU_CTRL_WORKBENCH.html`](TPU_CTRL_WORKBENCH.html) | Main design workbench |
| [`code/`](code/) | This module’s RTL and independent HDL testbenches |
| [`source-manifest.json`](source-manifest.json) | Source inventory and checksums |
| [`index.html`](index.html) | English project introduction and workbench link |

## Using the project

Open the workbench to browse the design report, waveforms and this module’s RTL/TB. Run simulation in the original local project environment.

## Latest simulation update

The current CTRL unit test passes 2,059 checks in Questa and VM VCS. A separate protocol-error test passes 807 checks in both simulators. The three-bit error count increments once per premature SA LAST incident, saturates at seven, and clears on reset or an accepted START.

## Related workbenches

- [TPU_CRG](https://github.com/Lin2513lp/TPU_CRG_WORKBENCH)
- [AXI_TOP](https://github.com/Lin2513lp/AXI_TOP_WORKBENCH)
- [AHB_SLAVE](https://github.com/Lin2513lp/AHB_SLAVE_WORKBENCH)
- [SA_TOP](https://github.com/Lin2513lp/sa-workbench)
- [PE_MP](https://github.com/Lin2513lp/pe-mp-workbench)

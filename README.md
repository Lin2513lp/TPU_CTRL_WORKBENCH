# TPU_CTRL Design Workbench

**[Open the TPU_CTRL Workbench](https://lin2513lp.github.io/TPU_CTRL_WORKBENCH/TPU_CTRL_WORKBENCH.html)**

Dataflow control and 16-lane input alignment between FIFO_IN and SA_TOP. The workbench runs in a browser and requires no installation.

## Workbench contents

- FIFO reads, zero padding, and skew alignment for 16 x 32-bit input lanes.
- Enable/start synchronization, input counting, and completion feedback from SA_TOP.
- Protocol-error detection, a three-bit error count, and AHB register-map access.
- Architecture reports, simulation captures, design notes, and source browsing.

## Source files

[`code/`](code/) contains only CTRL RTL, its register module and independent TBs: **9 RTL/TB files**. Other IP sources are available in their own workbenches.

## Repository layout

| Path | Contents |
| --- | --- |
| [`TPU_CTRL_WORKBENCH.html`](TPU_CTRL_WORKBENCH.html) | Main design workbench |
| [`code/`](code/) | CTRL RTL and independent TBs |
| [`source-manifest.json`](source-manifest.json) | Source inventory and checksums |
| [`index.html`](index.html) | English project introduction and workbench link |

## Using the project

Open the workbench for reports, waveforms and CTRL RTL/TB. Simulation uses the original local project.

## Latest simulation update

Current VM VCS regression passes: CTRL 2,245 checks; reg_list 9,216; DONE read-only 101; AHB regmap 13,747. Bound assertions are enabled. DONE remains set through writes and clock gating, and clears only on reset or an accepted START. The request/acknowledgment ports and all software-clear handshake logic are removed.

## Related workbenches

- [TPU_CRG](https://github.com/Lin2513lp/TPU_CRG_WORKBENCH)
- [AXI_TOP](https://github.com/Lin2513lp/AXI_TOP_WORKBENCH)
- [AHB_SLAVE](https://github.com/Lin2513lp/AHB_SLAVE_WORKBENCH)
- [SA_TOP](https://github.com/Lin2513lp/sa-workbench)
- [PE_MP](https://github.com/Lin2513lp/pe-mp-workbench)

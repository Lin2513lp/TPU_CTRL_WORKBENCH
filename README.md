# TPU_CTRL Design Workbench

**[Open the TPU_CTRL Workbench](https://lin2513lp.github.io/TPU_CTRL_WORKBENCH/TPU_CTRL_WORKBENCH.html)**

Dataflow control and 16-lane input alignment between FIFO_IN and SA_TOP. The workbench runs in a browser and requires no installation.

## Workbench contents

- FIFO reads, zero padding, and skew alignment for 16 x 32-bit input lanes.
- Enable/start synchronization, input counting, and completion feedback from SA_TOP.
- Protocol-error detection, a three-bit error count, and AHB register-map access.
- Architecture reports, simulation captures, design notes, and source browsing.

## Source files

[`code/`](code/) contains the current `TPU_CTRL` source snapshot and the FIFO/SA integration references shown in the workbench. Relative paths are retained, including RTL, testbenches, Makefiles, file lists, and available helper scripts. The workbench's code viewer displays this same snapshot.

There are **22 project files** in this snapshot. [`source-manifest.json`](source-manifest.json) records the source inventory and SHA-256 checksums. Generated simulator databases, waveform dumps, editor temporary files, and license logs are excluded. The upstream reference files are for source browsing rather than a complete TPU simulation checkout.

## Repository layout

| Path | Contents |
| --- | --- |
| [`TPU_CTRL_WORKBENCH.html`](TPU_CTRL_WORKBENCH.html) | Main design workbench |
| [`code/`](code/) | Project source files, build entry points, and integration references |
| [`source-manifest.json`](source-manifest.json) | Source inventory and checksums |
| [`index.html`](index.html) | English project introduction and workbench link |

## Using the project

Open the workbench through the link above to browse the report, code, and waveforms. For standalone CTRL simulation, clone this repository, enter `code/TPU_CTRL/`, and use its Makefile in a configured Linux EDA environment. The original tool paths and environment variables in the shared Makefile are preserved; configure these for your installation.

## Latest simulation update

The current CTRL unit test passes 2,059 checks in Questa and VM VCS. A separate protocol-error test passes 807 checks in both simulators. The three-bit error count increments once per premature SA LAST incident, saturates at seven, and clears on reset or an accepted START.

## Related workbenches

- [TPU_CRG](https://github.com/Lin2513lp/TPU_CRG_WORKBENCH)
- [AXI_TOP](https://github.com/Lin2513lp/AXI_TOP_WORKBENCH)
- [AHB_SLAVE](https://github.com/Lin2513lp/AHB_SLAVE_WORKBENCH)
- [SA_TOP](https://github.com/Lin2513lp/sa-workbench)
- [PE_MP](https://github.com/Lin2513lp/pe-mp-workbench)

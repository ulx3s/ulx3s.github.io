# ULX3S Tiny Tapeout

Turn your FPGA design into an ASIC with [Tiny Tapeout](https://tinytapeout.com/).

Use the [ulx3s/ttsky-verilog-template](https://github.com/ulx3s/ttsky-verilog-template) as a starting point for your submission 
(or any of the other [TinyTapeout templates](https://github.com/orgs/TinyTapeout/repositories?q=template)).

A working minimal example is the [Hazard3-Doom tt-fpga-ulx workflow](https://github.com/ulx3s/Hazard3-Doom/blob/main/.github/workflows/tt-fpga-ulx.yaml).

Add a job step such as this to the workflow file:

```yaml
jobs:
  fpga-ulx3s:
    runs-on: ubuntu-24.04
    steps:
      - name: checkout repo
        uses: actions/checkout@v7
        with:
          submodules: recursive

      - name: FPGA bitstream for TT ASIC Sim (ULX3S ECP5)
        uses: ulx3s/tt-gds-action/fpga/ulx3s@experimental
        with:
          ecp5-device: 85k
          lpf: tt/fpga/ulx3s/ulx3s_v316.lpf
          artifact-name: fpga_ulx3s_ecp5
          uart-enabled: true
```

For more details, see the [Tiny Tapeout Action on GitHub Marketplace](https://github.com/marketplace/actions/tiny-tapeout-gds-action-for-the-ulx3s-and-ulx4m-ecp5-fpga).


---

## Chat and support

Discord Channel

  - [https://discord.gg/qwMUk6W](https://discord.gg/qwMUk6W) (problems/question/general chat); [#hazard3-doom](https://discord.com/channels/690209441953480758/1546280673822642186)

Gitter Channel

  - [https://gitter.im/ulx3s/Lobby](https://gitter.im/ulx3s/Lobby) (Focused on development)

--- 

Back to [ULX3S project site](https://ulx3s.github.io/). Improve [this page](https://github.com/ulx3s/ulx3s.github.io/blob/master/ulx-doom/index.md).

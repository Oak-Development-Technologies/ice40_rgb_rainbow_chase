# ICE40 RGB Rainbow Chase

This repository is a simple RGB Rainbow Chase test for the IcyBlue FPGA. This would also be compatible with any other iCE40 FPGA.

### How to build

To build, make sure the Yosys OSS CAD Suite tools are installed.

Download the most recent release from GitHub, `source ${BASE_DIR}/oss-cad-suite/environment` on Mac/Linux or install directly on Windows 10/11.

Once OSS CAD Suite is available, type the following into your command line terminal.

`make build` - this builds the binary file (bitstream) from the FPGA

`make prog` - this will program the SRAM on the FPGA directly, use this if you don't have on board flash. You'll need to reflash this bitstream any time you reset the FPGA or lose power.

`make prog_flash` - this will program the SPI Flash on the IcyBlue FPGA, or the SPI Flash on other boards that use the FT232H to program the on board FLASH.

**Coming Soon**

`make load_cirpy` - This will check for a circuitpython drive mounted (will start Mac only), copy over the bin file to the circuitpython drive as well as a `code.py` containing the code to program a standalone fpga.

It will also clone down the Oakdevtech_Icepython library and copy it to the `lib` folder of the circuitpython drive.

### issues?

If you experience any issues, file an issue. :)
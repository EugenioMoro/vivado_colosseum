# USRP fpga flashing on colosseum through Vivado 
## Download and install Vivado

1. Download Vivado 2015.4 Lab Edition [here](https://www.xilinx.com/member/forms/download/xef.html?filename=Xilinx_Vivado_Lab_Lin_2015.4_1118_2.tar.gz)
2. Unpack with `tar -xzvf`
3. Install with `./xsetup -b Install -e "Vivado Lab Edition (Standalone)" --agree XilinxEULA,3rdPartyEULA,WebTalkTerms`
4. Clone this repo and source the environment
```
git clone https://github.com/EugenioMoro/vivado_colosseum.git
cd vivado_colosseum
source setupenv.sh
```
5. Test with `viv_jtag_list`

## Download and flash images
```
uhd_images_downloader
viv_jtag_program /usr/share/uhd/images/usrp_x310_fpga_HG.bit
```
Test with `uhd_usrp_probe`
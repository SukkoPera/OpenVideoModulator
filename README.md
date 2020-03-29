# OpenVideoModulator
OpenVideoModulator is an Open Hardware adapter that converts an RGB video signal to Composite and S-Video.

![Board](https://raw.githubusercontent.com/SukkoPera/OpenVideoModulator/master/img/render-top.png)

## Summary
OpenVideoModulator is an Open Hardware implementation of [a small circuit found on the Amstrad CPC Wiki](http://www.cpcwiki.eu/index.php/RGB_SVideo) that is able to produce a composite video signal from separate red, green and blue color component signals (plus sync). Since it uses the AD724 encoder, it is also able to produce an S-Video (Y/C) signal and it supports both the PAL and NTSC standards.

It has a compact form factor, a low component count and it only requires a +5V power supply. This makes it useful with old computers that do not have a native composite or S-Video output, like the Amstrad CPC or the Commodore Amiga 500 (which actually has a composite output but it's only black & white). It also tries to maintain the smallest possible form factor, which might allow for an internal installation.

## Assembly and Usage
First of all you need to choose whether you want PAL or NTSC output. The board is preconfigured for PAL, if you need NTSC you will need to cut the link between pads 1-2 on the top of the board and solder 2-3 together. The crystal frequency also depends on your choice: use 4.433620 MHz for PAL or 3.579545 MHz for NTSC.

Solder the AD724 chip first, then all surface-mount components. Finally complete the board with the through-hole connectors and crystal.

One of C6 and C7 should be enough. I use a 100uF on C6 but that is probably overkill. Play with them if your output video signal is unstable.

The Composite/S-Video connector can be found from many Chinese sellers under the name *AV-MDC-401*. I chose this one as it was perfect for my needs, but the board should be easy to adapt to different connectors.

Usage should be straightforward: just provide power (make sure to match the polarity!) and video signals to the board, then get your output from the other side. Note that the *sync* input requires a *composite sync* signal.

## License
The OpenVideoModulator documentation, including the design itself, is copyright &copy; SukkoPera 2019-2020.

OpenVideoModulator is Open Hardware licensed under the [CERN OHL v. 1.2](http://ohwr.org/cernohl).

You may redistribute and modify this documentation under the terms of the CERN OHL v.1.2. This documentation is distributed *as is* and WITHOUT ANY EXPRESS OR IMPLIED WARRANTIES whatsoever with respect to its functionality, operability or use, including, without limitation, any implied warranties OF MERCHANTABILITY, SATISFACTORY QUALITY, FITNESS FOR A PARTICULAR PURPOSE or infringement. We expressly disclaim any liability whatsoever for any direct, indirect, consequential, incidental or special damages, including, without limitation, lost revenues, lost profits, losses resulting from business interruption or loss of data, regardless of the form of action or legal theory under which the liability may be asserted, even if advised of the possibility or likelihood of such damages.

A copy of the full license is included in file [LICENSE.pdf](LICENSE.pdf), please refer to it for applicable conditions. In order to properly deal with its terms, please see file [LICENSE_HOWTO.pdf](LICENSE_HOWTO.pdf).

The contact points for information about manufactured Products (see section 4.2) are listed in file [PRODUCT.md](PRODUCT.md).

Any modifications made by Licensees (see section 3.4.b) shall be recorded in file [CHANGES.md](CHANGES.md).

The Documentation Location of the original project is https://github.com/SukkoPera/OpenVideoModulator/.

## Support the Project
Since the project is open you are free to get the PCBs made by your preferred manufacturer, however in case you want to support the development, you can order them from PCBWay through this link:

[![PCB from PCBWay](https://www.pcbway.com/project/img/images/frompcbway.png)](https://www.pcbway.com/project/shareproject/OpenVideoModulator_V1.html)

You get my gratitude and cheap, professionally-made and good quality PCBs, I get some credit that will help with this and [other projects](https://www.pcbway.com/project/member/shareproject/?bmbid=41100). You won't even have to worry about the various PCB options, it's all pre-configured for you!

Also, if you still have to register to that site, [you can use this link](https://www.pcbway.com/setinvite.aspx?inviteid=41100) to get some bonus initial credit (and yield me some more).

Again, if you want to use another manufacturer, feel free to, don't feel obligated :). But then you can buy me a coffee if you want:

<a href='https://ko-fi.com/L3L0U18L' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi2.png?v=2' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>


## Get Help
If you need help or have questions, you can join [the official Telegram group](https://t.me/joinchat/HUHdWBC9J9JnYIrvTYfZmg).

## Thanks
- CPC Wiki for the original circuit.

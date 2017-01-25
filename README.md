# S88-Train-detection-bus
PCB designs for an S88 bus for detecting model trains on a track. The Marklin S88 bus is based on a shift register. More information on the Marklin S88 bus can be found here:
* [S88-N - s88 over RJ45](http://www.s88-n.eu/index-en.html) (English)
* [Digital Bahn.de](https://www.digital-bahn.de/info_tech/s88.htm) (Deutsch)
* [Marklin S88 Link](http://www.maerklin.de/en/products/details/article/60883/) ([PDF manual](https://static.maerklin.de/damcontent/d1/65/d1652564aaf7fea4ec6f6f887203d2681464362779.pdf)) (English/Deutsch)
* [Avontuur in miniatuur - Terugmelding](http://www.floodland.nl/aim/info_terugmelding_1.htm) (Nederlands)

This design uses master and slave boards, connected to a single bus controller (e.g. a Marklin CS or an Arduino). Both boards are suitable for DIY-etching (master: uv-lighting, slave: toner-tranfer). The number of drilling-holes is kept to a minimum. **Note: there is no hysteresis on the inputs. This must be implemented in the controller software.**
## Master board
The master board uses 3 74hc165 ICs, resulting in 24 inputs. The master boards can be chained together. Each connector on the master board serves a group of 3 inputs, which are connected via a slave board. All inputs are fitted with pullups. The train wheels connect the inputs to ground when entering a track section.

[See the InputModule for the design files of the master board](InputModule/README.md)

<img alt="Breadboard schematic of the master board" src="simplified breadboard schematic arduino 74hc165.png" width="350" />

## Slave board
A small slave board can be mounted close to the tracks, and connects up to 3 track segments. The board features a led for diagnostic purposes.  
<img alt="Picture of the slave board" src="3 track connector pcb.jpg" width="350" />
## Video of result
[!<img alt="A train is detected on the track" src="train detecting demo.jpg" width="350" />](https://www.youtube.com/watch?v=ed31EqeW7o0)

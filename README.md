# S88-Train-detection-bus
PCB designs for an S88 bus for detecting model trains on a track. The Marklin S88 bus is based on a shift register. This design uses master and slave boards. Both boards are suitable for DIY-etching (master: uv-lighting, slave: toner-tranfer). The number of drilling-holes is kept to a minimum. **Note: there is no hysteresis on the inputs. This must be implemented in the controller software.**
## Master board
The master board uses 3 74hc165 ICs, resulting in 24 inputs. The master boards can be chained together. Each connector on the master board serves a group of 3 inputs, which are connected via a slave board. All inputs are fitted with pullups, since the train wheels are connected to ground.
<img alt="Breadboard schematic of the master board" src="simplified breadboard schematic arduino 74hc165.png" width="350" />
## Slave board
A small slave board can be mounted close to the tracks, and connects up to 3 track segments. The board features a led for diagnostic purposes.  
<img alt="Picture of the slave board" src="3 track connector pcb.jpg" width="350" />
## Video of result
[!<img alt="A train is detected on the track" src="train detecting demo.jpg" width="350" />](https://www.youtube.com/watch?v=ed31EqeW7o0)

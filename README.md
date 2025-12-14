# Door Security System Design for FPGA using Verilog  
## 📝 __Overview__  
This project aimed to design a simple door security system that allows users holding a 4-digit password to access a room. If a wrong password is keyed in, a red LED would be lit. Otherwise, a green LED would be lit and the user’s designated ID number would be shown. The system would allow users to change the password if necessary.  
The project involved proper understanding of the objective, deriving the system’s finite state diagram accordingly, as well as coding and integration of FSM and datapath in Verilog. The software used for coding and simulation was Intel Quartus Prime 20.1.1 (Lite edition).  
  
## 📂 __Contents__  
| File Name | File Type | Description |
|-----------|-----------|-------------|
| README | MD | Read this before anything else |
| Concept | PNG | Conceptual representation of the system’s physical appearance |
| Flowchart | PNG | Steps of operation the system is expected to follow |
| System Layout | PDF | Description of the major components within the system and their correlation |
| State Diagram | PNG | Visually shows state transitions based on inputs and conditions |
| State Table | PNG | Tabulates present state, inputs, next state, and outputs |
| Code | TXT | The code implemented in the project, copied for convenience |
| Doors2 | QPF | The project file generated in Quartus |
| Waveform3 | VWF | Waveform derived from the compiled code in Quartus |  

## ▶️ __How to Run the Code & Simulate the Waveform__  
i)	Open the program Intel Quartus Prime, provided you have it installed on your computer.
ii)	Click on New Project Wizard. Then click on Next.
iii)	Enter a working directory for the project and the name of the project. The name should be same as the topmodule declared in the code, in this case, Door2. Then click on Finish.
iv)	Copy the code from the file Code.txt and paste in the workspace.
v)	Press Ctrl + L to compile the code.
vi)	To simulate the waveform, click on File -> New -> University Program VWF.
vii)	In the Simulation Waveform Editor, click on Edit -> Insert -> Insert Node or Bus. Open the Node Finder window by clicking on ‘Node Finder’.
viii)	Select the appropriate filters and click on List to list down the signals and I/O to be shown in the simulation. Then close the windows clicking on OK.
ix)	Click on the “Run Functional Simulation” icon to begin simulating.  

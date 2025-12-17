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
  
## 📊 __Expected Output Waveform__  
<img width="1919" height="528" alt="Screenshot 2025-12-17 223409" src="https://github.com/user-attachments/assets/83e9f705-c1b5-475f-adab-99ca322e8e9c" />  
When input password 'i' corresponds to the default correct password 6666, the present state gradually transitions from the states S0 to S1, S1 to S2, S2 to S3, S3 to S4, before finally returning to S0. The green LED lights up when PS reaches state S4.  

<img width="1919" height="527" alt="Screenshot 2025-12-17 223440" src="https://github.com/user-attachments/assets/a29bb310-c8d6-468d-92df-21a28b76b514" />  
When the input password 'i’ is 6656, the present state gradually transitions from the states S0 to S1, S1 to S2, but then instead of progressing to S3, S2 transitions to S6 detecting a value in the input that is different from the correct digit. Then it returns to S0. The red LED lights up when PS reaches state S6.  
  
<img width="1919" height="526" alt="Screenshot 2025-12-17 223451" src="https://github.com/user-attachments/assets/2dbd4732-99a9-403f-8c83-dc62c0571a9d" />  
When mode = 1, the present state transitions from S3 to S5 instead of S4 while the green LED gets lit.  
  













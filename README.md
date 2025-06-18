# Tyre Pressure Monitoring System  

## Description  
A CAN-based ECU simulation project integrating **Engine ECU, TPMS ECU, and HMI ECU**, utilizing **17 messages and 17 signals** for real-time monitoring and control. The project is divided into four phases: **Simulation, Database Creation, Panel Design, and CAPL Scripting**—ensuring seamless interaction between modules.

## How does it work?

![image](https://github.com/user-attachments/assets/950cafb4-12a3-4ac0-ab75-b5268334516f)
Source: https://virginiaweathermap.pages.dev/new-ypkimb-understanding-and-utilizing-tire-pressure-monitoring-system-tpms-data-visualization-bkpicc-pics/

A typical visualization displays each tire’s pressure individually, often using a graphical representation such as a tire icon or a numerical value within a designated area corresponding to a specific wheel position. Color-coding is frequently employed to highlight deviations from the recommended pressure. Green might indicate optimal pressure, orange a slightly low pressure, and red a critically low pressure. Some systems incorporate additional data points, such as temperature readings, which can further refine the analysis. The visual layout ensures quick identification of any pressure discrepancies across the four tires.

## Project Overview

![ScreenRecording2025-06-18020142-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/4c5876bb-a712-4a59-ad22-e892b5be886b)


The **Tyre Pressure Monitoring System (TPMS)** activates upon engine startup, utilizing the **Engine ECU** to wake up and read tyre pressures from TPMS across all four wheels:  
- **FLW** – Front Left Wheel  
- **FRW** – Front Right Wheel  
- **RLW** – Rear Left Wheel  
- **RRW** – Rear Right Wheel  

These pressure readings are processed through a control function, which evaluates the values and displays results on the **HMI screen**. Color-coded indicators provide easy visualization:  
- 🟢 **Green** – Optimal pressure  
- 🟠 **Orange** – Medium pressure  
- 🔴 **Red** – Critically low pressure  

![Screenshot 2025-06-18 021549](https://github.com/user-attachments/assets/1201c148-e1bb-49b0-b985-900f10eabaf9)

## Project Phases  
### 1. Simulation  

![Screenshot 2025-06-18 014803](https://github.com/user-attachments/assets/0f7899fb-d237-4949-9441-7595d08efc13)

![Screenshot 2025-06-18 014819](https://github.com/user-attachments/assets/f101acbb-066d-425e-a868-01ba9b4524f5)



- Configure **network nodes** to integrate the required ECUs for accurate simulation.  
- Load the relevant **DBC (database file)** once created, ensuring correct signal transmission.  
- Define the **message flow** between ECUs.  

### 2. Database Creation  

![Screenshot 2025-06-17 232248](https://github.com/user-attachments/assets/c2c11007-99c6-499c-af11-f2c935f4be1f)

- Develop a **new DBC file** containing all necessary ECUs, messages, signals, and environment variables.  
- Define **signal transmission and reception** mechanisms between ECUs.  
- Establish **communication rules** for seamless data exchange.  

### 3. Panel Creation  

![Screenshot 2025-06-18 021853](https://github.com/user-attachments/assets/28cd08ec-2517-4cb4-845a-062c0b273382)

![Screenshot 2025-06-18 021946](https://github.com/user-attachments/assets/f25c8454-135e-49da-815a-25f02256b422)


- Design a **user interface** for inputting values and visualizing real-time system behavior.  
- Display **sensor data** and ECU interactions through an organized panel.  
- Ensure **functional validation** through user controls and feedback visualization.  

### 4. CAPL Script  

![Screenshot 2025-06-18 014613](https://github.com/user-attachments/assets/066d3dae-3144-4ffe-b134-862ee0d757af)


- Define **variables** and **logic** for managing input and output processes.  
- Utilize **environment variables** to store and process user inputs dynamically.  
- Implement **control logic** to transmit processed signals onto the **CAN bus** for accurate monitoring.  

## How to Run the Project  
1. **Install Vector CANoe** (Ensure you have the required version).  
2. **Load the project files** into CANoe.  
3. **Start the simulation** to activate the TPMS functionality.  
4. **Interact via the panel** and observe tyre pressure readings and ECU responses.  

## License  
This project is **open-source** and can be used for learning and development purposes.  

---

Feel free to modify or expand based on additional details you wish to include! 🚀

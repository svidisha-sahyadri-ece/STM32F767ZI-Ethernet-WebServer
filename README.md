# STM32F767ZI Ethernet Web Server

## About Me

**Name:** S VIDISHA

**College:** Sahyadri College of Engineering and Management

**Email ID:** vidisha.ec23@sahyadri.edu.in

### LinkedIn

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](YOUR_LINKEDIN_LINK)

---

## About the Project

This project demonstrates the implementation of an **Embedded Ethernet Web Server** using the **STM32F767ZI Nucleo-144** development board.

The web server is developed using the **LwIP TCP/IP stack** and **HTTP Server middleware** provided by STM32CubeMX. A browser-based graphical interface allows users to control the onboard LEDs using the **Common Gateway Interface (CGI)**.

The project covers the complete workflow from Ethernet configuration to serving HTML pages and processing HTTP requests.

---

## Features

- Embedded HTTP Server
- Ethernet Communication using LAN8742 PHY
- Browser-Based LED Control
- CGI (Common Gateway Interface)
- Static IP Configuration
- HTML Web Interface
- Embedded File System using Perl (makefsdata)
- Developed using STM32CubeIDE & STM32CubeMX

---

## Hardware Used

| Component | Description |
|-----------|-------------|
| STM32F767ZI Nucleo-144 | Development Board |
| LAN8742 PHY | Ethernet Interface |
| Ethernet Cable | Network Connection |
| Router | Local Network |
| Laptop/PC | Web Browser |

---

## Software Used

- STM32CubeIDE
- STM32CubeMX
- LwIP Middleware
- Embedded C
- Perl
- HTML & CSS

---

## Project Workflow

```
Browser
        │
HTTP Request
        │
Router
        │
STM32F767ZI
        │
LwIP Stack
        │
HTTP Server
        │
CGI Handler
        │
GPIO
        │
LED Control
```

---

<details>

<summary>Task 1 - STM32CubeIDE Project Creation</summary>

## Step 1 - Create a New STM32 Project

- Open STM32CubeIDE
- Create a new STM32 Project
- Select **STM32F767ZI Nucleo-144**
- Finish project creation

### Project Screenshot

(Add Screenshot)

</details>

---

<details>

<summary>Task 2 - Ethernet Configuration</summary>

## Configure Ethernet Peripheral

Enable

- ETH Peripheral
- RMII Mode

Configure Ethernet Pins

| Pin | Function |
|------|----------|
| PA1 | REF_CLK |
| PA2 | MDIO |
| PC1 | MDC |
| PA7 | CRS_DV |
| PC4 | RXD0 |
| PC5 | RXD1 |
| PG11 | TX_EN |
| PG13 | TXD0 |
| PB13 | TXD1 |

### CubeMX Screenshot

(Add Screenshot)

</details>

---

<details>

<summary>Task 3 - LwIP Middleware Configuration</summary>

Enable

- LwIP Middleware
- LAN8742 PHY
- Static IP Address

Configure

- IP Address
- Gateway
- Subnet Mask

### Screenshot

(Add Screenshot)

</details>

---

<details>

<summary>Task 4 - HTTP Server Configuration</summary>

Enable

- HTTP Server
- CGI Support

The HTTP server allows the STM32 board to host web pages accessible through any browser connected to the same network.

### Screenshot

(Add Screenshot)

</details>

---

<details>

<summary>Task 5 - GPIO Configuration</summary>

Configure the onboard LEDs as GPIO Outputs.

| GPIO | LED |
|------|-----|
| PB0 | Green |
| PB7 | Blue |
| PB14 | Red |

### Screenshot

(Add Screenshot)

</details>

---

<details>

<summary>Task 6 - HTML User Interface</summary>

A responsive HTML interface was created to allow users to control the onboard LEDs through a web browser.

Features

- Green LED Control
- Blue LED Control
- Red LED Control
- Submit Button

### Webpage

(Add Screenshot)

</details>

---

<details>

<summary>Task 7 - CGI Implementation</summary>

The CGI Handler receives HTTP GET requests from the browser and updates the LED states.

Example Request

```
LEDControl.cgi?green=ON&blue=OFF&red=ON
```

The handler parses each parameter and controls the GPIO pins using STM32 HAL functions.

</details>

---

<details>

<summary>Task 8 - Embedded Filesystem Generation</summary>

The HTML pages were converted into embedded C arrays using the **makefsdata.pl** Perl script.

Generated Files

- fsdata.c
- fsdata_custom.c

These files were added to the HTTP server directory so the web pages could be served directly from Flash memory.

</details>

---

<details>

<summary>Task 9 - Testing</summary>

### Build

Compile the project using STM32CubeIDE.

### Flash

Flash the firmware using ST-LINK.

### Connect

- Connect STM32 to the router
- Connect the PC to the same network

Open

```
http://192.168.0.150
```

The browser loads the embedded webpage where the LEDs can be controlled remotely.

### Output

(Add Browser Screenshot)

(Add Board Screenshot)

</details>

---

## Folder Structure

```
STM32F767ZI-Ethernet-WebServer
│
├── Core
├── Drivers
├── Middlewares
├── LWIP
├── HTML
├── README.md
└── STM32F767ZI.ioc
```

---

## Learning Outcomes

- STM32 Ethernet Peripheral Configuration
- LwIP TCP/IP Stack
- HTTP Protocol
- Common Gateway Interface (CGI)
- Embedded Web Server Development
- STM32CubeMX
- STM32CubeIDE
- HTML Integration
- Embedded File System
- GPIO Control through HTTP

---


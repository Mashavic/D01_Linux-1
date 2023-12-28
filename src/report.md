## Part 1. Installation of the OS
1. Check Ubuntu version by running the command \
  `cat /etc/issue`

2. Add a screenshot of the command output to the report.

![](./image/Part1/P_1.png)

## Part 2. Creating a user
1. Add a screenshot of command call to create user.

![](./image/Part2/P_2_1.png)

2. The new user must be in the output of the command: \
  `cat /etc/passwd`
  
3. Add a screenshot of the command output.

![](./image/Part2/P_2_2.png)

## Part 3. Setting up the OS network
1. Set the machine name as user-1
         
- sudo vim /etc/hostname
- sudo vim /etc/hosts
- sudo reboot        
   
![](./image/Part3/P_3_1_1.png)  ![](./image/Part3/P_3_1_2.png)  

2. Set the time zone corresponding to your current location.

![](./image/Part3/P_3_2_1.png) ![](./image/Part3/P_3_2_2.png)

3. Output the names of the network interfaces using a console command.

- sudo apt install net-tools

![](./image/Part3/P_3_3.png)

- lo (loopback device) – виртуальный интерфейс, присутствующий по умолчанию в любом Linux. Он используется для отладки сетевых программ и запуска серверных приложений на локальной машине. С этим интерфейсом всегда связан адрес 127.0.0.1. У него есть dns-имя – localhost.

4. Use the console command to get the ip address of the device you are working on from the DHCP server.

![](./image/Part3/P_3_4.png)

- Протокол динамической конфигурации узлов (Dynamic Host Configuration Protocol, DHCP) — это сетевой протокол, используемый для автоматического получения узлами IP-адресов и сетевой конфигурации с сервера.

5. Define and display the external ip address of the gateway (ip) and the internal IP address of the gateway, aka default ip address (gw).

* внешний ip-адрес шлюза (ip):    

![](./image/Part3/P_3_5_1.png)

* внутренний IP-адрес шлюза:    

![](./image/Part3/P_3_5_2.png)

6. Set static (manually set, not received from DHCP server) ip, gw, dns settings (use public DNS servers, e.g. 1.1.1.1 or 8.8.8.8).

- sudo vim /etc/netplan/*.yaml

![](./image/Part3/P_3_6_1.png) ![](./image/Part3/P_3_6_2.png)  

7. Reboot the virtual machine. Make sure that the static network settings (ip, gw, dns) correspond to those set in the previous point.

- reboot

![](./image/Part3/P_3_7_1.png)

## Part 4. OS Update
1. Update the system packages to the latest version

- sudo apt update
- sudo apt dist-upgrade
- sudo reboot

![](./image/Part4/P_4_1_1.png)

![](./image/Part4/P_4_1_2.png)

## Part 5. Using the **sudo** command

1. ##### Allow user created in [Part 2](#part-2-creating-a-user) to execute sudo command.

- sudo vim /etc/hostname
- sudo vim /etc/hosts
- sudo reboot 

![](./image/Part4/P_5_1_1.png)

![](./image/Part4/P_5_1_2.png)
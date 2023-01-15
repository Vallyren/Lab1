# Lab1
## Lab - Configure Administrative Roles
### Topology
##### ![image](https://user-images.githubusercontent.com/122459067/212534391-d0081029-13e9-4637-83f1-b3109a0ac70b.png)
###	Addressing Table
##### ![image](https://user-images.githubusercontent.com/122459067/212534584-46317399-8825-4b77-aca6-481ba25d7d11.png)
### Objectives
#### Part 1: Configure Basic Device Settings
#####	Cable the network as shown in the topology.
### ![topology](https://user-images.githubusercontent.com/122459067/212535156-368f0ca3-750a-44e8-bfd9-2b7d30a213bb.png)
#####	Configure basic IP addressing for routers and PCs.
### R1
![2023-01-15_13-50-54](https://user-images.githubusercontent.com/122459067/212536475-ffbcd572-c630-407f-b358-39bf2d81f4a9.png)
### [R1_startup-config.txt](https://github.com/Vallyren/Lab1/blob/main/R1_startup-config.txt)
### R2
![2023-01-15_13-52-28](https://user-images.githubusercontent.com/122459067/212536542-e706a1b0-b516-4616-b0b7-3d598fbd62ec.png)
### [R2_startup-config.txt](https://github.com/Vallyren/Lab1/blob/main/R2_startup-config.txt)
### R3
![2023-01-15_13-54-07](https://user-images.githubusercontent.com/122459067/212536594-ff5a852b-a1c2-4e1d-8d07-717fdb316714.png)
### [R3_startup-config.txt](https://github.com/Vallyren/Lab1/blob/main/R3_startup-config.txt)
#####	Configure OSPF routing.
### R1
![2023-01-15_13-58-46](https://user-images.githubusercontent.com/122459067/212536927-34162694-9b13-48b3-8462-99b00e84f2f8.png)
### R2
![2023-01-15_14-03-55](https://user-images.githubusercontent.com/122459067/212537007-f0d11f69-dad6-49f9-b6c2-6e6166a00dce.png)
### R3
![2023-01-15_14-05-15](https://user-images.githubusercontent.com/122459067/212537091-9618d412-f2f2-4098-9ef3-0759b51783ac.png)
##	Configure PC hosts.
### PC-A
![2023-01-15_14-11-20](https://user-images.githubusercontent.com/122459067/212537325-0e24290f-20dd-492b-9d94-c0201ccbfc9e.png)
### PC-C
![2023-01-15_14-12-21](https://user-images.githubusercontent.com/122459067/212537346-670d32e0-f764-41ae-a56e-0f78f7294f6a.png)
#####	Verify connectivity between hosts and routers.
### a.	Ping from R1 to R3.
![2023-01-15_14-14-16](https://user-images.githubusercontent.com/122459067/212537432-938e0ff4-487a-4a39-9d29-daaf74f69b5c.png)
### b.  Ping from PC-A, on the R1 LAN, to PC-C, on the R3 LAN
![2023-01-15_11-12-18](https://user-images.githubusercontent.com/122459067/212537573-4ff95671-7c6f-4e63-b03c-704f71f2f497.png)
![2023-01-15_11-13-03 (2)](https://user-images.githubusercontent.com/122459067/212537595-33f0ad31-6882-4868-b1d2-b7bf54e57cc7.png)
#### Part 2: Configure Administrative Roles
#####	Create multiple role views and grant varying privileges.
##### A privileged EXEC mode password is required to access the root view. The password cisco12345 is used in this example
![2023-01-15_14-23-34](https://user-images.githubusercontent.com/122459067/212537825-4b0a2713-1fd2-46dc-9328-55fc852a7fcc.png)
![2023-01-15_14-37-33](https://user-images.githubusercontent.com/122459067/212538373-f409458e-e25b-4d3e-8bd8-eae8fc797d82.png)
##### The admin1 user is the top-level user below root that is allowed to access this router. It has the most authority. The admin1 user can use all show, config, and debug commands. 
![2023-01-15_14-27-37](https://user-images.githubusercontent.com/122459067/212537999-0995bc01-5280-470c-a781-9966e633c94a.png)
![2023-01-15_14-31-02](https://user-images.githubusercontent.com/122459067/212538140-bb22c5b3-1751-4a6d-8d51-aaf4e1416eac.png)
![2023-01-15_14-39-29](https://user-images.githubusercontent.com/122459067/212538449-7ad7130d-ffdd-4375-b0c1-375ca32e9e5b.png)
![2023-01-15_14-40-42](https://user-images.githubusercontent.com/122459067/212538492-803aebed-230e-44d6-8c14-02bdb9e876eb.png)
### What is missing from the list of admin2 commands that is present in the admin1 commands?
##### configure    Enter configuration mode and debug        Debugging functions (see also 'undebug')
### The tech user typically installs end-user devices and cabling. Tech users are only allowed to use selected show commands.
![2023-01-15_14-34-29](https://user-images.githubusercontent.com/122459067/212538291-15f7ecbf-ce13-48fa-aa11-1e6fdc1d9b81.png)
![2023-01-15_14-41-55](https://user-images.githubusercontent.com/122459067/212538563-e0f2bc98-4cbb-4244-819a-ccc30b40e324.png)
### i.	Issue the show ip interface brief command.
### j.	Issue the show ip route command.
### k.	Return to root view with the enable view command.
### l.	Issue the show run command to see the views you created.
![2023-01-15_14-48-15](https://user-images.githubusercontent.com/122459067/212538874-f9f16a7f-e594-4cea-be65-eb2ec1e9dcad.png)
![2023-01-15_14-53-48](https://user-images.githubusercontent.com/122459067/212539083-320fc894-f9e4-4d30-9614-7d813aac4e14.png)
### Save the running configuration to the startup configuration from the privileged EXEC prompt.
### [R1_startup-config2.txt](https://github.com/Vallyren/Lab1/files/10420073/R1_startup-config2.txt)
### [R3_startup-config2.txt](https://github.com/Vallyren/Lab1/files/10420074/R3_startup-config2.txt)

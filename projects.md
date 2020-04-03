---
layout: default
---

# University Projects

Lists of projects in chronological order from oldest to most-recent project.


### Software Praktikum (Java)

Implementation of a fully fledged turn-based game including GUI in Java. Won price for best additional feature with a fully automatic map-generation that used image processing on topographic maps fetched from Google Maps, that allowed to play your game on a realistic map of e.g. Hawaii or Greenland.


### Bachelor Thesis (C#)
My thesis [Development and Evaluation of Authentication Schemes for Mobile Virtual Reality](https://schaefer-dev.de/thesis.pdf) was about developing a novel approach to authenticate in a VR environment. This new authentication scheme was implemented in C# in Unity3D for GoogleVR (can be used e.g. on Daydream)

**Abstract of my Thesis:**
In recent years Virtual Reality has grown very quickly and found more and more use- cases. With new commercial releases of affordable mobile HMDs such as Google Day- dream, Samsung Gear VR combined with the rising potential of mobile AR glasses, the unsolved security problem for these devices grows continuously. Existing knowledge-based and biometric authentication schemes all come with critical disadvantages especially because they are usually not designed with Virtual Reality usage in mind. I implemented a novel graphical authentication scheme called "Personal Environment Authentication" specifically aimed at Virtual Reality. In this new scheme the user will authenticate herself using an ordered selection of objects in a (personal) virtual environment in form of of a 360-degree image. It offers significantly improved memorability of passwords compared to knowledge-based systems making use of the Pictorial Superiority Effect. In a study I was able to additionally confirm significantly improved user-experience and security of this scheme compared to the prominent solutions "PIN" and "Android Pattern" authentication.


### Plagiarism detection tool (Python/JavaScript/PHP/HTML)

Developed per request for professor at Saarland University. The tool is now successfully used to detect plagiarism cases among students and supports up to 4000 submissions with up to 1000 lines each and checks every submission pair for possible plagiarism cases. Obvious plagiarism cases are highlighted and the professor is automatically notified with a human readable overview of why the set of submissions are obvious plagiarism cases including a colored mapping of copied parts of the code. The tool is completely robust against many options to easily bypass most ordinary plagiarism detection tools for both python and C code (variable renaming, moving of code blocks etc.).


### PINTOS Operating System (C)

Implementation of the Pintos Operating System for the x86 architecture. We implemented: Kernel threads, loading and running of user-specified programs with scheduling of these programs and Virtual Memory. Last iteration of the project included a filesystem implementation, including writing Swapfiles with intelligent paging to avoid Disk access as much as possible.


### Embedded Systems Project (C/C++)

In this project groups of 3 students each developed a strategy for two different kinds of robots every group had access to. To solve problems that were important to win the competition that would take place in the end of the semester, it was essential to write very efficient and low-memory footprint code, as computational resources on both robots very only very limited. The robots used an ATMEGA328 AVR controller and could communicate using a nRF24L01+ RF module. Efficient communication including acknowledgements were essential to balance the work between both robots, as one of them was loaded with sensors, while its bigger brother was basically 'blind'. In early stages of development, a Simulink Model we built, that implemented a simplified version of out tactic already indicated a very big problem: keeping track of out position on the map was significantly harder than we expected, as Drift was very large on such lightweight robots. Additionally we had to make sure that we reliably recognize and predict collisions with other robots, which was another scenario which could significantly impact out concrete position in the arena.

At a later date, I might add a detailed description of our implemented tactic and important implementation details here.

While it was quite challenging to implement these Embedded Systems from scratch, we learned a lot about reading Datasheets, Communication Protocols and Sensor usage (particularly handling high noise).

Our team ended up winning the competition between all student-teams at the end of the semester.


### Hands on Networking Project LLDPA Agent (Python)

In this small project I implemented a LLDPA agent which is able to announce itself by sending LLDP messages to the network on the Link Layer. Additionally the agent parses all LLDP messages that are sent to one of the LLDP multicast addresses of the network. I also implemented a set of tests to verify the agents behaviour and robustness against e.g. invalid TLVs. Wireshark can be used to listen to network traffic and observe the correct behaviour of the agent.


### Hands on Networking Project Multimedia Codec (Python)

In this small project I implemented encoding and decoding functions suited to send multimedia files over a noisy channel in an efficient way. The goal of this codec is to be able to correct errors that are introduced by the communication channel in a sufficiently fast way which also does not require too much redudancy overhead. The channel introduced randomized bit flips, which could also occur in bursts. To solve this problem I essentially implemented a Hamming Code with interleaving to be able to handle the error correction for burst of errors better. My implementation was able to correct 100% of all errors (including bursts) on all provided grading-networks, with a redundancy of only 100% (passing criterion was 300%).



### Research Assistant Project

Implementation of a Rust Library that communicates over a USB interface with a Arduino board which is mounted on a fairly large 4-wheeled robot. The implemented Rust library is running on a Intel NUC that is built on top of the robot chassis. Additionally the NUC is connected to a Lidar which is used to scan and reconstruct the room surrounding the robot, which allows for safe navigation and avoiding of obstacles.



# Freetime Projects

- Teaching myself Python
- Teaching myself Rust
- Home Network Setup implementing QoS with Traffic Analysis and DPI
- Home-server running DNS server and VPN-tunnel (to get safe and ad-free browsing everywhere in the world)
- Managing my [dotfiles](https://github.com/schaefer-dev/dotfiles) and improving workflows
- Project Euler
- This website :)

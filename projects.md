---
layout: default
title: "Daniel Schäfer | Projects and Courses"
description: "Descriptions for various projects I have worked at in my freetime and during university. Inclusing course work."
---

# Work projects

List of projects for my time at semvox in reverse chronological order, starting with my most-recent projects.


### geni:OS genAI (Python)

As Lead Software Architect for the next generation assistant system for the Volkswagen Group, I own the technical vision and the key architectural decisions of the genAI solution. The role spans system design across loud boundaries, hands-on development of core LLM agents and capabilities, and the definition of technical solutions for safety, privacy, latency, and reliability under in-vehicle constraints. I maintain architecture documentation and decision records to keep cross-functional teams aligned and to make trade-offs transparent. I act as the primary technical counterpart for internal stakeholders and external partners and I routinely explore new concepts to determine which novel concepts are worth integrating already, versus which should remain in research/exploration phase. The focus is on building a sustainable AI-driven platform rather than a collection of demos, which means actively balancing experimentation and predictable delivery and setting clear deprecation and migration paths as the technology evolves.


### Automotive LLM Demonstrator (Python)

I led the development of a proof of concept that showed what a deep LLM integration can contribute to the in-car assistant experience for all VW brands. The demonstrator ran on production hardware and was integrated into the existing vehicle architecture. Beyond building the full featureset, I established automated testing and regression analysis for llm-agent behavior to catch regressions in prompts, tools, and retrieval logic early. The PoC significantly exceeded expectations of internal and external stakeholders and it directly led to successful customer acquisition. Semvox is now fully committed to this new product generation, now called geni:OS genAI, that builds on top of the findings in this PoC.


### Automated Testing Framework (Java)

I designed and implemented an end to end test framework for automotive hardware prototypes from the ground up. The system automates the complete loop from injecting generated audio to simulate driver utterances to validating the speech output of the assistant, while hiding the complexity of fragile lab setups and prototype hardware. Over time the framework replaced over 30 percent of manual QA with automated testruns and it covered key integration scenarios that previously required significant coordination effort and human involvement. Beyond raw automation, the framework significantly improved repeatability and reduced the risk of hardware mishandling during tests. After stabilizing the platform and implementing all key features, I handed it over to a dedicated QA team. I still supported roadmap and design decisions for another year to ensure a clean transition. The main challenge throughout was to keep the framework reliable across frequent hardware and software changes.


### Cybersecurity Certification (ISO 21434)

I contributed to and helped establish the topic of cybersecurity throughout our internal product development lifecycle with the explicit goal of achieving an eventual ISO 21434 certification. My technical responsibilities included Threat Analysis and Risk Assessment for our software framework, triage and mitigation planning for CVE findings, and the definition of development and release practices that make security considerations routine rather than an exception. The work resulted in a successful ISO 21434 certification of our product and it established a path for continuous security maintenance. The pragmatic trade-off was to design processes that the teams would actually follow under real-world project pressure and to keep documentation precise and concise so it supports engineering teams instead of slowing it down.

# University Projects

Lists of projects in chronological order from my earliest to my most-recent projects.


### Master Thesis Project (Swift)

My master thesis was written in the field of program synthesis which is a concept used to construct a program that solves a given formal specification automatically. My thesis aims to enhance existing approaches by allowing the use of higher-level semantics to be used as part of these specifications. This decreases not only the risk of human-error in providing the intended formal specification but also simplifies the process overall. My proposed algorithm is implemented entirely in object orriented Swift code. I may discuss details of my concept or implementation in a private conversation, however I would like to keep this website "spoiler-free" regarding the concent of my thesis until it is graded :)


### Research Assistant Project (Rust)

Implementation of a Rust Library that communicates over a USB interface with a Arduino board which is mounted on a fairly large 4-wheeled robot. The implemented Rust library is running on a Intel NUC that is built on top of the robot chassis. Additionally the NUC is connected to a Lidar which is used to scan and reconstruct the room surrounding the robot, which allows for safe navigation and avoiding of obstacles.


### Hands on Networking Project Multimedia Codec (Python)

In this small project I implemented encoding and decoding functions suited to send multimedia files over a noisy channel in an efficient way. The goal of this codec is to be able to correct errors that are introduced by the communication channel in a sufficiently fast way which also does not require too much redudancy overhead. The channel introduced randomized bit flips, which could also occur in bursts. To solve this problem I essentially implemented a Hamming Code with interleaving to be able to handle the error correction for burst of errors better. My implementation was able to correct 100% of all errors (including bursts) on all provided grading-networks, with a redundancy of only 100% (passing criterion was 300%).


### Hands on Networking Project LLDPA Agent (Python)

In this small project I implemented a LLDPA agent which is able to announce itself by sending LLDP messages to the network on the Link Layer. Additionally the agent parses all LLDP messages that are sent to one of the LLDP multicast addresses of the network. I also implemented a set of tests to verify the agents behaviour and robustness against e.g. invalid TLVs. Wireshark can be used to listen to network traffic and observe the correct behaviour of the agent.


### Embedded Systems Project (C/C++)

In this project groups of 3 students each developed a strategy for two different kinds of robots every group had access to. To solve problems that were important to win the competition that would take place in the end of the semester, it was essential to write very efficient and low-memory footprint code, as computational resources on both robots very only very limited. The robots used an ATMEGA328 AVR controller and could communicate using a nRF24L01+ RF module. Efficient communication including acknowledgements were essential to balance the work between both robots, as one of them was loaded with sensors, while its bigger brother was basically 'blind'. In early stages of development, a Simulink Model we built, that implemented a simplified version of out tactic already indicated a very big problem: keeping track of out position on the map was significantly harder than we expected, as Drift was very large on such lightweight robots. Additionally we had to make sure that we reliably recognize and predict collisions with other robots, which was another scenario which could significantly impact out concrete position in the arena.

At a later date, I might add a detailed description of our implemented tactic and important implementation details here.

While it was quite challenging to implement these Embedded Systems from scratch, we learned a lot about reading Datasheets, Communication Protocols and Sensor usage (particularly handling high noise).

Our team ended up winning the competition between all student-teams at the end of the semester.


### PINTOS Operating System (C)

Implementation of the Pintos Operating System for the x86 architecture. We implemented: Kernel threads, loading and running of user-specified programs with scheduling of these programs and Virtual Memory. Last iteration of the project included a filesystem implementation, including writing Swapfiles with intelligent paging to avoid Disk access as much as possible.


### Plagiarism detection tool (Python/JavaScript/PHP/HTML)

Developed per request for professor at Saarland University. The tool is now successfully used to detect plagiarism cases among students and supports up to 4000 submissions with up to 1000 lines each and checks every submission pair for possible plagiarism cases. Obvious plagiarism cases are highlighted and the professor is automatically notified with a human readable overview of why the set of submissions are obvious plagiarism cases including a colored mapping of copied parts of the code. The tool is completely robust against many options to easily bypass most ordinary plagiarism detection tools for both python and C code (variable renaming, moving of code blocks etc.).

[Project Video](https://youtu.be/Lcn0QEfDHL4)


### Bachelor Thesis (C#)
My thesis [Development and Evaluation of Authentication Schemes for Mobile Virtual Reality](https://schaefer-dev.de/thesis.pdf) was about developing a novel approach to authenticate in a VR environment. This new authentication scheme was implemented in C# in Unity3D for GoogleVR (can be used e.g. on Daydream)

**Abstract of my Thesis:**
In recent years Virtual Reality has grown very quickly and found more and more use- cases. With new commercial releases of affordable mobile HMDs such as Google Day- dream, Samsung Gear VR combined with the rising potential of mobile AR glasses, the unsolved security problem for these devices grows continuously. Existing knowledge-based and biometric authentication schemes all come with critical disadvantages especially because they are usually not designed with Virtual Reality usage in mind. I implemented a novel graphical authentication scheme called "Personal Environment Authentication" specifically aimed at Virtual Reality. In this new scheme the user will authenticate herself using an ordered selection of objects in a (personal) virtual environment in form of of a 360-degree image. It offers significantly improved memorability of passwords compared to knowledge-based systems making use of the Pictorial Superiority Effect. In a study I was able to additionally confirm significantly improved user-experience and security of this scheme compared to the prominent solutions "PIN" and "Android Pattern" authentication.


### Software Praktikum (Java)

Implementation of a fully fledged turn-based game including GUI in Java. Won price for best additional feature with a fully automatic map-generation that used image processing on topographic maps fetched from Google Maps, that allowed to play your game on a realistic map of e.g. Hawaii or Greenland.



# University Courses

A list of lectures I visited at during my time at Saarland University. Includes B.Sc. and M.Sc. lectures.

Year | Term | Course Description
-----|-------|--------
2013 | Winter | Maths for Computer Science I
2014 | Summer | Maths for Computer Science II
2014 | Winter | Maths for Computer Science III
2013 | Winter | Programming I (functional Programming in ML)
2014 | Summer | Programming II (MIPS, C, Java)
2014 | Summer | System Architecture
2014 | Winter | Theoretical Computer Science
2014 | Winter | Algorithms and Data Structures
2014 | Winter | Software Project (Design Practicum)
2015 | Summer | Concurrent Programming
2015 | Summer | Information Systems (Databases)
2013 | Winter | Perspectives of Computer Science
2015 | Summer | Hacking Seminar
2015 | Summer | Artificial Intelligence
2015 | Winter | Introduction to media computer science
2016 | Summer | Security
2016 | Summer | Software Development in HCI
2016 | Summer | High-Level Computer Vision (Convolutional Neural Networks)
2016 | Winter | Speech Technology - Pattern and Speech Recognition
2016 | Winter | Law of Cybersecurity
2017 | Summer | Programming for engineers
2017 | Summer | Human Computer Interactions
2017 | Summer | Software Engineering
2017 | Summer | Ethics for Nerds
2017 | Winter | Operating Systems
2017 | Winter | Automatic Planning
2018 | Summer | Cryptography
2018 | Summer | Embedded Systems
2018 | Summer | Web Security
2018 | Winter  | Automata, Games, Verification
2018 | Winter | Selected Topics in Formal Methods for Security
2019 | Summer | Hands on Networking
 | |
2013 | Winter | Introduction to Computational linguistics
2014 | Winter | Introduction to Semantics
2015 | Winter | Investing
2015 | Winter | Game Theory
2016 | Winter | Business Finance



# Freetime Projects

- Teaching myself Python
- Teaching myself Rust
- Teaching myself Swift
- Custom ATMega32U4 Controller installed in Keyboard to support [QMK Firmware](https://github.com/schaefer-dev/qmk_firmware) setup to implement fancy features like mouse-control, tap-modifiers and more :)
- Home Network Setup implementing QoS with Traffic Analysis and DPI
- Home-server running DNS server and VPN-tunnel (to get safe and ad-free browsing everywhere in the world)
- Home-server running backup and file servers to manage family documents and keep family photo library up to date
- Running my own Hackintosh for 4+ years
- Managing my [dotfiles](https://github.com/schaefer-dev/dotfiles) and improving workflows
- Geeksforgeeks.org and leetcode challenges
- Project Euler
- This website :)
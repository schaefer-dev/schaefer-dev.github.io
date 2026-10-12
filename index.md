---
layout: default
title: "Daniel Schäfer | Developer & passionate Learner"
description: "A portfolio targeted at people who want to find out what I've been up to in recent years. Includes a detailed description of projects and my university career and a very brief outlook of what I've been up to since my graduation."
---

# About Myself

<img class="profile-picture" src="me.jpg">

Hi! My name is Daniel and I am Head of Software Architecture & Engineering at [semvox](https://www.semvox.de/), a 100% subsidiary of CARIAD SE as of May 2023. I finished my masters in Computer Science at University of Saarland, Saarbruecken in Oktober of 2020 with an average grade of 1.5. My thesis was about synthesis of KLTL specifications and supported by the [Reactive Systems Group](https://www.react.uni-saarland.de).

Currently I lead one of the two Software Architecture & Engineering teams in semvox's Applied Research & Development department, while continuing to act as Lead Software Architect for our genAI product generation, geni:OS genAI.

I used to be a quite unorganized and spontaneous person, but in late 2018 I read about the principle of "Getting Things Done" by David Allen. Nowadays there is no way I leave the house without a way of putting down my thoughts (usually ends up being phone or laptop) which helps me to organize and plan my week properly. This step forward had a significant impact not only on my overall enjoyment of working but also resulted in me being way more productive in the same amount of time.

In 2021 lockdown I found a new passion: cycling and striving for improvements in the sport. During holidays I love traveling to new countries and discovering new places in nature I haven't been at before at [capturing my experiences with my camera](https://schaefer-dev.de/photos).




# My Work Experience at semvox

## 2020-2023

After graduation I started working as product Engineer at semvox. We develop a personalized smart assistant that is used by Volkswagen, Audi, Porsche and Skoda. My responsibilities early on included the development and maintenance of our internal prototype project that is used to analyze and demonstrate new feature-sets before they are being brought into production. At the same time this project is used as our demonstrator, which is used to present the strength of our Software-Framework to new potential customers.

Additionally, I was the sole developer and maintainer of an internal test framework that is used to automate end to end tests in the Volkswagen-group project for semvox. This testframework mainly automates a variety of processes on automotive hardware prototypes, which are used internally to simulate a real-world car. The goal of this framework is to improve reliability of test results compared to manual testing and reduce the know-how that is required to work on the sensitive prototype hardware. Currently, around 40% of all in-car testing has been replaced with automated tests, performed by the testframework I developed, relieving a lot of pressure from the QA department.

I have since handed over this project to a new team inside the QA department that is able to focus all its effort into improving the framework further while I tackle new challenges. For another year I was still involved in design-decisions and roadmap planning.

After my time developing the test framework, a significant portion of my time has been spent working towards a cyber security management system certification in form of ISO 21434 for semvox. I was mainly involved in establishing new processes to cover cyber security related subjects from the design phase, through the development cycle, until product releases and deployments.
Analyzing the impact of CVE findings in our product and determining the best mitigation path for those vulnerabilities is still part of my day to day work.
I am responsible for the technical risk assessment and threat analysis for our software framework.

Another focus of mine has been the analysis of performance bottlenecks in in our automotive project with the Volkswagen-group. I was able to discover and implement crucial improvements to performance, memory management and overall system stability in the process.

During this timeframe at work I write almost exclusively Java code.


## 2024-2025

In early 2024, I took on the role of workstream lead for Embedded LLM Development at semvox, focusing on exploring efficient large language model solutions tailored to the hardware constraints within the Volkswagen Group. Following an internal reprioritization, driven by specific customer requirements and timelines, my responsibilities shifted to leading the PNP workstream. I was responsible for the technical development and evaluation of 14 specialized LLM agents, covering diverse domains such as current and historical weather data, financial market information, and news integration, specifically tailored for integration in Volkswagen projects.

One of my most notable achievements in 2024 was the development of the \"GDA Embedded Demo\". This demonstrator significantly exceeded initial expectations of internal and  external stakeholders, positioning semvox as a leading-edge integrator of LLM technologies within the VW assistance systems. Additionally, I developed numerous demonstrable features and delivered key insights on agentic concepts and novel automated testing strategies. Over time, this demonstrator has developed into semvox new product generation: geni:OS genAI.

Since January 2025, I have the role of Lead Software Architect for this new product generation. I have full technical responsibility for the architectural direction of the genAI solution, including overseeing integration within Volkswagen customer projects. I act as the primary technical contact for solution concepts throughout the genAI ecosystem, ensuring clear communication and effective coordination with external stakeholders and interdisciplinary teams, such as the Solutions department, CARIAD, and other stakeholders.

My responsibilities further include establishing and documenting the technical vision and making critical architecture decisions. I have created and maintained architecture documentation on Confluence to support development processes and maintain high-quality standards. Additionally, I actively contribute to software development for LLM agents and features within the genAI framework.

Throughout this period I have significantly contributed to the growth and establishment of the semvox genAI solution. From initial in-vehicle demonstrations to its current prominence as a vital project for semvox.

From early 2024 onwards, most development happened in python. However, integration into the existing embedded + cloud stack of our largest projects happened mostly in Java. 


## 2026-today

In April 2026, alongside the restructuring of semvox into a new Applied Research & Development (AR&D) department, I took on the role of **Head of Software Architecture & Engineering**. I lead one of two sister teams in this capability field and combine people leadership with technical capability ownership in a matrix organization: my team members work day to day in cross-functional workstreams and projects, while I am responsible for their development, feedback and the systematic growth of our expertise in software architecture, requirements engineering, testing, documentation and end-to-end software development. As a member of the department's steering committee, I bring feedback from my team and the workstreams into tactical and strategic decisions. I work closely with the other team lead to keep technical standards and staffing consistent across both teams.

A big part of this role is making technical responsibility and decision ownership clearer across teams. I align with project and workstream leads, represent architecture and engineering expertise toward internal stakeholders, and help the organization scale technical quality without slowing down delivery.

In parallel, I remain Lead Software Architect for geni:OS genAI. I own the big picture of the genAI stack: the genAI framework, our automated test framework for AI-driven assistants, and the surrounding developer tooling. I stay close to the integration work in customer projects so that I can derive future features and developer-experience improvements from it.

Another focus of mine is modernizing how we build software. I push AI-assisted software delivery within our genAI development: AI coding agents with repository-specific instructions, AI-supported test case creation and AI-assisted log and trace analysis. Developers stay in control of every decision. The aim is to reduce the coordination effort that comes from changes spanning code, prompts, tool definitions, tests and evaluations.

In the future I might update this website with more content related to my work. However, right now the remaining sections on this page will remain mainly focused on stuff I have worked on during my studies.


# My Computer Science Degree

My main interests at university were the fields of embedded systems and operating systems and verification of such systems. However, I intentionally visted a broad selection of courses at university to develop skills in a variety of fields.

I very much enjoy the 'challenge' of writing 'low-level' code. In my time as a student this usually resulted in me writing efficient Code in C. Recently I discovered Rust which sparked my interest a couple of times already in the past, mainly because of the strong guarantees (safe) rust code gives by design while getting reasonably close to C performance. This time I actually gave it a serious shot and so far I have been really happy with my decision.

In my free time, I like to keep myself in shape by exercising regularly at home - particularly my back is very thankful for those breaks after hours of sitting in a chair. I would consider myself very passionate about a wide variety of music and audio gear, which also helps me relax after a long day of working if im not reading a book on my Kindle. One of my favorite things to do after university is to optimize my workflow, for the tasks I am currently facing. This mainly ends up in me fine-tuning my zsh, tmux, vim or vscode configurations to solve some annoyance I encountered that day.
# EchoLink: WebRTC-based LAN Online Chat Software Platform

**Team Kind Koalas: Zhongsheng Wang, Kairui Liu, Xiaojun Xiao, Hongfei Rong, Siyu Lu, Shuzheng Mi, Jiahao Wang**

All project plans were approved by the whole group after three rounds of team discussions within Week 3.

## Introduction

With the advancement of technology and changes in work practices, instant messaging software has become a vital tool for business communication and collaboration. However, existing communication solutions typically rely on an internet connection and may not fully meet an organization's needs in terms of security, privacy protection, and cost-effectiveness. In response to these challenges, our team plans to develop a LAN online chat software platform based on WebRTC technology, EchoLink, which is specifically designed to meet the internal communication needs of small businesses.


### Motivation

Our core objective is to provide a secure and reliable internal communication platform that allows users to conduct real-time text, voice, and video communications within a LAN environment, without the need for an external internet connection. We believe such a platform will offer users the following unique values:

- High security and privacy protection: By deploying within a local area network, data does not travel through external networks, significantly enhancing data security and privacy protection.
- Low-latency communication experience: Leveraging the advantages of a LAN, the platform provides a communication experience with lower latency than traditional internet solutions, making voice and video calls smoother.
- Easy to deploy and maintain: Designed with the IT resource constraints of small businesses in mind, the solution is easy to deploy and maintain, reducing technical barriers and operational costs.


## Related Work

In response to the existing similar software & platforms in the application market, every member of our team engaged in intensive use of these tools, conducting detailed analyses and summarizing their strengths and weaknesses as follows (we only focused on functionalities that we could implement or improve, given our team's capabilities cannot be compared to an entire development team):

### Google Meet

#### Strengths:

- Seamless Integration: Google Meet's integration with Google Workspace offers a seamless workflow, facilitating easy management of schedules, emails, and documents for users.
- Usability: Its clean user interface and easy-to-understand control options allow users to quickly start or join meetings.
- Accessibility: As a browser-based solution, it enables users to join meetings without the need to download any applications, lowering the barrier to entry.
- Stable Performance: Google's vast infrastructure ensures the stability and reliability of meetings, maintaining good communication quality even under poor network conditions.

#### Areas for Improvement:

- Feature Richness: Compared to Zoom, Google Meet has room for improvement in advanced meeting features, such as breakout rooms and meeting recordings.
- Customizability: Business users may require more customization options to better integrate Meet into their internal communication systems. (This might not need to be considered in EchoLink, but it is one of its strengths.)

### Slack

#### Strengths:

- Exceptional Collaboration Features: Slack offers robust messaging and file-sharing capabilities, supports cross-team collaboration, and enhances work efficiency through channels and private messages.
- Rich Integrations: It integrates with a variety of third-party services and tools, such as Trello, GitHub, and Salesforce, making Slack a centralized communication and collaboration platform for businesses.
- Customization and Automation: Slack provides extensive customization options and bots, reducing the burden of repetitive tasks through automation processes. (The application of AI tools should not be within our development scope.)

#### Areas for Improvement:

- User Interface: For new users, Slack's user interface can seem complex, requiring a learning curve.
- Functionality for a Fee: Some of the features frequently used by businesses require purchasing a membership service for employees, which can be relatively costly. (We will attempt to implement some of these features.)

### Zoom

#### Strengths:

- High-Quality Video Meetings: Zoom is known for its high-quality video and audio meeting capabilities, supporting large-scale video conferences and webinars.
- Powerful Features: Features like breakout rooms, meeting recording, and screen sharing meet the diverse needs of users.

#### Areas for Improvement:

- Security and Privacy: Concerns about Zoom's information security are still an issue for some people. Software vulnerabilities can potentially affect users' frequency of use and intention to use. (Refer to the blog link: https://cloudsecurityalliance.org/blog/2022/03/13/an-analysis-of-the-2020-zoom-breach)
- Resource Consumption: The Zoom application may consume significant computer resources under certain circumstances, affecting the performance of other applications.

### Summary

In summarizing the advantages and issues of the aforementioned software, we plan to integrate certain functionalities into EchoLink and optimize for weaknesses:

- Security and Privacy Protection: The security and privacy issues highlighted by Zoom remind us that in designing software, security should be a primary consideration. Implementing end-to-end encryption, ensuring data transmission within the LAN, and providing transparent privacy policies are key measures to enhance user trust.

- User Interface and Experience: EchoLink will pursue a simple and intuitive design, reducing the difficulty for users to understand interaction logic and minimizing cumbersome and meaningless operation processes, to achieve the best user experience.

- Performance and Resource Consumption: Considering the potential high computer resource consumption by Zoom, the development process should focus on software performance optimization to ensure smooth operation on various hardware configurations and reduce system resource usage. (This is an aspect we hope and expect to achieve technical capability in.)

Through a comprehensive analysis of these core requirements and improvements on existing problems identified in competitive products, EchoLink aims to provide a secure and efficient internal communication solution, meeting the specific needs of small businesses in terms of data security, communication quality, and team collaboration.

## Requirements

Based on group discussions and a reasonable analysis of each individual's technology stack, we've outlined the features that our team can implement in EchoLink. We anticipate tackling some potential technical challenges through learning and problem-solving in the future development cycles. We've categorized the functionalities into four sections: Must-Haves, Should-Haves, Could-Haves, and Nice-to-Haves. (Due to word count limitations, only a brief description of the functionalities is provided here.)

### Must-Haves

- User Authentication and Management: Implement basic user registration, login, and personal information management functionalities to ensure the security and uniqueness of user identities.
- Real-Time Communication: Includes text chat and the ability to send pictures and simple files, meeting the basic communication needs of users.
- Security and Privacy Protection: Implement basic data encryption and user authentication to ensure communication security.
- Message Storage and History: Store and display user chat history, providing basic viewing and search functionalities.

### Should-Haves

- Interface Design and User Experience: An intuitive and user-friendly interface design, including clear chat windows and contact lists.
- Cross-Platform Compatibility: Support for basic versions on major operating systems (Windows, macOS) to ensure the software can be used across multiple platforms.
- Network and Performance Optimization: Ensure a smooth communication experience in a stable LAN environment.

### Could-Haves

- Voice and Video Call Functionality: Provide simple voice or video call options on top of the basic chat functionality.
- Message Notifications and Alerts: Offer notifications and alerts for new messages to enhance user experience.
- Enhanced File Transfer: Provide better file transfer progress indications and support for a wider variety of file types.

### Nice-to-Haves

- Broader Cross-Platform Support: Extend to mobile platforms such as iOS and Android to increase the software’s accessibility and convenience.
- Advanced Message Management: Offer more advanced chat history management features, such as tagging, categorization, and advanced search.
- Enhanced Network Stability: Further optimize the software to perform well in unstable network conditions, increasing user satisfaction.


## Technologies

To optimize the development process and ensure the performance and availability of EchoLink, our team has decided to make some minor adjustments to the traditional MERN stack to better meet the demands of instant communication and multimedia data transmission, while also considering future scalability and cross-platform compatibility. Below is a list of the necessary technology stack for EchoLink's development and potential optimizations we consider for the future.

#### Core Technology Stack

- **React.js**: As the core framework for front-end development, React not only provides a rich ecosystem but also excellent compatibility with real-time communication technologies like WebRTC, aiding us in quickly implementing high-quality user interfaces and interaction designs.
- **Node.js**: With its non-blocking I/O model and good support for WebRTC and WebSocket, Node.js will serve as our development platform for the signaling server, ensuring efficient and stable real-time communication.
- **Coturn**（Reference：https://github.com/coturn/coturn）: Chosen as the STUN and TURN server, Coturn is one of the most popular solutions in the network services open-source projects, capable of providing reliable NAT traversal services, crucial for enhancing the stability and accessibility of P2P video conferencing applications.

#### Advanced Technology Planning

To further enhance user experience and system performance, we plan to introduce the following advanced technologies in the later stages of the project, time and resources permitting:
- **GoLang**: Considering GoLang's excellent performance in concurrency handling and network services, especially its native concurrency model goroutine, we plan to use GoLang to refactor the signaling server as well as STUN and TURN servers, aiming for higher performance and efficiency.
- **React Native**（Reference：https://reactnative.dev/）: By using React Native, we will be able to extend the frontend web to cross-platform applications, allowing users to enjoy a seamless EchoLink experience on mobile devices.
- **WebAssembly (WASM)**（Reference：https://developer.mozilla.org/en-US/docs/WebAssembly）: Considering using WASM to implement special effects in video processing. It can efficiently perform complex computational tasks on the client-side, such as image processing, further enriching the user's interactive experience.

## Project Management

To ensure efficient progress and quality delivery of the project, we will adopt an agile development strategy to enhance teamwork, adaptability, and rapid feedback capabilities. Here are the specific details of our project management strategy:

### Scrum Framework

- **Sprint Planning**: The project will be divided into several two-week sprints. Before each sprint, we will hold planning meetings to clarify the goals and task lists for the next two weeks. Everyone is required to detail their plans for the upcoming two weeks and tag them accordingly for review at the end of the sprint.
- **Sprint Review and Retrospective**: At the end of each sprint, we will hold review meetings to showcase and evaluate the work completed during the phase. This is followed by a retrospective meeting to discuss how to improve efficiency in the next sprint. The Team Leader for each sprint will be rotated among team members to avoid the additional stress of having one person in the role for too long.

### Team Communication and Coordination

- **Communication Tools**: To ensure effective communication among team members, we will mainly use WeChat for daily message exchange and file sharing. We plan to hold full-team meetings every Monday and Friday to plan for the week's work and conduct timely reviews. We have created a Weekly Zoom Meeting room for online situations, although face-to-face meetings are generally preferred.
- **Project Management**: We have chosen GitHub KANBAN as our project management platform, tracking development tasks and bugs through Issues, using a custom tagging system for task classification, setting milestones for planning key phases, and organizing workflows with project boards.

### Version Control Strategy

- **Git and GitHub**: We will use Git for code version control and GitHub as the code repository hosting platform.
- **Branching Strategy**: We will adopt a feature branch strategy, with each new feature or fix developed in independent branches and merged back into the main branch through PRs. This ensures the stability of the main branch and promotes code review. Before each merge, a team member not involved in the branch's development will conduct a code review to ensure code stability.

EchoLink's development is divided into several sprints, the specific number of which can be flexibly adjusted according to project progress and team capability. Through the above management strategies, our team can collaborate efficiently while ensuring development quality and quickly responding to changes in project requirements.


## Risks in Team Projects

In team projects, the risks faced are often multifaceted. Effectively identifying and mitigating these risks is crucial for ensuring project success. Below are the risks anticipated in our project, along with corresponding strategies for response, as discussed in detail by our team:

### Technical Risks

Technical risks involve the possibility that the technology used in the project may not meet expectations or may be more difficult to implement than anticipated (since we have only outlined the basic requirements for the software so far). Possible technical risks for our EchoLink product include but are not limited to compatibility issues with WebRTC technology, performance problems, or security vulnerabilities (even though this is a local LAN development project, there are still inherent risks).

To this end, we have made the following contingency plans:

- In the early stages of the project, conduct prototype design and testing of key technologies to assess their applicability and performance. For the non-essential features listed above, we will make modifications as deemed appropriate after collective discussion and evaluation by the team.
- Regularly conduct code and architecture security reviews to ensure timely discovery and repair of security vulnerabilities. (This is necessary as not everyone is completely proficient in development, and adequate time needs to be allocated for debugging.)

### Project Management Risks

Project management risks involve the scope, timing, and cost of the project being affected by unreasonable arrangements. This also includes sudden events involving team members, skill mismatches, or uneven work distribution, which could lead to project delays or stagnation.

To this end, we have made the following contingency plans:

- Clearly define the entire scope of the project to avoid it expanding indefinitely and becoming unfinishable. The potential future optimizations listed will be considered after the entire project has been implemented and grounded.
- Regularly conduct project reviews and retrospectives, adjusting plans in a timely manner based on project progress and feedback from personnel. We plan to hold two meetings every Monday and Friday for task planning and review for the week, with members taking turns to compile meeting summaries (with the aid of AI tools) for subsequent tracking.
- Clearly define the roles and responsibilities of each team member to ensure reasonable task allocation. (There is no clear technical division of labor yet; PM, UI/UX, Front-End, Back-End, Tester roles will be assumed by those proficient in the relevant tasks.)
- Establish backup plans for each person and task to guard against sudden personnel changes and accidents.
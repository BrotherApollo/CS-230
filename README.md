# Draw It or Lose It – Software Design Reflection  
**Caleb Hicks – CS 230**

---

## Project Summary  

The client was The Gaming Room, the company behind *Draw It or Lose It*. The game originally ran only on Android, and they wanted a web-based version that could run across Windows, Mac, Linux, and mobile browsers.

My role was to design the backend structure for that web version. I created a Java-based solution using object-oriented principles. The system includes a singleton `GameService` to manage all active games, enforces unique game and team names, and supports multiple teams and players per game. The goal was to preserve the original gameplay while making the system scalable and platform independent.

---

## What I Did Well  

I clearly defined the domain model and explained how the classes relate to each other. The inheritance structure (`Game`, `Team`, and `Player` extending a shared `Entity` base class) kept the design clean and avoided duplicated code.

I also connected design patterns directly to requirements. The singleton pattern supports maintaining a single authoritative game state, and iterator-based validation enforces uniqueness constraints.

---

## How the Design Document Helped  

Working through the design document helped me think more intentionally before coding. It required me to define relationships, constraints, and architectural decisions up front.

Instead of writing code first and restructuring later, I had a clear blueprint. That made implementation more efficient and reduced uncertainty during development.

---

## What I Would Revise  

Based on instructor feedback, most sections could use more detail, discussion, and analysis. The security section especially needs expansion.

If I revised this document, I would provide a deeper explanation of authentication, TLS implementation, session handling, and secure data storage. Rather than briefly mentioning OAuth and HTTPS, I would describe how they would function within the system and why they are appropriate.

More broadly, I would strengthen each subsection with clearer reasoning and analysis of trade-offs, particularly in distributed systems, storage management, and system architecture.

---

## Interpreting User Needs  

The Gaming Room wanted cross-platform access while maintaining the original gameplay experience. I addressed this by designing a JVM-based backend, enforcing strict uniqueness rules, and structuring the system to support multiple teams and players per game.

Considering user needs is critical because software must solve real problems. A technically sound system that fails to meet user expectations does not fulfill its purpose.

---

## My Approach to Design  

My approach included:

- Identifying business and technical requirements  
- Designing the domain model  
- Applying appropriate design patterns  
- Evaluating deployment platforms  

In the future, I would incorporate more detailed architectural diagrams and expand my analysis of design trade-offs. This project reinforced the importance of structured planning before implementation.
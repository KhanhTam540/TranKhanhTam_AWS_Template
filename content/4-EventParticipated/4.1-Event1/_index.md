---
title: "Event 1"
date: 2026-05-23
weight: 2
chapter: false
pre: " <b> 4.1. </b> "
---

# Summary Report: â€œFCAJ Community Dayâ€

### Event Objectives

- Share practical knowledge about AWS, AI, cloud architecture, DevOps, and modern application development
- Introduce real-world applications of AI agents, LLMs, Amazon CloudFront, Amazon Quick, and multi-agent systems
- Help students and cloud learners understand how AI can be used effectively with proper context and system design
- Present practical lessons from hackathons, production AI systems, CDN architecture, and enterprise-grade AI deployment
- Provide a learning and networking space for students, developers, DevOps engineers, AI builders, and AWS community members

### Speakers

- **Tinh Truong** â€“ Platform Engineer, GoTymeX  
  Topic: **Context Is Everything - Making AI Actually Work for You**

- **Pham Ng Hai Anh** â€“ G-AsiaPacific Vietnam, AWS Community Builder  
  Topic: **Friendly AI Assistant with Amazon Quick**

- **Nguyen Tuan Thinh** â€“ DevOps Engineer, First Cloud AI Journey  
  Topic: **From Edge to Origin: CloudFront as Your Foundation**

- **Team VIB**  
  Topic: **36 hrs with LotusHacks â€“ Building UTMorpho from Idea to Reality**

- **Duc Dao** â€“ Solution Architect, Cloud Kinetics  
  Topic: **Non-Determinism of â€œDeterministicâ€ LLM Settings**

- **Vy Lam** â€“ Senior Business Systems Analyst, VPBank  
  Topic: **Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring**

### Event Overview

**FCAJ Community Day** was a community event that brought together multiple technical sessions about AWS, AI, cloud architecture, DevOps, LLM behavior, hackathon product building, and enterprise-grade multi-agent systems. The event provided both technical knowledge and practical experience from speakers who work with cloud and AI in real-world environments.

The event was valuable because it did not focus on only one topic. Instead, it covered a wide range of modern technology areas. Participants could learn how to use AI more effectively through better context, how Amazon Quick can support business users, how Amazon CloudFront improves performance and security from edge to origin, how a hackathon team builds a product under pressure, why LLM outputs may still be non-deterministic even with temperature set to zero, and how multi-agent systems can be designed for enterprise credit scoring.

### Key Highlights

#### Context Is Everything - Making AI Actually Work for You

This session explained that AI models are already powerful, but many poor AI responses come from weak context rather than weak models. The speaker emphasized that AI cannot perfectly infer the userâ€™s goal, situation, constraints, or success criteria unless the user provides them clearly.

The session introduced the meaning of context in AI usage. Context includes the userâ€™s goal, current situation, constraints, relevant evidence, expected output format, and success criteria. When these elements are provided clearly, AI can produce more useful and accurate responses.

Several common mistakes were discussed:

- Giving the AI too much unrelated information
- Copying full articles, screenshots, or documents without filtering useful evidence
- Telling AI information it already knows
- Asking vague questions without goals or constraints
- Providing quantity of context instead of quality of context

The session also introduced the idea of moving from **prompt** to **context** and then to **memory**. A better AI system is not only a chatbot that answers one question at a time. It can become a second AI brain that remembers what the user is learning, understands projects and goals, retrieves relevant information, and improves over time.

#### Friendly AI Assistant with Amazon Quick

This session introduced how Amazon Quick can support business users by creating a more unified AI assistant experience. In many organizations, business users need to gather information from different sources, analyze documents, consult experts, and repeat routine tasks. These tasks can be time-consuming and reduce productivity.

Amazon Quick provides an integrated experience where users can work with company data, world knowledge, user-uploaded files, databases, data warehouses, dashboards, automation flows, and third-party actions. It also includes governance, data security, access controls, guardrails, and responsible AI features.

One use case discussed in the session was a **PM assistant**. This assistant can help automatically create meeting minutes, send emails to stakeholders, and schedule the next meeting. This shows how AI can support common office tasks and reduce repetitive manual work.

#### From Edge to Origin: CloudFront as Your Foundation

This session focused on Amazon CloudFront and how it can serve as a foundation for performance, security, resiliency, and cost optimization. The speaker explained that pay-as-you-go cloud pricing is powerful but can also create fear of unexpected cost spikes when traffic grows suddenly or when attacks happen.

Amazon CloudFront helps solve several problems by caching content closer to users, reducing origin load, improving latency, and supporting security features at the edge.

The session discussed several important capabilities:

- CDN and edge caching
- AWS WAF integration
- DDoS protection
- Route 53 and DNS integration
- Origin Shield
- Request collapsing
- Rate limiting and throttling
- HTTPS encryption in transit
- Origin Access Control
- Signed URLs
- Geographic restrictions
- Origin failover
- Custom error pages
- HTTP compression
- HTTP/3 support
- Edge logic with CloudFront Functions and Lambda@Edge

The session also explained how CloudFront can reduce origin costs. For example, when CloudFront handles caching and compression, the origin server receives fewer requests and consumes less CPU. CloudFront can also reduce data transfer and load balancer usage in some scenarios.

#### 36 hrs with LotusHacks â€“ Building UTMorpho from Idea to Reality

This session shared the experience of Team VIB during LotusHacks 2026. The team joined Vietnamâ€™s largest hackathon and had 36 hours to create a product from idea to implementation.

The session walked through the journey from joining the hackathon with uncertainty, discovering a real problem from daily work, defining the product idea, building under time pressure, and finally preparing the product overview and demo.

The product discussed in the session was **UTMorpho**. Although the available slide data focused mainly on the journey rather than technical implementation details, the session clearly showed the process of turning a vague idea into a working product under limited time.

Several practical lessons were highlighted:

- Real frustration can become a real product idea
- More ideas do not always mean better ideas
- Hackathons test endurance and teamwork
- Team synchronization is extremely important
- Building under pressure requires prioritization
- A focused editing experience can improve product usability

The session also discussed challenges such as AI overgeneration, token limits, burnout near pitch time, and the difficulty of polishing a product within a short deadline.

#### Non-Determinism of â€œDeterministicâ€ LLM Settings

This session explained why large language models may still produce different outputs even when settings appear deterministic. Many users assume that setting temperature to zero guarantees the same output every time. However, the speaker explained that this assumption is not always true.

The session first explained how LLMs generate text. At each step, the model outputs scores for possible next tokens. These scores are converted into probabilities using softmax, and the next token is selected based on the decoding settings.

Temperature controls randomness:

- Higher temperature increases randomness and creativity
- Temperature near zero makes outputs more consistent
- Temperature zero theoretically selects the highest-probability token

However, in real systems, non-determinism can still happen. The speaker referenced research showing that several LLMs produced inconsistent outputs across repeated runs with the same prompt, same settings, and temperature equal to zero.

The reasons include:

- Floating-point arithmetic on GPUs
- Non-associative mathematical operations
- Parallel GPU execution order
- Inference batching by API providers
- Tiny rounding differences that can change the selected token

This matters because many production use cases require reliability, such as medical information retrieval, legal document analysis, financial planning, structured output generation, benchmarking, and regression testing.

The session suggested several mitigation strategies:

- Run multiple times and use majority voting
- Use structured outputs such as JSON mode or function calling
- Use constrained decoding when possible
- Self-host models when deterministic infrastructure is required
- Build downstream systems that can handle variance
- Test thoroughly and repeatedly
- Consider using temperature 0.1 if temperature 0 causes repetitive loops

#### Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring

This session introduced how multi-agent systems can be used for startup credit scoring. The speaker explained that traditional banking credit scoring systems were designed for established businesses, not startups.

Traditional credit scoring often expects:

- Several years of financial statements
- Established credit history
- Physical collateral
- Predictable revenue
- Standardized reporting
- Industry benchmarks

However, startups often have different characteristics:

- Only a short operating history
- Little or no credit history
- Intellectual property, team, and traction as key assets
- Hypergrowth or pivot patterns
- Novel business models
- Unstructured data

Because startup data is multi-dimensional, a single AI agent may not be enough. Different domains require different expertise, such as financial analysis, market analysis, team evaluation, risk assessment, and compliance review.

The session proposed a **virtual credit committee** architecture where specialized agents collaborate:

- Manager agent
- Financial Analyst agent
- Market Analyst agent
- Team Evaluator agent
- Risk Assessor agent
- Compliance agent

The system produces outputs such as credit score, risk rating, confidence level, and audit trail.

The session also explained why multi-agent systems work well:

- Specialized expertise
- Checks and balances
- Parallel processing
- Auditability
- Scalability
- Fault tolerance

A strong part of the session was the focus on enterprise-grade thinking. A proof of concept is not enough for production. Enterprise AI systems need security, data governance, network isolation, operations, human factors, and compliance.

### Key Takeaways

#### AI and Context

- AI models are powerful, but weak context can lead to poor results.
- Better context helps AI understand the real goal, constraints, and expected output.
- Context engineering is becoming an important future skill.
- A second AI brain can be built by combining context, memory, retrieval, and generation.

#### AI Assistants and Productivity

- AI assistants can support business users by connecting to company data and workflows.
- Amazon Quick can help users work with datasets, dashboards, automation, chat, research, and third-party actions.
- Practical AI assistants can reduce repetitive tasks such as creating meeting minutes, sending emails, and scheduling meetings.

#### CloudFront and Cloud Architecture

- Amazon CloudFront is more than a CDN.
- CloudFront improves performance, security, resiliency, and cost optimization.
- Caching, compression, origin shielding, signed URLs, and failover can reduce origin load and improve user experience.
- Edge services help protect applications from attacks and unexpected traffic spikes.

#### Hackathon and Product Building

- Good product ideas can come from real daily frustrations.
- Hackathons require focus, teamwork, and endurance.
- A working product needs prioritization, integration, demo preparation, and clear storytelling.
- Team synchronization is often more important than having many ideas.

#### LLM Reliability

- Temperature zero does not fully guarantee deterministic output.
- GPU execution, floating-point differences, and inference batching can cause output variation.
- Production LLM systems should be designed to handle variance.
- Structured outputs, multiple runs, testing, and constrained decoding can improve reliability.

#### Enterprise Multi-Agent Systems

- Single-agent systems are suitable for simple workflows, but complex enterprise decisions may require multi-agent architecture.
- Specialized agents can provide better reasoning, auditability, and fault tolerance.
- Enterprise AI must include security, compliance, governance, monitoring, and clear ROI.
- Guardrails are essential for production AI systems.

### Applying to Work

- Prepare better context before asking AI to solve technical or learning tasks.
- Use a context framework including goal, relevant information, constraints, and success criteria.
- Explore AI assistant use cases for automating repetitive business or project tasks.
- Use CloudFront as a foundation layer for performance, security, caching, and origin protection.
- Design systems with cost awareness, especially when traffic may grow unexpectedly.
- Treat LLM outputs as probabilistic and test AI features with multiple runs.
- Use structured output features such as JSON mode or function calling when building AI applications.
- Consider multi-agent systems for complex workflows that require multiple areas of expertise.
- Add guardrails, monitoring, and compliance checks when moving AI systems toward production.
- Build small prototypes first, then improve them into more reliable production-ready solutions.

### Event Experience

Attending **â€œAWS Vietnam Community Day - May 2026â€** was a valuable learning experience because the event covered both technical depth and practical implementation lessons. The sessions were diverse, ranging from AI usage mindset to cloud architecture, LLM reliability, hackathon experience, and enterprise AI deployment.

#### Learning how to use AI better

The session about context helped me realize that the quality of AI output depends heavily on the quality of input. Instead of only writing short prompts, users should provide clear goals, relevant information, constraints, and success criteria. This changed my view of AI from a simple chatbot into a system that needs proper context design.

#### Understanding AI assistants for business users

The Amazon Quick session showed that AI assistants can be useful beyond software development. They can support business users by gathering information, analyzing company data, creating meeting notes, sending emails, and automating repetitive tasks. This helped me understand how AI can become part of daily work.

#### Learning CloudFront as a foundation layer

The CloudFront session was useful because it showed that CloudFront is not only used to speed up static websites. It can also improve security, reduce origin load, protect against attacks, support failover, and help control cost. This gave me a broader view of CDN architecture and edge computing.

#### Learning from a hackathon journey

The LotusHacks session was inspiring because it showed the real process of building a product under pressure. The team had to move from idea discovery to implementation, integration, demo, and pitch in only 36 hours. This session showed that product building requires focus, communication, and endurance.

#### Understanding LLM non-determinism

The LLM session was one of the most technical sessions. It helped me understand that even with temperature set to zero, LLM outputs may still vary because of GPU computation, floating-point differences, and inference batching. This is important for anyone building production AI applications.

#### Understanding enterprise multi-agent systems

The multi-agent credit scoring session helped me understand when multi-agent architecture is useful. For complex, high-stakes, and auditable decisions, multiple specialized agents can work like a virtual committee. This architecture improves reasoning quality, traceability, and fault tolerance.

#### Lessons learned

- Good AI results require good context.
- AI assistants should be connected to trusted data and business workflows.
- CloudFront can improve cost, performance, security, and reliability.
- Hackathons teach teamwork, prioritization, and fast decision-making.
- LLMs should be tested carefully because deterministic settings may still produce variation.
- Enterprise AI requires security, compliance, monitoring, guardrails, and clear ROI.

#### Some event photos

![Your event picture](/TranKhanhTam_AWS_Template/images/4-Event/Event_1/picture-event1-1.jpg)
![Your event picture](/TranKhanhTam_AWS_Template/images/4-Event/Event_1/picture-event1-2.jpg)
![Your event picture](/TranKhanhTam_AWS_Template/images/4-Event/Event_1/picture-event1-3.jpg)

> Overall, the event helped me understand how AWS and AI can be applied in many real-world scenarios. It also showed that successful cloud and AI systems require not only technical tools, but also good design thinking, security awareness, testing, and practical experience.

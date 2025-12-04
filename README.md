# Mental Health Support Agent System

## The Problem

Mental health support for students is often fragmented. When struggling, students face a "paradox of choice": Should they call a crisis line, book a university counselor, research self-help techniques, or vent to a friend?

Existing solutions fail in two critical ways:

- **Static Chatbots**: Lack empathy and context, providing generic "canned" responses
- **Search Engines**: Overwhelm users with links during cognitive overload

The real challenge isn't just providing answers—it's **triaging safety**. A student experiencing exam stress needs breathing exercises, while a student expressing self-harm requires immediate emergency intervention. Treating these scenarios identically is dangerous. This system understands that nuance.

## Why an Agentic Approach?

Standard LLMs (like basic ChatGPT wrappers) predict the next likely word. While articulate, they're non-deterministic regarding safety—potentially hallucinating crisis hotline numbers or offering "wellness tips" to someone in immediate danger.

**Agents solve this through:**

### Enforced Safety Protocols
A deterministic Python tool (`assess_mental_health`) calculates risk before generating responses. If keywords like "suicide" are detected, the system routes to the Crisis Agent, bypassing standard chat behaviors.

### Specialized Agents
A single prompt can't excel at everything. This system uses:
- **Crisis Specialist**: Direct, authoritative intervention
- **Empathetic Listener**: Warm, supportive conversation

The tone matches the user's specific need.

### State & Memory
Agents maintain a structured `MentalHealthMemoryBank`, tracking mood scores over time (e.g., "Your mood dropped from 7 to 4 this week")—something stateless LLM chats cannot effectively provide.

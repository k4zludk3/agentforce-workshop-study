# Agentforce Builder

## Exercise 1: Get Started with Agentforce

In this section, we learn how to set up our first Agent in the new Agentforce Builder. We built the **Pronto Service Agent**, designed to help customers with food delivery orders.

### Key Concepts

1. **Creating an Agent from a Prompt:**
   Agentforce allows you to quickly scaffold an agent by writing a natural language prompt that describes its persona and goals. For example:
   > "Create a customer support agent for Pronto, a food delivery platform... Ask clarifying questions when needed and avoid asking users for Salesforce record IDs."

2. **Builder Interface:**
   - **Navigation Explorer:** (Left pane) Shows the Agent Definition, Subagents, and Variables.
   - **Main Editor View:** (Center pane) Allows editing the agent configuration via visual Canvas or YAML-based Script.
   - **Authoring Agent:** (Right pane) Provides quick access to test and modify the agent using AI.

3. **System Instructions & Tone:**
   The base instructions dictate how the agent should behave globally. We set it to be friendly, concise, and protective of user privacy (never asking for sensitive info or record IDs).

4. **Agent Router (The Entry Point):**
   The Agent Router is the primary subagent that evaluates the user's input and routes the conversation to the most appropriate subagent. The only actions an Agent Router should have are "transition" actions.

5. **Variables:**
   Variables hold state during the conversation.
   - **Linked Variables:** Set by the system (e.g., `@MessagingSession.Id`) and are read-only for the agent.
   - **Mutable Variables:** Can be modified by the agent to store context across the conversation.

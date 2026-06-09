# Prompting

## Prompt Types

* **Zero-Shot Prompting** – Direct instructions without examples.
* **Few-Shot Prompting** – Provide examples to guide output format and style.
* **Chain-of-Thought Prompting** – Encourage step-by-step reasoning for complex tasks.
* **Role-Based Prompting** – Assign a role/persona to improve relevance and tone.
* **Conversational Prompting** – Create interactive, multi-turn experiences.
* **Counterfactual Prompting** – Explore "what-if" scenarios and alternative outcomes.
* **Creative Prompting** – Generate ideas, names, content, and marketing concepts.

## Prompt Lifecycle

1. **Develop** – Create prompts based on business requirements.
2. **Test** – Validate outputs against expected goals.
3. **Monitor** – Track performance, accuracy, and security.
4. **Iterate** – Refine prompts using feedback and analytics.

## Prompting Best Practices

* Break complex use cases into smaller tasks.
* Provide clear context and input definitions.
* Specify tone, format, and expected response length.
* Use examples to improve consistency.
* Reuse successful prompts whenever possible.
* Be specific and detailed in instructions.

## Flows in Agentforce - Key Takeaways

### Why Use Flows?

* Flows are the only low-code way for agents to create, update, or delete Salesforce records.
* Flows provide agents with precise data, improving accuracy and reducing hallucinations.

### Best Practices

* Use **Autolaunched Flow (No Trigger)** only.
* Create clear and descriptive flow, variable names, and descriptions.
* Always define at least one **Input** and **Output** variable.
* Include output variables for error handling.
* Use record variables/collections instead of multiple individual variables.
* Return only the fields the agent actually needs.
* Build multiple small, reusable flows rather than one large flow.

### Security & Permissions

* Grant agents only the permissions they require.
* External-facing agents run using a dedicated **Agent User**.

### Limitations

* Text variables support a maximum of **255 characters**.
* Avoid unsupported output types:

  * Currency
  * Picklist
  * Multi-Select Picklist
  * Apex-Defined

### Important Notes

* Flow descriptions become agent instructions.
* Agents cannot pause a flow to ask users questions mid-execution.
* If flow input/output variables change, recreate the Agent Action to refresh the variable mappings.


***Multimodal-AI-Agent***

This project builds a multimodal intelligent agent that can process both text and images using a combination of Large Language Models (LLMs) and Stable Diffusion. The goal is to allow natural language interaction where the agent can either respond with text explanations or generate relevant illustrations, depending on the query.


**Project Overview**
* Integrated **Groq LLaMA 3.1** as the core LLM for reasoning and text generation.
* Added **Stable Diffusion** for text-to-image generation tasks.
* Incorporated optional external tools such as **Wikipedia** and **YouTube** for retrieving factual information.
* Designed an agent workflow with **LangChain / LangGraph** to decide when to answer in text or generate an image.
* Created a unified interface where users can ask questions or request illustrations, and the system provides the most suitable output.


**Methods Implemented**
* **Tool binding**: connected LLaMA with Stable Diffusion, Wikipedia, and YouTube tools.
* **Agent design**: built a ReAct-style agent to reason about tool use and decide between text and image output.
* **Prompt handling**: customized system prompts to guide the assistant’s behavior.
* **Error handling**: managed tool call validation, schema mismatches, and unsupported requests.
* **User Interface**: developed a Gradio-based front end where users can type queries and view responses (text or image).


**Results**
* The agent successfully generates diagrams or illustrations when users request visual explanations (e.g., *“Draw a mountain bike on a winding trail”*).
* Provides accurate, conversational text answers for conceptual or factual queries (e.g., *“Explain the Fourier Series visually”*).
* Combines reasoning with external retrieval tools for more grounded answers.
* Flexible output: users receive either **text explanations** or **generated images**, not both at once.


**Future Work**
* Transition the image-generation component from LLaMA/Stable Diffusion to OpenAI’s DALL·E, leveraging cloud-based generation   for faster, more scalable results.
* Extend the interface to mobile or web apps for broader accessibility.
* Experiment with fine-tuned multimodal LLMs that natively handle both text and image reasoning.

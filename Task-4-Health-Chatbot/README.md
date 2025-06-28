# Task 4: General Health Query Chatbot

This project introduces the application of Large Language Models (LLMs) and prompt engineering to create a safe and helpful conversational AI.

### Objective
To build a chatbot capable of answering general health-related questions without providing direct or harmful medical advice.

### Tools & Models
-   **Library:** Hugging Face `transformers`.
-   **Model:** An open-source, instruction-tuned model (`Mistral-7B-Instruct-v0.2` or `Zephyr-7B-Beta`).
-   **Technique:** 4-bit quantization was used to run the model efficiently in a Google Colab environment.

### Key Steps
1.  **Environment Setup:** Handled common challenges, including authenticating with Hugging Face and ensuring correct GPU library configurations.
2.  **Prompt Engineering:** A comprehensive system prompt was designed to define the chatbot's persona as a "friendly and helpful medical assistant."
3.  **Safety Filter Implementation:** A critical instruction was embedded in the prompt, forbidding the model from giving medical advice and requiring it to always include a disclaimer to consult a doctor.
4.  **Testing:** The chatbot was tested with general queries and specific questions seeking advice to validate the effectiveness of the safety filter.

### Conclusion
The chatbot successfully provided informative and contextually appropriate answers while strictly adhering to its safety protocols. This project demonstrates the power of prompt engineering in controlling LLM behavior, a crucial skill for developing responsible AI applications in sensitive fields like healthcare.

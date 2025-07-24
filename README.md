## AI-Powered Code Wiring Assistant for Effortless Variable Mapping in Reused Code

### Summary

Tired of manually renaming variables after pasting code snippets? **WIRL** is an intelligent "Code Wiring" assistant powered by LLMs and RAG. When you reuse a code snippet from sources like Stack Overflow, GitHub, or AI models, WIRL automatically analyzes your local context and suggests the correct variable mappings. It helps you replace unresolved variables with existing ones in your current scope with a single click, dramatically speeding up code reuse and integration.

### The Problem: Why WIRL?

Copy-paste-modify is an unavoidable practice in software development. However, over 85% of reused code snippets require manual adaptation before they can be integrated. A prevalent and error-prone part of this process is **variable adaptation**:

*   **Compilation Errors:** Undeclared or conflicting variables lead to immediate build failures.
*   **Logical Flaws:** Incorrect variable substitutions can introduce subtle, hard-to-find bugs.
*   **Inefficiency:** Manually searching for and replacing variables is tedious and inefficient.

Existing IDE features often rely on simple heuristics (e.g., name/type matching) and fail to grasp complex contextual semantics. Using general-purpose large LLMs directly suffers from high latency, making them impractical for real-time development needs.

### The WIRL Solution: Agent + RAG

WIRL introduces an innovative agent-based architecture that thinks and acts like an experienced developer:

1.  **Auto-Detection:** Upon pasting code, WIRL instantly identifies all unresolved variables (the "unplugged wires").
2.  **Context-Aware Analysis:** Leveraging **Retrieval-Augmented Generation (RAG)**, WIRL's agent iteratively and dynamically gathers the most relevant context from your local codebase via static analysis.
3.  **Intelligent Suggestions:** WIRL reframes the "variable mapping" task into a **"code completion"** task, which is a natural strength of LLMs. It treats unresolved variables as blanks to be filled, and by feeding the retrieved context to the LLM, it accurately suggests the most suitable local variables for replacement.

This approach enables even smaller, distilled LLMs to achieve performance comparable to or even better than full-parameter LLMs on this task, striking the perfect balance between **accuracy** and **low latency**.

### Key Features

*   🚀 **Intelligent Variable Mapping:** Automatically analyzes unresolved symbols in pasted code and suggests optimal local variable replacements based on deep contextual understanding.
*   🧠 **Context-Aware Agent:** Utilizes an Agent + RAG architecture to dynamically retrieve and reason about the most relevant local code context for highly accurate suggestions.
*   ⚡ **Efficient Hybrid Execution:** Optimizes the agent's workflow by executing critical steps (like syntax analysis) locally without LLM calls, ensuring a fast and responsive experience.
*   🤖 **State Machine-Guided Exploration:** A built-in state machine guides the agent's analysis process, preventing redundant or invalid attempts and improving overall efficiency.
*   🔒 **Secure and Reliable:** Your API keys are securely stored using IntelliJ IDEA's built-in `PasswordSafe`. They are never hard-coded or exposed in plain text.
*   💡 **Seamless Integration:** Seamless Integration:</strong> Works seamlessly within your IDEA workflow. Simply paste code, select method, and invoke WIRL via Right-Click.

### Getting Started
**Search "WIRL" in IntelliJ IDEA Plugin Marketplace and Download it.**
1. Configure your LLM API key in <code> File | Settings | Tools | WIRL AI Settings</code>.</li>
2. Copy a code snippet from any source and paste it into your editor.</li>
3. Select an unresolved variable, Right-Click it, and select "WIRL: Map variables" to get suggestions.</li>
4. All the unresolved variables in the method where the selected one located will be addressed together!</li>

Say goodbye to tedious manual variable renaming. Let WIRL be your indispensable assistant for efficient code reuse!
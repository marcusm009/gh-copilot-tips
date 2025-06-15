To help you understand effective communication with AI in a coding context, here are examples of good and bad prompts, along with explanations drawn from the sources:

## Good Prompts

Good prompts are characterized by their simplicity, specificity, and conciseness, ensuring the AI understands your intent and provides relevant, high-quality output. They provide adequate context, break down complex tasks, and leverage the AI's capabilities effectively.

1. **Specifying Technologies and Design Details:**

    > **Prompt:**  
    > Build a search feature for a product listing page. Use JavaScript with React for the frontend and integrate with a PostgreSQL database on the backend. The search should filter products by title and description, include an option to sort by price (ascending/descending), and allow filtering by product category (e.g., 'electronics', 'apparel').

    > **Explanation:**  
    > This prompt is excellent because it explicitly lists the technologies to use, which helps the AI generate compatible and high-quality code, as AI is more familiar with popular languages and frameworks. It also designs the solution by detailing specific features (filters, sorting, search criteria) before asking the AI to build it, ensuring the AI understands exactly what is desired and reducing ambiguity. Breaking down the requirements into a list of tasks helps the AI focus and integrate everything cohesively.

2. **Providing Explicit Context (e.g., using @workspace or highlighting code):**

    > **Prompt:**  
    > (With `cabin.model.ts` and `cabin.service.ts` open and the `CabinService` class highlighted)  
    > "Using @workspace, generate a unit test for the CabinService class. Ensure the tests use mock cabin data and mock out the cabinService (which makes HTTP calls) to prevent real calls. Include both positive and negative test cases, specifically testing null values for cabinService being returned."

    > **Explanation:**  
    > By using @workspace, you give GitHub Copilot context of your entire working codebase, which is crucial for relevant solutions. Highlighting specific code ensures the AI focuses on the correct scope. This level of detail in the prompt allows the AI to generate highly specific and accurate tests, as demonstrated in the sources for creating unit tests with specific requirements.

3. **Breaking Down Complex Tasks (Stepwise Chain of Thought):**

    > **Prompt:**  
    > Refactor the `user_profile.js` file to improve modularity and readability. Break this task into small, manageable steps, and wait for me to type 'next' before proceeding with the next step.

    > **Explanation:**  
    > This prompt uses the "Stepwise Chain of Thought" strategy, which asks the AI to tackle a large task by breaking it into sequential steps. This allows you to validate changes incrementally and prevent the AI from making too many changes at once, which can be difficult to manage. The "next" keyword ensures you control the pace of the refactoring process.

4. **Role-Playing and Learning:**

    > **Prompt:**  
    > Act as an experienced Python teacher for a beginner. Your goal is to explain this `data_processing.py` script line by line. Add comments to the code for clarity. If I ask a follow-up question, provide a hint or a nudge rather than the direct answer, encouraging me to figure it out myself.

    > **Explanation:**  
    > Assigning a specific "role" to the AI (e.g., "teacher") can significantly influence its output style and effectiveness. Asking it to keep things simple and explain line by line helps new developers understand the code syntax and patterns. The instruction to "nudge" rather than "give the answer" promotes active learning, which is a key benefit of using AI for education.

5. **Requesting Alternative Solutions and Pros/Cons:**

    > **Prompt:**  
    > (With a database connection module highlighted)  
    > "Suggest three different architectural patterns for implementing this database connection logic. For each pattern, list its pros and cons, specifically considering factors like scalability, maintainability, and potential resource management issues for a medium-to-large scale web application."

    > **Explanation:**  
    > This prompt leverages the AI's ability to provide alternative solutions and analyze their trade-offs. Asking for pros and cons helps you make informed decisions, acknowledging that "there is rarely a single right way to do anything" in programming.

---

## Bad Prompts

Bad prompts often suffer from being too generic, lacking context, or misusing the AI's intended functionalities. They can lead to irrelevant, incorrect, or inefficient outputs, causing frustration and wasted time.

1. **Generic and Ambiguous Requests:**

    > **Prompt:**  
    > "Make this code better." or "Build a web application."

    > **Explanation:**  
    > These prompts are too generic and lack specificity. The AI won't know what "better" means (e.g., more readable, faster, more secure) or what type of web application you envision, leading to outputs that likely won't meet your unstated expectations. This is akin to asking for "food" when you wanted "pizza with a salad and a soft drink".

2. **Lack of Relevant Context:**

    > **Prompt:**  
    > "Fix the bug in the auth.js file." (without `auth.js` being open, selected, or referenced)

    > **Explanation:**  
    > If the AI doesn't have the relevant file open or explicitly provided in its context (e.g., via #file or @workspace), it will make assumptions that might be inaccurate, leading to fundamentally non-working code or an "infinite loop" of troubleshooting.

3. **Overly Broad Scope in a Single Request:**

    > **Prompt:**  
    > "Build a full-stack e-commerce application with user authentication, product management, shopping cart functionality, and payment gateway integration."

    > **Explanation:**  
    > While tempting, asking the AI to build an entire application in one go is generally inefficient. The AI is not a replacement for a developer and "does not always produce correct optimal secure code" for such large tasks. Breaking it down into smaller, manageable steps is recommended for better results and easier validation.

4. **Misusing Comments for Prompting in Code:**

    > **Prompt:**  
    > `// Add a product rating system to this form, including stars and user reviews.` (as a comment in the middle of a code file)

    > **Explanation:**  
    > While technically possible, using comments for prompting Copilot inline is inefficient. For quick, in-code modifications, inline chat (e.g., Ctrl+I or Cmd+I) is the more appropriate and efficient tool. Comments should be for code documentation, not active prompting.

5. **Recreating Existing Slash Commands:**

    > **Prompt:**  
    > "Can you please explain this selected code block to me?"

    > **Explanation:**  
    > This prompt duplicates functionality that GitHub Copilot provides via slash commands (e.g., /explain). Knowing and using these commands (/fix, /test, /doc, /explain) is a more concise and efficient way to interact with the AI for common tasks.

6. **Providing Too Much Irrelevant Context:**

    > **Prompt:**  
    > (Pasting an entire 5000-line software project into the chat for a small modification) or (Continuing a long, multi-hour conversation for a new, unrelated feature).

    > **Explanation:**  
    > The AI can get confused if given too much context, especially with very long files or excessively long conversation histories. This can lead to the AI deleting code, creating duplicates, or failing to understand your request. It's often better to start a new conversation and include only the directly relevant files.

---

By understanding these distinctions, you can significantly improve your productivity and the quality of the AI's assistance in your coding tasks.
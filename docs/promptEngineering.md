### <span style="color: blue"> **Prompt Engineering** </span>

Prompt engineering is the process of designing and refining prompts to effectively interact with AI language models. It involves crafting inputs that guide the model to produce desired outputs, improving accuracy, relevance, and usefulness.

### <span style="color: blue"> **Prompt as 2 main elements** </span>

#### 🔧 <span style="color: green"> **Prompt Parameters (Summary)** </span>
1. **Temperature**      
    Controls how creative or random the response is.
    -   Lower values like `0.0` make answers more exact and predictable (good for code).
    -   Higher values like `0.7–0.8` make answers more creative and varied.       
- **Top-p**     
    Controls how many word choices the model considers.
    - Higher values allow more creative and diverse answers.
    - Often used together with temperature. 
- **Max length**    
    Limits how long the response can be (in tokens, which are words or parts of words).
    - Helps keep responses short and manage cost.


#### ✅ <span style="color: green"> **Key Structure of a Good Prompt** </span>

1. **Context**  
   Give some background so the model understands the situation.  
   _Example:_ Act as an analyst for an OTT platform. You will do sentiment analysis on customer feedback.       

2. **Instruction**  
   Tell the model what task to do.  
   _Example:_ Classify feedback as positive (promoter), negative (demoter), or neutral (neither).

3. **Input Data**  
   Share the actual question or content you want a response for.  
   _Example:_ Feedback - "The storyline was repetitive and abysmal."

4. **Example**: Show sample input and expected output to guide the model.   
    > feedback: "The series was okay" → Sentiment: neutral  
    > feedback: "The acting was awesome" → Sentiment: positive/promoter


5. **Response Format**  
   Tell the model how the output should look.  l=
   Example: Output - negative, json, tablue etc
  


### <span style="color: blue">**✅ Prompt Checklist**</span>

1. **Give context**  
Provide background information to help the model understand the task.  
**Example:** You are helping analyze customer reviews for a streaming platform.

2. **Create a role**  
Tell the model what role it should take. This shapes how it responds.  
**Example:** Act as a data analyst.

3. **Define the goal**  
Clearly state what you want the model to do. Be specific.  
**Example:** Classify each review as positive, negative, or neutral.

4. **Clarify the audience**  
Say who will use or read the output. This affects the tone and format.  
**Example:** The output is for the product team to improve user experience.

5. **Detail the output format**  
Explain how you want the response to look (bullet points, JSON, table, etc.).  
**Example:** Return the result in this format: `Feedback: [text] → Sentiment: [label]`

6. **Give examples**  
Provide input-output samples to guide the model.  
**Example:**  
    - Feedback: "The acting was great" → Sentiment: positive  
    - Feedback: "It was okay" → Sentiment: neutral

7. **Specify style or tone**  
Mention the desired tone or writing style (formal, casual, concise, etc.).  
**Example:** Keep the tone professional and concise.

8. **Define the scope**  
Clarify what to include or exclude in the response.  
**Example:** Only focus on the emotional tone of the feedback, not grammar or length.

9. **Apply restrictions or rules**  
Set clear limits to avoid unwanted results.  
**Example:** Do not generate examples. Do not explain the output.

10. **(Optional) Add fallback instructions**  
Tell the model what to do if it can't complete the task.  
**Example:** If unsure, respond with “Cannot determine sentiment.”


### <span style="color: blue">***✨ Prompt Patterns ***</span>

1. **Persona Pattern**  
   Ask the model to take on a specific role.  
   **Format:** Act as X, do task Y.  
   **Example:** Act as a career coach and help me write a resume summary.

2. **Audience Persona Pattern**  
   Tailor the explanation for a specific audience.  
   **Format:** Explain X assuming I am Y.  
   **Example:** Explain blockchain to me like I’m a 10-year-old.

3. **Visualization Generator Pattern**  
   Ask the model to create content usable by another tool or system.  
   **Format:** Generate X that can be used with tool Y.  
   **Example:** Generate a flowchart outline that can be used in draw.io.

4. **Recipe Pattern**  
   Request a step-by-step process for completing a task.  
   **Format:** In order to do X, provide steps A, B, C...  
   **Example:** In order to create a business plan, give me the full sequence of steps from research to presentation.

5. **Template Pattern**  
   Provide a structure with placeholders, and ask the model to fill in the content.  
   **Format:** I will provide a template; fill in the placeholders.  
   **Example:** Here’s an email template with [name], [date], and [action] — fill it out for a meeting reminder.

6. **Few-Shot Prompts**  
Give some examples first, then ask the model to continue or follow the pattern.  
_Example:_  
Translate English to French:  
    - Hello → Bonjour  
    - Thank you → Merci  
    - Good night →

7. **Zero-Shot Prompts**
Ask the model to do a task without giving any examples.  
_Example:_  
Classify this review as positive, negative, or neutral: "The movie was fantastic and engaging."

## <span style="color: blue"> References </span>

- [OpenAI Cookbook: Prompt Engineering](https://platform.openai.com/docs/guides/prompt-engineering)
- [Prompt Engineering Guide](https://www.promptingguide.ai/)

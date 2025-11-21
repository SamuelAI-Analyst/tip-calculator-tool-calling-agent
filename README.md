
Then it detects that a **calculation is needed**, automatically calls the `calculate_tip` tool, and returns the result in a natural language response.

---

## 🚀 Features

✔ Accepts natural language queries (example: *“Tip on $120 at 15%”*)  
✔ Uses **LangChain tool calling mechanism**  
✔ Processes tool results and returns final AI response  
✔ Implemented in **Python (Jupyter Notebook in VS Code)**  
✔ Uses **OpenAI model (`gpt-4o-mini`)** with tool binding  

---

## 🛠️ Technologies Used

| Component | Description |
|-----------|-------------|
| 🐍 Python | Programming language |
| ⚙ LangChain | Agent and tool calling framework |
| 🤖 OpenAI GPT Model | LLM used to process natural language |
| 📒 VS Code Jupyter | Notebook environment |
| 🔧 Tool Decorator | Used to define custom tools |

---

## 🧮 Tool Function (Tip Calculator)

```python
@tool
def calculate_tip(total_bill: int, tip_percent: int) -> int:
    """Calculate tip"""
    return total_bill * tip_percent * 0.01

This function is registered as a tool that can be called by the AI model when it detects calculation is needed.


---

🧠 Agent Workflow

agent = TipAgent(llm)
agent.run("How much should I tip on $60 at 20%?")

🔄 How the agent works

➤ Takes user query
➤ Interprets required tool (calculate_tip)
➤ Extracts parameters (total_bill = 60, tip_percent = 20)
➤ Calls tool and gets numeric result
➤ Sends result back to LLM for natural language response
➤ Outputs: “You should tip $12.”


---

📂 Project Structure

📁 tip-calculator-tool-calling-agent
│── 📄 tip_agent.ipynb     # Main notebook with implementation
│── 📄 README.md           # Project documentation
│── 📁 screenshots         # Images showing code and output


---

📸 Sample Output

(Add your screenshot using this format — replace the file name)

![Tool Calling Example](screenshots/tool-calling-output.png)


---

📘 What I Learned

🔹 How to define and register tools in LangChain
🔹 How tool calling works in AI agents
🔹 How an agent reads tool arguments from natural language
🔹 How to work with VS Code + Jupyter Notebook
🔹 How to structure a simple AI project


---

🚀 Next Improvements

Add multiple tools (tax, currency conversion, etc.)

Create a web interface using Streamlit or Flask

Deploy using Render or Hugging Face Spaces



---

🙌 Acknowledgments

Thanks to LangChain and OpenAI documentation, plus guidance from ChatGPT (AI tutor) for understanding tool calling.


---

📎 Author

Samuel Tochukwu
💼 AI | Data Science | Agentic AI Projects
📍 Based in Nigeria

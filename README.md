AI-Powered Research Assistant
Overview
This project is a Python-based tool designed to automate research paper creation by leveraging the power of LangChain, Pydantic, and the OpenRouter API (using the Google Gemma 3n 4B model). It integrates Wikipedia and DuckDuckGo APIs to gather information, process user queries, and generate structured research outputs, which are saved to a text file for easy reference.
Features

Automated Research: Generates research summaries based on user queries using web and Wikipedia searches.
Structured Output: Utilizes Pydantic to format responses with topic, summary, sources, and tools used.
File Storage: Saves research outputs to a text file with timestamps for record-keeping.
Technologies:
Python
LangChain
Pydantic
OpenRouter API (Google Gemma 3n 4B model)
Wikipedia API
DuckDuckGo Search API

Prerequisites

Python 3.8+
An OpenRouter API key (set up an account at OpenRouter)

Installation

Clone the Repository:
git clone https://github.com/your-username/ai-research-assistant.git
cd ai-research-assistant

Set Up a Virtual Environment (optional but recommended):
python -m venv venv
source venv/bin/activate # On Windows: venv\Scripts\activate

Install Dependencies:Install the required Python packages listed in requirements.txt:
pip install -r requirements.txt

The required packages are:

langchain
langchain-community
openrouter
python-dotenv
pydantic
duckduckgo-search

Set Up Environment Variables:Create a .env file in the project root and add your OpenRouter API key:
OPENROUTER_API_KEY=your_openrouter_api_key_here

Usage

Run the Application:Execute the main script to start the research assistant:
python main.py

Input a Query:When prompted with What can I help you research?, enter a topic or question. The tool will:

Search Wikipedia and DuckDuckGo for relevant information.
Generate a structured response with a summary, sources, and tools used.
Save the output to research_output.txt with a timestamp.

Example Output:The output is saved in research_output.txt in the following format:
--- Research Output ---
Timestamp: 2025-05-21 22:32:45
Topic: Artificial Intelligence
Summary: Artificial Intelligence (AI) refers to the simulation of human intelligence in machines...
Sources: [https://en.wikipedia.org/wiki/Artificial_intelligence, https://www.example.com]
Tools Used: [wikipedia, duckduckgo_search]

Project Structure

main.py: Core script containing the research assistant logic.
tools.py: Custom tools for searching (Wikipedia, DuckDuckGo) and saving outputs.
.env: Environment file for storing the OpenRouter API key.
research_output.txt: Output file for storing research results.
requirements.txt: List of Python dependencies.

How It Works

LangChain: Manages the agent workflow, integrating tools and the language model.
Pydantic: Ensures structured output with defined fields (topic, summary, sources, tools_used).
OpenRouter API: Powers the research assistant with the Google Gemma 3n 4B model for query processing.
Tools:
search_tool: Uses DuckDuckGo to perform web searches.
wiki_tool: Queries Wikipedia for concise, relevant information.
save_tool: Saves the structured output to a text file.

Contributing
Contributions are welcome! Please:

Fork the repository.
Create a feature branch (git checkout -b feature/your-feature).
Commit your changes (git commit -m 'Add your feature').
Push to the branch (git push origin feature/your-feature).
Open a pull request.


# Commands to set up the project

```
git checkout --orphan project/hello-world
git rm -rf .
git status
```

- Install uv
`powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"`

or in Linux
`pip3 install uv`         


`uv --help`

- Add this to your system environment variables:
`UV_LINK_MODE=copy`


- install packages, create virtual environment with uv

- uv init a project
`uv init`

- add the langchain package to the project (it also creates .venv/ folder for virtual environment)
`uv add langchain`

`.venv\Scripts\activate`

- add the langchain-openai package
`uv add langchain-openai`

- [OpenAI](https://docs.langchain.com/oss/python/integrations/providers/openai#openai)

- [Providers](https://docs.langchain.com/oss/python/integrations/providers/all_providers#all-integration-providers)

- Add [.env](https://pypi.org/project/python-dotenv/) package
`uv add python-dotenv`

- Add Formatting packages
`uv add black isort`

- Add open source model package
`uv add langchain-ollama`

```python
from langchain_ollama import OllamaLLM

def main():

    llm = OllamaLLM(model="llama3.1:8b")
    print(llm.invoke("What is the capital of France?"))
```

- Setting your IDE's Python interpreter to use the virtual environment where python-dotenv is installed.

1. Press Ctrl+Shift+P (Command Palette)

2. Type "Python: Select Interpreter"

3. Choose the interpreter from .venv: d:\workspaces\workspace-agentic\langchain-course\.venv\Scripts\python.exe
   
- Run the app
`python.exe main.py`

- Reformat the main.py
`black .`

```
git remote set-url origin https://github.com/yonyu/langchain-projects.git

git branch -M project/hello-world

git push --set-upstream origin project/hello-world
# equivalent to:
git push -u origin project/hello-world

```
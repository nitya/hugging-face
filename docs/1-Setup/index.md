# Setup Environment

Hugging Face is a community for machine learning and artificial intelligence practitioners, with rich open-source tools and resources for developers. The [Hugging Face Hub](https://hf.co/) is the core platform for discovering and exploring _repositories_, _models_, _datasets_, _spaces_ and other features available to developers. Hugging Face also has a number of tools and libraries to support developers:

1. [`huggingface_hub`](https://huggingface.co/docs/huggingface_hub/index) - Python SDK for Hugging Face Hub interactions.
1. [`llm-vscode`](https://marketplace.visualstudio.com/items?itemName=HuggingFace.huggingface-vscode) - VSCode extension to streamline working with LLM backends.
1. [Spaces Dev Mode](https://huggingface.co/blog/spaces-dev-mode) - (for Pro subscribers) connect VSCode to Docker container in Spaces.
1. [Gradio](https://www.gradio.app/guides/quickstart) - Python library for building ML & web application demos rapidly.

To jumpstart development, I setup a [dev container](https://containers.dev) that has all required tools and dependencies pre-configured. Just launch the container in the cloud (with GitHub Codespaces) or on the local device (with Docker Desktop) - and you're ready to code. Let's validate this.

---

## 1. Dev Environment 

This repository is instrumented with a `devcontainer.json` file that pre-installs all Python dependencies listed in the `requirements.txt` file. 

**1.1 | Launch Dev Container:**

To get started, **fork the repo* to your profile, then pick one of these 2 options to launch your development environment:

1. **Use GitHub Codespaces** - launch the dev container in the cloud by selecting `Code > Codespaces > Create New Codespace` from your fork. This launches a codespaces session in a browser tab.
1. **Use Docker Desktop** - clone the forked repo to your local device, open in VS Code. Launch Docker Desktop & select `Reopen in Container` in VS Code (from prompt or command palette).

**1.2 | Validate Setup**:

You should have a Visual Studio Code IDE connected to a runtime that has all required tools and dependencies pre-installed. Open the terminal in VS Code and run the following commands to check:

```bash
# Check Hub Python SDK is installed
pip show huggingface-hub

# Check Hugging Face CLI is installed
hugginface-cli --help
```

**1.3 | Set Env Variables**:

Setup env variables during initial setup by copying the `.env.sample` file to `.env`. 

```bash
cp .env.sample .env
```
We can then populate it with required values as we go (based on labs requirements). If you run in GitHub Codespaces, you will _also_ get any _secrets_ you associated with the repo auto-injected into the dev container runtime.

---

## 2. Learning Resources

Once the development environment is ready, we can start using it to explore various learning resources including:

1. [Open-Source AI Cookbook](https://huggingface.co/learn/cookbook/en/index) - recipes for familiar AI tasks and workflows
1. [Tokenizers](https://huggingface.co/docs/tokenizers/index) - fast, SOTA tokenization for NLP
1. [Datasets](https://huggingface.co/docs/datasets) - library to access and share datasets
1. [Gradio](https://www.gradio.app/docs/) - build applications in a few lines of code 
1. [Inference API](https://huggingface.co/docs/api-inference) - experiment with 200K+ models on serverless tier
1. [Evaluate](https://huggingface.co/docs/evaluate) - assess and report model performance
1. [Distilable](https://distilabel.argilla.io/) - synthesize data for AI and add feedback
1. [Tasks](https://huggingface.co/tasks) - understanding tasks taxonomy for inference

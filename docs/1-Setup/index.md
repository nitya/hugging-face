# Setup Environment

Hugging Face is a community for machine learning and artificial intelligence practitioners, with rich open-source tools and resources for developers. The [Hugging Face Hub](https://hf.co/) is the core platform for discovering and exploring _repositories_, _models_, _datasets_, _spaces_ and other features available to developers. 

---

## 1. Learning Resources

This section tracks resources for hands-on learning and exploration of the platform.

1. [Open-Source AI Cookbook](https://huggingface.co/learn/cookbook/en/index) - recipes for familiar AI tasks and workflows
1. [Tokenizers](https://huggingface.co/docs/tokenizers/index) - fast, SOTA tokenization for NLP
1. [Datasets](https://huggingface.co/docs/datasets) - library to access and share datasets
1. [Gradio](https://www.gradio.app/docs/) - build applications in a few lines of code 
1. [Inference API](https://huggingface.co/docs/api-inference) - experiment with 200K+ models on serverless tier
1. [Evaluate](https://huggingface.co/docs/evaluate) - assess and report model performance
1. [Distilable](https://distilabel.argilla.io/) - synthesize data for AI and add feedback
1. [Tasks](https://huggingface.co/tasks) - understanding tasks taxonomy for inference

## 2. Dev Environment Setup

Before we get started exploring, we need to setup and validate our development environment. This repository is configured with a `devcontainer.json` that pre-installs required dependencies including Visual Studio Code extensions and Python libraries. The latter are `pip`-installed from the `requirements.txt` file.

The **recommended** approach is to launch the dev container in GitHub Codespaces. This has three benefits:

 - Get a cloud-based dev environment we can access from any device
 - Take advantage of GitHub Codespaces secrets for secure, consistent env variables
 - Benefit from richer hardware and configurability for the VM.

### Launch Dev Container

The **alternative** approach is to launch the dev container with Docker Desktop on the local device, from a Visual Studio Code session. This has two benefits:
 
 - Does not require (or use up) GitHub Codespaces quota
 - Can be access and used offline (e.g., with local model deployments) when required

In both cases, the **preferred** development IDE is Visual Studio Code, which is pre-configured in the dev container. Use it in the browser (default for GitHub Codespaces) or from your local device installation (default for Docker Desktop).

### Set Environment Variables
The `.env.sample` file in the repository root describes required env variables for various labs. Copy it to `.env` and populate based on [this guidance](https://huggingface.co/docs/huggingface_hub/package_reference/environment_variables) for a _consistent experience_ (local+cloud).

Any GitHub Codespaces secrets associated with the repo are auto-injected into the dev container for a more secure, effortless experience - but one that works only in the cloud.

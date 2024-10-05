# Setup Environment

Hugging Face is a community for machine learning and artificial intelligence practitioners, with rich open-source tools and resources for developers. The [Hugging Face Hub](https://hf.co/) is the core platform for discovering and exploring _models_, _datasets_, and _apps_ (spaces) maintained by the community. 

In this section we'll validate our development environment to work effectively with the Hub and other Hugging Face tools & resources.

---

## 1. Activate Dev Container

This repository is setup with a `devcontainer.json` that will create a pre-configured development environment for you when activated. 

 - Launch it with GitHub Codespaces (in the cloud)
 - Launch it with Docker Desktop (on local device)

Once the dev container is ready, you can continue on to validate setup.


## 2. Python SDK

The [`huggingface_hub`](https://huggingface.co/docs/huggingface_hub/index) library is the default Python client for working with the Hub capabilities in a code-first manner. It is pre-installed in the devcontainer associated with this repository.

??? info "Validate installation"

    Run the following command in an active Codespaces or Dev Container session:

    ```bash
    pip show huggingface-hub
    ```

    You should see something like this:

    ```bash

    Name: huggingface-hub
    Version: 0.25.1
    Summary: Client library to download and publish models, datasets and other repos on the huggingface.co hub
    Home-page: https://github.com/huggingface/huggingface_hub
    Author: Hugging Face, Inc.
    Author-email: julien@huggingface.co
    License: Apache
    Location: /usr/local/lib/python3.12/site-packages
    Requires: filelock, fsspec, packaging, pyyaml, requests, tqdm, typing-extensions
    Required-by: 
    ```

## 3. Visual Studio Code Extension

The [Hugging Face Extension](https://marketplace.visualstudio.com/items?itemName=HuggingFace.huggingface-vscode) for Visual Studio Code is a great way to interact with the Hub from your development environment. It is pre-installed in the dev container.


??? info "Validate the installation"

    Click the `extensions` icon in the sidebar - or use <kbd>Shift-Cmd-X</kbd> - and verify that the `Dev Container` panel shows the `llm-vscode` extension in the installed list.

    You can now configure the extension to work with different backends including:

    1. Hugging Face Inference API (default)
    1. [Ollama](https://ollama.com/) - get up and running locally with LLMs
    1. openai: any OpenAI compatible API (e.g. [llama-cpp-python](https://github.com/abetlen/llama-cpp-python))
    1. [tgi](https://github.com/huggingface/text-generation-inference): Text Generation Inference

??? info "Authenticate with Hugging Face"

    1. Type this command into the VS Code terminal:
        ```bash
        huggingface-cli login
        ```
    1. Enter your Hugging Face token at the prompt
    1. Type this command to validate the login:
        ```bash
        huggingface-cli whoami
        ```
    1. You should see your username and organizations you belong to, on Hugging Face

??? example "Explore the documentation"

    - Visit [llm-vscode](https://github.com/huggingface/llm-vscode) on GitHub.
    - Read the [Code Llama](https://huggingface.co/blog/codellama#using-vs-code-extension) blog post for an example use case.

## 3. Resources & Documentation

Now that our development environment is setup, we can explore some of these resources to get hands-on experience with the platform and its usage.

1. [Open-Source AI Cookbook](https://huggingface.co/learn/cookbook/en/index) - recipes for familiar AI tasks and workflows
1. [Tokenizers](https://huggingface.co/docs/tokenizers/index) - fast, SOTA tokenization for NLP
1. [Datasets](https://huggingface.co/docs/datasets) - library to access and share datasets
1. [Gradio](https://www.gradio.app/docs/) - build applications in a few lines of code 
1. [Inference API](https://huggingface.co/docs/api-inference) - experiment with 200K+ models on serverless tier
1. [Evaluate](https://huggingface.co/docs/evaluate) - assess and report model performance
1. [Distilable](https://distilabel.argilla.io/) - synthesize data for AI and add feedback
1. [Tasks](https://huggingface.co/tasks) - understanding tasks taxonomy for inference
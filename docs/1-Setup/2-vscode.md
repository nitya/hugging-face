# 2. VS Code Extension

The [Hugging Face Extension](https://marketplace.visualstudio.com/items?itemName=HuggingFace.huggingface-vscode) for Visual Studio Code is a great way to interact with the Hub from your development environment. To get started, validate the extension is installed and log into your Hugging Face account.

??? info "Validate & Authenticate Extension"

    1. Type this command to verify the extension is installed:
        ```bash
        huggingface-cli --help
        ```
    1. Type this command to authenticate with Hugging Face:
        ```bash
        huggingface-cli login
        ```
    1. Enter your Hugging Face token when prompted
    1. Type this command to verify your identity:
        ```bash
        huggingface-cli whoami
        ```
    1. You should see: your Hugging Face username and organizations

## 2.1 Configure Extension

We can now configure the extension to work with different backends including:

1. Hugging Face Inference API (default)
1. [Ollama](https://ollama.com/) - get up and running locally with LLMs
1. openai: any OpenAI compatible API (e.g. [llama-cpp-python](https://github.com/abetlen/llama-cpp-python))
1. [tgi](https://github.com/huggingface/text-generation-inference): Text Generation Inference

??? task "TODO → Explore this further"

    - Read the [llm-vscode docs](https://github.com/huggingface/llm-vscode) on GitHub.
    - Read the [Code Llama blog post](https://huggingface.co/blog/codellama#using-vs-code-extension) for an example use case.

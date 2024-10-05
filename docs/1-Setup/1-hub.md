# 1. Hub Python SDK

The [`huggingface_hub`](https://huggingface.co/docs/huggingface_hub/index) library is the default Python client for working with the Hub capabilities in a code-first manner. Once you launch the dev container (previous step) you should have the relevant library and CLI available locally. Just validate it and add any optional dependencies you need.

??? task "Validate package installation"

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

??? task "Review optional packages"

    The following are optional dependencies for the `huggingface_hub`. Install what you need, as you need it. 
    
    - `cli` → provide a more convenient CLI interface for huggingface_hub.
    - `fastai`, `torch`, `tensorflow` → dependencies to run framework-specific features.
    - `dev` → dependencies to contribute to back to the lib. Includes
        - `testing` (to run tests), 
        - `typing` (to run type checker) 
        - `quality` (to run linters).

    To install use the following command with the select subset. (The `cli` is already installed) 

    ```bash
    pip install huggingface-hub[cli,fastai,torch,tensorflow,dev]
    ```

??? task "Validate usage with test command"

    Run the following command in the terminal:

    ```bash
    python -c "from huggingface_hub import model_info; print(model_info('gpt2'))"
    ```

    You should see output like this, validing the library is working:

    ```bash
    ModelInfo(id='openai-community/gpt2', author='openai-community', ...)
    ```

??? task "Configure environment variables"

    The repo has a `.env.sample` with environment variables required for various labs, including those using the Hugging Face Hub. Copy that a `.env` file and populate it with the relevant values as you go through the labs - the file provides links to relevant guidance. **The `.env` file is git-ignored to prevent sensitive secrets getting checked in.**

    ```bash
    cp .env.sample .env
    ```


!!! info "Hugging Face Hub Docs"

    We can now start exploring the Hugging Face hub capabilities using these resources:

    - [Conceptual guides](https://huggingface.co/docs/huggingface_hub/concepts/git_vs_http) - high-level explainers of the Hub features.
    - [API reference](https://huggingface.co/docs/huggingface_hub/package_reference/overview) - `huggingface_hub` package classes and methods.
    - [How-to guides](https://huggingface.co/docs/huggingface_hub/guides/overview) - practical guides for achieving core tasks

--- 

Each lab below has a notebook in this repo with links to relevant docs.

1. 
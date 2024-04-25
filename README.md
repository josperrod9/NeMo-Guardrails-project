# Set Up

NeMo Guardrails is written in Python, so we chose to use pip to install the toolkits and kept our sandbox in a virtual environment (ve) using venv. If you prefer to use a container or anything else, then set that up and skip the instructions for creating a ve. After creating a directory for your project, create the ve there and install all necessary packages. We will be using OpenAI’s text-davinci-003 as our LLM for both examples, so we also installed the openai package. If you choose to use OpenAI's models, you will need an API key. It is pretty simple to do so.

## Getting an OpenAI API Key

1. Go to [platform.openai.com](https://platform.openai.com) and sign in to your account.
2. In your profile dropdown menu, click on ‘View API Keys’.
3. Click on ‘API Keys’, then on ‘Create New Secret Key’.
4. Name and save your key, then exit.

## Installing Packages in a Virtual Environment

```bash
mkdir my_project
cd my_project

python -m venv venv
source venv/bin/activate

pip install nemoguardrails
pip install openai

export OPENAI_API_KEY=<paste your key here>
```

Now, if all went well, the guardrails CLI should be ready to use. To test this out:

```bash
nemoguardrails --help
```

If you want to test with Local LLM, read the [official documentation](https://github.com/NVIDIA/NeMo-Guardrails).

To deploy as a server with UI use the following command:

```bash
nemoguardrails server --config abc --auto-reload
```
The `abc` refers to the folder name where the configuration is stored, but you can replace it with any other config folder name.

Related Links:
- [LLM Guardrails Ultimate Guide](https://medium.com/@jaykumaran2217/llm-guardrails-ultimate-guide-4559d3a850ca)
- [How To Build Better Conversational Apps with NeMo Guardrails](https://medium.com/enfuse-io/how-to-build-better-conversational-apps-with-nemo-guardrails-6cbe7a9d9964#b0bb)




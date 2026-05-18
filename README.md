# R + LLM demo

Instructions how to use VSCode to connect an AI agent with a LLM via API.

# VSCode 
Get VSCode: https://code.visualstudio.com/download


# Install an AI agent in VSCode

## RooCode

[Roo Code GitHub](https://github.com/RooCodeInc/Roo-Code).

<img width="500"  alt="roocode-extension" src="https://github.com/user-attachments/assets/72ecc72d-1a46-47d8-9774-499de17cc0df" />

## Cline

Alternative to RooCode is Cline.

[Cline Open Coding Agent](https://cline.bot/)

<img width="500"  alt="cline-in-vscode" src="https://github.com/user-attachments/assets/7f4ad3d2-8f99-4577-ba9b-2442a94d3d99" />


# Configure API access to the local models

API access info and setup in Roo in VSCode for the different local models we have running. The available models are now all through gpt.uio.no. 

<img width="500" height="418" alt="roocode-api-config" src="https://github.com/user-attachments/assets/f4cfbb4e-2e75-49dc-bd58-0811f17f6c3a" />


## Models at NTNU through gpt.uio.no
You get your personal **API key** through the new functionality in gpt.uio.no

1. Find it under your username top right corner.
2. If you do not already have a valid key, click "Generate new key" to get your key!

<img width="500" alt="How to find API keys" src="https://github.com/user-attachments/assets/f15a08a2-36b6-403c-813f-4905bc2d9bf8" />

There are two types of keys, one for models supporting red data and one for models supporting up to yellow data.

Click on the model that you want to use, and you will find the information that you need to connect your application with the model via API, which will be minimally the base-url and the model name. 

<img width="500" alt="model-api-info" src="https://github.com/user-attachments/assets/a6629147-d667-400c-94f0-7f4893923b3c" />


### Base URL
```https://gpt.uio.no/api/v1/```
  
### Modell names for the local models at NTNU
Supports either up to yellow or red data: 

- `zai-org/GLM-4.7-FP8` 
- `moonshotai/Kimi-K2.5` 
- `moonshotai/Kimi-K2.6` 
- `mistralai/Mistral-Large-3-675B-Instruct-2512-NVFP4` 
- `NorwAI/NorwAI-Magistral-24B-reasoning` 
- `multilingual-e5-large-instruct` 
- `gpt-oss-120b`

## Azure model names - models running in Microsoft Azure cloud

Support up to yellow data:

- `gpt-5.2-codex`
- `gpt-5`
- `gpt-5-mini`
- `gpt-5.1`


## Check that your API key is working

First generate a token at gpt.uio.no if you don't have one already. Copy it to your clipboard. Then in a terminal do:

```
export GPT_TOKEN=<paste-in-your-token>
curl -H "authorization: Bearer ${GPT_TOKEN}" https://gpt.uio.no/api/v1/models
```

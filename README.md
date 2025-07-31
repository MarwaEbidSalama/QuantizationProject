# QuantizationProject

This code repo contains the files for the module "AI and its Applications" and for the final assingment (summer semester 2025). This project is about quantizing open-source LLMs with different quantization alorihtms, and to benchmark each LLM. The LLM should be run on the Jetson Nano Development Kit with only 4GB of RAM.

## Jetson Nano Development Kit
- 4GB LPDDR4 RAM
- Maxwell Architecture GPU
- CUDA 10.2
- Ubuntu 18.02
- Python 3.6
- Quad Core Processor

Link to the docu: https://www.nvidia.com/de-de/autonomous-machines/embedded-systems/jetson-nano/product-development/ 

## LLMs Chosen 
- TinyLLama
- Phi 1.5
- Gemma-3
- Flan-T5

## Quantization Methods
- GPTQ
- BitsAndBytes
- SpQR
- AWQ
- GGUF Llama-quantize
- ONNX RUntime Quantization

## Benchmark Files
- txt files are the output of running tegrastats on the Jetson nano
- csv files contain the data from the tegrastats so that they can be processed furhter
- LLM_Benchmarks.ipynb contains the data analysis code for evaluating the LLMs on Jetson Nano
- LLM_Benchmarks.ipynb adds average RAM consumption for each model variant (I am aware that adding another file verion (with (1) for example is not the right way; usually you would simply add those things in the original file)
- Note: LLM_Benchmarks.ipynb can be run in Google Colab for example. It can be the case that the CSV files must be added /uploaded manually into Colab workspace and that the path of pandas import needs to be adjusted

## New_2_Quantize_tinyLlama (3).ipynb File
- Qunantize using SpQR 
- If an error occurs on the Git Website that this is an invalid Notebook, download the notebook and open in an code editor of your choice, for example Google Colab.
- The Code was executed with T4 GPU on Google Colab 
- If you want to run, ensure GPU is selected. Simply run all cells one after another

## Running Models on Jetson Nano
- navigate into home directory
- go into the folder ollama-models
- run command ``ollama list`` which will show you all models available
- to run one model, use ``ollama run model_name --verbose`` and replace model_name with a name that is listed in ``ollama list`` command 
- you will be able to chat with the model


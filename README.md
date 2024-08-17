# AI Doctor Chatbot


---


This project involves creating an AI doctor chatbot powered by a fine-tuned Llama model. The chatbot offers detailed medical information and advice by leveraging a pre-trained Llama model, fine-tuned with a specialized medical dataset. This approach enables the chatbot to understand and respond accurately to user queries about various medical conditions.

## Key Features

- **Pre-trained Model**: Utilizes a pre-trained Llama model, which is initially trained on a broad dataset.
- **Fine-Tuning**: The model is fine-tuned with a specialized medical dataset to enhance its accuracy in providing medical advice.
- **Medical Information**: Provides detailed and relevant responses to health-related queries, based on the fine-tuned model’s knowledge.

## Setup Instructions

### Prerequisites

Ensure you have the following libraries installed:

- `transformers`
- `datasets`
- `torch`
- `trl`
- `peft`
- `bitsandbytes`
- `huggingface_hub`

Install the required libraries using:

```bash
pip install transformers datasets torch trl peft bitsandbytes huggingface_hub
```

### Loading the Model

1. **Load the Pre-trained Model**: Use the `AutoModelForCausalLM` from the `transformers` library to load the pre-trained Llama model.
2. **Configure Quantization**: Apply quantization settings if needed (e.g., 4-bit quantization).

### Loading the Tokenizer

1. **Load the Tokenizer**: Use `AutoTokenizer` to load the tokenizer corresponding to the Llama model.
2. **Configuration**: Set padding and special tokens if required.

### Fine-Tuning the Model

1. **Set Training Arguments**: Define training parameters such as batch size and number of steps.
2. **Create the Trainer**: Use `SFTTrainer` to set up the fine-tuning process with the medical dataset and training arguments.
3. **Train the Model**: Execute the training process to fine-tune the model with the medical dataset.

### Using the Chatbot

1. **Interact with the Model**: Utilize the fine-tuned model to generate responses to user queries related to medical conditions.
2. **Generate Text**: Use the text generation pipeline to obtain and display responses.

## Usage

After setting up, you can interact with the chatbot to get detailed medical advice. Simply input a medical query, and the chatbot will provide a relevant response based on its training.

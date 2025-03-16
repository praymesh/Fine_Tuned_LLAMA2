# **Fine-Tuning LLaMA2-7B Chat on the Puffin Dataset**

## **Introduction**
I have fine-tuned the **LLaMA2-7B Chat** model using the **Puffin Dataset**.

- **Model**: [Meta's LLaMA-2-7B-Chat](https://huggingface.co/meta-llama/Llama-2-7b-chat-hf)
- **Dataset**: [Puffin Dataset](https://huggingface.co/datasets/LDJnr/Puffin)
- **Transformed Dataset**: `transformed_dataset.txt`

The **Puffin Dataset** is known for fine-tuning models to generate creative and humorous responses. The dataset was modified to fit the **LLaMA2 prompt template** manually by me .

## **Training Setup**
- **Platform**: Google Colab -Free Version
- **Steps Performed**: **250 steps** (less than 1 epoch due to RAM limitations, couldnt train the model cuz the dataset had 3000 examples)
- **Quantization**: **4-bit quantization** using `bitsandbytes` for memory efficiency
- **Parameter Efficient Fine-Tuning (PEFT)**: Applied to reduce the number of trainable parameters and enable efficient adaptation

## **Training Strategy**
Due to limited hardware, the following optimizations were implemented:
- **Quantization**: 4-bit quantization with `bitsandbytes`
- **LoRA (Low-Rank Adaptation)**: Used for fine-tuning to reduce memory consumption
- **Gradient Accumulation**: Implemented to simulate larger batch sizes
  

## **Next Steps**
- Train for **more steps** using a better hardware setup
- Experiment with **different learning rates** and hyperparameters
- Evaluate model performance on **creative text generation tasks**
- Deploy the fine-tuned model for real-world usage


## **Acknowledgments**
- **Meta AI** ,**Hugging Face** ,**Google Colab**



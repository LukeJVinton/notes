# LLM vRAM requirements

https://huggingface.co/blog/optimize-llm

Following from HF:

    - GPT3 requires 2 * 175 GB = 350 GB VRAM
    - Bloom requires 2 * 176 GB = 352 GB VRAM
    - Llama-2-70b requires 2 * 70 GB = 140 GB VRAM
    - Falcon-40b requires 2 * 40 GB = 80 GB VRAM
    - MPT-30b requires 2 * 30 GB = 60 GB VRAM
    - bigcode/starcoder requires 2 * 15.5 = 31 GB VRAM

Rule of thumb: to load models in float16 takes VRAM GBs equal to twice the model size. 

Most models are trained in float16 precision.

For other precisions the rule goes as:

    - float32 -> 4x
    - 8bit -> 1x
    - 4bit -> ~1/2 x (+ a bit)

Quantising often **increases** inference time as more calculations are required to de-quantise and quantise. 

#LLM 
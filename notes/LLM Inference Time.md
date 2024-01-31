# LLM Inference Time

Query = "Hello! What is the best recipee for eggs?"
### GPU
```
llama_print_timings:        load time =  5213.54 ms
llama_print_timings:      sample time =   290.49 ms /   841 runs   (    0.35 ms per token,  2895.11 tokens per second)
llama_print_timings: prompt eval time =  5213.11 ms /    32 tokens (  162.91 ms per token,     6.14 tokens per second)
llama_print_timings:        eval time =  9563.92 ms /   840 runs   (   11.39 ms per token,    87.83 tokens per second)
llama_print_timings:       total time = 15208.89 ms
```

### CPU
```
llama_print_timings:        load time =  1446.64 ms
llama_print_timings:      sample time =   271.72 ms /   727 runs   (    0.37 ms per token,  2675.52 tokens per second)
llama_print_timings: prompt eval time =  1446.22 ms /    32 tokens (   45.19 ms per token,    22.13 tokens per second)
llama_print_timings:        eval time = 76192.76 ms /   726 runs   (  104.95 ms per token,     9.53 tokens per second)
llama_print_timings:       total time = 78047.89 ms
```

### Comparison
Total times: GPU - 15s, CPU - 78s 
--> GPU is ~5x faster


# Further studies:
https://azure.microsoft.com/en-us/blog/gpus-vs-cpus-for-deployment-of-deep-learning-models/

#LLM
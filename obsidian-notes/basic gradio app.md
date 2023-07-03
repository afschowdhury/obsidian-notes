#gradio 

```python 
import gradio as gr

  
  

demo = gr.Interface(fn=get_answer, inputs="text", outputs="text")

  

 demo.launch()
```

the main component is `gr.Interface()`

[[gradio Interface Class]]]
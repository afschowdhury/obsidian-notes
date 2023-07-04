#gradio 

it has three parameters


The core `Interface` class is initialized with three required parameters:

-   `fn`: the function to wrap a UI around
-   `inputs`: which component(s) to use for the input (e.g. `"text"`, `"image"` or `"audio"`)
-   `outputs`: which component(s) to use for the output (e.g. `"text"`, `"image"` or `"label"`)
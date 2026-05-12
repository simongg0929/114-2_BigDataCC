# Exercises
## EX01
```
import gradio as gr def greet(name): 	return "你好: " + name + "!" 	app = gr.Interface(fn=greet, 					inputs="text", 			outputs="text") 
app.launch()
```
## EX02
```
inputs = gr.Textbox(lines=2, placeholder="請輸入姓名..." label="請輸入使用者姓名") outputs = gr.Label() examples = ["陳會安", "江小魚"] app = gr.Interface(fn=greet, inputs=inputs, outputs=outputs, examples=examples, title = "歡迎使用者", description = "輸入姓名顯示歡迎訊息") app.launch()
```


## EX03

```
def greet(name, is_lady, fahrenheit): 	if is_lady: greeting = name + "女士你好!" 
	else: greeting = name + "男士你好!"  	greeting += "今天溫度是華氏: " + str(fahrenheit) 	celsius = (fahrenheit - 32) * 5 / 9 	return greeting, round(celsius, 2) app = gr.Interface(fn=greet, inputs=["text", "checkbox", gr.Slider(0, 100)], 		outputs=["text", "number"]) app.launch()
```


# Software installation
## Download Miniconda

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

## Install Miniconda
```
bash Miniconda3-latest-Linux-x86_64.sh
```

## Setting Path for Miniconda

```
vi ~/.bashrc
```

add the following content into .bashrc file.

```
export PATH="$HOME/miniconda3/bin:$PATH"
```

## Validate the installation
```
conda --version
```

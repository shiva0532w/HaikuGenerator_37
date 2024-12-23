# HaikuGenerator_37


contribution by the team members:
suram shiva - se22uari169 -- 35 percent
maddu yashwanth - se22uari187 -- 25  percent 
kacham ashish - se22uari064 -- 20   percent
dharani - se22uari149 -- 20 percent

yashwanth,ashish, dharani did the dataset preparation.
suram shiva and yashwanth did the complete model traning 
suram shiva done the coding work 

code:-
please install all the modules needed for the project. we did the code in the kaggle so please make sure you  do the same.
// just ignore the error that you kget  like the name errors etc.. the still works if you try to rectify the code it will become worse
There are two projects but both of them are the haiku generator haiku generators. with two different ways.

**Process of Working:**
**The haiku(1)** 
You need another dataset to run the code that is the >25MB so i can't upload it in the github iam keepin the link for the file in a one drive and the onedrive link is         https://mahindraecolecentrale-my.sharepoint.com/:f:/g/personal/se22uari169_mahindrauniversity_edu_in/EvRjkHTVXc5GvfbE2X0aeMkBmKSYgNScnR47gxCQpzm1-Q?e=HNGF4Z

please upload the dataset in the haiku(1)

**haiku_2**
to run this code you need to do it in the kaggle itself. the dataset for  this generator is the dasaset which is in the github itself.
please make sure you install all the modules.

*** Setup and Requirements ***
Install Required Libraries - 
pip install torch torchvision torchaudio
pip install transformers
pip install pandas
pip install bitsandbytes
pip install huggingface-hub

*** Prepare the Environment - ***
-Save the files haiku-2nd.ipynb or haiku(1).ipynb to a directory on your system.
-Include the datasets (final_dataset.json and any associated text files) in the same directory.

*** Dataset Preparation - ***
Load the dataset from the provided JSON file (final_dataset.json) by placing it in the same directory.
Dataset structure - 
[
    {
        "Question": "What is the role of AI in art?",
        "Haiku": "Brush of code creates..."
    },
    ...
]

*** Running the Notebook - ***
jupyter notebook haiku(1).ipynb
           or
jupyter notebook haiku-2nd.ipynb

***Testing on the Provided Range - ***
To test a specific range of data from the dataset (e.g., iloc: 44:45, 1:2):
Load the dataset into a DataFrame:
command - 
import pandas as pd
data = pd.read_json("final_dataset.json")
Select the desired range:
command - 
subset = data.iloc[44:45, 1:2]
print(subset)
Pass the selected question as input to the haiku generator:
command - 
prompt = subset["Question"].iloc[0]
generated_haiku = generate_haiku(prompt, model, tokenizer)
print(generated_haiku)


*** Save the Model - ***
save the trained model for reuse:
command - 
trainer.save_model("haiku-generator")

*** load the model later - ***
command - 
from transformers import AutoModelForCausalLM, AutoTokenizer
model = AutoModelForCausalLM.from_pretrained("haiku-generator")
tokenizer = AutoTokenizer.from_pretrained("haiku-generator")

*** Common Issues and Solutions - ***
- Missing Libraries
Reinstall the missing library:
pip install <library_name>

- Dataset Errors
Ensure the dataset is correctly formatted and paths are accurate.
- CUDA Errors
Check CUDA compatibility or switch to CPU by modifying the device setting:
command - 
device = "cpu"
model.to(device)

















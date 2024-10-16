# Workshop - Prototyping an LLM-powered App for #herHACK20.24 female-led hackathon

In this hands-on workshop you will learn how to create and deploy your very own LLM-powered app using Streamlit and OpenAI API, and explore the possibilities of taking it to the cloud.

As the result you will build and deploy a similar [Streamlit app](https://herhack2024llm.streamlit.app/)  which allows users to upload text articles and ask questions about the content of these articles. It uses OpenAI's GPT model to generate answers, providing an interactive way to explore information within documents.


📅 Tuesday, October, 15  
🕘17:30–19:30 CET   
📍Online via Zoom  
🎯Who: participants with no or basic knowledge of Python and already have a GitHub account+ Python IDE installed (VSCode or PyCharm).  
📊 Slides: can be found [here](slides/HerHack20.24%20-%20Prototyping%20an%20LLM-Powered%20App.pdf)  
🎥 Recording of this workshop with step-by-step instructions is [here](https://drive.google.com/drive/folders/1NqHAuTIQxZ15qqkFqq_9cUaH53-eu2Fk?usp=sharing)

## 1) Who is this workshop directed to?

This workshop is for anyone who wants to learn how to build the data applications from scratch without prior front-end knowledge. We will explore how to turn Python scripts into shareable web apps in minutes.

You might be able to relate to one of the following scenarios:

1. You have a business problem (or hackathon challenge) and a lot of text data. You want to chat with this data and create an interactive chatbot to share with stakeholders.

2. Your code perform well on your laptop and you want the general public to benefit from it.

3. You want to build your own powerful generative AI app and don’t know where to start.

4. Ideally you know some basic Python. But if not, we’ll guide you through the learning process step by step.

## 2) Structure of the Repo 

- For the general information and clarifications you can refer to [slides](slides/HerHack20.24%20-%20Prototyping%20an%20LLM-Powered%20App.pdf). You can find all the links in slides as well. 
- Your first step would be to run "Hello World" of Streamlit and open a local tunnel from Colab. All the files and instructions for this, as well as solutions, are located in [notebooks](notebooks) folder.
- There are several files in this folder:
  - `app.py` - This is a Python script, using Streamlit package to build a web application that allows users to upload text or markdown articles and ask questions about the content using OpenAI’s GPT-3.5 model.
  - `requirements.txt` - The requirements.txt file lists the necessary dependencies to run the Streamlit app, including libraries such as streamlit for building the web interface and openai for integrating GPT models. Other required libraries may include those related to file handling, text processing, and any additional components the app relies on for functionality. This file ensures that all required packages are installed in the environment.
  - `.gitignore` - file specifies which files and directories should be excluded from version control in Git, such as sensitive data (e.g., API keys), environment files, or unnecessary build artifacts. More information can be found in [git docs](https://git-scm.com/docs/gitignore).

## 3) App Overwiev and Deployment 


### Features

- Upload text or markdown files and ask the app to answer questions based on the content.
- Secure input for OpenAI API keys with a sidebar widget.
- Interactive questioning with enabled/disabled state based on file upload status.

### How to Use

1. **Get an OpenAI API Key:** If you do not already have one, obtain an OpenAI API key by [creating an account here](https://platform.openai.com/account/api-keys).
2. **Run the Streamlit App:** Follow the instructions provided in the next section. 
 
### Deploy to Streamlit Cloud

If you don't have your own app ready, you can download this 
[template streamlit app](app.py) and try out the deployment with it.

Streamlit Cloud will fetch all the files required for the app deployment from Github, so first of all, we need to ensure that everything is available in a public repo.
The instructions below are adapted from the official [Streamlit documentation](https://docs.streamlit.io/streamlit-cloud/get-started/deploy-an-app).

### 1) Set up your Github repo 

**Note**: This first part is only relevant, if you haven't created a Github repo for this mini project yet.

- If you do not have a git folder set up yet, create a new directory and save your app script (``qa_bot_app.py``) and the data file(s) in this folder. ``cd`` into it and initialize a git folder:

```bash
    mkdir my-qa-app
    cd my-qa-app
    git init
```

- If you haven't already done so, create a public Github repo for your app (suggested name: my-qa-app). Connect this repo to your local git folder and push the files to Github.

```bash
    git commit -m "first commit"
    git remote add origin git@github.com:<user_name>/<repo_name>.git
    git push
```
### 2) Create and test the requirements file ##

- Use a text editor to create a file named `requirements.txt`, which will contain information on all the packages required to run your project. 
For example, if you're using the template streamlit app, write the lines below in it and save it in your git folder.

```bash
streamlit
openai
```

- Test if your app runs in a new environment, with only the packages listed in your requirements file.
- Once everything works fine, commit and push the new/modified files to Github.

### 3) Deploy the app to the Streamlit Cloud ##


- Log in to Streamlit with your Github account [here](https://share.streamlit.io/).

- Click on the button ``Create app`` and enter the repository name, branch and main file path (to your app.py file).

- Go to ``Advanced settings...`` and choose the Python version that you need for your app.

- Click ``Deploy!`` and watch your app launch. It is now hosted in the cloud so you can share the assigned streamlit link with others.

### 4) Optional: Showcase your app ##


- Brush up the Github repo to make it more attractive and understandable: Adapt the README file to explain your work, add a screenshot of your app, etc.

- Get acquainted with the vibrant online data and LLM community by posting about your app. Include a screenshot of your app and a link to your Github repo. 
- Feel free to tag [Constructor Academy](https://www.linkedin.com/school/constructor-academy/) and [@streamlit](https://twitter.com/streamlit?lang=en).




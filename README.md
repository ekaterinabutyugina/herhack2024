# ChatGPT Q&A Streamlit App

This [Streamlit app](https://herhack2024llm.streamlit.app/) allows users to upload text articles and ask questions about the content of these articles. It uses OpenAI's GPT model to generate answers, providing an interactive way to explore information within documents.

## Features

- Upload text or markdown files and ask the app to answer questions based on the content.
- Secure input for OpenAI API keys with a sidebar widget.
- Interactive questioning with enabled/disabled state based on file upload status.

## How to Use

1. **Get an OpenAI API Key:** If you do not already have one, obtain an OpenAI API key by [creating an account here](https://platform.openai.com/account/api-keys).
2. **Run the Streamlit App:** Follow the instructions provided in the next section. 
 

If you don't have your own app ready, you can download this 
[template streamlit app](qa_bot_app.py) and try out the deployment with it.

Streamlit Cloud will fetch all the files required for the app deployment from Github, so first of all, we need to ensure that everything is available in a public repo.
The instructions below are adapted from the official [Streamlit documentation](https://docs.streamlit.io/streamlit-cloud/get-started/deploy-an-app).

## 1) Set up your Github repo ##

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
## 2) Create and test the requirements file ##

- Use a text editor to create a file named `requirements.txt`, which will contain information on all the packages required to run your project. 
For example, if you're using the template streamlit app, write the lines below in it and save it in your git folder.

```bash
streamlit>=1.26.0
langchain>=0.0.217
openai<1.0.0
duckduckgo-search
streamlit-feedback
```

- Test if your app runs in a new environment, with only the packages listed in your requirements file.
- Once everything works fine, commit and push the new/modified files to Github.

## 3) Deploy the app to the Streamlit Cloud ##


- Log in to Streamlit with your Github account [here](https://share.streamlit.io/).

- Click on the button ``New app`` and enter the repository name, branch and main file path (to your app.py file).

- Go to ``Advanced settings...`` and choose the Python version that you need for your app.

- Click ``Deploy!`` and watch your app launch. It is now hosted in the cloud so you can share the assigned streamlit link with others.

## 4) Optional: Showcase your app ##


- Brush up the Github repo to make it more attractive and understandable: Adapt the README file to explain your work, add a screenshot of your app, etc.

- Get acquainted with the vibrant online data and LLM community by posting about your app. Include a screenshot of your app and a link to your Github repo. 
- Feel free to tag [COLearning](https://www.linkedin.com/school/constructor-learning/) and [@streamlit](https://twitter.com/streamlit?lang=en).




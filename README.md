# Comp3608Project

# Dependencies
* Python3/pip3
* Packages listed in requirements.txt

# Installing Dependencies
```bash
$ pip install -r requirements.txt
```

## Usage with GitHub Codespaces
GitHub Codespaces allows you to spin up a fully configured development environment directly within your browser, making it easy to run Jupyter notebooks without any local setup. Here's how to use GitHub Codespaces with this repository:

1. Click on the "Code" button and select "Open with Codespaces".
2. GitHub will create a new Codespace for you and launch it in your browser.
3. Once the Codespace is ready, create a vritual environment:
   ```bash
   $ python3 -m venv venv
   ```
   - OR by pressing control + shift + p, then type "Python", you should see an option to create a virtual environment, then choose desired version of python interpretor.
   - you can check the box for requirements.txt, after selecting your interpretor, or just press "OK" and run the pip command after the venv is set up
5. Go to either `Test1, Test2 or Test3` and run the desired Jupyter notebook.

## Contents
- `data/`: Contains the dataset files.
- `Test1, Test2 & Test3`: Jupyter notebooks for data exploration, preprocessing, modeling, and evaluation.
- `requirements.txt`: List of Python packages required to run the notebooks.

# Contacts App

## Setup

### Install from repo

- Based on book [Hypermedia Systems](https://hypermedia.systems/) by Carson Gross, Adam Stepinski, and Deniz Akşimşek; and their example app copied from [bigskysoftware / contact-app](https://github.com/bigskysoftware/contact-app)
- If you are working from this repo (I'm going step by step, from the original "Web 1.0" hypermedia version onwards), then open a system terminal and do the following (I'm on Linux Ubuntu with Python 3.8.10):

```bash
victor@victorpc:dev$ mkdir contact-app
victor@victorpc:dev$ cd contact-app
victor@victorpc:contact-app$ ls -l
total 0
victor@victorpc:contact-app$
```

- copy in all files from repo (except .git dir)
- add in our .vscode

```bash
victor@victorpc:contact-app$ cat .gitignore
env
.venv
__pycache__
/venv/
victor@victorpc:contact-app$
```

- add in our .vscode/settings.json

```bash

victor@victorpc:contact-app$ cat .vscode/settings.json
{
  "workbench.preferredDarkColorTheme": "Default Dark Modern",
  "workbench.colorTheme": "Noctis Azureus",
  "[python]": {
    "editor.defaultFormatter": "ms-python.black-formatter"
  },
  "python.formatting.provider": "none"
}
```

- In the terminal, do

```bash
code .
```

### Open a terminal within VS Code to create virtual environment

```bash
victor@victorpc:contact-app$ python3 -m venv .venv
```

- Perform `developer reload window` from command palette
- now there appears a yellow warning on bash label in upper bar of terminal; hover over, and click on relaunch terminal link at bottom
- If the Terminal doesn't restart, do a Terminal / New Terminal, should see (.venv) prefix showing environment activated:
- `(.venv) victor@victorpc:contact-app$`

### Install Flask and other dependencies

```bash
(.venv) victor@victorpc:contact-app$ pip install -r requirements.txt
```

### Run app!

- Open app.py in the editor (recognized as python program)
- To run:
  - From menu: Run > Run without debugging
  - right button then select "Run Python file in Terminal"
  - or open another terminal and type `(.venv) victor@victorpc:contact-app$ /home/victor/Work/Learn/Python/HypermediaSystemsBook/dev/contact-app/.venv/bin/python /home/victor/Work/Learn/Python/HypermediaSystemsBook/dev/contact-app/app.py`
    - or simply `python app.py`

### View in browser

- Point browser at `http://127.0.0.1:5000`, it redirects to `http://127.0.0.1:5000/contacts` and the contacts are listed on the page

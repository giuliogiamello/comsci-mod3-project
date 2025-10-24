# comsci-mod3-project

Today is `2025/10/24`, I already installed ROOT (see [Cern-ROOT](https://github.com/giuliogiamello/Cern-ROOT)), now I need to install `jupyter-notebook`.
The prof told us to install it globally from here: [statistical-data-analysis/howto/root_on_wsl.md at main · gabriele-sirri/statistical-data-analysis](https://github.com/gabriele-sirri/statistical-data-analysis/blob/main/howto/root_on_wsl.md).
I prefer to use it inside a virtual environment.
In more detail:

## Create venv and use jupyter in venv

- [Create virtual environment in Python](https://www.geeksforgeeks.org/create-virtual-environment-using-venv-python/)
- [Using Jupyter Notebook in Virtual Environment](https://www.geeksforgeeks.org/using-jupyter-notebook-in-virtual-environment/)

I created the directory `comsci-mod3-project` in the path: `/home/jamal/giulioDATA/Link to IMAPP-Bologna/IMAPP-03-03_Computer science for High energy physics/comsci/comsci-mod3`

```bash
mkdir comsci-mod3-project
```

- to create a virtual environment (`venv`) inside the directory `comsci-mod3-project`, move into it

```bash
cd /home/jamal/giulioDATA/Link to IMAPP-Bologna/IMAPP-03-03_Computer science for High energy physics/comsci/comsci-mod3comsci-mod3-project
```

- create the `venv` (`mod3_venv` is the name I chosed)

```bash
python -m venv mod3_venv
```

- activate the `venv` with

```bash
source mod3_venv/bin/activate
```

Now the virtual environment is active. 

- to deactivate (still from inside the directory all'interno della cartella `comsci-mod3-project`):

```bash
deactivate
```

In order to use `jupyter-notebook` inside the `venv`, you need to install it inside it, so:

- **while the`venv` is active** (still from inside the directory all'interno della cartella `comsci-mod3-project`, you should see something like: `(mod3_venv) jamal@jpc:...etc...` where `(mod3_venv)` means the `venv` is active) install jupyter

```bash
pip install jupyter notebook
```

- run it with`jupyter-notebook` (or with `jupyter notebook`) from your terminal.

To check which`jupyter-notebook` you are currently using (meaning, to check you are using the one inside the `venv`)

- (execute this command from inside the `venv`, with `jupyter notebook` **not** running)

```bash
which jupyter-notebook
```

- the output should look like:

```bash
(mod3_venv) jamal@jpc:~/.../comsci-mod3/comsci-mod3-project$ which jupyter-notebook
/home/jamal/giulioDATA/universita/jam_universita/Testi_e_appunti/IMAPP/IMAPP-Bologna/IMAPP-03-03_Computer science for High energy physics/comsci/comsci-mod3/comsci-mod3-project/mod3_venv/bin/jupyter-notebook
```

## Use the venv with VSCode

(See [Python environments in VS Code](https://code.visualstudio.com/docs/python/environments))

- open VSCode
- open the folder you want to work in (`comsci-mod3-project`)
- `Ctrl`+`Shift`+`p` to show all commands
- search for: "Python: Select Interpreter"
- select your `venv` (like `Python 3.12.3 (mod3_venv) ./mod3_venv/bin/python`)
- press `Enter`
- to check the `venv` was activated correctly, open a terminal inside VSCode and write:

```bash
which python
```

- the output should look like:

```bash
(mod3_venv) jamal@jpc:~/.../comsci-mod3/comsci-mod3-project$ which python
/home/jamal/giulioDATA/universita/jam_universita/Testi_e_appunti/IMAPP/IMAPP-Bologna/IMAPP-03-03_Computer science for High energy physics/comsci/comsci-mod3/comsci-mod3-project/mod3_venv/bin/python
```

## Use jupyter in a venv with VSCode

- See [Jupyter Notebooks in VS Code](https://code.visualstudio.com/docs/datascience/jupyter-notebooks)

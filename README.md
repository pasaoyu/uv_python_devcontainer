## Python Dev Env with Devcontainer & uv
This guide assumes you are using VSCode.

### 1. Start Devcontainer
Launch the Devcontainer by clicking `Reopen in Container` at the bottom left of VSCode.<br> 
This will start a Debian container with uv pre-installed.<br>

### 2. Initialize uv
Run the following command to initialize uv for Python:<br>
```
uv init --python x.x
```
(replace x.x with your required Python version)

### 3. Sync the Environment
Run the following command to sync the environment:
```
uv sync
```

### 4. Activate venv
Activate the virtual environment with:
```
. .venv/bin/activate

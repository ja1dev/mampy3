# mampy3 - Portable Python Environment for Windows

Portable Miniforge3 + Mamba + Python 3.11 environment for Windows machines where you cannot run installers.

## Building the Environment

1. Create a new GitHub repository
2. Push this folder's contents to the repo
3. Go to **Actions** tab → **Build Portable Python Environment** → **Run workflow**
4. Wait for build to complete (~5 minutes)
5. Download the `mampy3-portable` artifact (zip file)

## Installing on Windows Work PC

1. Copy `mampy3-portable.zip` to your work machine
2. Extract to a user-writable folder, e.g.:
   ```
   C:\Users\YourName\mampy3\
   ```
3. Double-click `activate.bat` to open a terminal with the environment activated

## Using the Environment

After running `activate.bat`:

```batch
python --version          # Python 3.11.x
mamba --version           # Latest mamba
mamba install numpy       # Install packages
python script.py          # Run your scripts
```

## Folder Structure After Extraction

```
mampy3/
├── activate.bat           # Double-click to activate
└── miniforge3/
    ├── python.exe         # Python interpreter
    ├── Scripts/
    │   ├── mamba.exe      # Mamba package manager
    │   ├── conda.exe      # Conda (also available)
    │   └── pip.exe        # Pip
    └── Lib/               # Python libraries
```

## Notes

- The zip file will be ~500MB, extracted ~1.5GB
- Packages installed via mamba/pip are stored in the miniforge3 folder
- Fully portable - move the entire folder anywhere

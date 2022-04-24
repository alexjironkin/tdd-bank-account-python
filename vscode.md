## VSCode setup instructions

Many developers choose to use VS Code as their IDE of choice for developing in python. Below are some simple instructions to help with this kata

### Recommended extensions

- Python (extension ID: ms-python.python)
  - This should also come with Test Runner UI (Flask icon on the left. In case it doesn't use the following extension: LittleFoxTeam.vscode-python-test-adapter)
- Pylance (extension ID: ms-python.vscode-pylance)

### Inital Setup

1. Open folder in vs code by clicking: "File" > "Open Folder..."
2. Open a python file
3. Select a Python version in the bottom right corner of the window: Python... (This may not be visible if you do not have a python file open)

4. Open Test Explorer Extension and click refresh to discover tests

### Troubleshooting

#### Missing tests

Sometimes you have written a test, but it doesn't appear in your panel. This usually means the new test function doesn't start with "test", e.g. instead of

```python
def check_balance():
    ...
```

do

```python
def test_check_balance():
    ...
```

## Smart Debug
This Python script uses the OpenAI API to provide explanations for error messages.

### Requirements
- Python 3
- openai module

### Usage
1. Sign up for an OpenAI API key at https://beta.openai.com/signup/api
2. Export your API key to an environment variable:

```export OPEN_AI_KEY=your_api_key```

3. Pipe the stderr output of a command into the script:

```$ command arg1 arg2 2>&1 | python script.py```
### Example
```
$ some_command 2>&1 | python script.py
Error: invalid input
Explanation: The input provided to the command is not in the correct format.
```
### Notes
- The OpenAI API is currently in beta and may have limited availability.
- The environment variable will only be available in the current terminal session. If you open a new terminal window or log out, you'll need to export the API key again.
- To make the environment variable permanently available, you can add the export command to your shell's startup script. For example, if you're using the Bash shell, you can add it to the ~/.bashrc file. If you're using the Z shell, you can add it to the ~/.zshrc file.
- Alternatively, you can use a tool like dotenv to store your API key in a .env file and load it into your environment automatically.
# LLM-based Dockerfile Generator
This project uses Large Language Model (LLM) — hosted (via [Google Gemini 2.0 flash ](https://aistudio.google.com/prompts/new_chat)) — to generate custom Dockerfiles based on your application language and requirements.

# Hosted LLM with Google Gemini 2.0 flash
Google Gemini 2.0 Flash, that likely means  leveraging Google's latest Gemini API offering, which includes a lighter, faster version optimized for performance — great for low-latency applications.

## Prerequisites
 1.Install Python in your VM & then create venv for env logical isolation
  ```sudo apt update
sudo apt install python3
python3 --version
sudo apt install python3.12-venv
python3 -m venv venv
source venv/bin/activate
```
if python3 doesn't works for you check the version and use 
```
python -m venv venv
```
The activation command is different depending on your shell and operating system.\
```
.\venv\Scripts\Activate.ps1
```
🧠 Here’s a quick reference for activating virtual environments:

| Shell            | Activation Command                     |
|------------------|----------------------------------------|
| PowerShell       | `.\venv\Scripts\Activate.ps1`          |
| Command Prompt  | `.\venv\Scripts\activate.bat`         |
| Git Bash / WSL  | `source venv/bin/activate`            |
| Python (any OS) | `python -m venv venv` *(to create)*   |

If you get a “running scripts is disabled” error next, you might need to allow script execution by running:
```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```
2.Setting up the LLM\
      Head over to  [Google Gemini 2.0 flash ](https://aistudio.google.com/prompts/new_chat) on Google AI Studio → generate an API key for your current project. Once the project is complete, remember to delete the API key for security purposes.

3.Installation steps\
   3.1 for Linux
   ```
   # to install the requirements or the sam can be installed manually 
   bash pip3 install -r requirements.txt
   # to declare API key and upgrade
   export GOOGLE_AI_STUDIO_API_KEY="<your_api_key_paste_here>"
   pip3 install --upgrade google-generativeai
   #to run the python promt file
   python3 dockerfile_generator-gemini.py
   deactivate
   #after completion stop the venv
   ```
3.2 for command prompt(windows)
  ```
   bash pip3 install -r requirements.txt
   $env:GOOGLE_AI_STUDIO_API_KEY="<your_api_key_paste_here>"
   pip install --upgrade google-generativeai
   python dockerfile_generator-gemini.py
   deactivate
   #after completion stop the venv
   ```

    



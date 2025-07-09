# 🧠 CMDGPT

CMDGPT is a GPT-powered Windows command-line assistant that translates natural language into real executable CMD or PowerShell commands. MicahAI runs in your terminal and uses `gpt-4o-mini` to interpret your intent and execute commands on the fly — with retry logic, clipboard copying, and more.

---

## 🚀 Features

* 🤖 **Natural Language to Command Execution** — Just type "create a folder with a file in it" and watch it run.
* 🎯 **PowerShell & CMD Detection** — Automatically detects PowerShell syntax and runs appropriately.
* 🔁 **GPT Retry System** — Fails? It'll ask GPT to revise until it works.
* 🧠 **GPT Chat Mode** — Use `gpt your question here` to ask questions right from the terminal.
* 📋 **Clipboard Support** — Use `c` to copy the generated command without running it.
* 🔐 **First-Run API Key Setup** — Automatically prompts for and saves your OpenAI API key securely in a config file.

---

## 🛠️ How to Install

1. Extract the cmdgpt.zip
2. Open Command Prompt
3. `cd` into the directory containing the cloned/extracted project
4. Run this command:

```bash
python install_and_setup.py
```

This sets up CMDGPT so you can run it globally using:

```bash
cmdgpt
```

---

## 📦 Dependencies

* `openai`
* `pyperclip`

Make sure you’ve installed these by running:

```bash
pip install openai pyperclip
```

---

## 💡 How to Use

Once installed, run `cmdgpt` in any command prompt.

You’ll see:

```
🧠 MicahAI v0.1 — Dual-Mode Desktop Assistant with Infinite Retry Power
Type commands like: 'Create a folder with ideas.txt inside it'
Type 'gpt your-question-here' to chat with GPT directly.
Type 'exit' to shut down.
```

### Example

```
You ➤ create a folder named test with a file readme.txt inside
[MicahAI 🧠] Attempt 1 generating command...
[MicahAI 📋] Suggested command(s):
mkdir test && echo. > test\readme.txt

Execute this? (y/c/n): y
```

And boom, it’s done.

---

## 🧪 Development Notes

* Configuration is saved to: `~/.cmdgpt/config.json`
* The entry point is `cli.py`
* You can run it manually using:

```bash
python cmdgpt/cli.py
```

---

Made by **MicahThePro** with terminal wizardry and GPT magic.

---

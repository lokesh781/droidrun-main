<picture align="center">
  <source media="(prefers-color-scheme: dark)" srcset="./static/droidrun-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="./static/droidrun.png">
  <img src="./static/droidrun.png"  width="full">
</picture>

<div align="center">

[![Docs](https://img.shields.io/badge/Docs-📕-0D9373?style=for-the-badge)](https://docs.droidrun.ai)
[![Cloud](https://img.shields.io/badge/Cloud-☁️-0D9373?style=for-the-badge)](https://cloud.droidrun.ai/sign-in?waitlist=true)


[![GitHub stars](https://img.shields.io/github/stars/droidrun/droidrun?style=social)](https://github.com/droidrun/droidrun/stargazers)
[![droidrun.ai](https://img.shields.io/badge/droidrun.ai-white)](https://droidrun.ai)
[![Twitter Follow](https://img.shields.io/twitter/follow/droid_run?style=social)](https://x.com/droid_run)
[![Discord](https://img.shields.io/discord/1360219330318696488?color=white&label=Discord&logo=discord&logoColor=white)](https://discord.gg/ZZbKEZZkwK)
[![Benchmark](https://img.shields.io/badge/Benchmark-91.4﹪-white)](https://droidrun.ai/benchmark)



<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=983810&theme=dark&period=daily&t=1753948032207">
  <source media="(prefers-color-scheme: light)" srcset="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=983810&theme=neutral&period=daily&t=1753948125523">
  <a href="https://www.producthunt.com/products/droidrun-framework-for-mobile-agent?embed=true&utm_source=badge-top-post-badge&utm_medium=badge&utm_source=badge-droidrun" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=983810&theme=neutral&period=daily&t=1753948125523" alt="Droidrun - Give&#0032;AI&#0032;native&#0032;control&#0032;of&#0032;physical&#0032;&#0038;&#0032;virtual&#0032;phones&#0046; | Product Hunt" style="width: 200px; height: 54px;" width="200" height="54" /></a>
</picture>


[Deutsch](https://zdoc.app/de/droidrun/droidrun) | 
[Español](https://zdoc.app/es/droidrun/droidrun) | 
[français](https://zdoc.app/fr/droidrun/droidrun) | 
[日本語](https://zdoc.app/ja/droidrun/droidrun) | 
[한국어](https://zdoc.app/ko/droidrun/droidrun) | 
[Português](https://zdoc.app/pt/droidrun/droidrun) | 
[Русский](https://zdoc.app/ru/droidrun/droidrun) | 
[中文](https://zdoc.app/zh/droidrun/droidrun)

</div>



DroidRun is a powerful framework for controlling Android and iOS devices through LLM agents. It allows you to automate device interactions using natural language commands. [Checkout our benchmark results](https://droidrun.ai/benchmark)

## ⚡ Performance & Architecture

**Code Execution**: Runs on your **host machine** (computer), NOT on Android device
- LLM processing happens on your computer (fast with local Ollama or cloud APIs)
- Python agent code executes on host machine
- Only a lightweight Portal APK runs on Android device

**Device Communication**: Fast ADB-based communication
- **TCP Mode** (default): Direct HTTP communication via port forwarding - **Fast** (~50-100ms per action)
- **Content Provider Mode**: ADB shell commands - **Moderate** (~200-500ms per action)
- Portal app on Android provides UI state and executes actions natively

**Speed Characteristics**:
- Action execution: ~100-300ms per tap/swipe (depends on device)
- UI state retrieval: ~200-500ms (screenshot + accessibility tree)
- LLM response: Varies by model (local Ollama: 1-5s, cloud APIs: 2-10s)
- Total per step: ~2-15 seconds (depending on LLM and task complexity)

## Why Droidrun?

- 🤖 Control Android and iOS devices with natural language commands
- 🔀 Supports multiple LLM providers (OpenAI, Anthropic, Gemini, Ollama, DeepSeek)
- 🧠 Planning capabilities for complex multi-step tasks
- 💻 Easy to use CLI with enhanced debugging features
- 🐍 Extendable Python API for custom automations
- 📸 Screenshot analysis for visual understanding of the device
- 🫆 Execution tracing with Arize Phoenix
- 🔐 **No API Keys Needed**: Works directly with Android apps (Google Sheets, Calendar, etc.) - perfect for recruitment automation

## 📦 Installation

```bash
pip install 'droidrun[google,anthropic,openai,deepseek,ollama,dev]'
```

## 🚀 Quickstart
Read on how to get droidrun up and running within seconds in [our docs](https://docs.droidrun.ai/v3/quickstart)!   

[![Quickstart Video](https://img.youtube.com/vi/4WT7FXJah2I/0.jpg)](https://www.youtube.com/watch?v=4WT7FXJah2I)

## 🎬 Demo Videos

1. **Accommodation booking**: Let Droidrun search for an apartment for you

   [![Droidrun Accommodation Booking Demo](https://img.youtube.com/vi/VUpCyq1PSXw/0.jpg)](https://youtu.be/VUpCyq1PSXw)

<br>

2. **Trend Hunter**: Let Droidrun hunt down trending posts

   [![Droidrun Trend Hunter Demo](https://img.youtube.com/vi/7V8S2f8PnkQ/0.jpg)](https://youtu.be/7V8S2f8PnkQ)

<br>

3. **Streak Saver**: Let Droidrun save your streak on your favorite language learning app

   [![Droidrun Streak Saver Demo](https://img.youtube.com/vi/B5q2B467HKw/0.jpg)](https://youtu.be/B5q2B467HKw)


## 💡 Example Use Cases

- Automated UI testing of mobile applications
- Creating guided workflows for non-technical users
- Automating repetitive tasks on mobile devices
- Remote assistance for less technical users
- Exploring mobile UI with natural language commands
- **Recruitment Agent**: Automate candidate search, shortlisting, and interview scheduling using Google Sheets and local LLMs (no API keys needed when using Android apps directly)

## 🎯 Recruitment Agent Use Case

DroidRun can be configured as an autonomous recruitment agent that:

- **Searches and Shortlists Candidates**: Uses Android Google Sheets app to read candidate criteria and filter candidates based on your requirements
- **Schedules Interviews**: Automatically lines up interviews by interacting with calendar and communication apps
- **Works with Local LLMs**: Uses Ollama or other local LLM providers, bypassing the need for API keys when working directly with Android apps
- **No API Keys Required**: Since it interacts with Android apps directly (Google Sheets, Calendar, Email, etc.), you don't need Google Sheets API keys or other service credentials

### Example: Recruitment Agent Setup

```bash
# Using local LLM (Ollama) for recruitment tasks
droidrun "Search Google Sheets for candidates matching Python developer with 3+ years experience, shortlist top 5, and schedule interviews for next week" \
  --provider Ollama \
  --model llama3.2 \
  --reasoning \
  --vision \
  --steps 30
```

The agent will:
1. Open Google Sheets app on your Android device
2. Read and analyze candidate data based on your criteria
3. Shortlist candidates according to your requirements
4. Open calendar/email apps to schedule interviews
5. Complete the entire workflow autonomously

## 👥 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details. 

## Security Checks

To ensure the security of the codebase, we have integrated security checks using `bandit` and `safety`. These tools help identify potential security issues in the code and dependencies.

### Running Security Checks

Before submitting any code, please run the following security checks:

1. **Bandit**: A tool to find common security issues in Python code.
   ```bash
   bandit -r droidrun
   ```

2. **Safety**: A tool to check your installed dependencies for known security vulnerabilities.
   ```bash
   safety scan
   ```

 
# 🛰️ MOSDAC_PARENT_REPO

This is the central control hub for the **MOSDAC scraping ecosystem**, combining multiple repositories and tools for intelligent data scraping, AI processing (via Ollama + Gemma/LLaMA 3), and API access.

---

## 📦 Repository Structure

### 🔗 Linked Repositories

- 🔍 [`MOSDAC_SCRAPPING_SCRIPT`](https://github.com/Hireonova/MOSDAC_SCRAPPING_SCRIPT)  
  Python-based web scraper using Playwright + BeautifulSoup. Feeds data to LLMs (Gemma/LLaMA 3 via Ollama).

- ⚙️ [`MOSDAC_EXPRESS_API`](https://github.com/Hireonova/MOSDAC_EXPRESS_API)  
  Express.js backend API for serving processed job listings or any other scraped output from MongoDB.

---

## 🧠 Features

- 🧹 Clean, modular structure with separation of scraper + API
- ⚡ GitHub push automation for updating sub-repos with one command
- 🌐 RESTful API endpoints to serve AI-processed results
- 🧠 Integrates with Ollama to feed scraped data to local Gemma/LLaMA models
- 🎥 YouTube demo coming soon

---

## 🚀 Quick Start

### 📁 1. Clone the Parent Repo

```bash
git clone --recurse-submodules https://github.com/Hireonova/MOSDAC_PARENT_REPO.git
cd MOSDAC_PARENT_REPO
````

> If you didn’t use `--recurse-submodules`:

```bash
git submodule update --init --recursive
```

---

### 📤 2. Push All Repos at Once (Script Provided)

A helper script `push_all.sh` is included to commit and push all changes from the parent and sub-repos.

```bash
bash push_all.sh "Your commit message"
```

> 🔐 Ensure your Git credentials are cached or SSH keys are set up.

---

### 🧪 3. Run Express API Locally

```bash
cd MOSDAC_EXPRESS_API
npm install
npm start
```

API will be served at: [http://localhost:5000](http://localhost:5000)

---

### 📡 4. Run Python Scraper + LLM

```bash
cd MOSDAC_SCRAPPING_SCRIPT
python main.py
```

Make sure:

* Ollama is running locally
* `.env` file is configured with Mongo URI + model info

---

## 🎬 YouTube Demo

[![Watch the Demo Video](https://img.youtube.com/vi/oXbNl3tMYuc/hqdefault.jpg)](https://youtu.be/oXbNl3tMYuc?si=JhL7lzNYiVs90Oz5)

📺 A full walkthrough of the scraping, LLM processing, and API system in action.


* Real-time scraping
* LLM-based job matching
* MongoDB integration
* API usage

Stay tuned and subscribe for updates!

---

## 🧩 Tech Stack

* **Python** — Playwright, BeautifulSoup, LangChain
* **Node.js / Express** — API handling
* **MongoDB** — Central data storage
* **Ollama + Gemma 3 / LLaMA 3** — Local AI inference

---

 
 

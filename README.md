# Alexsander Corvello da Silveira

### Senior QA Engineer · Test Automation · AI-Powered Quality Engineering

📍 São Leopoldo, Brazil &nbsp;|&nbsp; 🧪 10+ years in software quality &nbsp;|&nbsp; 🤖 Bringing generative AI into the testing lifecycle

---

## 👋 About me

I'm a **Senior QA Engineer / SDET** with more than a decade of experience in software testing and quality assurance. I started with manual and functional testing, moved into **test automation** (Selenium, Cypress, Playwright), and today I focus on a question I find fascinating:

> **How can AI make testing faster, smarter and more reliable, without giving up control over sensitive project data?**

That question drives most of my current work: generating test scenarios from user stories with LLMs, predicting software failures before deployment, validating test suites with AI agents, and running **local LLMs** (Ollama) so project data never has to leave the machine.

I'm currently pursuing an **MBA in Applied Artificial Intelligence (UNISINOS, 2026)** and I'm **open to opportunities** as a Senior QA Engineer, SDET, or Quality Specialist with an AI focus.

---

## 🛠️ Tech stack

| Area | Tools |
|---|---|
| **Test automation (UI)** | Playwright (Python), Cypress (JavaScript), Selenium |
| **API testing** | pytest, requests, Postman |
| **Languages** | Python, JavaScript, Java |
| **CI/CD & infrastructure** | Jenkins, Docker, Docker Compose, GitHub |
| **Methodologies** | BDD, Scrum, Kanban, continuous integration |
| **Messaging & data** | Kafka, PostgreSQL, Oracle/SQL, Azure Blob Storage |
| **AI & LLMs** | LangChain, LangGraph, Ollama (local LLMs), prompt engineering |

---

## 🚀 Featured projects

### 🔧 Test automation portfolio, built against OWASP Juice Shop

Three independent test suites that validate the same target application ([OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)), all executed by one containerized Jenkins pipeline.

| Repository | What it is | Stack |
|---|---|---|
| [**e2e-cypress-js**](https://github.com/acorvello/e2e-cypress-js) | End-to-end UI tests for the login flow, with video and failure screenshots | Cypress, JavaScript |
| [**e2e-playwright-python**](https://github.com/acorvello/e2e-playwright-python) | Cross-browser UI tests (Chromium, Firefox, WebKit) with HTML and JUnit reports | Playwright, pytest, Python |
| [**api-testing**](https://github.com/acorvello/api-testing) | REST API tests covering products, authentication and user registration | pytest, requests, Python |

**What makes it more than three test folders:**

- 🐳 **Everything runs in Docker.** The target app, each test runner and Jenkins itself are containers, so the whole environment is reproducible on any machine.
- 🔁 **One Jenkins pipeline** brings up the app, runs the three suites independently (a failure in one never blocks the others) and tears everything down.
- 📊 **Unified reporting.** JUnit results from all suites are merged into Jenkins' native test report, while videos, screenshots and HTML reports are archived per build.
- 🧩 **Test code lives in separate repositories** from the infrastructure, the same way real teams separate them.

```mermaid
flowchart LR
    J[Jenkins pipeline] --> D[Docker Compose]
    D --> A[OWASP Juice Shop]
    D --> C[Cypress suite]
    D --> P[Playwright suite]
    D --> T[API test suite]
    C --> R[Unified JUnit report]
    P --> R
    T --> R
    C --> V[Videos & screenshots]
    P --> H[HTML reports]
```

### 🤖 AI applied to software quality

Projects where generative AI and machine learning meet testing:

- **AI-generated test scenarios**: automatically producing test cases from user stories using LLMs.
- **Cypress suite validator**: an agent built with **LangChain + LangGraph** that reviews Cypress test suites for best practices, flaky logic and fragile selectors, then produces a structured report.
- **Failure prediction model**: a model trained on test execution logs to estimate the probability of a software failure *before* deployment (academic project, MBA in Applied AI).
- **Local AI for test development**: running **Ollama** with a local model, connected to VS Code, to help write automation code while keeping project data under my own governance.

---

## 🧠 What I learned building this

The most valuable part of this portfolio isn't the green pipeline, it's the debugging that got it there. A few lessons that came straight from real failures:

- **Visibility is not the same as clickability.** Modal overlays and animated menus can make an element "visible" but unclickable. Cypress and Playwright handle this differently (`force`, `trigger` and `dispatch_event` are *not* interchangeable), and knowing why matters more than knowing the flag.
- **Retry-ability beats fixed waits.** Replacing `cy.wait(1000)` with an assertion that Cypress retries automatically removed an entire class of flaky failures.
- **Pin your versions.** An unpinned `@playwright/test` silently drifted away from the browsers baked into the Docker image and broke every test at once.
- **Containers talking to containers is its own problem.** Running Docker from inside Jenkins on Windows required understanding how paths are resolved by the daemon, not just by the client.
- **Read the screenshot.** After several rounds of educated guessing, a single failure screenshot revealed the real cause in seconds.

---

## 🎓 Education

- **MBA in Applied Artificial Intelligence**: UNISINOS (in progress, 2026)
- **Postgraduate degree in Project Management**: UNISINOS (2022)
- **Bachelor's degree in Information Systems**: UNISINOS (2010)

---

## 📫 Let's connect

I'm open to opportunities in **software quality engineering, test automation and AI-driven testing**, and always happy to talk about QA, automation strategy, or using LLMs responsibly in testing.

- 💼 **LinkedIn:** [https://www.linkedin.com/in/acorvello]
- 📧 **Email:** [alexsander.corvello@gmail.com]
- 🐙 **GitHub:** [@acorvello](https://github.com/acorvello)

---

<sub>Keywords: Senior QA Engineer, SDET, Test Automation Engineer, Quality Engineering, Playwright, Cypress, Selenium, pytest, API Testing, Jenkins, Docker, CI/CD, BDD, AI in Software Testing, Generative AI Testing, LLM Test Generation, LangChain, LangGraph, Ollama, Brazil.</sub>

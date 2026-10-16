<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:3b1f7a,100:6E40C9&height=220&section=header&text=Mansi%20Singh&fontSize=58&fontColor=ffffff&fontAlignY=36&desc=AI%20Engineer%20%C2%B7%20Agentic%20Systems%20%C2%B7%20LLM%20Applications&descSize=18&descAlignY=58&animation=fadeIn" width="100%" alt="Mansi Singh, AI Engineer"/>

<img src="https://readme-typing-svg.demolab.com?font=Inter&weight=500&size=19&duration=3200&pause=900&color=8B6CEF&center=true&vCenter=true&width=640&lines=I+build+AI+agents+that+show+their+sources;LangGraph+%C2%B7+MCP+%C2%B7+Gemini+%C2%B7+OpenAI+%C2%B7+RAG;Evaluated%2C+traced%2C+tested+%E2%80%94+then+shipped" alt="I build AI agents that show their sources"/>

<br/>

<p><a href="https://mansijaysingh.netlify.app"><img src="https://img.shields.io/badge/Portfolio-6E40C9?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio"/></a> <a href="https://linkedin.com/in/mansi-ai"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a> <a href="mailto:mansisingh.am000@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a> <a href="https://multi-agent-research-mansijaysingh.streamlit.app/"><img src="https://img.shields.io/badge/Live_Demo-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Live demo"/></a></p>

</div>

<br/>

## About

I'm an AI engineer from Kanpur, India. I build LLM applications and multi-agent systems in Python, and I care most about the part that usually gets skipped: **proving the output is right**. My agents check their own citations in code, pause for human review, and are measured with an evaluation set before I call them done.

- **Building:** agentic workflows with LangGraph, MCP tool servers and Gemini
- **Focus:** grounded generation, RAG, evaluation and tracing (LangSmith)
- **Open to:** AI / LLM engineering roles and interesting agent projects

<br/>

## Featured project

<table>
<tr>
<td width="100%">

### [Multi-Agent Research Assistant](https://github.com/mansijaysingh/multi-agent-research) &nbsp;·&nbsp; [Live demo](https://multi-agent-research-mansijaysingh.streamlit.app/)

A LangGraph supervisor agent that searches the web through its **own MCP server**, drops off-topic sources, **pauses for human review**, and writes a report whose citations are verified in code, not trusted from the model.

<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph"/> <img src="https://img.shields.io/badge/MCP-000000?style=flat-square&logo=modelcontextprotocol&logoColor=white" alt="MCP"/> <img src="https://img.shields.io/badge/Gemini-4285F4?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini"/> <img src="https://img.shields.io/badge/Tavily-0F172A?style=flat-square" alt="Tavily"/> <img src="https://img.shields.io/badge/LangSmith-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangSmith"/> <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit"/> <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest"/>

| Completed runs | Citation coverage | Groundedness | Median latency | Cost per report | Tests |
|:---:|:---:|:---:|:---:|:---:|:---:|
| **100%** | **0.96** | **0.99** | **26 s** | **~$0.004** | **52** |

<sub>Measured on a 15-topic evaluation set with an LLM judge. The eval caught a nonsense query producing a confident, fully cited report, and led to a relevance check that turned it into a clean fail.</sub>

</td>
</tr>
</table>

<br/>

## More work

<table>
<tr>
<td width="50%" valign="top">

#### [Scholarship Intelligence Crawler](https://github.com/mansijaysingh/scholarship-crawler)
Auto-crawler that finds scholarships for Indian students, ties every key field to an exact quote on the official source, and scores confidence with rules, not the LLM. Re-runs detect changes and expired records.

<sub>**179** records · **118** from official sources · change detection · SQLite · [live dashboard](https://scholarship-crawler-mzwcfnrgpqpsmjbc4bbv2e.streamlit.app/)</sub>

</td>
<td width="50%" valign="top">

#### [Micro-Influencer Outreach System](https://github.com/mansijaysingh/influencer-outreach)
Pipeline that discovers fitness creators on YouTube, enriches them with real public data, filters with explainable PASS/FAIL reasons, and writes a personalised email and DM for each with Gemini.

<sub>**309** channels discovered · **36** passed filtering · duplicate-safe sending · YouTube Data API · SQLite</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [AI Financial Audit Assistant](https://github.com/mansijaysingh/ai-financial-audit-assistant)
Multi-agent RAG system for CA offices. Upload five financial documents and get an automated audit report with consistency checks, financial validations and 3CB verification.

<sub>LangGraph · multi-agent · RAG · LLMs</sub>

</td>
<td width="50%" valign="top">

#### [Healthcare AI Chatbot](https://github.com/mansijaysingh/healthcare-ai-chatbot)
A safety-focused healthcare chatbot that answers questions with retrieval-augmented generation over a FAISS index.

<sub>RAG · FAISS · LangChain · OpenAI · Streamlit</sub>

</td>
</tr>
</table>

<sub>Also: [YouTube Video Q&A Bot](https://github.com/mansijaysingh/youtube-qa-bot) (RAG over transcripts) · [AI Resume Assistant](https://github.com/mansijaysingh/ai-resume-assistant) (match score, cover letter, tailoring) · [AI Interview Coach](https://github.com/mansijaysingh/ai-interview-coach) (role-specific mock interviews with scoring)</sub>

<br/>

## How I build

| Principle | In practice |
|---|---|
| **Ground everything** | The model reads and writes; code checks. Citations, quotes and numbers are verified against the source before they're shown. |
| **Rules where rules work** | If the state decides the next step, a tested function routes it, not an LLM. LLMs are used where language is needed. |
| **Measure before claiming** | Every agent gets an evaluation set, tracing and unit tests. The numbers above come from those, not from a demo run. |
| **Fail cleanly** | When there's nothing good to say, the system says so instead of inventing an answer. |

<br/>

## Tech stack

**AI & LLM**

<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangGraph"/> <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain"/> <img src="https://img.shields.io/badge/MCP-000000?style=for-the-badge&logo=modelcontextprotocol&logoColor=white" alt="MCP"/> <img src="https://img.shields.io/badge/Gemini-4285F4?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Gemini"/> <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge" alt="OpenAI"/> <img src="https://img.shields.io/badge/LangSmith-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangSmith"/> <img src="https://img.shields.io/badge/FAISS-0467DF?style=for-the-badge&logo=meta&logoColor=white" alt="FAISS"/> <img src="https://img.shields.io/badge/RAG-6E40C9?style=for-the-badge" alt="RAG"/>

**Backend, data & tools**

<img src="https://skillicons.dev/icons?i=python,fastapi,flask,sqlite,html,css,js,git,github,vscode,netlify&perline=11" alt="Python, FastAPI, Flask, SQLite, HTML, CSS, JavaScript, Git, GitHub, VS Code, Netlify"/>

<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit"/> <img src="https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" alt="pytest"/> <img src="https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=black" alt="Render"/>

<br/>

## GitHub activity

<div align="center">

<img height="165" src="https://streak-stats.demolab.com/?user=mansijaysingh&hide_border=true&background=00000000&ring=8B6CEF&fire=8B6CEF&currStreakLabel=8B6CEF&sideLabels=8b949e&dates=8b949e&currStreakNum=8b949e&sideNums=8b949e" alt="GitHub streak"/>

</div>

<br/>

## Education

- **Full Stack Web Development**, Masai School
- **Bachelor of Arts**, Bundelkhand University, Jhansi (2022)
- **AI engineering**, self-taught through building: Python, LLMs, LangChain, LangGraph, MCP

<br/>

<div align="center">

**Open to AI engineering roles and collaborations.** The quickest way to reach me is [email](mailto:mansisingh.am000@gmail.com) or [LinkedIn](https://linkedin.com/in/mansi-ai).

<img src="https://komarev.com/ghpvc/?username=mansijaysingh&label=Profile%20views&color=6E40C9&style=flat-square" alt="Profile views"/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6E40C9,50:3b1f7a,100:0d1117&height=110&section=footer" width="100%" alt=""/>

</div>

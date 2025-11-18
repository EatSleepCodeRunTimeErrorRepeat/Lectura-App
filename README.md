<a id="readme-top"></a>
<!-- 
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url] -->


<br />
<div align="center">
  <a href="https://lectura.minpainghein.com/">
    <img src="./frontend/src/assets/LecturaLogo.png" alt="Lectura Logo" width="120" height="120">
  </a>

  <h2 align="center">Lectura</h2>

  <p align="center">
    Personalized AI Lecture Notes — <em>Your Lectures, Your Notes, Your Way</em>
    <br />
    <a href="#about-the-project"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://lectura.minpainghein.com/">🌐 View Demo</a>
    ·
    <a href="https://www.canva.com/design/DAG1A71rtAg/wzNGBYXxx3xdC14ADXQOoQ/view?utm_content=DAG1A71rtAg&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h10479c1cde">🖼️ View Slides</a>
    ·
    <a href="https://github.com/yourusername/lectura/issues">Report Bug</a>
    ·
    <a href="https://github.com/yourusername/lectura/issues">Request Feature</a>
  </p>
</div>


📑 Table of Contents
  <ol>
    <li>
      <a href="#-about-the-project">About The Project</a>
      <ul>
        <li><a href="#-core-features">Core Features</a></li>
        <li><a href="#-architecture">System Architecture</a></li>
        <li><a href="#-built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#-getting-started">Getting Started</a>
      <ul>
        <li><a href="#-prerequisites">Prerequisites</a></li>
        <li><a href="#-installation">Installation</a></li>
        <li><a href="#-environment-variables">Environment Variables</a></li>
      </ul>
    </li>
    <li><a href="#-usage">Usage</a></li>
    <li><a href="#-screenshots">Screenshots</a></li>
    <li><a href="#-roadmap">Roadmap</a></li>
    <li><a href="#-contributors">Contributors</a></li>
    <li><a href="#-license">License</a></li>
    <li><a href="#-acknowledgments">Acknowledgments</a></li>

---

## 🧠 About The Project

**Lectura** is an AI-powered platform that transforms recorded lectures into structured, personalized study notes.
It’s built to support **multiple learning styles** using the **VARK framework** (Visual, Auditory, Reading/Writing, Kinesthetic).
Learners can upload a lecture, get instant transcription and summarization in a way that best suits their learning style.

<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

### ✨ Core Features
* 🎥 **Video Upload → Audio Conversion**
* 🗣️ **Whisper Transcription Module**
* 🧾 **Mistral AI Note Summarization**
* 💬 **Markdown Editor (React-MD-Editor + Mermaid)**
* 🔊 **Text-to-Speech for Auditory Learners**
* 🧩 **VARK Questionnaire for Personalization**

### 🧱 Application Architecture

Here is a high-level overview of the project's architecture and data flow.

![Frontend Backend Architecture](https://myoctocat.com/assets/images/base-octocat.svg) <br/>
![Detailed Flow Diagram](https://myoctocat.com/assets/images/base-octocat.svg) <br/>

<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

### 🛠️ Built With

This project was bootstrapped with the following technologies:

* [![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
* [![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
* [![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
* [![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=for-the-badge&logo=ffmpeg&logoColor=white)](https://ffmpeg.org/)
* [![Mistral AI](https://img.shields.io/badge/Mistral_AI-FDB032?style=for-the-badge&logo=openai&logoColor=black)](https://mistral.ai/)
* [![Cloudflare R2](https://img.shields.io/badge/Cloudflare_R2-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)](https://www.cloudflare.com/developer-platform/r2/)

<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>


## ⚙️ Getting Started

To get a local copy up and running, follow these simple steps.

### 📋 Prerequisites

Ensure you have the following installed on your machine:
* Node.js (v18+)
* npm
* A Database (e.g. PostgreSQL)
* Cloudflare R2 credentials
* API keys for **Whisper**, **Mistral**, and **Lemonfox**

### Installation

1.  Clone the repository
    ```sh
    git clone [https://github.com/yourusername/lectura.git](https://github.com/yourusername/lectura.git)
    cd lectura
    ```
2.  Install dependencies for both frontend and backend
    ```sh
    # Install backend dependencies
    cd backend && npm install
    
    # Install frontend dependencies
    cd ../frontend && npm install
    ```

<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

### 🔐 Environment Variables

Create `.env` files in both the `frontend` and `backend` directories. Then fill in the variables with *your own credentials*.

> [!CAUTION]
> ⚠️ **Never** commit your `.env` files to GitHub. They contain sensitive credentials.

#### 🖥️ `backend/.env`
```env
# Database Configuration
DB_HOST=localhost
DB_PORT=4000
DB_USERNAME=admin
DB_PASSWORD=yourpassword
DB_DATABASE=lectura_db
SECRET_KEY=somesecretkey

# Cloudflare R2 Storage
R2_ACCOUNT_ID=your_id
R2_ACCESS_KEY_ID=your_key
R2_SECRET_ACCESS_KEY=your_secret
R2_BUCKET_NAME=lectura-temp

# API Keys
GROQ_API_KEY=your_key
MISTRAL_API_KEY=your_key
LEMONFOX_API_KEY=your_key
```

🌐 frontend/.env
```
# Code snippet
VITE_API_URL=http://localhost:4000
```
<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

▶️ Start the backend server: Navigate to backend (./backend/...) 
<br />
```npm run dev```
<br />
▶️ Start the frontend server: Navigate to frontend (./frontend/...)
<br />
```npm run dev```
<br />
Visit http://localhost:4000 in your browser.
<br />
> [!IMPORTANT]
> User Flow: Upload a lecture → transcribe → summarize → explore notes → listen via TTS 🎧

---

## 🌐 Backend API Routes
| Route	| Method	| Description
| --- | :---: | --- |
| /upload | 	POST	| Uploads lecture video to R2 storage
| /generate | 	POST | 	Triggers transcription + note generation
| /status | :noteId	GET	|  Returns note generation status
| /notes | :noteId	GET	 |  Fetches completed notes
| /tts| 	POST | 	Converts text notes into audio
| /vark	| POST	|  Submits or fetches VARK questionnaire data

<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

---

## 🖼️ Screenshots
> [!NOTE]
> More screenshots, user flow diagrams, and other visual assets will be added here soon!
## Feature Preview
🏠 Homepage ![Coming Soon](https://myoctocat.com/assets/images/base-octocat.svg)<br />
❓ VARK Questionnaire ![Coming Soon](https://myoctocat.com/assets/images/base-octocat.svg)<br />
🧾 Note Generation Page ![Coming Soon](https://myoctocat.com/assets/images/base-octocat.svg)<br />
🗣️ Text-to-Speech Output ![Coming Soon](https://myoctocat.com/assets/images/base-octocat.svg)<br />

<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

---

## 🧭 Roadmap
- [x] Multi-language transcription
- [x] Flashcard & quiz generation
- [ ] ***************
- [ ] *******************
- [x] User accounts (login / save notes)
<br />
See the open issues for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

---

## 👥 Contributors 
<br />
Thanks to these amazing people who contributed to this project.
<table><tr>
  <td align="center"><a href="https://www.google.com/search?q=https://github.com/MinPaingHein">
    <img src="https://www.google.com/search?q=https://github.com/MinPaingHein.png%3Fsize%3D100" alt="Min Paing Hein" width="100px;">
    <br />
    <sub>
      <b>Min Paing Hein</b></sub></a></td>
  
  <td align="center"><a href="https://www.google.com/search?q=https://github.com/BadeesornS">
    <img src="https://www.google.com/search?q=https://github.com/BadeesornS.png%3Fsize%3D100" alt="Badeesorn Sittikong" width="100px;">
    <br />
    <sub>
      <b>Badeesorn Sittikong</b></sub></a></td>
  
  <td align="center"><a href="https://www.google.com/search?q=https://github.com/louise-maganda">
    <img src="https://www.google.com/search?q=https://github.com/louise-maganda.png%3Fsize%3D100" alt="Louise Madison Maganda" width="100px;">
    <br />
    <sub>
      <b>Louise M. Maganda</b></sub></a></td>
  
  <td align="center"><a href="https://www.google.com/search?q=https://github.com/PearlOu">
    <img src="https://www.google.com/search?q=https://github.com/PearlOu.png%3Fsize%3D100" alt="Ngwe Yee Pearl Ou" width="100px;">
    <br />
    <sub><b>Ngwe Yee Pearl Ou</b></sub></a></td>
  
  <td align="center"><a href="https://www.google.com/search?q=https://github.com/EatSleepCodeRunTimeErrorRepeat">
    <img src="https://www.google.com/search?q=https://github.com/EatSleepCodeRunTimeErrorRepeat.png%3Fsize%3D100" alt="EatSleepCodeRunTimeErrorRepeat" width="100px;">
    <br />
    <sub><b>EatSleepCode...</b></sub></a></td></tr></table>

<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

---

🪪 License Distributed under the ***************** License. See LICENSE.txt for more information.
<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

---

## 🙇 Acknowledgments
- OpenAI Whisper
- Mistral AI
- Cloudflare R2
- React Markdown Editor
- FFmpeg
- Img Shields
- GitHub Pages

<p align="right">(<a href="#readme-top">⬆️ Back to Top</a>)</p>

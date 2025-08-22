---
layout: default
title: Demo
---

# AI Job Matcher

## Project Description  

This project consists of a **Java Spring Boot backend** and a **React frontend**.  

- **Backend**  
  - Scrapes job listings from a job portal using Selenium WebDriver.  
  - Analyzes jobs with a local LLM AI model (such as **Mistral:7B** or **LLaMA3:8B**) running locally via [Ollama](https://ollama.com/) as an API endpoint.  
  - Provides the candidate profile and job description to the AI, which decides whether the job is suitable.  
  - Stores matching results in a **PostgreSQL database** and sends email notifications when relevant jobs are found.  
  - Includes stealth Selenium settings, retry logic, regex-based parsing, and a modular design for future integration with **Docker** and **CI/CD**.  

- **Frontend**  
  - Allows users to **trigger job matching on demand**.  
  - Displays results, including **AI verdicts and models used**.  
  - Provides UI for managing candidate profile settings.  

The overall goal is to automatically identify job posts that match a predefined candidate profile while keeping scraping activity efficient and respectful to the target website.  

 ![Ollama interactive UI](/assets/images/Ollama_demo.png)

 ![Ollama API access](/assets/images/Ollama_api_demo.png)

 ![AI Matcher Email](/assets/images/aimatcheremail.png)

 ![AI Matcher Result](/assets/images/aimatcherresult.png)

 ![UI Result 1](/assets/images/AIJobMatcherUI-1.png)
 
 ![UI Result 2](/assets/images/AIJobMatcherUI-2.png)

 [Source](https://github.com/waimanlam2019/AIJobSuggestion)

# React Personal Portfolio

 This particular website was built with Jekyll ( A static website engine written with Ruby ) loaded with minimalist style template. I tried to create an exact same website with React. I inspected the html elements and css with by the Jekyll website and tried to mimic it. It is hosted on Vercel.

 [Link](https://personalwebsite-gamma-nine.vercel.app/)

 [Source](https://github.com/waimanlam2019/personalwebsite)

# Browser Cache Deleter

 This tool was written to have external control deletion over browser cache when we don't trust browser's promise to delete cache after closing the browser. Adopted Strategy pattern to facilitate use with different browsers such as Google Chrome, Vivaldi and different platforms such as Windows and Mac because they store cache in different location.

 I created this tool for my own use when I found need to reliably clear browser cache automatically (How could you trust the browser to do the job for you when it is important?), it got the job done and later I don't need it anymore so development stopped right there.

 [Link](https://github.com/waimanlam2019/browser-cache-deleter/tree/master)

# Anmeldung Bot (Germany address registration appointment finder)

The tool was written to help a German to find address registration (German need to register their new address with government when they move to new address) appointment. I used Java + Selenium to automate the process of looking up the appointment on the website. If a good appointment slot is found, it would pop a dialog box to let me know.

[Link](https://github.com/waimanlam2019/AnmeldungBot)

# PDF file splitter demo with Java FX ( apply ForkJoinPool )

A demo program I created with help of ChatGPT to demo ForkJoinPool concurrency. I demanded ChatGPT to create a tool to split a PDF file page by page with JavaFX UI + ForkJoinPool technique. The first version works and I proposed further improvement that its memory management can be improved by extracting the line which load the pdf into the memory from threads.

[Link](https://github.com/waimanlam2019/pdfsplit-forkjoinpool) 

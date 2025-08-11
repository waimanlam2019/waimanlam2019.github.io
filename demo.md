---
layout: default
title: Demo
---

# AI-Powered Job Matcher

 This Java Spring Boot application scrapes job listings from job portal using Selenium WebDriver and analyzes them with a local LLM AI model such as Mistral:7B and LLaMA3:8B running locally via [Ollama](https://ollama.com/) as api endpoint. The java program would talk to the local AI via API, provide the candidate profile, job description and ask the AI to decide whether the job is suitable for the candidate to apply. The goal is to identify job posts that match a predefined candidate profile. The program would send an email to the candidate if there is a matching job. It includes stealth selenium setting, retry logic, regex-based parsing, and is designed with modularity in mind for future integration with a frontend, Docker, and CI/CD. Results are stored in Postgresql database to minimize impact to website being scraped.

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

---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
layout: singleabout
redirect_from:
  - /about/
  - /about.html
github_projects:
  - title: Quantum Keypad and Classical Joytick
    github_user: akarazeevprojects
    github_repo: joystick
  - title: QISKit bot for Slack
    github_user: akarazeev
    github_repo: qiskit-slack-bot
  - title: A series of jupyter notebooks dedicated to introduction to Quantum Computing
    github_user: RQC-QApp
    github_repo: Seminars
  - title: Converter of Jupyter notebooks to PDF
    github_user: akarazeevprojects
    github_repo: ipy2pdf
  - title: Analysis of methods and drugs discussed in papers submitted to PubMed (created during a hackathon on bioinformatics Biohack2017)
    github_user: akarazeev
    github_repo: BioHack2017
  - title: Reverse Engineering in Dispersion Engineering
    github_user: akarazeev
    github_repo: REDE
  - title: Automation for macOS that allows to launch Jupyter notebooks directly from Finder with double click
    github_user: akarazeev
    github_repo: click_click_ipynb
  - title: Legal Engine service (created during Junction2017)
    github_user: akarazeev
    github_repo: LegalTech
  - title: Set of projects with stepper motor (including demonstration of Quantum State Tomography)
    github_user: akarazeevprojects
    github_repo: StepperProjects
---

Hi! Here you can check out my [projects](https://akarazeevprojects.github.io/en) and [CV](assets/data/karazeev_cv.pdf) (added below).

<a href="assets/data/karazeev_cv.pdf"><embed src="assets/data/karazeev_cv.pdf" style="border:1px solid black;" type="application/pdf" width="100%" height="80%"/></a>

<h3>Highlighted projects</h3>

<ul>
  {% for proj in page.github_projects %}
    <li>
      {{ proj.title }}
      <br>
      {% include github user=proj.github_user repo=proj.github_repo %}
    </li>
  {% endfor %}
</ul>

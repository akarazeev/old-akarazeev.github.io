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
    post_url: /proj-quantum-keypad-en/
  - title: QISKit bot for Slack
    github_user: akarazeev
    github_repo: qiskit-slack-bot
    post_url: /bot-qc-sl-en/
  - title: A series of jupyter notebooks dedicated to introduction to Quantum Computing
    github_user: RQC-QApp
    github_repo: Seminars
  - title: Converter of Jupyter notebooks to PDF
    github_user: akarazeevprojects
    github_repo: ipy2pdf
  - title: Analysis of methods and drugs discussed in papers submitted to PubMed (created during a hackathon on bioinformatics Biohack2017)
    github_user: akarazeev
    github_repo: BioHack2017
    post_url: /biohack-en/
  - title: Reverse Engineering in Dispersion Engineering
    github_user: akarazeev
    github_repo: REDE
    post_url: /proj-rede-en/
  - title: Automation for macOS that allows to launch Jupyter notebooks directly from Finder with double click
    github_user: akarazeev
    github_repo: click_click_ipynb
    post_url: /proj-click-click-ipynb-en/
  - title: Legal Engine service (created during Junction2017)
    github_user: akarazeev
    github_repo: LegalTech
    post_url: /hack-junction2017-en/
  - title: Set of projects with stepper motor (including demonstration of Quantum State Tomography)
    github_user: akarazeevprojects
    github_repo: StepperProjects
    post_url: /demo-qst-en/
---
<!-- <img src="images/me_hand.png" style="max-height: 500px; height: auto; width: auto;" class="align-center"> -->
<img src="images/me_hand.jpg" style="max-height: 700px; height: auto; width: auto;">

Here you can check out my [projects](https://akarazeevprojects.github.io/projects-en/) and [CV](assets/data/karazeev_cv.pdf) (added below).

<h3>Highlighted projects</h3>

<ul>
  {% for proj in page.github_projects %}
    <li>
      {{ proj.title }}
      <br>
      {% include github user=proj.github_user repo=proj.github_repo %} {% if proj.post_url %} [<a href="{{ site.url }}{{ site.baseurl }}{{ proj.post_url }}">post</a>] {% endif %}
    </li>
  {% endfor %}
</ul>

<a href="/proj-quantum-keypad-en/"><img src="images/quantum_keypad.jpg" style="max-height: 150px; height: auto; width: auto;" class="align-center"></a>

<a href="assets/data/karazeev_cv.pdf"><embed src="assets/data/karazeev_cv.pdf" style="border:1px solid black;" type="application/pdf" width="100%" height="80%"/></a>

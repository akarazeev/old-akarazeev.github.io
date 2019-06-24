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
  - title: Generative Adversarial Networks (GANs) - Engine and Applications
    post_url: /gans-en/
    extra: 💎 citations on <a href="https://scholar.google.ru/scholar?oi=bibs&hl=en&cites=11164216020026419168">Google Scholar</a>
    extra2: <a href="https://blog.statsbot.co/generative-adversarial-networks-gans-engine-and-applications-f96291965b47">Medium Story</a>
  - title: Quantum Keypad and Classical Joytick
    github_user: akarazeevprojects
    github_repo: joystick
    post_url: /proj-quantum-keypad-en/
    extra: ⭐️ recognised by <a href="https://www.research.ibm.com/ibm-q/">IBM Research</a>
  - title: QISKit bot for Slack
    github_user: akarazeev
    github_repo: qiskit-slack-bot
    post_url: /bot-qc-sl-en/
  - title: Converter of Jupyter notebooks to PDF
    github_user: akarazeevprojects
    github_repo: ipy2pdf
  - title: Legal Engine service (created during Junction2017)
    github_user: akarazeev
    github_repo: LegalTech
    post_url: /hack-junction2017-en/
  - title: A series of jupyter notebooks dedicated to introduction to Quantum Computing
    github_user: RQC-QApp
    github_repo: Seminars
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
  - title: Set of projects with stepper motor (including demonstration of Quantum State Tomography)
    github_user: akarazeevprojects
    github_repo: StepperProjects
    post_url: /demo-qst-en/
---
Here you can find my [projects](https://akarazeevprojects.github.io/projects-en/) and [CV](files/karazeev_cv.pdf) (added below)

<img src="images/me_hand.jpg" style="max-height: 700px; height: auto; width: auto;">

<h3>Highlighted projects</h3>

<ul>
  {% for proj in page.github_projects %}
    <li>
      {{ proj.title }}
      {% if proj.extra or proj.extra2 or proj.post_url%}<br>{% endif %}
      {% if proj.extra %}[{{ proj.extra }}]{% endif %} {% if proj.extra2 %}[{{ proj.extra2 }}]{% endif %} {% if proj.post_url %}[<a href="{{ site.url }}{{ site.baseurl }}{{ proj.post_url }}">Blog Post</a>]{% endif %}
      {% if proj.github_user %}<br>{% include github user=proj.github_user repo=proj.github_repo %}{% endif %}
    </li>
  {% endfor %}
</ul>

<a href="/proj-quantum-keypad-en/"><img src="images/quantum_keypad_small.jpg" style="max-height: 150px; height: auto; width: auto;" class="align-center"></a>

<a href="files/karazeev_cv.pdf"><embed src="files/karazeev_cv.pdf" style="border:1px solid black;" type="application/pdf" width="100%" height="80%"/></a>

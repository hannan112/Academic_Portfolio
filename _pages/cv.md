---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<div style="margin-bottom: 20px;">
  <a href="{{ base_path }}/files/Hannan_CV.pdf" class="btn btn--primary" target="_blank" style="text-decoration: none;">
    <i class="fa fa-download" aria-hidden="true"></i> Download Full CV (PDF)
  </a>
</div>

Education
======
* **B.S. in Software Engineering** — COMSATS University Islamabad, Lahore Campus (*Graduated 2026*)
  * *Focus Area:* Computer Systems, Systems Security, Software Engineering

Professional Experience
======
* **Software Engineer** — Utilexa Labs Pvt Ltd (*Current*)
  * Developing and maintaining scalable backend services and systems software.
  * Engineering robust API integrations, automated workflows, and database systems.

Research Interests
======
* **High-Performance Computing (HPC) & Computer Systems**
* **Distributed & Cloud Computing**
* **Systems for Machine Learning & AI Infrastructure**
* **Computer Architecture, Operating Systems & Networking**
* **Systems & Application Security**

Technical Skills
======
* **Programming Languages:** Python, C/C++, SQL, Bash, JavaScript
* **Frameworks & Libraries:** Django, REST APIs, Scikit-learn (Random Forest), Pandas, NumPy
* **Systems & Security Tools:** Linux/Unix, Docker, Git, OWASP ZAP, Nikto, Nuclei Vulnerability Scanner
* **Databases:** PostgreSQL, SQLite

Research Projects & Papers
======
* **Performance and Scalability Evaluation of the Nuclei Vulnerability Scanner Under Different Execution Architectures** (*2026*)
  * Comprehensive benchmarking of vulnerability scanner throughput, resource utilization, and architectural scaling bottlenecks. (*Under Supervisor Review*)
* **Low-Latency Order Book for NASDAQ ITCH Market Data** (*2025 – 2026*)
  * Cache-conscious, zero-allocation limit order book in modern C++ engineered for sub-microsecond NASDAQ TotalView-ITCH 5.0 feed processing.
* **Reducing False Positives in Automated Web Vulnerability Scanning** (*2025 – 2026*)
  * Final Year Undergraduate Thesis, COMSATS University Islamabad (Team Lead).
  * Developed a weakly supervised confidence-estimation approach (Random Forest) suppressing 29.5% of alerts across 94,256 findings while preserving high-severity results.

Publications & Working Papers
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

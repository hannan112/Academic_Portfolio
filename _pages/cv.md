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
  <a href="{{ base_path }}/files/CV.pdf" class="btn btn--primary" target="_blank" style="text-decoration: none;">
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
* **Automated Web Application Penetration Testing Using Machine Learning Models** (*2025 – 2026*)
  * Final Year Research Project, COMSATS University Islamabad.
  * Built an automated ML-assisted pentesting platform with 16+ functional modules integrating OWASP ZAP, Nikto, and Random Forest classification.

Publications & Working Papers
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

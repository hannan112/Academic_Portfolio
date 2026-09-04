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
  <a href="{{ base_path }}/files/cv.pdf" class="btn btn--primary" target="_blank" style="text-decoration: none;">
    <i class="fa fa-download" aria-hidden="true"></i> Download Full CV (PDF)
  </a>
</div>

Education
======
* **Ph.D. in Computer Science** — University Name, *2024 – Present*
  * *Advisor:* Prof. Advisor Name
  * *Focus Area:* High-Performance Computing, AI/ML Systems
* **B.S. in Computer Science** — University Name, *2020 – 2024*
  * *GPA / Honors:* Magna Cum Laude / Dean's Honor List

Research & Work Experience
======
* **Graduate Research Assistant** (*2024 – Present*)
  * *Lab / Department:* High Performance Systems Lab
  * Designed and benchmarked parallel algorithms and GPU-accelerated computing pipelines.
  * Collaborated with cross-functional research teams to draft conference papers and open-source packages.

* **Software Engineering Intern / Researcher** (*Summer 2023*)
  * *Organization / Company:* Research Institute / Company Name
  * Developed distributed data processing pipelines and automated CI/CD workflows.
  * Optimized algorithmic performance, achieving a 2.5x speedup in throughput.

Technical Skills
======
* **Languages:** Python, C/C++, CUDA, Rust, JavaScript/TypeScript, SQL, Bash
* **Frameworks & Tools:** PyTorch, TensorFlow, MPI, OpenMP, Git, Docker, Linux/Unix, Jekyll
* **Specializations:** Distributed Systems, High-Performance Computing, Deep Learning, Performance Profiling

Honors & Awards
======
* **Graduate Fellowship / Research Award**, University Department (*2024*)
* **Dean's Honor List / Academic Excellence Award**, University (*2020 – 2024*)
* **Hackathon / Competition Winner / Finalist**, National Level (*2023*)

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Academic Service & Leadership
======
* **Peer Reviewer:** IEEE / ACM Conferences and Workshops
* **Mentor:** Undergraduate Research Mentorship Program
* **Member:** Association for Computing Machinery (ACM), IEEE Computer Society

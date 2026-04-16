---
layout: post
title: "Beyond the Button, The Next Steps: When Validation Becomes Empirical"
date: 2026-04-16 09:00:00
categories: method-validation
---

In my 2026 *Journal of Forensic Sciences* (JFS) paper, *A research‑focused framework for empirical method validation in digital and multimedia evidence*, I outlined a structured pathway for developing and validating novel forensic methods. The early stages of that framework—**feasibility studies and scientific foundation gap analyses**—were designed to help researchers move beyond tool‑centric habits and into the scientific discipline that courts and standards bodies now expect.

Recently, during a discussion about my long‑term Forensic Machine Learning (ML) Framework project, someone asked a deceptively simple question:

**“What is the real difference between an exploratory study and a gap analysis?”**

The question is timely. As machine learning accelerates into forensic practice, the distinctions between feasibility studies, gap analyses, and exploratory studies are becoming increasingly important. These study types serve different scientific purposes, answer different questions, and occupy different positions in the validation framework. Treating them as interchangeable undermines both scientific rigor and legal defensibility.

This post revisits the structure I published in my 2026 JFS paper and expands it to clarify how these study types function within the validation framework—especially for novel method development such as forensic ML. In particular, I explain why **exploratory studies** have become an essential third category for emerging domains where the scientific and legal foundations are not yet established.

---

# **1. Where These Study Types Fit in the Validation Framework**

In my validation‑study framework, the early stages of novel method development fall into three categories:

- **Feasibility Study**  
- **Scientific Foundation Gap Analysis**  
- **Scientific Foundation Exploratory Study**

These stages are not interchangeable.  
They build on each other in a forensic‑driven sequence.

A feasibility study asks whether a scenario, signal, or mechanism is scientifically plausible and worth investigating.  
> **Feasibility → discovery**

A scientific foundation gap analysis examines what the literature, current practice, and existing protocols provide—and identifies what is missing relative to forensic requirements.  
> **Scientific Foundation Gap Analysis → identify what is missing**

A scientific foundation exploratory study then defines the scientific, legal, and operational foundations of the domain so that a forensic‑grade method or protocol can be developed.  
> **Scientific Foundation Exploratory Study → define the domain**

This structure was present in my 2026 JFS paper, but the role of exploratory studies—especially for emerging domains like forensic ML—deserves clearer articulation. In practice, exploratory studies often arise only after a feasibility study and a gap analysis reveal that the domain itself must be defined before validation can occur.

---

# **2. What a Feasibility Study Really Is**

A **feasibility study** is the earliest, lowest‑stakes scientific activity.  
It is not forensic.  
It is not evidentiary.  
It is not admissibility‑focused.

Its purpose is simple:

> **Determine whether a concept, signal, or mechanism appears to exist and is worth further scientific investigation.**

A feasibility study:

- explores whether a measurable effect exists  
- uses small datasets or controlled conditions  
- does not attempt to generalize  
- does not evaluate forensic requirements  
- does not claim operational readiness  

In ML, feasibility studies often look like:

- “Can a model distinguish real vs. synthetic audio under ideal conditions?”  
- “Is there a detectable artifact in diffusion‑model images?”  
- “Does a classifier show promise on a narrow, controlled dataset?”

Feasibility studies are **discovery‑oriented**, not evaluative.

---

# **3. What a Scientific Foundation Gap Analysis Is**

A **Scientific Foundation Gap Analysis (SFGA)** plays a very specific role in the early stages of novel method development. In my workflow, a gap analysis is only appropriate **after** feasibility is established and **before** an exploratory study is undertaken.

Its purpose is:

> **Identify what is missing between current practice and the forensic requirements that would apply to the scenario or method under consideration.**

A gap analysis is not about defining the domain.  
It is about determining whether the existing scientific, operational, or legal foundations are sufficient—and if not, where the deficiencies lie.

A scientific foundation gap analysis:

- examines what the literature, standards, and existing protocols currently provide  
- maps **claims → requirements → evidence → gaps**  
- evaluates whether current methods or assumptions satisfy forensic requirements  
- identifies missing validation, missing transparency, and missing error‑rate characterization  
- highlights risks to admissibility, reliability, and due process  
- is inherently forensic in nature, because it is grounded in forensic requirements  

In my own work, this step often reveals that the **domain itself is not yet defined**.  
For example, when evaluating whether existing digital and multimedia forensic methods could support an investigation into an ML‑driven incident (such as a hypothetical lunar‑lander failure), the gap analysis showed:

- no public ML‑forensic investigative protocol exists  
- existing DME methods do not address ML decision pathways  
- publicly available documentation from agencies such as NASA does not describe ML‑specific, forensic‑ready incident investigation procedures for spacecraft systems; existing guidance focuses on general mishap investigation, software assurance, and AI risk management rather than forensic reconstruction of ML decision pathways
- forensic requirements cannot be met with current tools or workflows  

That is the gap.

Gap analyses are **evaluative**, not exploratory.  
They tell us **what is missing**, not **what the domain should be**.

Once the gaps are identified, the next step is the **Scientific Foundation Exploratory Study**, which defines the domain and articulates the scientific and legal foundations needed to build a forensic‑grade method or protocol.

---

# **4. Why Exploratory Studies Are Needed in Forensic ML**

In traditional forensic disciplines, the scientific foundations already exist.  
In machine learning, they often do not. This becomes clear only after feasibility and a scientific foundation gap analysis reveal that the domain itself is undefined.

This is where **Scientific Foundation Exploratory Studies (SFES)** become essential.

An exploratory study is appropriate when:

- a feasibility study shows the scenario is scientifically plausible  
- a gap analysis reveals that existing methods, standards, or protocols cannot meet forensic requirements  
- the domain lacks established forensic requirements or investigative frameworks  
- the scientific, legal, and operational foundations must be articulated before a method can be built  

Its purpose is:

> **Define, characterize, and articulate the scientific, legal, and operational foundations of a domain so that a forensic‑grade method or protocol can be developed.**

A scientific foundation exploratory study:

- defines the domain and its boundaries  
- identifies the scientific principles relevant to forensic use  
- maps legal, evidentiary, and due‑process constraints  
- explores operational contexts and investigative pathways  
- articulates what “forensic‑grade” would require in this domain  
- establishes the foundations needed for future validation studies  

Exploratory studies are **foundational**, not evaluative.  
They do not test tools or claims.  
They **build the domain** that future forensic methods must inhabit.

This is why two of my current Forensic ML Framework papers—  
**(1) Legal Requirements for Forensic ML** and  
**(2) Investigative‑Only ML Use by Law Enforcement**—are not gap analyses. They are exploratory studies.

The gap analyses revealed that:

- no forensic ML investigative protocols exist  
- existing digital and multimedia forensic methods do not address ML decision pathways  
- agencies such as NASA, NTSB, or DoD have no public ML‑forensic incident procedures  
- forensic requirements cannot be met with current tools or workflows  

The exploratory studies then take the next step:  
**defining the scientific and legal architecture needed to build a forensic ML investigative method or protocol.**

In other words:

- **Gap Analysis → identifies what is missing**  
- **Exploratory Study → defines what must exist**  

This is the role exploratory studies play in novel forensic method development—and why they are indispensable for emerging domains where the scientific foundations do not yet exist.

---

# **5. How These Three Study Types Work Together in Novel ML Method Development**

Here is the sequence as it actually functions in my validation‑study framework and in my own research workflow:

### **Step 1 — Feasibility Study**  
“Is this scenario, signal, or mechanism scientifically plausible and worth studying?”

A feasibility study answers the “What if?” question.  
If the answer is yes, the work moves forward.

---

### **Step 2 — Scientific Foundation Gap Analysis**  
“What is missing between current practice and the forensic requirements that would apply?”

Once feasibility is established, the next step is to examine:

- what the literature provides  
- what current forensic methods claim  
- what agencies or standards bodies have in place  
- what forensic requirements would apply  
- where the deficiencies are  

The gap analysis identifies **what we do not have**.

---

### **Step 3 — Scientific Foundation Exploratory Study**  
“What scientific, legal, and operational foundations must be defined so a forensic‑grade method or protocol can be developed?”

Only after the gaps are identified does it become clear that:

- the domain itself may not be defined  
- forensic requirements may not yet exist  
- operational pathways may be unclear  
- legal constraints may be unarticulated  

The exploratory study defines the domain so that a forensic‑grade method can be built.

---

In forensic ML, this sequence is especially important.  
Feasibility reveals whether the scenario is worth studying.  
Gap analysis reveals that existing methods cannot meet forensic requirements.  
Exploratory studies then define the scientific and legal foundations needed to build a forensic ML investigative method or protocol.

This is the workflow I used in the lunar‑lander ML failure scenario, and it is the workflow I use in the Forensic ML Framework: feasibility → identify the gaps → define the domain.

---

# **6. Why the Distinction Matters**

Because each study type answers a different question:

- **Feasibility** → Is this scenario scientifically plausible and worth studying?  
- **Scientific Foundation Gap Analysis** → What is missing between current practice and the forensic requirements that would apply?  
- **Scientific Foundation Exploratory Study** → What scientific, legal, and operational foundations must be defined so a forensic‑grade method or protocol can be built?

If we collapse these categories:

- feasibility studies get mistaken for validation  
- gap analyses get performed without requirements  
- exploratory studies get mistaken for operational guidance  
- ML tools get misrepresented as “forensic‑ready”  
- courts receive misleading or incomplete scientific claims  

Clear distinctions protect:

- scientific integrity  
- legal reliability  
- due process  
- the credibility of forensic ML as a discipline  

---

# **7. Closing: Building the Scientific Foundations for Forensic ML**

The forensic community is entering a period where ML tools are advancing faster than the scientific foundations needed to evaluate them. This makes it essential to distinguish:

- **discovery** (feasibility)  
- **evaluation** (gap analysis)  
- **foundation‑building** (exploratory study)

By clarifying these study types—and using them intentionally—we can build forensic‑grade ML methods that are scientifically defensible, legally sound, and operationally meaningful.

---

## **References**

Wales, G. S. (2026). *A research‑focused framework for empirical method validation in digital and multimedia evidence*. *Journal of Forensic Sciences*, 00, 1–14. `https://doi.org/10.1111/1556-4029.70253` 
---
layout: post
title: "Forensic Research Foundations: How to Build a Study That Solves Mysteries and Advances Science"
date: 2025-04-28 09:30:00
categories: updates
---


### Two Paths to Forensic Inquiry: Explaining Anomalies vs. Advancing Research

#### Introduction

In forensic research, ensuring the integrity of digital evidence is paramount. Whether it's images, audio files, or video recordings, even the smallest alteration can lead to discrepancies in forensic analysis. Before diving into deeper statistical analysis and data interpretation, it’s essential to first establish a strong foundation. This includes validating the tools and methodologies used to examine digital media. In this post, we explore how to build a study that evaluates forensic image integrity, covering essential control tests and validation methods. By the end, you'll gain insights into how a structured forensic study is set up, tested, and prepared for deeper statistical evaluation. Let’s start by laying the groundwork for future investigations that aim to solve real-world mysteries and push the boundaries of forensic science.

In forensic science, investigations typically begin along one of two paths:

- A **practitioner** encounters an anomaly—such as an unexpected digital artifact or file alteration—and must determine its cause for courtroom testimony.  
- A **researcher** identifies a gap in knowledge and designs a structured study to advance forensic science literature.  

Both paths require a **methodical, evidence-driven approach**, whether the goal is courtroom defense or peer-reviewed publication.

To illustrate, consider a simple research question (RQ):  
> *"Does uploading an image to Google Drive alter its integrity?"*  

A **forensic examiner** may need to verify file authenticity during litigation, while a **researcher** may seek to assess cloud storage’s impact on digital evidence preservation.

This post walks you through the foundational phases of forensic research, whether you’re solving an urgent mystery or building a publishable study.

---

### 1. Formulating the Research Question and Hypothesis

A strong **research question (RQ)** sets the foundation for any forensic study. It ensures the work remains relevant, focused, and investigable.

**A good forensic RQ should be:**

- **Specific and Clear**  
  - Broad questions create confusion. Narrow the focus.  
  - Example refinement:  
    > *"What happens to a JPEG image when uploaded to Google Drive?"*

- **Forensically Relevant**  
  - The question must contribute meaningfully to forensic science or practice.  
  - Further refinement:  
    > *"Does uploading a JPEG image to Google Drive alter its original integrity?"*

- **Investigable**  
  - There must be a clear, systematic method to gather and analyze evidence.

With a specific and forensically relevant RQ, we next ensure we can **test** it—requiring appropriate forensic measurement tools.

---

#### Forensic Tools for Testing Image Integrity

To evaluate whether a JPEG’s integrity is altered after upload/download from Google Drive, we will use:

- **Hash Verification**  
  - Generate cryptographic hashes (e.g., SHA-256, MD5) before and after upload to detect bit-level changes.

- **Pixel-Level Comparison Metrics** (full-reference metrics, since we have a control/original image):  
  - **Pearson Correlation Coefficient (PCC)** — Measures similarity of pixel intensity distributions.  
  - **Peak Signal-to-Noise Ratio (PSNR)** — Evaluates signal loss; higher values = greater similarity.  
  - **Structural Similarity Index (SSIM)** — Assesses structural distortion with perceptual quality in mind.  
  - **Multi-Scale Structural Similarity (MS-SSIM)** — A multi-resolution version of SSIM for deeper analysis.

These tools offer a structured, measurable way to assess forensic integrity.

---

#### Final Research Question

> *"Does uploading a JPEG image to Google Drive alter its original integrity?"*

---

### 2. From Research Question to Hypothesis

Now that we have the RQ, we can develop a **hypothesis**—a formal, testable prediction.

---

#### Hypothesis vs. Theory: Key Distinctions

|                       | **Hypothesis**                                             | **Theory**                                             |
|-----------------------|------------------------------------------------------------|--------------------------------------------------------|
| **Definition**         | A specific, testable prediction about a phenomenon.        | A well-substantiated explanation developed through repeated testing. |
| **Testability**        | Designed to be tested and falsified.                       | Supported by extensive empirical evidence.             |
| **Scope**              | Narrow—targets specific variables.                         | Broad—explains general principles and multiple phenomena. |
| **Example**            | *Hypothesis:* "Uploading a JPEG to Google Drive alters its integrity." | *Theory:* "Digital image compression algorithms systematically introduce forensic artifacts." |



A **hypothesis** is **early-stage** and **study-specific**, while a **theory** represents **long-term scientific consensus**.

---

#### Developing the Hypotheses

In forensic work, it’s best to clearly define **both** the null and alternative hypotheses:

- **Null Hypothesis (H₀):**  
  > *Uploading a JPEG image to Google Drive does not alter its original integrity.*  
  - Predicts no change: identical hashes, identical or highly similar pixel structures (PCC, PSNR, SSIM, MS-SSIM).

- **Alternative Hypothesis (Ha):**  
  > *Uploading a JPEG image to Google Drive alters its original integrity.*  
  - Predicts some detectable change: hash mismatches or measurable pixel-level differences.

Whether the results **fail to reject** the null (no change) or **support** the alternative (changes detected), these hypotheses provide a clear forensic framework for interpreting the findings.

*(Note: I use "Ha" rather than "H₁" for alternative hypothesis, following the notation style taught in my academic training—both are correct; it's simply a matter of preference.)*

---

### 3. Conducting a Literature Review

Before launching an experiment, a solid forensic study must be grounded in existing knowledge. A literature review ensures:

- Your study builds on validated methods.  
- You aren’t duplicating existing work without adding value.  
- You identify gaps or contradictions your research can address.

---

#### Strategies for Effective Literature Review

Focus on **high-quality forensic sources**, such as:

- **Peer-Reviewed Journals** — *Journal of Forensic Sciences*, *Digital Investigation*, *Forensic Science International*.
- **Conference Proceedings** — *International Conference on Digital Forensics & Cybersecurity*.
- **Technical Standards and Reports** — *NIST*, *SWGDE*, *ISO standards*.
- **Case Studies** — Published examples of forensic anomalies and digital evidence handling.

When analyzing sources:

- **Track Citations** — Use tools like Google Scholar’s **"Cited by"** to understand how a method or study has evolved.
- **Compare Methodologies** — Assess the strengths and weaknesses of prior approaches.
- **Prioritize Forensic Relevance** — Ensure studies address digital evidence concerns, not just general computer science problems.

> Important: Forensic adoption of new techniques (e.g., SSIM, MS-SSIM) often lags behind innovation. Be cautious not to dismiss newer methods solely because they’re not yet widespread.

---

#### Identifying Gaps and Articulating Your Contribution

Ask:

- Are previous studies limited by sample size or outdated tools?  
- Are there contradictory findings about cloud storage’s effect on file integrity?  
- Has anyone tested modern perceptual metrics (like SSIM) in this context?

If your study systematically compares JPEG integrity across platforms using updated forensic techniques, you offer **new, practical insights** that could shape future digital evidence validation practices.

---

#### "But I Don't Have Access to Academic Databases"

It’s common to lack university library access, but you can still conduct a solid review.

Best free tool: **Google Scholar**.

Use strategies like:

- **Reference Mining** — Read the reference lists of paywalled papers.
- **Author Search** — Check if the same author published similar open-access work.
- **Look for Preprints** — Some researchers upload preprint versions on sites like arXiv or ResearchGate.

Even restricted papers can often be leveraged for framing your study, as abstracts, methods, and cited references are usually visible.

---

#### **4. Moving into Exploratory Mode**

Once a research question is formulated and an initial literature review is completed, the next step is **exploratory analysis**, a critical phase where researchers determine whether an experiment is feasible and refine study parameters before committing to full-scale data collection. Exploratory analysis ensures that the research is **methodologically sound and capable of yielding meaningful forensic insights**.

##### **Sketching a Pilot Study to Assess Feasibility**

Before launching a full experiment, a **pilot study** acts as a small-scale trial to:

- **Verify whether data collection methods are effective**  
  - Pilot studies provide an opportunity to refine workflows, minimizing risks later in the larger research phase. This prevents flawed methodologies that could compromise forensic integrity.
  - However, **unexpected variables often emerge** during pilots. I regularly encounter issues that force adjustments, even when the process initially seems sound. Pilot testing is essential for identifying and mitigating **extraneous variables** early.

- **Identify unforeseen obstacles in the research process**  
  - Pilot studies help surface challenges that might not be obvious during planning. Flexibility is key; researchers must be prepared to pivot methodologies when necessary to maintain forensic rigor.

- **Ensure measurement instruments produce reliable results**  
  - If problems arise with measurement tools, the literature review is revisited to identify validated methodologies or explore published alternatives.
  - Sometimes, **existing tools can be adapted** with minimal changes. Other times, researchers must develop custom scripts—but referencing a **peer-reviewed scientific source** strengthens the validation of these new methods.

**Example:**  
For our working research question (*Does uploading a JPEG image to Google Drive alter its original integrity?*), a pilot study would involve uploading a small set of controlled images, retrieving them, and analyzing for detectable changes.

**Key Considerations:**  
- **Selection of Test Images** – Use JPEGs with varying resolutions and compression levels.  
- **Controlled Environment** – Maintain consistent upload/download procedures.  
- **Preliminary Analysis Methods** – Perform **file hash verification** and **image quality assessments** before scaling up.

##### **Incorporating Control Tests During Pilot Studies**

Control tests are essential before analyzing experimental data. They help validate that **measurement instruments are functioning properly**.

**Lessons Learned from Pilot Studies:**  
- I have encountered cases where **custom measurement tools failed** to detect known file alterations.
- By conducting **controlled alterations** (e.g., applying known compression levels), researchers can verify whether tools identify the expected changes.
- **Pilot studies are the ideal phase to catch flaws** in measurement techniques before proceeding to full datasets.
- **Software validation** should also occur during pilots to ensure forensic tools detect **deep alterations**, not just superficial metadata changes.

##### **Defining Key Variables**

Clear definition of variables is critical:

- **Independent Variable** – What is manipulated (e.g., uploading to Google Drive).  
- **Dependent Variable** – What is measured (e.g., file integrity changes detected by hash comparison or SSIM analysis).  
- **Extraneous Variables** – Other factors potentially impacting results (e.g., cloud service compression, network conditions).

Researchers must determine if **automatic file processing** (like compression) occurs during upload, since it may require separate evaluation.

#### **Selecting and Validating Measurement Instruments**

For forensic imaging studies, typical measurement tools include:

- **File Hash Verification** – Using SHA-256 or MD5 before and after upload.  
- **Multimedia Stream Hash Verification** – Analyzing the embedded media stream content itself [1-2]
- **Image Quality Metrics** – Full-reference measures like **PCC, PSNR, SSIM, and MS-SSIM** [1-2]

Reliability is established through **repeatability**, consistent results across repeated trials signal valid methods.

By methodically structuring exploratory research, forensic practitioners lay the groundwork for reliable full-scale data collection.

---

#### **5. Preparing for Full-Scale Data Collection**

Once exploratory testing is complete, attention shifts to **structuring the full-scale data collection process**, ensuring forensic validity, minimizing sources of error, and maintaining consistency.

##### **Structuring Your Methodology for Forensic Rigor**

An effective forensic methodology must be **repeatable, transparent, and defensible**. Key elements include:

- **Controlled Environment** – Maintain consistency in upload/download processes, device settings, and network conditions.  
  - I have had to **pivot collection methods** due to unexpected factors like software licensing changes. **Version control** of forensic tools is essential to preserve repeatability if environments shift.

- **Standardized Procedures** – Create clear protocols for tasks like image preprocessing, metadata extraction, and comparison techniques.  
  - Personally, I prefer **visual workflows** and **step-by-step guides** to enhance consistency.

- **Chain of Custody Documentation** – Tightly track data from collection through analysis, using hashes at multiple stages.  
  - Hashing is my first action during data collection. Multiple verifications during the process maintain forensic confidence—even if primary documentation is lost.

- **Validation with Replication** – Repeat testing across samples to confirm result consistency.

For example, in studying **Google Drive image integrity**, rigorous controls and documentation are critical to ensure forensic defensibility.

##### **Identifying Potential Limitations Before Full Collection**

Anticipating limitations strengthens study design:

- **Cloud Processing Risks** – Some platforms automatically re-encode images. **Google Drive's behavior must be tested** before assuming no alteration.  
- **Environmental Factors** – Standardizing upload/download conditions minimizes variability.  
- **Measurement Tool Sensitivity** – Tools that fail to detect subtle changes could mislead forensic conclusions. Sensitivity testing is critical.  
- **Sample Size and Variety** – A broad dataset prevents bias. Researchers might also consider comparative tests across services like Dropbox or OneDrive for generalizability.

##### **Refining Techniques Ahead of Statistical Analysis**

Strong statistical analysis relies on **clean, structured data**. Refine collection methods by:

- **Standardizing Naming and Organization** – Clear filenames and directory structures simplify tracking.  
- **Automating Where Possible** – Scripts reduce human error in hash verification, metadata extraction, and comparisons.  
- **Predefining Metrics** – Ensure collected data matches analysis needs (hashes, SSIM scores, etc.).  
- **Preparing for Anomaly Detection** – Develop protocols to flag unexpected findings.

I also deliberately **introduce errors** during pilot phases, such as compression, noise addition, or format changes, to confirm that my anomaly detection and measurement instruments are truly sensitive.

By refining techniques early, forensic researchers ensure **credible, replicable, and statistically sound** findings.

---

#### **Mini-Pilot Study Set-Up**  

Forensic validation requires ensuring that **measurement instruments correctly detect expected image changes** while avoiding false detections of intact images. Before proceeding, we will conduct **two control tests**:  

1. **Control-Test-1: Validate measurement instruments by testing identical images**—ensuring forensic tools **correctly classify matching images as identical**.  
2. **Control-Test-2: Evaluate forensic detection of compression artifacts**—confirming that measurement instruments **accurately flag compression-induced alterations** in digital images.  

---  

##### **Control-Test-1: Measuring Identical Image Similarity**  

This control test **validates whether forensic tools correctly identify two identical images as unchanged**, ensuring they do not falsely detect variations when none exist.  

##### **Testing Hypothesis:**  
- **Null Hypothesis (H₀):** There are NO differences between the JPEG images.  
- **Alternative Hypothesis (Ha):** There ARE differences between the JPEG images.  

##### **Test Files:**  
- **Reference:** `Control-1.jpg`  
- **Questioned:** `Control-1-copy.jpg`  

> *The questioned file was created by making an exact copy of the reference image. Since no modifications occurred, forensic tests should confirm an exact match.*  

---  

##### **Hash Analysis**  

Used **Hasher v2.0** to conduct a file hash analysis:  

| **FileName** | **SHA256 Hash** |  
|--------------|-----------------|  
| Control-1.JPG | `02BC049.....9F9F8FB0F` |  
| Control-1-copy.JPG | `02BC049.....9F9F8FB0F` |  

**Findings:** Hashes match, confirming bitstream-level integrity.  

---  

##### **Image Quality Assessment Measurements (IQA)**  

| **IMG Stream** | **IMG Sub Diff** | **PCC** | **PSNR** | **SSIM** | **MS-SSIM** |
|----------------|------------------|---------|----------|----------|-------------|
| **Match**      | **0**            | **1**   | **1**    | **1**    | **1**       |



##### **Interpretation of Metrics:**  
 All forensic metrics confirm integrity preservation, verifying that forensic measurement tools correctly classify identical images as unchanged.  

---  

##### **Control-Test-1 Conclusion:**  
*We accept the Null Hypothesis—there are NO differences between the JPEG images.*  

---  

#### **Control-Test-2: Measuring Compression-Induced Image Variations**  

This control test evaluates whether forensic tools correctly detect compression induced image degradation confirming measurable differences between an original and highly compressed image.  

##### **Testing Hypothesis:**  
- **Null Hypothesis (H₀):** There are NO differences between the JPEG images.  
- **Alternative Hypothesis (Ha):** There ARE differences between the JPEG images.  

##### **Test Files:**  
- **Reference:** `Control-2.jpg`  
- **Questioned:** `Compressed-Control-2.jpg`  

> *The questioned file was created using MATLAB to apply increased compression to the reference image. Forensic tests should confirm measurable integrity loss.*  

---  

##### **JPEG Compression Levels (Measured via ImageMagick)**  

| **FileName**               | **Magick Quality Score**              |  
|----------------------------|--------------------------------------|  
| Control-2.jpg              | **95** (Minimal Compression)         |  
| Compressed-Control-2.jpg   | **25** (High Compression)            |  
 

- **A JPEG compressed at 25** loses significant detail, introduces artifacts, and reduces color accuracy—appearing **blurred or blocky**, especially in fine textures.  
- **A JPEG saved at 95** preserves detail and color fidelity, maintaining **sharp edges and smoother gradients**, though with a larger file size.  

---  

##### **Hash Analysis**  

Used **Hasher v2.0** to conduct a file hash analysis:  

| **FileName**              | **SHA256 Hash**                    |  
|---------------------------|------------------------------------|  
| Control-2.JPG             | `02BC049.....9F9F8FB0F`            |  
| Compressed-Control-2.JPG  | `2C186C8.....420156959`            |  

**Findings:** Hashes do NOT match—confirming compression-induced modifications.  

---

##### **Image Quality Assessment Measurements (IQA)**  

| **IMG Stream** | **IMG Sub Diff** | **PCC**    | **PSNR**   | **SSIM**   | **MS-SSIM** |  
|----------------|------------------|------------|------------|------------|-------------|  
| **No Match**   | **5605554**       | **0.99653**| **0**      | **0.86622**| **0.95843** |  


##### **Interpretation of Metrics:**  
- **IMG Stream mismatch** confirms **byte-level differences in compressed images**.  
- **High pixel difference (IMG Sub Diff: 5605554)** suggests noticeable structural alterations.  
- **PCC (0.99653)** indicates high similarity, but **not a perfect match** due to compression artifacts.  
- **PSNR (0)** suggests **extreme signal loss**, a hallmark of aggressive compression.  
- **SSIM (0.86622)** indicates **moderate structural degradation** affecting forensic authentication.  
- **MS-SSIM (0.95843)** confirms **multi-scale integrity loss, but retains some resemblance**.  

---  

##### **Control-Test-2 Conclusion:**  
*We reject the Null Hypothesis—compression introduces measurable differences between the JPEG images.*  

---  

#### **Mini-Pilot Test**  

This **mini-pilot test** illustrates one of several forensic validation tests designed to determine whether **uploading a JPEG image to Google Drive affects its integrity**.  

In this instance, I created a subfolder in Google Drive named `"Pilot-Study"` and **dragged and dropped** the image into the folder. When conducting a full forensic validation, researchers should test **both drag-and-drop uploads and file selection uploads**, as different methods could introduce variations in processing.  

To ensure controlled retrieval, I selected the `"Pilot-Study"` folder for download, which automatically converted it into a **ZIP file**—this ensures the download process does not introduce external handling effects that could alter the test file.  

---  

##### **Testing Hypothesis:**  
- **Null Hypothesis (H₀)** -- Uploading a JPEG image to Google Drive does not alter its original integrity.  
- **Alternative Hypothesis (Ha)** -- Uploading a JPEG image to Google Drive does alter its original integrity.  

---  

##### **Test Files:**  
- **Reference** -- `Control-Copy-4-Upload.jpg`  
- **Questioned** -- `Download-Control-Copy-4-Upload.jpg`  

> *The reference file was manually uploaded to Google Drive. The questioned file was downloaded from the `"Pilot-Study"` folder and extracted from the ZIP archive. If no modifications occurred, forensic tests should confirm an exact match.*  

---  

##### **Hash Analysis**  

Used **Hasher v2.0** to conduct file hash analysis:  

| **FileName**                      | **SHA256 Hash**                |  
|-----------------------------------|--------------------------------|  
| Control-Copy-4-Upload.jpg         | `02BC049.....9F9F8FB0F`        |  
| Download-Control-Copy-4-Upload.jpg| `02BC049.....9F9F8FB0F`        |  

**Findings:** Hashes match, indicating no byte-level modifications during upload or download.  

---

##### **Image Quality Assessment Measurements (IQA)**  

| **IMG Stream**    | **IMG Sub Diff**    | **PCC**     | **PSNR**    | **SSIM**    | **MS-SSIM**    |
|-------------------|---------------------|-------------|-------------|-------------|----------------|
| **Match**         | **0**               | **1**       | **1**       | **1**       | **1**          |




**Findings:** All IQA metrics confirm the images are identical, reinforcing forensic integrity.  

---  

##### **Mini-Pilot Study Test Conclusion:**  
*We **accept the Null Hypothesis**—Uploading a JPEG image to Google Drive **does not alter its original integrity**.*  

---  

##### **Final Considerations:**  
It is essential to note that this **represents only one of several validation tests** required for a complete forensic study. Additional tests should evaluate **different upload/download methods** — API-based transfers vs. manual uploads.  

By conducting **multiple controlled experiments**, forensic researchers ensure findings are **comprehensive, repeatable, and applicable to real-world forensic investigations**.  

---  

#### **Moving Forward: Data Analysis & Descriptive Statistics**

In the next post, we will transition into data analysis, where we systematically examine collected data using descriptive statistics to summarize findings. This will include:  
- Central tendency measures – Analyzing mean, median, and mode to determine patterns.  
- Variability metrics – Exploring standard deviation and variance in forensic image integrity.  

By applying quantitative analysis techniques, we will further validate forensic image integrity metrics and explore deeper insights into potential anomalies and compression effects.  

This concludes our mini-pilot study phase, setting the stage for statistical evaluation and forensic data analysis. Stay tuned for the next post!  

---  

### REFERENCES

1. **Wales, G. S., Smith, J. M., Lacey, D. S., & Grigoras, C.** (2022). *Multimedia Stream Hashing: A Forensic Method for Content Verification*. Journal of Forensic Sciences. DOI: [10.1111/1556-4029.15148](https://doi.org/10.1111/1556-4029.15148)  

2. **Wales, G. S.** (2024). *Validation of Image Stream Hashing: A Forensic Method for Content Verification*. Journal of Forensic Sciences. DOI: [10.1111/1556-4029.15432](https://doi.org/10.1111/1556-4029.15432)  

3. **NIST** (2022). *Digital Investigation Techniques: A NIST Scientific Foundation Review*. [Available here](https://nvlpubs.nist.gov/nistpubs/ir/2022/NIST.IR.8354-draft.pdf)  

4. **SWGDE** (2025). *Tool and Method Testing for Digital Forensics*. [Available here](https://www.swgde.org/wp-content/uploads/2024/04/2024-03-07-SWGDE-Minimum-Requirements-for-Testing-Tools-Used-in-Digital-and-Multimedia-Forensics-18-Q-001-2.1.pdf)  

---

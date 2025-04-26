---
layout: post
title: "From Idea to Experiment: The Early Phases of Forensic Science Research"
date: 2025-04-26 09:30:00
categories: updates
---

### **Introduction: Two Paths to Forensic Inquiry—Explaining Anomalies vs. Advancing Research**  

In forensic science, structured investigation often emerges in two distinct ways:  

- A **practitioner** encounters an anomaly—such as a digital artifact, unexpected file alteration, or forensic inconsistency—and must determine its cause for courtroom testimony.  
- A **researcher** identifies a gap in existing knowledge and sets out to conduct a structured study that contributes to forensic science literature.  

Both paths demand a **methodical approach**, whether the goal is to defend an analysis in court or publish findings in an academic journal.  

Let’s use a simple research topic framed as a **research question (RQ)**:  
*"Does uploading an image to Google Drive alter its integrity?"*  

A **digital forensic examiner** may need to verify file authenticity for litigation, while a **researcher** may see an opportunity to assess cloud storage’s impact on forensic preservation.  

This post will guide you through the foundational phases of forensic research, whether you’re solving an urgent forensic mystery or setting the stage for peer-reviewed research.  

---

### **1. Formulating the Research Question & Hypothesis**  

A strong **research question (RQ)** provides direction for the study and ensures relevance to forensic science applications.  

Whether addressing an anomaly encountered in a forensic case or expanding published research, the question should be:  

- **Specific and Clear** – Avoid overly broad inquiries that lack focus.  
  - If our research interest is focused only on **JPEG files**, we refine the question:  
    > *"What happens to a JPEG image when we upload it to Google Drive?"*  

- **Forensically Relevant** – The question must contribute to the field, whether by solving practical issues or advancing theoretical understanding.  
  - To make the question **forensically relevant**, we refine it further:  
    > *"Does uploading a JPEG image to Google Drive alter its original integrity?"*  

- **Investigable** – Can data be systematically gathered to answer the RQ? If the question can’t be tested, it needs refinement.  

Now that we’ve established a **specific and forensically relevant research question**, the next step is determining whether we can **test whether uploading a JPEG image to Google Drive alters its original integrity**. This requires selecting appropriate forensic measurement tools to detect potential changes.  

### **Forensic Measurement Tools for Image Integrity**  

To assess image integrity, we will use:  

- **Hash Verification** – Generating cryptographic hash values (e.g., SHA-256, MD5) before and after upload to detect bit-level modifications. If the hash values remain identical, the image is unchanged.  
- **Exif Metadata Analysis** – Examining embedded metadata using tools like **ExifTool** to identify alterations in parameters such as resolution, compression, timestamps, or embedded thumbnails.  
- **Pixel-Level Comparison Metrics** – Since we have a control image, full-reference metrics will provide meaningful integrity assessments:  
  - **Pearson Correlation Coefficient (PCC)** – Measures similarity between pixel intensity distributions across images.  
  - **Peak Signal-to-Noise Ratio (PSNR)** – Evaluates the degree of signal loss, with higher values indicating closer similarity to the control image.  
  - **Structural Similarity Index (SSIM)** – Quantifies structural distortions, offering a perceptual quality comparison.  
  - **Multi-Scale Structural Similarity (MS-SSIM)** – A refined version of SSIM that accounts for variations at different resolution levels.  

These methods provide a **structured way to assess forensic integrity**, ensuring our research question is not only investigable but that results can be validated with empirical evidence.  

### **Final Research Question:**  
> *"Does uploading a JPEG image to Google Drive alter its original integrity?"*  

---

### **RQ to Hypothesis**  

Now that we have our **Research Question (RQ)**, we turn it into a **hypothesis**.  

### **Difference Between Hypothesis and Theory**  

A **hypothesis** is a **testable prediction** based on prior knowledge, observations, or literature. It suggests a possible relationship between variables and can be confirmed or refuted through experimentation.  

A **theory**, on the other hand, is a **well-established explanation** of a phenomenon supported by extensive empirical evidence over time. While a hypothesis is an **early-stage assumption**, a theory is the **result of repeated validation and refinement** across multiple studies.  

#### **Key Differences:**  

| **Aspect**           | **Hypothesis**                                     | **Theory**                                      |  
|----------------|-----------------------------------|-----------------------------------|  
| **Definition**     | A proposed explanation or prediction for a specific phenomenon. | A well-substantiated explanation based on repeated testing and observations. |  
| **Testability**   | Designed to be tested and falsified through empirical research. | Broadly validated by multiple experiments and research over time. |  
| **Scope**         | Narrow—focuses on a specific question or relationship between variables. | Wide—explains multiple phenomena and general principles. |  
| **Example**       | **Hypothesis:** "Uploading a JPEG image to Google Drive alters its original integrity." | **Theory:** Digital image compression algorithms systematically introduce artifacts that impact forensic analysis. |  

### **Developing the Hypothesis**  

I prefer using both **Null and Alternative hypotheses** rather than just stating the Null. Defining both ensures clarity in forensic testing.  

#### **Null Hypothesis (H₀):**  
*"Uploading a JPEG image to Google Drive does not alter its original integrity."*  

- This assumes that **Google Drive preserves the file** without introducing compression, re-encoding, or other modifications that impact forensic analysis.  
- If results show **identical hash values** and **unchanged pixel structures (PCC, SSIM, PSNR, MS-SSIM)** between the original and downloaded image, **we fail to reject the null hypothesis**, indicating no alteration occurred.  

#### **Alternative Hypothesis (Ha):**  
*"Uploading a JPEG image to Google Drive alters its original integrity."*  

- This suggests that **Google Drive modifies the image** in some way—whether through **compression, metadata changes, or pixel-level distortions**.  
- If findings show **hash mismatches**, **metadata alterations**, or **measurable differences in structural integrity metrics (PSNR, SSIM, MS-SSIM)**, we **reject the null hypothesis** in favor of the alternative hypothesis, confirming changes occurred.  

These hypotheses establish a **clear forensic testing framework**, if no detectable changes occur, the **null hypothesis holds**; if integrity alterations are confirmed, the **alternative hypothesis is supported**.  

Notice that the alternative includes **Ha** instead of **H₁**, both are acceptable, but I lean toward **Ha** because that was the notation required in my college courses. **In other words, it comes down to personal preference.**  


---

### **2. Conducting a Literature Review**  

Before diving into experimentation, researchers and forensic practitioners must assess existing knowledge to ensure their study is built upon solid groundwork. A well-executed literature review helps:  

- **Frame the research within current forensic practices**  
- **Validate the necessity of the study by identifying gaps or contradictions**  
- **Avoid redundant studies and ensure methodological improvements**  

#### **Strategies for Sourcing and Analyzing Existing Studies**  

To conduct a meaningful review, researchers should focus on **high-quality sources** such as:  

- **Peer-Reviewed Journals** – The **Journal of Forensic Sciences**, **Digital Investigation**, and **Forensic Science International** publish rigorously vetted studies.  
  
- **Conference Proceedings** – Events like the **International Conference on Digital Forensics & Cybersecurity** often present cutting-edge forensic techniques before formal journal publication.  
  
- **Technical Reports & Standards** – Organizations like **NIST**, **SWGDE**, and **ISO** publish guidelines that shape forensic best practices.  
  
- **Published Case Studies** – Examining forensic cases where similar anomalies have been investigated can provide insight into methodological approaches.  

To analyze sources effectively:  
- **Use citation tracking** to trace how theories and methodologies have evolved.  
  - Google Scholar’s **“Cited by” feature** allows researchers to track how a study has influenced subsequent research.  
  
  - However, in forensic multimedia analysis, adoption of new methodologies takes time especially in foundational areas such as collection procedures and pre-analysis preparation. Researchers should remain aware that forensic techniques may not immediately gain widespread use, even if validated in peer-reviewed studies.

- **Compare methodologies** in prior research to assess strengths, weaknesses, and where your study can refine or expand.  
- **Prioritize forensic applicability**—research unrelated to forensic investigations may lack practical relevance.  

#### **Determining if There’s an Unresolved Gap or Contradiction in the Field**  

A strong forensic research study should **address a gap or contradiction** within existing literature. Consider:  

- **Are prior studies limited by sample size or outdated methodologies?**  
  
- **Do contradictory findings exist regarding the forensic integrity of digital images stored in the cloud?**  
  
- **Has cloud storage’s impact on forensic image authentication been addressed using modern techniques like PCC, PSNR, SSIM, or MS-SSIM?**  

Historically, forensic image authentication has relied on **cryptographic hash verification**, but modern forensic validation increasingly incorporates **perceptual metrics like SSIM and MS-SSIM** to detect subtle alterations.  

#### **Articulating How Your Research Contributes New Insight**  

Once gaps are identified, the literature review must clarify **how your study advances forensic science**:  

- **Does it refine forensic methodologies?**  
- **Does it improve digital evidence validation?**  
- **Does it introduce new approaches for forensic practitioners?**  

For example, if your study systematically compares **image integrity across different cloud storage services**, it could influence forensic best practices for authenticating digital evidence in court.  

By framing the literature review within forensic science's practical demands, researchers ensure their study is both **methodologically sound** and **impactful in forensic investigations**.  

#### **But I Don't Have Access to Academic Library Research Resources**  

Conducting a thorough literature review without access to academic databases can be challenging, but it’s not impossible. One of the best freely available tools for forensic researchers is **Google Scholar**.  

Using Google Scholar, you can search for keywords and phrases related to your proposed research and locate relevant papers. Some are publicly available and can be downloaded, but others may be restricted behind paywalls. So, how can you still leverage those papers if full access isn’t possible?  

### **Alternative Strategies for Accessing Key Research**  

Even without direct access, you can extract valuable insights from restricted papers by employing the following approaches:  

- ***Review References*** – Many papers provide full access to their reference lists. These cited sources may offer foundational information that supports your study or lead you to publicly accessible versions of prior research.  
- ***Explore Related Works by the Same Authors*** – Researchers often publish earlier versions of their work or follow up on previous findings with newer studies. Searching for additional publications by the same authors may uncover accessible versions that contain key details.  
- ***Find Papers That Cite the Work*** – Other researchers referencing the restricted paper may summarize its findings in publicly available studies. Reviewing these secondary sources can help contextualize the research and provide sufficient insight for your own literature review.  
- ***Check Preprint Archives*** – Some researchers share open-access versions of their studies on platforms like **arXiv**, **ResearchGate**, or **Social Science Research Network** before formal journal publication. Searching for your topic on these sites may uncover full-text versions of relevant studies.  

By combining these techniques, you can construct a meaningful review of existing forensic research—even without formal library database access. While direct access to academic sources is always preferable, **strategic searching and citation tracing** can ensure your research remains well-informed and methodologically grounded.  

---

Your **exploratory research section** is well-structured, methodologically sound, and highly practical for forensic practitioners. Below are **recommended refinements** to improve clarity, readability, and depth while reinforcing forensic best practices:  

### **Refinements & Enhancements**  

1. **Clarifying Pilot Study Purpose:**  
   - Consider reinforcing that **pilot studies help prevent false starts** in forensic research, ensuring that flawed methodologies **do not compromise larger data collection efforts**.  

2. **Expanding the Role of Control Tests:**  
   - You discuss **controlled alterations**—consider briefly mentioning that control tests **can also validate software behaviors**, ensuring forensic tools accurately detect expected changes.  

3. **Enhancing the Discussion on Measurement Instruments:**  
   - Consider briefly reinforcing that **multimedia stream hashing provides forensic verification beyond traditional file hashing**, helping detect **embedded content alterations** rather than just container-level changes.  

4. **Reference Citations:**  
   - I’ve sourced **relevant references** discussing forensic validation, pilot study methodologies, and multimedia stream hashing for content verification.  

---

### **3. Moving into Exploratory Mode**  

Once a research question is formulated and an initial literature review is completed, the next step is **exploratory analysis**—a critical phase where researchers determine whether an experiment is feasible and refine study parameters before committing to full-scale data collection. This process ensures the research is **methodologically sound and capable of yielding meaningful forensic data**.  

#### **Sketching a Pilot Study to Assess Feasibility**  

Before conducting a full experiment, a **pilot study** serves as a preliminary test to:  

- **Verify whether data collection methods are effective**  
  - Pilot studies provide an opportunity to refine data collection workflows. Establishing good methods here prevents **issues later in larger research datasets**, avoiding flawed methodologies that could compromise forensic integrity.  

  - However, **unexpected variables tend to appear** just when you think the process is solid—Murphy’s Law applies. I frequently find issues at this stage that require adjustments before the full study can begin. This phase is critical for identifying and mitigating **extraneous variables** before they impact final results.  

- **Identify unforeseen obstacles in the research process**  
  - Unexpected challenges often emerge during pilot studies. Researchers must remain flexible and ready to pivot methodologies as needed to ensure forensic accuracy.  

- **Ensure measurement techniques (also called measurement instruments) provide reliable forensic insights**  
  - If an issue arises with measurement instruments, it’s essential to **revisit the literature review** to find validated methodologies or published alternatives that improve reliability.  
  - Sometimes, existing tools can be **adapted** for forensic research with minimal adjustments. Otherwise, researchers must develop custom scripts—but referencing a **peer-reviewed scientific paper** strengthens validation of new methodologies.  

For our example research question (*Does uploading a JPEG image to Google Drive alter its original integrity?*), a pilot study could involve uploading a small, controlled dataset of images to Google Drive, then retrieving and analyzing them to detect changes.  

**Key Considerations:**  
- **Selection of Test Images** – Choose a representative sample of JPEGs with varying resolutions and compression levels.  
- **Controlled Environment** – Ensure consistent upload/download procedures to minimize external influences.  
- **Preliminary Analysis Methods** – Perform **hash verification (file container and stream hash), and image quality assessments** before large-scale testing.  

#### **Incorporating Control Tests in Pilot Studies**  

A crucial step in pilot studies is establishing **control tests** to ensure that measurement instruments function as expected **before analyzing experimental data**.  

**Lessons Learned from Pilot Studies:**  
- During past research projects, I’ve encountered instances where a **custom measurement instrument** failed to detect anticipated file alterations (e.g., compression artifacts introduced intentionally).  
- By running **controlled alterations**, such as applying **known compression levels**, researchers verify whether their tools correctly identify expected changes before moving on to larger datasets.  
- The pilot study phase is the ideal time to **catch flaws** in measurement techniques, ensuring that later forensic analysis does not yield unreliable results.  
- **Software validation can also be tested** during pilot studies, ensuring that forensic tools properly detect embedded alterations **beyond superficial file metadata checks**.  

#### **Defining Key Variables (Dependent, Independent, Extraneous)**  

To ensure clarity in analysis, researchers must define **variables**:  

- **Independent Variable** – The factor being tested or manipulated (e.g., uploading a JPEG image to Google Drive).  
- **Dependent Variable** – The outcome being measured (e.g., integrity changes detected through hash comparison or image quality analysis using PCC, SSIM).  
- **Extraneous Variables** – Uncontrolled factors that could affect results (e.g., Google Drive’s potential compression algorithms, file format settings, external network conditions).  

Researchers should also determine whether **automatic re-encoding or compression adjustments** occur when files are uploaded to cloud storage, as this could be an extraneous variable requiring separate evaluation.  

#### **Establishing Measurement Instruments—Ensuring Reliability and Validity**  

Selecting appropriate measurement instruments is essential for forensic validity. For image integrity analysis, common tools include:  

- **File Hash Verification** – SHA-256 and MD5 comparisons before and after upload.  
- **Multimedia Stream Hash Verification** – SHA-256 comparisons of the **multimedia contents rather than just the file container**, detecting embedded video or image alterations.  
- **Image Quality Metrics** – Full-reference metrics like **PCC, PSNR, SSIM, and MS-SSIM** provide **structural integrity comparisons** between the control and uploaded images.  

Reliability is established by ensuring **repeatability**—if repeated tests yield identical results, the measurement method is considered valid.  

By carefully structuring **exploratory research**, forensic practitioners and researchers can refine methodologies, test measurement instruments, and address potential challenges **before committing to full-scale data collection**.  

---

### **4. Preparing for Data Collection**  

Once exploratory testing is complete, the next phase involves **structuring the full-scale data collection process** to ensure validity, accuracy, and forensic reliability. Proper preparation safeguards the integrity of findings and minimizes sources of error before transitioning to statistical analysis. This is where we take our **lessons learned from the pilot study** and refine our data collection processes for maximum efficiency and forensic rigor.  

#### **Structuring Your Methodology for Forensic Rigor**  

A well-defined methodology ensures that forensic research is **repeatable, transparent, and defensible**, whether applied in academic settings or court proceedings. Consider the following key aspects:  

- **Controlled Environment** – Ensure consistency across all test conditions, such as upload/download protocols, network stability, and device settings.  
  - I cannot stress this enough—I’ve had to **pivot collection methods** due to **external issues**, like unexpected changes in licensing for forensic software. These are situations outside of your control, and sometimes you may need to **redo collections or completely shift** to a different method. Maintaining **version control** for forensic tools ensures repeatability if software changes affect results.  

- **Standardized Procedures** – Establish clear steps for data collection, including image preprocessing, metadata extraction, and forensic comparison techniques.  
  - I like to create **visual workflows** or **step-by-step guides** because, as a visual person, they help maintain clarity and consistency across all collection phases.  

- **Chain of Custody Documentation** – If findings are intended for forensic testimony, strict data tracking is essential, including timestamps and audit logs for uploaded/downloaded images.  
  - My chain of custody **always begins with hashing**, and hash verification should occur **at multiple points throughout the data collection process** to ensure forensic integrity.  
  - In court, I’ve seen cases where critical documentation was lost or damaged—but **hash values of the original digital media** saved the case by proving data integrity.  

- **Validation with Replication** – Conduct multiple rounds of testing to confirm that results remain consistent across different samples.  

For our study on **Google Drive image integrity**, maintaining forensic rigor means controlling how images are uploaded, downloaded, and processed while thoroughly documenting all metadata changes.  

#### **Identifying Possible Limitations Before Running Full-Scale Experiments**  

Every forensic study encounters potential limitations—**identifying them early** helps prevent flawed conclusions and ensures robust methodologies. Some possible concerns include:  

- **Cloud Processing Interference** – Certain platforms **apply automatic compression or re-encoding** to specific file types, potentially impacting forensic measurements. Google Drive’s behavior toward JPEGs needs **verification**.  

- **External Environmental Factors** – Differences in upload/download speeds, device hardware, or software versions may influence results. **Standardizing test conditions** prevents variability.  

- **Measurement Instrument Sensitivity** – Some forensic tools **may fail to detect subtle alterations**, leading to potential misinterpretations of digital evidence. **Testing sensitivity during the pilot study** ensures measurement reliability before full-scale testing.  
  - *Forensic tools that fail to detect subtle changes could lead to misinterpretations in evidence analysis, underscoring the need for sensitivity testing.*  

- **Sample Size Considerations** – Ensure a **diverse dataset** of JPEG images to prevent findings from being overly dependent on a single image type or resolution.  
  - Since cloud storage platforms **apply different compression behaviors**, forensic researchers should consider testing **across multiple services** (e.g., Google Drive, Dropbox, OneDrive) if generalizing findings beyond one platform.  

By **acknowledging limitations before data collection**, researchers avoid wasted effort and ensure the study remains **methodologically sound**.  

#### **Refining Collection Techniques in Anticipation of Statistical Analysis**  

Statistical analysis depends on **clean, structured data**—refining collection methods ensures results are **interpretable and reliable**.  

- **Standardize Naming and Organization** – Maintain **clear file-naming conventions** and a structured directory for uploads/downloads to facilitate accurate tracking.  

- **Automate Data Collection Where Possible** – Using **scripted tools** minimizes human error in **hash verification, metadata extraction, and pixel-level comparisons**.  

- **Predefine Metrics for Image Integrity** – Ensure collected data aligns with planned statistical analysis, including variables such as **hash consistency, SSIM values, and metadata alterations**.  

- **Prepare for Anomaly Detection** – Implement protocols to flag **unexpected results**, such as images where hash mismatches occur unexpectedly or metadata changes contradict expectations.  
  - Remember my **Controlled Test**? I intentionally introduce errors and **break my expectations** of results to assess whether my anomaly detection methods are effective. Running **edge-case forensic tests**, such as testing **intentionally degraded images**, further ensures that measurement tools can **accurately capture alterations**.  
  - Controlled degradations—such as **adding compression artifacts, noise distortions, or format conversions**—help validate **measurement instrument sensitivity** before full-scale forensic testing.  

By refining these techniques **before collecting full-scale data**, forensic researchers ensure their study produces **credible, replicable, and statistically sound conclusions**.  


---

### **Mini-Pilot Study: Testing JPEG Integrity After Cloud Storage Upload**  

#### **Step 1: Control vs. High-Compression Baseline Test**  
- Compare the **original minimally compressed image** with the **highly compressed control** using:  
  - **PCC** (to measure pixel correlation),  
  - **PSNR** (to assess signal degradation),  
  - **SSIM/MS-SSIM** (to detect structural integrity differences).  
- Confirm that your measurement tools successfully identify differences between the two.  

#### **Step 2: Uploading to Google Drive**  
- **Upload the minimally compressed JPEG** to your Google Account.  
- Ensure consistent upload settings—preferably via a web browser rather than a third-party app to minimize extraneous variables.  

#### **Step 3: Downloading and Testing for Image Integrity**  
- Download the image from Google Drive and compare it against the original using:  
  - **File Hash Verification** (SHA-256 to detect byte-level differences),  
  - **Image Stream Hash Verification** (SHA-256 to detect byte-level differences),
  - **PCC, PSNR, SSIM, MS-SSIM** (to compare pixel structure before and after cloud transfer).  

#### **Step 4: Evaluating Findings**  
- If the **hash values remain identical**, Google Drive likely preserved the image without modification.  
- If the **Image Stream Hash values remain identical**, Google Drive likely preserved the image without modification.  
- If **structural integrity metrics (PSNR, SSIM) show variation**, discuss potential forensic implications.  

---  

### **Mini-Pilot Study Set-Up**  

Forensic validation requires ensuring that **measurement instruments correctly detect expected image changes** while avoiding false detections of intact images. Before proceeding, we will conduct **two control tests**:  

1. **Control-Test-1: Validate measurement instruments by testing identical images**—ensuring forensic tools **correctly classify matching images as identical**.  
2. **Control-Test-2: Evaluate forensic detection of compression artifacts**—confirming that measurement instruments **accurately flag compression-induced alterations** in digital images.  

---

#### **Control-Test-1: Measuring Identical Image Similarity**  

This control test **validates whether forensic tools correctly identify two identical images as unchanged**, ensuring they do not falsely detect variations when none exist.  

#### **Testing Hypothesis:**  
- **Null Hypothesis (H₀):** There are NO differences between the JPEG images.  
- **Alternative Hypothesis (Ha):** There ARE differences between the JPEG images.  

#### **Test Files:**  
- **Reference:** `Control-1.jpg`  
- **Questioned:** `Control-1-copy.jpg`  

> *The questioned file was created by making an exact copy of the reference image. Since no modifications occurred, forensic tests should confirm an exact match.*  

---

#### **Hash Analysis**  

Used **Hasher v2.0** to conduct a file hash analysis:  

| **FileName** | **SHA256 Hash** |  
|-------------|----------------|  
| Control-1.JPG | `02BC049.....9F9F8FB0F` |  
| Control-1-copy.JPG | `02BC049.....9F9F8FB0F` |  

**Findings:** Hashes match, confirming bitstream-level integrity.  

---

#### **Image Quality Assessment Measurements (IQA)**  

| **IMG Stream** | **IMG Sub Diff** | **PCC** | **PSNR** | **SSIM** | **MS-SSIM** |  
|--------------|----------------|------|------|------|---------|  
| **Match** | **0** | **1** | **1** | **1** | **1** |  

#### **Interpretation of Metrics:**  
 **All forensic metrics confirm integrity preservation**—verifying that forensic measurement tools **correctly classify identical images as unchanged**.  

---

#### **Control-Test-1 Conclusion:**  
*We accept the Null Hypothesis—there are NO differences between the JPEG images.*  

---

### **Control-Test-2: Measuring Compression-Induced Image Variations**  

This control test **evaluates whether forensic tools correctly detect compression-induced image degradation**—confirming measurable differences between an original and highly compressed image.  

#### **Testing Hypothesis:**  
- **Null Hypothesis (H₀):** There are NO differences between the JPEG images.  
- **Alternative Hypothesis (Ha):** There ARE differences between the JPEG images.  

#### **Test Files:**  
- **Reference:** `Control-2.jpg`  
- **Questioned:** `Compressed-Control-2.jpg`  

> *The questioned file was created using MATLAB to apply increased compression to the reference image. Forensic tests should confirm measurable integrity loss.*  

---

#### **JPEG Compression Levels (Measured via ImageMagick)**  

| **FileName** | **Magick Quality Score** |  
|-------------|---------------------|  
| Control-2.jpg | **95** (Minimal Compression) |  
| Compressed-Control-2.jpg | **25** (High Compression) |  

- **A JPEG compressed at 25** loses significant detail, introduces artifacts, and reduces color accuracy—appearing **blurred or blocky**, especially in fine textures.  
- **A JPEG saved at 95** preserves detail and color fidelity, maintaining **sharp edges and smoother gradients**, though with a larger file size.  

---

#### **Hash Analysis**  

Used **Hasher v2.0** to conduct a file hash analysis:  

| **FileName** | **SHA256 Hash** |  
|-------------|----------------|  
| Control-2.JPG | `02BC049.....9F9F8FB0F` |  
| Compressed-Control-2.JPG | `2C186C8.....420156959` |  

**Findings:** Hashes do NOT match—confirming compression-induced modifications.  

---

#### **Image Quality Assessment Measurements (IQA)**  

| **IMG Stream** | **IMG Sub Diff** | **PCC** | **PSNR** | **SSIM** | **MS-SSIM** |  
|--------------|----------------|------|------|------|---------|  
| **No Match** | **5605554** | **0.99653** | **0** | **0.86622** | **0.95843** |  

#### **Interpretation of Metrics:**  
-  **IMG Stream mismatch** confirms **byte-level differences in compressed images**.  
- **High pixel difference (IMG Sub Diff: 5605554)** suggests noticeable structural alterations.  
- **PCC (0.99653)** indicates high similarity, but **not a perfect match** due to compression artifacts.  
-  **PSNR (0)** suggests **extreme signal loss**, a hallmark of aggressive compression.  
-  **SSIM (0.86622)** indicates **moderate structural degradation** affecting forensic authentication.  
-  **MS-SSIM (0.95843)** confirms **multi-scale integrity loss, but retains some resemblance**.  

---

#### **Control-Test-2 Conclusion:**  
*We reject the Null Hypothesis—compression introduces measurable differences between the JPEG images.*  



---
Here is the **updated version**, ensuring all refinements while strictly using **dashes (- or --) instead of checkmarks** for formatting consistency:  

---

### **Mini-Pilot Test**  

This **mini-pilot test** illustrates one of several forensic validation tests designed to determine whether **uploading a JPEG image to Google Drive affects its integrity**.  

In this instance, I created a subfolder in Google Drive named `"Pilot-Study"` and **dragged and dropped** the image into the folder. When conducting a full forensic validation, researchers should test **both drag-and-drop uploads and file selection uploads**, as different methods could introduce variations in processing.  

To ensure controlled retrieval, I selected the `"Pilot-Study"` folder for download, which automatically converted it into a **ZIP file**—this ensures the download process does not introduce external handling effects that could alter the test file.  

---

#### **Testing Hypothesis:**  
- **Null Hypothesis (H₀)** -- Uploading a JPEG image to Google Drive does not alter its original integrity.  
- **Alternative Hypothesis (Ha)** -- Uploading a JPEG image to Google Drive does alter its original integrity.  

---

#### **Test Files:**  
- **Reference** -- `Control-Copy-4-Upload.jpg`  
- **Questioned** -- `Download-Control-Copy-4-Upload.jpg`  

-- The reference file was manually uploaded to Google Drive. The questioned file was downloaded from the `"Pilot-Study"` folder and extracted from the ZIP archive. If no modifications occurred, forensic tests should confirm an exact match.  

---

#### **Hash Analysis**  

Used **Hasher v2.0** to conduct file hash analysis:  

| **FileName** | **SHA256 Hash** |  
|-------------|----------------|  
| Control-Copy-4-Upload.jpg | `02BC049.....9F9F8FB0F` |  
| Download-Control-Copy-4-Upload.jpg | `02BC049.....9F9F8FB0F` |  

-- Findings -- Hashes match, indicating no byte-level modifications during upload or download.  

---

#### **Image Quality Assessment Measurements (IQA)**  

| **IMG Stream** | **IMG Sub Diff** | **PCC** | **PSNR** | **SSIM** | **MS-SSIM** |  
|--------------|----------------|------|------|------|---------|  
| **Match** | **0** | **1** | **1** | **1** | **1** |  

-- Findings -- All IQA metrics confirm the images are identical, reinforcing forensic integrity.  

---

#### **Mini-Pilot Study Test Conclusion:**  
-- We **accept the Null Hypothesis** -- Uploading a JPEG image to Google Drive **does not alter its original integrity**.  

---

#### **Final Considerations:**  
It is essential to note that this **represents only one of several validation tests** required for a complete forensic study. Additional tests should evaluate:  
- **Different upload/download methods** -- API-based transfers vs. manual uploads.  
- **Image alterations under various storage conditions** -- Including network congestion and metadata handling.  

By conducting **multiple controlled experiments**, forensic researchers ensure findings are **comprehensive, repeatable, and applicable to real-world forensic investigations**.  

---

### Moving Forward: Data Analysis & Descriptive Statistics

In the next post, we will transition into data analysis, where we systematically examine collected data using descriptive statistics to summarize findings. This will include:
- Central tendency measures – Analyzing mean, median, and mode to determine patterns.
- Variability metrics – Exploring standard deviation and variance in forensic image integrity.

By applying quantitative analysis techniques, we will further validate forensic image integrity metrics and explore deeper insights into potential anomalies and compression effects.

This concludes our mini-pilot study phase, setting the stage for statistical evaluation and forensic data analysis. Stay tuned for the next post!



---

## REFERENCES

1. **Wales, G. S., Smith, J. M., Lacey, D. S., & Grigoras, C.** (2022). *Multimedia Stream Hashing: A Forensic Method for Content Verification*. Journal of Forensic Sciences. DOI: [10.1111/1556-4029.15148](https://doi.org/10.1111/1556-4029.15148)  

2. **Wales, G. S.** (2024). *Validation of Image Stream Hashing: A Forensic Method for Content Verification*. Journal of Forensic Sciences. DOI: [10.1111/1556-4029.15432](https://doi.org/10.1111/1556-4029.15432)  

3. **NIST** (2022). *Digital Investigation Techniques: A NIST Scientific Foundation Review*. [Available here](https://nvlpubs.nist.gov/nistpubs/ir/2022/NIST.IR.8354-draft.pdf)  

4. **SWGDE** (2025). *Tool and Method Testing for Digital Forensics*. [Available here](https://www.swgde.org/wp-content/uploads/2024/04/2024-03-07-SWGDE-Minimum-Requirements-for-Testing-Tools-Used-in-Digital-and-Multimedia-Forensics-18-Q-001-2.1.pdf)  

5. **Breitinger, F., Hilgert, J.-N., Hargreaves, C., Sheppard, J., Overdorf, R., & Scanlon, M.** (2024). *DFRWS EU 10-Year Review and Future Directions in Digital Forensic Research*. Forensic Science International: Digital Investigation. DOI: [10.1016/j.fsidi.2024.301685](https://doi.org/10.1016/j.fsidi.2024.301685)  
   
6. **Faizal, A., & Luthfi, A.** (2024). *Comparison Study of NIST SP 800-86 and ISO/IEC 27037 Standards as a Framework for Digital Forensic Evidence Analysis*. Journal of Information Systems and Informatics. DOI: [10.51519/journalisi.v6i2.717](https://doi.org/10.51519/journalisi.v6i2.717)  
   

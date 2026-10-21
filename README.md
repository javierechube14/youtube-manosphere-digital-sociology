# Digital Sociology of the Manosphere and Stoicism on YouTube

**An exploratory computational sociology project examining online masculinity, contemporary Stoicism, audience engagement, emotional polarity, and external monetization links on YouTube.**

**Author:** Javier Echube Bestue  
**Degree:** BA in Sociology, Universitat de València, Spain  
**Academic context:** Undergraduate research and independent data-analysis learning project

---

## 1. Project Overview

This project explores how computational methods can be applied to sociological questions about digital platforms, online masculinity, and contemporary Stoicism.

It examines YouTube content at the intersection of Stoic self-development discourse and the manosphere, a broad and internally diverse online environment concerned with masculinity, gender relations, and men's identities.

The project combines sociological theory with exploratory data analysis to investigate patterns in video engagement, audience comment sentiment, manosphere-related terminology, and external links that may direct users towards other platforms or commercial spaces.

The purpose is not to classify all Stoic content as part of the manosphere, nor to assume that negative sentiment automatically indicates ideological radicalization. Instead, the project investigates whether observable patterns in digital content and audience responses can help formulate more precise sociological questions.

This is my **second independent learning project in data analysis**. It represents a step in my ongoing development towards computational social science and the application of quantitative and computational tools to social research.

## 2. Research Objectives

The project has four main objectives:

1. **Explore digital content:** Examine the intersection between contemporary Stoicism, online masculinity, and manosphere-related discourse on YouTube.
2. **Analyse audience responses:** Investigate the distribution of positive, neutral, and negative sentiment in selected comment samples.
3. **Examine terminology and sentiment:** Test whether the presence of manosphere-related vocabulary is associated with differences in comment sentiment.
4. **Identify exploratory content profiles:** Use clustering to investigate whether videos differ in engagement, negative sentiment, and the presence of external links.

A further exploratory objective is to compare sentiment classifications in Spanish- and German-language comment samples, while acknowledging the methodological limitations of cross-language comparison.

## 3. Sociological Background

The project draws on digital sociology, masculinity studies, and research on platform-mediated communication.

Its theoretical starting point is that digital platforms are not simply neutral spaces where social attitudes are expressed. Platform structures, recommendation systems, visibility incentives, and the circulation of content can shape how discourses become visible and how audiences interact with them.

The manosphere is treated as a heterogeneous field of online discourse rather than a single unified community. Contemporary Stoicism is also approached as a diverse set of practices and narratives, which can range from philosophical self-development to content focused on status, masculinity, and gender relations.

The project therefore investigates a possible intersection between these discourses without assuming that they are equivalent or that their association necessarily produces radicalization.

## 4. Data and Sources

The project uses YouTube content and comments collected for exploratory analysis.

The data collection workflow is based on the **YouTube Data API v3**. Depending on the analysis, the collected information includes video metadata, audience engagement indicators, comments, and external links found in video descriptions.

The project also explores a comparison between Spanish- and German-language content.

### Data considerations

- The findings refer to the content and comments collected for this project, not to all YouTube content or all users in Spain and Germany.
- YouTube search results and API-based collection do not constitute a random or representative sample of the platform.
- Comment sentiment is an automated classification, not a direct measurement of users' psychological states.
- The presence of an external link does not establish that a video generates revenue or that users complete a purchase.
- Only data that can be verified and appropriately shared should be included in the public repository.

**Data availability:** [Describe the actual public, processed, or reproducible data included in this repository. Do not claim that raw data are available unless they are included and can legally be shared.]

## 5. Methodology

The project follows an exploratory computational workflow.

### 5.1. Data collection and preparation

YouTube content and associated metadata are collected through the YouTube Data API v3. Python is used to organise the collected information into structured datasets suitable for analysis.

Data preparation includes selecting relevant variables, organising observations, and preparing video and comment datasets for subsequent analyses.

### 5.2. Engagement analysis

Engagement indicators are used to explore differences in audience interaction across videos.

These indicators are treated as descriptive measures. They do not directly establish the quality of a video, the beliefs of its audience, or its social influence.

### 5.3. Sentiment analysis

Comment sentiment is classified into three categories:

- **POS:** Positive sentiment
- **NEU:** Neutral sentiment
- **NEG:** Negative sentiment

The resulting distributions are used to explore patterns in audience responses and their association with selected terminology.

Automated sentiment analysis has important limitations, particularly when dealing with irony, context-dependent expressions, platform-specific language, and multilingual data.

### 5.4. Contingency tables and chi-square test

A contingency-table analysis is used to examine the association between the presence of manosphere-related terminology and comment sentiment.

The chi-square test evaluates whether the observed distribution differs from what would be expected under statistical independence. Cramér's V is used to assess the magnitude of the association.

A statistically significant association does not establish causality. It also does not demonstrate that a comment or its author is ideologically radicalised.

### 5.5. K-Means clustering

K-Means is used as an exploratory unsupervised-learning technique to group videos according to selected characteristics, including engagement, negative sentiment, and the presence of external links.

The analysis identifies three clusters in the reported sample:

| Cluster | Number of videos | Mean negative sentiment | Exploratory interpretation |
|---|---:|---:|---|
| Cluster 0 | 33 | 66.60% | Higher negative sentiment |
| Cluster 1 | 84 | 15.34% | Lower negative sentiment |
| Cluster 2 | 9 | 46.88% | Greater presence of external links |

These labels are descriptive interpretations of the observed variables, not definitive classifications of creators, ideological positions, or commercial strategies.

The figures should be read alongside the corresponding notebook outputs and the methodological limitations discussed below.

### 5.6. Spanish–German comparison

The project also compares the distribution of automated sentiment labels in Spanish- and German-language comment samples.

The reported distributions are:

| Corpus | Negative (NEG) | Neutral (NEU) | Positive (POS) |
|---|---:|---:|---:|
| Spanish | 29.60% | 25.20% | 45.20% |
| German | 7.87% | 61.57% | 30.56% |

These figures describe the output of the sentiment-classification procedure. They should not be interpreted as definitive measurements of national cultural differences.

## 6. Key Findings

The exploratory analyses suggest several patterns worth investigating further.

### 6.1. Differences between video profiles

The clustering procedure identifies three groups with different distributions of negative sentiment, engagement, and external links. The largest group contains 84 videos, while the other groups contain 33 and 9 videos, respectively.

This suggests that the selected characteristics are not distributed uniformly across the analysed sample. However, clustering alone does not establish why these differences occur or whether they correspond to stable social categories.

### 6.2. Manosphere-related terminology and comment sentiment

The reported contingency-table analysis examines whether comments containing manosphere-related terminology differ in sentiment distribution from comments without that terminology.

The interpretation focuses on statistical association rather than causal influence. The magnitude of the association is also important: statistical significance does not necessarily imply a strong relationship.

### 6.3. Cross-language differences require caution

The German-language corpus contains a substantially higher proportion of comments classified as neutral than the Spanish-language corpus.

However, the sentiment-classification procedure was not validated to an equivalent standard in both languages. The observed difference may therefore reflect differences in model performance as well as differences in the underlying comments.

The comparison is consequently treated as exploratory rather than as evidence that one national audience is inherently more neutral, analytical, emotional, or confrontational.

## 7. Limitations

The project has several limitations that are important for interpreting its findings.

**Sampling and platform coverage.** The collected videos and comments are not necessarily representative of YouTube as a whole. Platform search, content availability, and API constraints can influence the resulting sample.

**Automated sentiment classification.** Sentiment labels are model-generated estimates. They can misclassify irony, slang, context-dependent expressions, and ambiguous language.

**Cross-language comparability.** The sentiment model was primarily adapted to Spanish. Its use with German-language comments creates a risk of systematic classification errors, particularly in the neutral category. Without validation in both languages, direct cultural interpretations are not justified.

**Interpretation of negative sentiment.** Negative sentiment is not equivalent to ideological polarisation, misogyny, hostility, or radicalisation. These concepts require separate operational definitions and appropriate evidence.

**Interpretation of external links.** The detection of external URLs identifies potential pathways to other websites or services. It does not establish successful monetisation, commercial intent in every case, or actual user conversion.

**Clustering.** K-Means produces groups based on the variables and preprocessing choices supplied to the algorithm. Cluster labels are analytical interpretations, not naturally occurring categories.

**Reproducibility and data access.** Reproducing the analysis may require access to the relevant data, the required Python packages, and a valid YouTube API key. API access, data availability, and platform policies may affect whether the original collection process can be repeated exactly.

These limitations are part of the project's learning process and provide a basis for improving the design of future research.

## 8. Tools and Technologies

The project uses the following tools and methods where applicable in the notebook:

- **Python** — programming and analysis
- **Pandas** — data organisation and manipulation
- **NumPy** — numerical operations
- **SciPy** — statistical tests and contingency-table analysis
- **Scikit-learn** — K-Means clustering and machine-learning utilities
- **YouTube Data API v3** — video and metadata collection
- **Natural Language Processing (NLP)** — automated sentiment classification and text analysis
- **Jupyter Notebook / Google Colab** — interactive development and documentation
- **Matplotlib / Seaborn** — visualisation, if used in the notebook

The exact package requirements should be checked against `requirements.txt` before running the notebook.

## 9. Repository Structure

The repository is organised to separate code, documentation, and exported results.

```text
youtube-manosphere-digital-sociology/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   └── youtube_manosphere_analysis.ipynb
├── docs/
│   └── sociological_report_es.pdf
└── outputs/
    ├── tables/
    └── figures/
```

Only files that actually exist should be included. The `outputs` directory should contain verified tables or figures exported from the analysis. Data directories should only be added when the included data can appropriately be shared.

## 10. How to Run the Notebook

The notebook can be opened through GitHub or downloaded and executed in a compatible Jupyter environment or Google Colab.

### Option A: Google Colab

1. Open the notebook file from this repository.
2. Download the notebook if necessary.
3. Upload it to Google Colab.
4. Install the required packages listed in `requirements.txt`.
5. Provide a valid YouTube Data API key if the data-collection cells require one.
6. Run the cells in order.
7. Check that the expected input datasets are available before running the analysis cells.

### Option B: Local Jupyter environment

1. Install a compatible Python version.
2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Start Jupyter Notebook or JupyterLab.
4. Open the notebook in the `notebooks/` directory.
5. Configure any required API credentials securely.
6. Make sure the required input data are available and run the notebook from the beginning.

**Important:** The notebook may not reproduce every result if the original input data are unavailable or if API responses have changed. Never replace missing empirical data with simulated observations and present them as real findings.

Do not commit API keys, access tokens, passwords, or other private credentials to the repository.

## 11. Academic Report

The complete sociological report is written in Spanish and provides the theoretical framework, methodological discussion, results and conclusions

## 12. Author and Academic Context

Javier Echube Bestue
Sociology Undergraduate
Universitat de València, Spain
Former Erasmus Exchange Student
Eberhard Karls Universität Tübingen, Germany

Research interests:

Computational Social Science

Digital Sociology

Social Data Analysis

Artificial Intelligence and Society

Social Inequality and Online Communities

This project is part of an ongoing effort to connect sociological theory with practical data-analysis skills. My academic background is in Sociology, and I am progressively developing my technical abilities through independent projects involving data collection, data preparation, statistical analysis, and computational methods.

As an early-stage project, this work prioritises learning, transparency, and critical interpretation over claims of technical completeness. Future projects will build on these foundations and incorporate improvements in data validation, multilingual text analysis, and reproducible research workflows.

## 13. Ethical and Responsible Use

This project analyses publicly accessible platform content for educational and sociological research purposes.

Public availability does not remove all ethical considerations. Comments and other user-generated content can still contain personal information or sensitive statements. Data shared in this repository should be limited to what is necessary for understanding and reproducing the analysis, and should respect applicable platform policies and data-protection requirements.

No individual user's comment should be treated as sufficient evidence of their broader beliefs, psychological characteristics, or ideological identity.

## 14. Project Status

Status: Exploratory undergraduate research project.

This repository documents a learning process in computational sociology. The findings should be interpreted in light of the sampling, measurement, and language-related limitations described above.

The project is intended as a starting point for further learning and research, not as a definitive classification of online communities or a causal explanation of digital radicalisation.

Report language: Spanish. Repository documentation: English.

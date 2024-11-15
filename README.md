# Metabolomics Landscape App
Embeddings Explorer for The Landscape of Metabolomics Research

# Overview
This Streamlit app, Landscape of Metabolomics Research, is designed to help users visualize and explore trends in metabolomics research using data-driven techniques. The app provides interactive visualizations of research embeddings generated by a transformer-based model (PubMedBERT), which converts scientific abstracts into numerical representations. These embeddings are then visualized using t-SNE plots. The app also allows users to search for specific keywords and authors within the dataset.

# Features
1. Embeddings Explorer:
- Visualizes t-SNE embeddings colored by publication year and the presence of specific keywords within abstracts or titles.
- Users can select specific research clusters and keywords to narrow down their search.
- Customizable search parameters include selecting specific research clusters, keywords, and searching by abstract or title.

2. Author Highlighting:
- Users can search for publications by specific authors and visualize their work in the embeddings plot.                       
3. Email Findings:
- The app provides functionality to submit findings via email, allowing users to send their research results directly from the app.

# Usage
1. Home Page:
- Learn about the study, its goals, and the methods used.
- Watch an informative video about the research on metabolomics.
  
2. Embeddings Explorer:
- Navigate to the Embeddings Explorer via the sidebar.
- Enter the cluster name, keywords, and the location (abstract or title) to search for relevant studies.
- Click "Generate Plot" to display a t-SNE plot with research publications colored by keyword presence and publication year.
- Search for specific authors by name to highlight their work in the plot.
- Optional: Display all other papers not matching the search criteria for context.

3. Submit Findings:
- Users can enter their research findings in the provided text box and submit them via email.

# Installation
To run the app, ensure that the required dependencies are installed:

```bash
pip install streamlit pandas plotly openpyxl
```

To run the app locally, use the command:

```bash
streamlit run app.py
```

# Dependencies
The app relies on the following libraries:

- Streamlit: For the web interface.
- Pandas: For handling the dataset.
- Plotly: For creating interactive visualizations.
- Openpyxl: To read Excel files.
- Smtplib: For sending emails.

# Data
The dataset used is an Excel file (metabolomics_landscape_app_01MAR2024.xlsx) containing research papers with columns including:

- tsne_2D_x, tsne_2D_y: Embedding coordinates for plotting.
- predicted_category: The research cluster assigned to each paper.
- abstract, title, authors: Metadata for each paper.
- pub_year: Publication year.

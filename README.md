Visual Product Matcher

## Project Overview
This repository contains a **Visual Product Matcher ** web application that leverages **OpenAI's CLIP (Contrastive Language-Image Pretraining) model** and **FAISS (Facebook AI Similarity Search)** to enable fast and accurate visual similarity search. Users can upload an image file or provide an image URL to find visually similar products from a catalog of 50+ items. The app displays the uploaded image alongside the top matches, including metadata such as product name and category.

## Features
- **Image Upload:** Upload local image files or input image URLs.  
- **Visual Similarity Search:** Uses CLIP + FAISS to find visually similar products.  
- **Product Database:** Contains 50+ product images with metadata.  
- **Web Interface:** Built with Streamlit for easy and responsive usage.  
- **Filters & UX:** Results can be filtered by similarity score; includes loading indicators and error handling.  
- **Mobile Responsive:** UI adjusts for mobile devices.

## Installation
1. Clone the repository:
```bash
git clone https://github.com/<your-username>/Unthinkable_project.git
Navigate to the project folder:

bash
cd Unthinkable_project
(Optional) Create a virtual environment:

bash
python -m venv venv
Activate it:

Windows: venv\Scripts\activate

Mac/Linux: source venv/bin/activate

Install dependencies:

bash
pip install -r requirements.txt
Run the app:

bash
streamlit run app.py
Open your browser at http://localhost:8501/unthinkable to use the application.

Demo dataset includes 50+ product images with metadata.
Images stored in static/data/images/.
Mapping file: static/image_paths.json.
Index file: static/index.faiss.

Unthinkable_project/
├── static/
│   ├── data/
│   │   └── images/          # Product images
│   ├── image_paths.json     # Mapping file
│   └── index.faiss          # Index file
├── templates/
│   └── index.html           # Web app template
├── app.py                   # CLI app
├── index.py                 # Indexing images
├── serve.py                 # Web app
├── README.md                # This file
└── requirements.txt         # Python dependencies

Approach Summary
This project integrates OpenAI CLIP and Faiss to create a visual product search engine. Each product image is processed through the pretrained CLIP model to generate a vector embedding representing its visual features. These embeddings are stored and indexed with Faiss, enabling efficient similarity searches across a large dataset. Users can upload an image or provide an image URL, which is also converted into a CLIP embedding. Faiss then identifies the nearest embeddings in the index, returning the most visually similar products. The web interface displays the uploaded image alongside top results and their metadata, with optional filtering by similarity score.

The application emphasizes user experience through responsive design, loading states, and error handling. By combining a state-of-the-art vision model with an optimized similarity search library, this solution demonstrates a practical approach to visual search applications, suitable for e-commerce or catalog systems. The project is fully extendable, allowing additional products or dataset updates, and can be hosted locally or on compatible cloud services. Overall, it provides an intuitive and efficient tool for users to find products based on visual similarity, showcasing both the power of modern AI models and effective search algorithms.

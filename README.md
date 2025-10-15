Visual Product Build

## Project Overview
This repository contains a **Visual Product Build** web application that leverages **OpenAI's CLIP (Contrastive Language-Image Pretraining) model** and **FAISS (Facebook AI Similarity Search)** to enable fast and accurate visual similarity search. Users can upload an image file or provide an image URL to find visually similar products from a catalog of 50+ items. The app displays the uploaded image alongside the top matches, including metadata such as product name and category.

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
The project uses CLIP to extract embeddings from images, encoding visual information like color, shape, and texture into dense vectors. FAISS indexes these embeddings to allow fast similarity searches. When a user uploads an image or provides a URL, its embedding is computed and compared to the product database to retrieve the top visually similar items. The Streamlit frontend displays the uploaded image alongside results, including product metadata and similarity scores. Filters allow refinement of results. Error handling and loading states improve user experience, while the responsive design ensures usability on mobile devices. This approach demonstrates practical application of AI-powered image search for product matching in real-world scenarios.

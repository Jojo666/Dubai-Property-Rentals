# Dubai-Property-Rentals
# 🏡 Multimodal Property Search

A Hugging Face Space that allows users to search Dubai properties using natural language — with results including matching **rental listings** and **interior images**.

App Demo: https://minerva666-multimodalrental.hf.space/?__theme=system&deep_link=KkJ8r6uxJ-A
## 🚀 Features

- 💬 **Semantic Search:** Users can query using phrases like:
  - "affordable 2 bedroom in Business Bay"
  - "luxury flat in Bur Dubai"
- 🏠 **Property Matching:** Listings are scored based on:
  - Rent category (high/low)
  - Location match
  - Number of bedrooms
  - ML Assessment (overvalued/fair/etc.)
- 🖼️ **Image Display:** Results include interior photos pulled from the dataset (`Interior_Image_URL`)

---

## 📁 Files

- `app.py`: Gradio UI + semantic search logic
- `multimodal_df.csv`: Main dataset with property, pricing, and image info
- `requirements.txt`: Python dependencies

---

## 🧠 Tech Stack

| Tool | Purpose |
|------|---------|
| **Gradio** | Frontend UI for search |
| **Pandas** | DataFrame manipulation |
| **Python** | Semantic search logic |
| **Hugging Face Spaces** | Deployment |

---

## 💡 Project Background

This project is part of a **multimodal AI competition**, where the challenge is to integrate structured (e.g., rent, beds) and unstructured data (e.g., images) to build a **real-world, ML-powered experience**.

---

## 🧪 Development Journey

### ✅ **Phase 1: Kaggle + BigQuery**

Initially developed on Kaggle using:

- ✅ `BigQuery SQL` to query and aggregate 73K+ properties
- ✅ Data joins, type casts, and analytics via:
  - `SELECT`, `GROUP BY`, `COUNT()`, `CAST()`

**Attempted but not available due to restrictions:**

- ❌ `ML.GENERATE_EMBEDDING()`
- ❌ `ML.GENERATE_TEXT()`
- ❌ `VECTOR_SEARCH()`

> ❗ These were essential for Approach 1/3 but couldn't be used due to lack of access to required models/features.

---

### 🔄 **Phase 2: Colab for AI + Multimodal Integration**

Due to environment limitations, I migrated to Google Colab and implemented:

- ✅ Image embedding using CLIP
- ✅ Semantic scoring manually in Python
- ✅ Joined image URLs and metadata
- ✅ Built a search function that prioritizes query intent

---

### ✅ **Phase 3: Hugging Face Deployment**

- Deployed final working app to Hugging Face Spaces
- Ensured:
  - Query parsing
  - Matching property metadata
  - Display of top search results with **photo + rent + address**

---

## 📌 How to Use

1. Enter a search query (e.g., _"affordable 2 bedroom in Dubai"_)
2. Click **Submit**
3. View top 3–5 matching homes and their images

---

## 📈 Future Improvements

- Add CLIP-based **embedding search** for image/text semantic matching
- Introduce filters (sliders/dropdowns for price/area)
- Integrate map view using coordinates
- Expose an API for property search

---

## 🤝 Acknowledgements

- Google BigQuery Public Dataset
- Gradio + Hugging Face Spaces
- OpenAI CLIP (used in Colab for embeddings)


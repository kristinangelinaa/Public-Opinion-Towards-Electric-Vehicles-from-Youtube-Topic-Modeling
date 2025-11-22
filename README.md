# Analysis of Public Opinion on Electric Vehicles in Indonesia Through YouTube Comments

A topic modeling research project using BERTopic to analyze public sentiment and discourse around electric vehicles in Indonesia from 2018-2024.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![BERTopic](https://img.shields.io/badge/BERTopic-Neural%20Topic%20Modeling-orange)](https://github.com/MaartenGr/BERTopic)

## 📋 Overview

This research analyzes the evolution of public opinion regarding electric vehicles in Indonesia by examining YouTube comments using advanced topic modeling techniques. The study employs BERTopic, a state-of-the-art neural topic modeling approach, to identify and categorize discussion themes from 138,662 YouTube comments collected over seven years.

### Key Findings

- **Dataset**: 138,662 raw comments → 49,104 processed comments
- **Timeframe**: 2018-2024
- **Top Topic**: "Electric vs Gasoline Car Economics" (6,856 comments)
- **Main Focus**: Economic comparisons between electric and fossil fuel vehicles

## 🎯 Research Objectives

1. Analyze changes in public opinion on electric vehicles in Indonesia through YouTube comments
2. Apply BERTopic topic modeling to identify key discussion themes
3. Evaluate the results to understand public concerns and interests
4. Provide insights for policymakers and EV manufacturers

## 🔬 Methodology

### Data Collection
- **Method**: Web crawling from YouTube
- **Source**: Comments from various EV-related videos
- **Fields Collected**: 
  - Author
  - Timestamp (updated_at)
  - Like count
  - Comment text
  - Video ID
  - Public visibility status

### Data Preprocessing

1. **Indonesian Language Filter**
   - Filtered using `langid` library
   - Result: 82,074 Indonesian comments from 138,662 total

2. **Word Distribution Filter**
   - Minimum 8 words per comment
   - Final dataset: 49,104 comments

### Topic Modeling Pipeline

```
Raw Data → Preprocessing → Embedding (IndoBERTweet) → 
Dimensionality Reduction (UMAP) → Clustering (K-Means) → 
Vectorization (CountVectorizer) → Weighting (c-TF-IDF) → 
Representation Tuning (OpenAI)
```

#### Key Components

- **Embedding Model**: IndoBERTweet - Indonesian language pre-trained BERT model
- **Dimensionality Reduction**: UMAP (Uniform Manifold Approximation and Projection)
- **Clustering**: K-Means algorithm
- **Vectorization**: CountVectorizer with stopword removal
- **Weighting Scheme**: c-TF-IDF (class-based TF-IDF)
- **Representation**: OpenAI GPT for human-readable topic labels

## 📊 Results

### Top 5 Topics Identified

| Rank | Topic | Count | Description |
|------|-------|-------|-------------|
| 1 | Electric vs Gasoline Car Economics | 6,856 | Economic comparison between EV and gasoline vehicles |
| 2 | Mobil Subsidi Beli YG | 5,800 | Discussion on vehicle subsidies |
| 3 | Future of Affordable Electric Vehicles | 5,380 | Affordability and future prospects of EVs |
| 4 | Pricing of Vehicle in Indonesia | 5,174 | Vehicle pricing discussions |
| 5 | Indonesian Electric Vehicle Subsidies | 4,735 | Government subsidy programs |

### Key Insights

- Public discourse remains focused on **economic considerations** when comparing electric and fossil fuel vehicles
- **Affordability** and **subsidies** are major concerns for Indonesian consumers
- The debate encompasses both economic and environmental impacts

## 🛠️ Technical Stack

- **Language**: Python 3.8+
- **Topic Modeling**: BERTopic
- **Embedding**: IndoBERTweet
- **Dimensionality Reduction**: UMAP
- **Clustering**: K-Means
- **Data Processing**: Pandas, NumPy
- **NLP**: langid, CountVectorizer
- **API**: OpenAI GPT for representation tuning

## 📈 Data Distribution

- **Total Comments Collected**: 138,662
- **After Language Filter**: 82,074 (Indonesian only)
- **After Word Distribution Filter**: 49,104 (≥8 words)
- **Processing Period**: 2018-2024
- **Number of Topics Generated**: 10

## 🎓 Authors

- **Kristine Angelina Simanjuntak** - Universitas Pertamina
- **Muhamad Koyimatu** - Universitas Pertamina
- **Yolla Putri Ervanisari** - Universitas Pertamina

## 📄 Citation

If you use this research or code, please cite:

```bibtex
@article{simanjuntak2024analysis,
  title={Analisis Perubahan Opini Publik Terhadap Kendaraan Listrik di Indonesia Melalui Komentar YouTube: Pendekatan Topic Modeling BERTopic},
  author={Simanjuntak, Kristine Angelina and Koyimatu, Muhamad and Ervanisari, Yolla Putri},
  journal={Jurnal Inovasi Kewirausahaan},
  volume={1},
  number={3},
  year={2024},
  publisher={Universitas Pertamina}
}
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Universitas Pertamina for supporting this research
- YouTube content creators and commenters for providing valuable data
- BERTopic development team for the excellent topic modeling framework
- IndoBERTweet team for the Indonesian language model

## 📧 Contact

For questions or collaborations:
- Email: koyimatu@universitaspertamina.ac.id
- Institution: Universitas Pertamina, Jakarta Selatan

## 🔗 Related Publications

- DOI: 10.37817/jurnalinovasikewirausahaan.v1i3
- Journal: Jurnal Inovasi Kewirausahaan Vol 1 No 3 Oktober 2024

---

**Keywords**: BERTopic, Crawling, Electric Vehicles, Public Opinion, Topic Modeling, YouTube, Indonesia, Natural Language Processing, IndoBERTweet

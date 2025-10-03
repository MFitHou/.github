# 🌍 MFitHou - Linked Open Data Platform

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![OLP PMNM 2025](https://img.shields.io/badge/OLP%20PMNM-2025-green.svg)](https://olp.edu.vn)
[![Open Data](https://img.shields.io/badge/Open%20Data-LOD-orange.svg)](https://www.w3.org/DesignIssues/LinkedData.html)
[![SPARQL](https://img.shields.io/badge/SPARQL-1.1-red.svg)](https://www.w3.org/TR/sparql11-query/)

> **Open Data for Digital Transformation** 🚀

**MFitHou** là nền tảng **dữ liệu mở liên kết (Linked Open Data)** phục vụ nghiên cứu và chuyển đổi số, được phát triển trong khuôn khổ **Olympic Tin học Sinh viên Việt Nam – Phần mềm nguồn mở (OLP PMNM 2025)**.

## 📋 Tổng quan dự án

Hệ thống thu thập, chuẩn hóa và trực quan hóa dữ liệu mở từ **OpenStreetMap**, **Wikidata** và các nguồn khác, cung cấp API SPARQL và giao diện bản đồ tương tác để khám phá dữ liệu địa lý.

## 🏗️ Kiến trúc hệ thống

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│  Data Sources   │    │   Backend API    │    │   Frontend Web  │
│                 │    │                  │    │                 │
│ • OpenStreetMap │───▶│ • NestJS API     │───▶│ • React + TS    │
│ • Wikidata      │    │ • SPARQL Engine  │    │ • Leaflet Maps  │
│ • RDF/Turtle    │    │ • Fuseki Server  │    │ • Interactive UI│
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

## 🔧 Các thành phần chính

### 📥 [OpenDataFitHou](https://github.com/MFitHou/OpenDataFitHou) - Thu thập & Xử lý dữ liệu
- � **Thu thập dữ liệu**: Overpass API (OpenStreetMap) và Wikidata SPARQL
- 📊 **Xử lý dữ liệu**: Jupyter Notebooks với Python (rdflib, geopandas)
- 🔄 **Chuyển đổi định dạng**: GeoJSON → RDF/Turtle (.ttl)
- 📈 **Chuẩn hóa**: Làm sạch và enrichment metadata từ nhiều nguồn

**Dữ liệu có sẵn**: ATM, trạm xe bus, bệnh viện, trường học, sân chơi, nhà vệ sinh công cộng, điểm nước uống

### ⚙️ [open_data_backend](https://github.com/MFitHou/open_data_backend) - API & SPARQL Service
- 🚀 **REST API**: NestJS framework với TypeScript
- 🔗 **SPARQL Endpoint**: Tích hợp Apache Jena Fuseki
- 🌐 **Data Management**: Quản lý và phục vụ dữ liệu RDF
- 🔌 **Integration**: Cung cấp API cho frontend và ứng dụng khác

### 🗺️ [open_data_map](https://github.com/MFitHou/open_data_map) - Interactive Web Map
- 🎨 **Modern UI**: React 19 + TypeScript + Vite
- 🗺️ **Interactive Maps**: Leaflet với OpenStreetMap tiles  
- 🔍 **Smart Search**: Tích hợp Wikidata với SPARQL queries
- 📍 **Nearby Services**: Tìm kiếm dịch vụ lân cận (ATM, bệnh viện, etc.)
- ⬇️ **Data Export**: Xuất dữ liệu dạng XML và RDF/XML

## ✨ Tính năng nổi bật

- 🔍 **Tìm kiếm thông minh** với SPARQL và Wikidata integration
- 🗺️ **Bản đồ tương tác** với auto-highlighting và focus
- 📍 **Dịch vụ lân cận** - tìm ATM, bệnh viện, trạm xe bus gần bạn
- ⬇️ **Export dữ liệu** - XML và RDF/XML tuân theo chuẩn Linked Data
- 🌐 **RESTful API** với SPARQL endpoint cho developers
- 📱 **Responsive design** - tương thích mobile và desktop

## 🚀 Quick Start

### 1️⃣ Clone tất cả repositories
```bash
# Data processing
git clone https://github.com/MFitHou/OpenDataFitHou.git

# Backend API
git clone https://github.com/MFitHou/open_data_backend.git

# Frontend Map
git clone https://github.com/MFitHou/open_data_map.git
```

### 2️⃣ Chạy Backend (NestJS + Fuseki)
```bash
cd open_data_backend
npm install
npm run start:dev
# Server chạy tại: http://localhost:3000
```

### 3️⃣ Chạy Frontend (React + Vite)
```bash
cd open_data_map  
npm install
npm run dev
# Web app chạy tại: http://localhost:5173
```

### 4️⃣ Xử lý dữ liệu (Python Notebooks)
```bash
cd OpenDataFitHou
pip install -r requirements.txt
jupyter notebook
# Mở OverpassApi.ipynb và ParseRDF.ipynb
```

## 🎯 Mục tiêu dự án

- 🌍 **Open Data Ecosystem**: Thu thập và chuẩn hóa dữ liệu mở từ nhiều nguồn
- 🔗 **Linked Open Data**: Xây dựng hệ thống LOD giúp tích hợp và tái sử dụng dễ dàng  
- 📊 **Data Visualization**: Trực quan hóa dữ liệu địa lý trên bản đồ tương tác
- 🚀 **Digital Transformation**: Hỗ trợ nghiên cứu và ứng dụng chuyển đổi số
- 🎓 **Education**: Phục vụ học tập và nghiên cứu về Semantic Web

## �️ Tech Stack

### Data Processing
- 🐍 **Python**: rdflib, geopandas, pandas, requests
- 📓 **Jupyter**: Interactive data processing notebooks
- 🌐 **APIs**: Overpass API, Wikidata SPARQL Service

### Backend
- 🚀 **NestJS**: Modern Node.js framework
- 📊 **Apache Jena Fuseki**: RDF database và SPARQL endpoint
- 🔍 **SPARQL**: Query language cho RDF data
- 📡 **REST API**: Chuẩn RESTful cho data access

### Frontend  
- ⚛️ **React 19**: Latest React với TypeScript
- ⚡ **Vite**: Fast build tool với HMR
- 🗺️ **Leaflet**: Interactive maps library
- 🎨 **Modern CSS**: Responsive và accessible UI

## 📊 Dữ liệu

### Nguồn dữ liệu
| Nguồn | Mục đích | Format |
|-------|----------|---------|
| 🌍 **OpenStreetMap** | Dữ liệu địa lý, POI | GeoJSON → RDF |
| 🔗 **Wikidata** | Metadata, identifiers | SPARQL → RDF |
| 📊 **Linked Data** | Semantic relationships | RDF/Turtle |

### Loại dữ liệu hiện có
- 🏧 **ATM** - Máy rút tiền tự động
- 🚌 **Bus Stops** - Trạm xe buýt  
- 🏥 **Hospitals** - Bệnh viện và phòng khám
- 🏫 **Schools** - Trường học các cấp
- 🚻 **Public Toilets** - Nhà vệ sinh công cộng
- 🚰 **Drinking Water** - Điểm nước uống
- 🎮 **Playgrounds** - Sân chơi trẻ em

## 🤝 Đóng góp

Chúng tôi hoan nghênh mọi đóng góp! Xem [CONTRIBUTING.md](CONTRIBUTING.md) để biết chi tiết.

### Cách đóng góp:
1. 🍴 Fork repository bạn muốn đóng góp
2. 🔧 Tạo feature branch (`git checkout -b feature/amazing-feature`)
3. ✅ Commit changes (`git commit -m 'Add amazing feature'`)
4. 📤 Push to branch (`git push origin feature/amazing-feature`)  
5. 🔄 Tạo Pull Request

## 📄 License

Dự án này được phân phối dưới [GNU General Public License v3.0](LICENSE). Xem `LICENSE` để biết chi tiết.

## 🏆 OLP PMNM 2025

Dự án được phát triển cho **Olympic Tin học Sinh viên Việt Nam – Phần mềm nguồn mở 2025**.

---
<div align="center">

**⭐ Nếu dự án hữu ích, hãy cho chúng tôi một star! ⭐**

[🌍 Demo](https://mfithou.github.io/open_data_map) • [📚 Docs](https://github.com/MFitHou/OpenDataFitHou/wiki) • [🐛 Issues](https://github.com/MFitHou/OpenDataFitHou/issues) • [💬 Discussions](https://github.com/MFitHou/OpenDataFitHou/discussions)

</div>  

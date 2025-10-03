<div align="center">

# 🌍 MFitHou - Linked Open Data Platform

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=32&duration=2800&pause=2000&color=36BCF7FF&center=true&vCenter=true&width=600&lines=Open+Data+Platform;Linked+Data+Solutions;Digital+Transformation" alt="Typing SVG" />

</div>

<div align="center">

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg?style=for-the-badge&logo=gnu&logoColor=white)](https://www.gnu.org/licenses/gpl-3.0)
[![Hackathon HOU](https://img.shields.io/badge/Hackathon-HOU%20IT-00D084?style=for-the-badge&logo=education&logoColor=white)](https://hou.edu.vn)
[![OLP PMNM 2025](https://img.shields.io/badge/OLP%20PMNM-2025-FF6B6B?style=for-the-badge&logo=medal&logoColor=white)](https://vfossa.vn/tin-tuc/gioi-thieu-chu-de-cuoc-thi-phan-mem-nguon-mo-olp-2025-746.html)

[![Open Data](https://img.shields.io/badge/Open%20Data-LOD-FF8C42?style=for-the-badge&logo=database&logoColor=white)](https://www.w3.org/DesignIssues/LinkedData.html)
[![SPARQL](https://img.shields.io/badge/SPARQL-1.1-E74C3C?style=for-the-badge&logo=apache&logoColor=white)](https://www.w3.org/TR/sparql11-query/)
[![GitHub stars](https://img.shields.io/github/stars/MFitHou?style=for-the-badge&logo=github&color=yellow)](https://github.com/MFitHou)

<img src="https://github.com/MFitHou/MFitHou/assets/74038190/0b335028-1d3d-4ee5-b5b3-a373d499be7e" width="800">

</div>

<div align="center">

> **🚀 Open Data for Digital Transformation 🚀**
> 
> *Transforming raw data into meaningful insights through the power of Linked Open Data*

</div>

**MFitHou** là nền tảng **dữ liệu mở liên kết (Linked Open Data)** phục vụ nghiên cứu và chuyển đổi số, được phát triển để tham gia **Hackathon Phần mềm Tự do Nguồn mở** cấp **Khoa Công nghệ Thông tin - Trường Đại học Mở Hà Nội** và tương lai là **Olympic Tin học Sinh viên Việt Nam – Phần mềm nguồn mở (OLP PMNM 2025)**.

## 📋 Tổng quan dự án

Hệ thống thu thập, chuẩn hóa và trực quan hóa dữ liệu mở từ **OpenStreetMap**, **Wikidata** và các nguồn khác, cung cấp API SPARQL và giao diện bản đồ tương tác để khám phá dữ liệu địa lý.

<div align="center">

## 🏗️ Kiến trúc hệ thống

<img src="https://github.com/MFitHou/MFitHou/assets/74038190/7d484dc9-a876-4d24-b4f2-88b0f99ec32d" width="50">

</div>

```mermaid
graph LR
    A[🌍 Data Sources<br/>OpenStreetMap<br/>Wikidata<br/>RDF/Turtle] 
    B[⚙️ Backend API<br/>NestJS API<br/>SPARQL Engine<br/>Fuseki Server]
    C[🗺️ Frontend Web<br/>React + TS<br/>Leaflet Maps<br/>Interactive UI]
    D[🗄️ Fuseki Storage<br/>103.77.246.176:3030<br/>RDF Database<br/>SPARQL Query]
    
    A -->|🔄 Process| B
    B -->|📡 API| C
    B -->|💾 Store| D
    D -->|🔍 Query| B
    
    style A fill:#FF6B6B,stroke:#333,stroke-width:2px,color:#fff
    style B fill:#4ECDC4,stroke:#333,stroke-width:2px,color:#fff
    style C fill:#45B7D1,stroke:#333,stroke-width:2px,color:#fff
    style D fill:#96CEB4,stroke:#333,stroke-width:2px,color:#fff
```

**🗄️ Lưu trữ dữ liệu**: Dữ liệu sau khi thu thập và xử lý sẽ được lưu trữ tại **Apache Jena Fuseki Server** với địa chỉ `103.77.246.176:3030/`. Hệ thống thực hiện truy xuất dữ liệu từ Fuseki thông qua SPARQL queries để hiển thị lên bản đồ tương tác.

<div align="center">

## 🔧 Các thành phần chính

<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="900">

</div>

<table>
<tr>
<td width="33%" align="center">

### 📥 [OpenDataFitHou](https://github.com/MFitHou/OpenDataFitHou)
**Thu thập & Xử lý dữ liệu**

<img src="https://skillicons.dev/icons?i=python,jupyter" />

🔍 **Thu thập dữ liệu**: Overpass API & Wikidata SPARQL  
📊 **Xử lý dữ liệu**: Jupyter Notebooks với Python  
🔄 **Chuyển đổi**: GeoJSON → RDF/Turtle (.ttl)  
📈 **Chuẩn hóa**: Enrichment metadata từ nhiều nguồn  

</td>
<td width="33%" align="center">

### ⚙️ [open_data_backend](https://github.com/MFitHou/open_data_backend)
**API & SPARQL Service**

<img src="https://skillicons.dev/icons?i=nestjs,nodejs,typescript" />

🚀 **REST API**: NestJS framework với TypeScript  
🔗 **SPARQL Endpoint**: Apache Jena Fuseki  
🗄️ **Data Storage**: RDF từ Fuseki server  
🔌 **Integration**: API cầu nối cho frontend  

</td>
<td width="33%" align="center">

### 🗺️ [open_data_map](https://github.com/MFitHou/open_data_map)
**Interactive Web Map**

<img src="https://skillicons.dev/icons?i=react,typescript,vite" />

🎨 **Modern UI**: React 19 + TypeScript + Vite  
🗺️ **Interactive Maps**: Leaflet với OSM tiles  
🔍 **Smart Search**: Wikidata SPARQL queries  
⬇️ **Data Export**: XML và RDF/XML formats  

</td>
</tr>
</table>

<div align="center">

**🏧 ATM** • **🚌 Bus Stops** • **🏥 Hospitals** • **🏫 Schools** • **🎮 Playgrounds** • **🚻 Public Toilets** • **🚰 Drinking Water**

</div>

### ⚙️ [open_data_backend](https://github.com/MFitHou/open_data_backend) - API & SPARQL Service
- 🚀 **REST API**: NestJS framework với TypeScript
- 🔗 **SPARQL Endpoint**: Tích hợp Apache Jena Fuseki tại `103.77.246.176:3030/`
- 🗄️ **Data Storage**: Lưu trữ và truy xuất dữ liệu RDF từ Fuseki server
- 🌐 **Data Management**: Quản lý và phục vụ dữ liệu RDF cho frontend
- 🔌 **Integration**: Cung cấp API cầu nối giữa Fuseki và ứng dụng bản đồ

### 🗺️ [open_data_map](https://github.com/MFitHou/open_data_map) - Interactive Web Map
- 🎨 **Modern UI**: React 19 + TypeScript + Vite
- 🗺️ **Interactive Maps**: Leaflet với OpenStreetMap tiles  
- 🔍 **Smart Search**: Tích hợp Wikidata với SPARQL queries
- 📍 **Nearby Services**: Tìm kiếm dịch vụ lân cận (ATM, bệnh viện, etc.)
- ⬇️ **Data Export**: Xuất dữ liệu dạng XML và RDF/XML

<div align="center">

## ✨ Tính năng nổi bật

<img src="https://user-images.githubusercontent.com/74038190/225813708-98b745f2-7d22-48cf-9150-083f1b00d6c9.gif" width="500">

</div>

<div align="center">
<table>
<tr>
<td align="center" width="50%">

### 🔍 Tìm kiếm thông minh
<img src="https://github.com/MFitHou/MFitHou/assets/74038190/d08f5cc2-8c4a-4f20-a45c-0a5b5e8b7c68" width="60">

**SPARQL & Wikidata Integration**  
Tích hợp AI-powered search với độ chính xác cao

---

### 📍 Dịch vụ lân cận  
<img src="https://github.com/MFitHou/MFitHou/assets/74038190/b3ef3a17-c5a8-4e9f-8c29-4e8c8b5c2a6f" width="60">

**Smart Location Services**  
Tìm ATM, bệnh viện, trạm xe bus gần bạn trong thời gian thực

---

### 🌐 RESTful API
<img src="https://github.com/MFitHou/MFitHou/assets/74038190/8c6e4d4c-0b8a-4f0e-8c29-4e8c8b5c2a6f" width="60">

**Developer-Friendly**  
SPARQL endpoint mạnh mẽ cho developers

</td>
<td align="center" width="50%">

### 🗺️ Bản đồ tương tác
<img src="https://github.com/MFitHou/MFitHou/assets/74038190/2c4c5a67-4d24-4f2e-8c29-4e8c8b5c2a6f" width="60">

**Interactive Mapping**  
Auto-highlighting và real-time focus

---

### ⬇️ Export dữ liệu
<img src="https://github.com/MFitHou/MFitHou/assets/74038190/7d484dc9-a876-4d24-b4f2-88b0f99ec32d" width="60">

**Multi-format Export**  
XML và RDF/XML tuân theo chuẩn Linked Data

---

### 📱 Responsive Design
<img src="https://github.com/MFitHou/MFitHou/assets/74038190/b48c1b47-4c8a-4f0e-8c29-4e8c8b5c2a6f" width="60">

**Cross-Platform**  
Tương thích hoàn hảo mobile và desktop

</td>
</tr>
</table>
</div>

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
# Kết nối với Fuseki server: 103.77.246.176:3030/
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
- 📊 **Apache Jena Fuseki**: RDF database và SPARQL endpoint (`103.77.246.176:3030/`)
- 🔍 **SPARQL**: Query language cho RDF data từ Fuseki server
- 📡 **REST API**: Chuẩn RESTful cho data access và integration

### Frontend  
- ⚛️ **React 19**: Latest React với TypeScript
- ⚡ **Vite**: Fast build tool với HMR
- 🗺️ **Leaflet**: Interactive maps library
- 🎨 **Modern CSS**: Responsive và accessible UI

## 📊 Dữ liệu

### Nguồn dữ liệu
| Nguồn | Mục đích | Format | Lưu trữ |
|-------|----------|---------|---------|
| 🌍 **OpenStreetMap** | Dữ liệu địa lý, POI | GeoJSON → RDF | Fuseki Server |
| 🔗 **Wikidata** | Metadata, identifiers | SPARQL → RDF | Fuseki Server |
| 📊 **Linked Data** | Semantic relationships | RDF/Turtle | `103.77.246.176:3030/` |

### Quy trình dữ liệu
```
Thu thập (OSM/Wikidata) → Xử lý (Python) → RDF/Turtle → Fuseki (103.77.246.176:3030/) → API → Bản đồ
```

### Loại dữ liệu hiện có
- 🏧 **ATM** - Máy rút tiền tự động
- 🚌 **Bus Stops** - Trạm xe buýt  
- 🏥 **Hospitals** - Bệnh viện và phòng khám
- 🏫 **Schools** - Trường học các cấp
- 🚻 **Public Toilets** - Nhà vệ sinh công cộng
- 🚰 **Drinking Water** - Điểm nước uống
- 🎮 **Playgrounds** - Sân chơi trẻ em

<div align="center">

## 👥 Đội ngũ phát triển

<img src="https://user-images.githubusercontent.com/74038190/219923809-b86dc415-a0c2-4a38-bc88-ad6cf06395a8.gif" width="300">

**Dự án được phát triển bởi đội ngũ sinh viên đam mê công nghệ và dữ liệu mở**

</div>

<div align="center">
<table>
<tr>
<td align="center" width="33%">

<img src="https://github.com/MFitHou/MFitHou/assets/74038190/d48893bd-0757-481c-8d7e-ba3e163feae7" width="100">

### 👨‍💻 **Vũ Hoàng Anh**
**� Data Engineer**

<img src="https://skillicons.dev/icons?i=python,jupyter,docker" />

⚙️ Fuseki Server Management  
🔧 API Design & Integration  
� Data Processing & ETL  

<img src="https://github-readme-stats.vercel.app/api?username=vuhoanganhdev&show_icons=true&theme=radical&hide_border=true" width="280">

</td>
<td align="center" width="33%">

<img src="https://github.com/MFitHou/MFitHou/assets/74038190/fe4eb68e-e2d1-4d48-b8b8-0e27a4b2e0f7" width="100">

### �‍💻 **Nguyễn Hồng Ánh**  
**🎨 Frontend Developer**

<img src="https://skillicons.dev/icons?i=react,typescript,css" />

🗺️ Interactive Map Features  
✨ Modern Web Development  
🎨 UI/UX Design Specialist  

<img src="https://github-readme-stats.vercel.app/api?username=nguyenhonganh&show_icons=true&theme=radical&hide_border=true" width="280">

</td>
<td align="center" width="33%">

<img src="https://github.com/MFitHou/MFitHou/assets/74038190/78f0025d-b85a-4a2d-8f3a-83fb2b4b3e9d" width="100">

### 👨‍💻 **Tống Tâm Xuân**
**🚀 Backend Architect**

<img src="https://skillicons.dev/icons?i=nestjs,nodejs,graphql" />

🔍 SPARQL Query Optimization  
🏗️ System Architecture  
⚡ Performance Optimization  

<img src="https://github-readme-stats.vercel.app/api?username=tongtamxuan&show_icons=true&theme=radical&hide_border=true" width="280">

</td>
</tr>
</table>
</div>

<div align="center">

<img src="https://user-images.githubusercontent.com/74038190/212284158-e840e285-664b-44d7-b79b-e264b5e54825.gif" width="600">

> *"🚀 Khi đam mê công nghệ kết hợp với tinh thần open source,  
> chúng ta tạo ra những giá trị tuyệt vời cho cộng đồng! 🌟"*

</div>

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

## 🏆 Cuộc thi & Mục tiêu

**Trước mắt**: Dự án được phát triển để tham gia **Hackathon Phần mềm Tự do Nguồn mở** cấp **Khoa Công nghệ Thông tin - Trường Đại học Mở Hà Nội**.

**Dài hạn**: Hướng tới tham gia **Olympic Tin học Sinh viên Việt Nam – Phần mềm nguồn mở (OLP PMNM 2025)**.

<div align="center">

<img src="https://user-images.githubusercontent.com/74038190/212284087-bbe7e430-757e-4901-90bf-4cd2ce3e1852.gif" width="800">

</div>

<div align="center">

## 🎯 Hãy ủng hộ dự án của chúng tôi!

<img src="https://github.com/MFitHou/MFitHou/assets/74038190/0b335028-1d3d-4ee5-b5b3-a373d499be7e" width="50">

**⭐ Nếu dự án hữu ích, hãy cho chúng tôi một star! ⭐**

<a href="https://mfithou.github.io/open_data_map">
  <img src="https://img.shields.io/badge/Demo-Live%20Preview-FF6B6B?style=for-the-badge&logo=vercel&logoColor=white" alt="Demo"/>
</a>
<a href="https://github.com/MFitHou/OpenDataFitHou/wiki">
  <img src="https://img.shields.io/badge/Docs-Documentation-4ECDC4?style=for-the-badge&logo=gitbook&logoColor=white" alt="Docs"/>
</a>
<a href="https://github.com/MFitHou/OpenDataFitHou/issues">
  <img src="https://img.shields.io/badge/Issues-Bug%20Reports-45B7D1?style=for-the-badge&logo=github&logoColor=white" alt="Issues"/>
</a>
<a href="https://github.com/MFitHou/OpenDataFitHou/discussions">
  <img src="https://img.shields.io/badge/Discussions-Community-96CEB4?style=for-the-badge&logo=discord&logoColor=white" alt="Discussions"/>
</a>

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=150&section=footer&text=Thank%20You%20for%20Visiting!&fontSize=42&fontColor=fff&animation=twinkling&fontAlignY=75"/>

</div>  

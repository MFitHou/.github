## Hi there 👋 Welcome to **MFitHou**

🙋‍♀️ **MFitHou** ứng dụng sử dụng **dữ liệu mở liên kết (Linked Open Data)** phục vụ nghiên cứu và chuyển đổi số.  
Dự án được triển khai trong khuôn khổ **Olympic Tin học Sinh viên Việt Nam – Phần mềm nguồn mở (OLP PMNM 2025)**.

🌍 Hệ thống của chúng tôi gồm 3 phần chính:
📥 **OpenDataFitHou (thu-thap)**
- Thu thập dữ liệu mở từ **Overpass API (OpenStreetMap)** và **Wikidata**.  
- Lưu trữ dữ liệu dạng **GeoJSON** và chuyển đổi sang **RDF (.ttl)**.  
- Cung cấp notebook xử lý, chuẩn hóa dữ liệu.

⚙️ **open_data_backend** – API và dịch vụ dữ liệu RDF/SPARQL.  
- Xây dựng API để quản lý và khai thác dữ liệu RDF.  
- Tích hợp **SPARQL endpoint** để truy vấn dữ liệu.  
- Cung cấp dịch vụ trung gian cho hệ thống bản đồ và các ứng dụng khác.
  
🗺 **open_data_map** – ứng dụng bản đồ trực quan hóa dữ liệu mở.  
- Ứng dụng web trực quan hóa dữ liệu trên bản đồ.  
- Hiển thị các đối tượng như: bến xe bus, ATM, bệnh viện, trường học…  
- Tương tác trực tiếp với API/backend để lấy dữ liệu.

## 🎯 Mục tiêu dự án
- Thu thập và chuẩn hóa **dữ liệu mở** từ nhiều nguồn khác nhau.  
- Xây dựng hệ thống **Linked Open Data** giúp dễ dàng tích hợp và tái sử dụng.  
- Cung cấp ứng dụng trực quan trên bản đồ để phục vụ **chuyển đổi số**.  

## 👩‍💻 Công nghệ
- **Thu thập dữ liệu**: Overpass API, Wikidata, Python (rdflib, geopandas).  
- **Backend**: .  
- **Frontend Map**: ReactJS + Leaflet/Mapbox.  

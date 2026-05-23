# Profesyonel OMR Sistemi (Professional OMR)

> Yapay Zeka Destekli, Multi-Platform Optik Okuma Sistemi

![Status](https://img.shields.io/badge/status-development-yellow)
![Python](https://img.shields.io/badge/python-3.10%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## 📋 Proje Hakkında

Profesyonel OMR Sistemi, optik işaretleme tanıma teknolojisini kullanarak sınav kağıtlarını otomatik olarak okur, işaretleri tanır ve puanlandırır. Yapay zeka teknolojisi ile hata tespiti yaparak profesyonel sonuçlar sunar.

### Temel Özellikler

✅ **Optik Tasarım Sistemi** - Profesyonel sınav şablonları oluşturma  
✅ **Otomatik Tanıma** - Kamera/Scanner ile okuma  
✅ **AI Doğrulama** - Hata ve anomali tespiti  
✅ **Ders Katsayıları** - Her ders için farklı katsayılar  
✅ **Otomatik Puanlama** - Hızlı ve doğru puanlama  
✅ **Raporlama** - PDF ve Excel çıktıları  
✅ **Multi-Platform** - Masaüstü, Web, Mobil  
✅ **Real-time Takip** - WebSocket ile canlı iletişim  

## 🏗️ Proje Mimarisi

```
professional-omr/
├── backend/                 # FastAPI Backend
│   ├── app/
│   │   ├── core/           # Optik, AI, Tanıma motorları
│   │   ├── api/            # API endpoints
│   │   ├── db/             # Database modelleri
│   │   ├── schemas/        # Pydantic schemas
│   │   └── main.py         # FastAPI app
│   ├── requirements.txt
│   └── Dockerfile
├── desktop/                 # PyQt5 Desktop App
├── web/                    # React Frontend
├── mobile/                 # React Native Mobile
└── docker-compose.yml
```

## 🚀 Başlangıç

### Backend Kurulumu

```bash
# Repository'yi klonla
git clone https://github.com/osmanfirdolas-hash/professional-omr.git
cd professional-omr

# Backend klasörüne gir
cd backend

# Virtual environment oluştur
python -m venv venv

# Aktivasyon
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# Gerekli paketleri yükle
pip install -r requirements.txt

# Sunucuyu başlat
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

### Docker ile Çalıştırma

```bash
docker-compose up -d
```

## 📚 Teknolojiler

### Backend
- **FastAPI** - Modern Python web framework
- **PostgreSQL** - İlişkisel veritabanı
- **Redis** - Cache ve session yönetimi
- **OpenCV** - Görüntü işleme
- **TensorFlow** - Yapay zeka modelleri
- **Celery** - Asenkron görevler

### Frontend
- **React** - Web arayüzü
- **React Native** - Mobil arayüzü
- **PyQt5** - Masaüstü arayüzü

## 🔧 API Endpoints

### Sınav Yönetimi
- `POST /api/v1/exams/create` - Sınav oluştur
- `GET /api/v1/exams/{exam_id}` - Sınav detayları
- `POST /api/v1/exams/{exam_id}/booklets` - Kitapçık oluştur

### Tarama
- `POST /api/v1/scans/upload` - Tarama yükle
- `WS /ws/scans/{session_id}` - Real-time tarama

### Puanlama
- `POST /api/v1/results/calculate` - Sonuç hesapla
- `GET /api/v1/results/{result_id}/pdf` - PDF dışa aktar
- `GET /api/v1/results/{result_id}/excel` - Excel dışa aktar

### AI
- `POST /api/v1/ai/detect-anomalies` - Anomali tespiti
- `POST /api/v1/ai/train-model` - Model eğitimi

## 📖 API Dokümantasyonu

Sunucu çalışırken şu adreslere erişebilirsiniz:
- **Swagger UI**: http://localhost:8000/docs
- **ReDoc**: http://localhost:8000/redoc

## 🤝 Katkı

Katkılar hoş geldindir! Lütfen:
1. Repository'yi fork et
2. Feature branch oluştur (`git checkout -b feature/amazing-feature`)
3. Değişiklikleri commit et (`git commit -m 'Add amazing feature'`)
4. Branch'i push et (`git push origin feature/amazing-feature`)
5. Pull Request aç

## 📝 Lisans

MIT License

## 👨‍💻 Yapımcı

**Osman Firdolas**
- GitHub: [@osmanfirdolas-hash](https://github.com/osmanfirdolas-hash)

---

**Durum:** 🔄 Aktif Geliştirme Aşamasında

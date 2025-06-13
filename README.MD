# 🚀 Vadim Kuzmitckii/ Вадим Кузьмицкий  
### Python Backend & Data Engineer, Web Scraping Specialist / Разработчик Python и Data Engineer, специалист по сбору и обработке информации с сайтов

**My projects / Мои проекты**

🏙️[vkpmonbot urban monitoring system / vkpmonbot — система мониторинга градостроительной документации Петербурга (Flask, BeautifulSoup, PyPDF, ocrmypdf,rosreestr2coord, telebot,...)](https://github.com/alfablend/vkpmonbot/tree/main).

⚖️[LLM Integration for Legal Document Analysis / Интеграция LLM для анализа юридических документов (Kontur.Focus + GPT4All)](https://github.com/alfablend/vkpcourt).     

📊[Проекты визуализации данных](https://github.com/alfablend/alfablend.github.io).

**Specialization / Специализация:**  
ETL processes, API integrations, data analysis / ETL-процессы, API-интеграции, анализ данных  

**Core Technologies / Ключевые технологии:**  
Python, Pandas, SQL, Telegram Bot API  

[![Telegram](https://img.shields.io/badge/Telegram-Contact-26A5E4?style=flat&logo=telegram)](https://t.me/alfablen)  
[![GitHub](https://img.shields.io/badge/GitHub-Projects-181717?style=flat&logo=github)](https://github.com/alfablend)  

---

## 🔥 **Problem Solved / Решение проблем:**  
Automation of urban data collection and analysis / 
Автоматизация сбора и анализа данных  

**Key Features / Основные функции:**  
- API data parsing / Парсинг данных через API   
- Data cleaning and transformation (Pandas) / Очистка и трансформация данных  
- Statistics visualization on the map (Geopandas/ Folium) / Визуализация статистики на карте
- Telegram notification bot / Telegram-бот для уведомлений  

---

## 🛠 Tech Stack / Технологический стек  
| Component / Компонент | Technologies / Технологии |
|-----------------------|---------------------------|
| **Data Extraction**<br>**Извлечение данных** | Python (requests/Selenium), Rosreestr2Coords API |PyPDF2, OpenCV, OCRmyPDF
| **Data Transformation**<br>**Трансформация данных** | Pandas, Regex, GPT4All python API |
| **Data Loading**<br>**Загрузка данных** | SQLite, CSV/Excel |
| **Automation**<br>**Автоматизация** | Telegram Bot API |
| **Analysis**<br>**Анализ** | Geopandas |

---

## 📊 Demonstration / Демонстрация  
### 1. ETL Pipeline: Government Permits Monitoring  


```python
import sqlite3
import requests
from time import sleep

# Config
DB_NAME = "permits.db"
API_URL = "https://api.example.com/permits"
HEADERS = {...} 

def init_db():
    """Initialize database with index for fast lookups"""
    conn = sqlite3.connect(DB_NAME)
    conn.execute("""
        CREATE TABLE IF NOT EXISTS permits (
            id TEXT PRIMARY KEY,
            stored_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
        );
    """)
    return conn

def process_permits(conn):
    """Fetch new permits and store unique ones"""
    response = requests.post(API_URL, headers=HEADERS)
    for permit in response.json():
        if not conn.execute("SELECT 1 FROM permits WHERE id=?", (permit['id'],)).fetchone():
            conn.execute("INSERT INTO permits (id) VALUES (?)", (permit['id'],))
            print(f"New permit: {permit['id']}")
            sleep(5)  # Polite delay

# Usage
if __name__ == "__main__":
    db = init_db()
    process_permits(db)
    db.commit()
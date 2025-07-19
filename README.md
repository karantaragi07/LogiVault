# LogiVault

👨‍💻 **Author:** Karan Taragi  
Backend Developer | Spring Boot | Kafka | IBM Db2  
📫 ksingh064002@gmail.com

---

LogiVault is a backend microservice that collects, stores, and retrieves system logs. It uses Spring Boot for REST APIs, Kafka for optional log ingestion, and IBM Db2 for log storage.

## 🔧 Tech Stack

- Spring Boot (Java 17+)
- Apache Kafka (optional)
- IBM Db2
- Maven / Gradle

## 🚀 Features

- Accepts logs via REST APIs
- Supports Kafka-based log ingestion
- Stores logs in IBM Db2
- Query logs by service, log level, or timestamp

## 📦 How to Run

```bash
# 1. Clone the project
git clone https://github.com/your-username/logivault.git
cd logivault

# 2. Start Kafka and Db2 (optional)
docker-compose up -d

# 3. Update `application.yml` with your Db2 config

# 4. Run services
cd log-ingestor
mvn spring-boot:run

cd ../log-query-service
mvn spring-boot:run


📬 Sample API JSON
POST /api/logs

{
  "service": "auth-service",
  "level": "ERROR",
  "message": "Invalid token",
  "timestamp": "2025-07-17T18:30:00"
}

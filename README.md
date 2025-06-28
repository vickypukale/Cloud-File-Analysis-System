# 📁 Cloud File Metadata Extractor using Cloud Storage, Cloud Run, Pub/Sub & GitHub Integration

This project demonstrates a **cloud-native architecture** where files uploaded to **Google Cloud Storage** trigger a workflow that identifies the file's **name**, **size**, and **format**. This data is processed using **Cloud Run**, deployed from a **GitHub repository**, and finally published to **Pub/Sub**, with logs viewable in both Pub/Sub subscriptions and Cloud Logging.

---

## 🚀 Features

- Upload file to Cloud Storage<br/>
- Trigger Cloud Run service (via GCS event)<br/>
- Extract file metadata: name, size, format<br/>
- Publish metadata to a Pub/Sub topic<br/>
- View results in Pub/Sub subscriber or logs

---

## 🧱 Architecture

```text
Cloud Storage --> Cloud Run (Trigger) --> Extract Metadata --> Publish to Pub/Sub --> View in Logs
                            |
                            |
                    Source code on GitHub
```

## 📂 Repository Structure

📁 your-project/<br/>
├── README.md           # Project documentation<br/>
├── index.js            # Core logic for metadata extraction & publishing<br/>
└── package.json        # Node.js project config & dependencies

## 🔧 Prerequisites
Make sure you have the following:<br/>
- A Google Cloud Project<br/>
- Billing enabled<br/>
- Enabled APIs:<br/>
-- Cloud Run<br/>
-- Cloud Storage<br/>
-- Cloud Pub/Sub<br/>
-- Artifact Registry (if deploying from source)<br/>
- GitHub repo with index.js and package.json<br/>
- Node.js 18+ installed locally (for testing)<br/>

## Format of results in Pub/Sub subscriber or logs

  File name  <br/> File size (in bytes)  <br/> File format (extension)

![image](https://github.com/user-attachments/assets/7e861fed-3de9-441c-96ba-515d294c9239)
![image](https://github.com/user-attachments/assets/412bcdfb-220f-480d-ac9d-d8379fed211c)

  
This project is maintained by Vicky Pukale
GitHub: https://github.com/vickypukale

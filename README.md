# 📁 Cloud File Metadata Extractor using Cloud Storage, Cloud Run, Pub/Sub & GitHub Integration

This project demonstrates a **cloud-native architecture** where files uploaded to **Google Cloud Storage** trigger a workflow that identifies the file's **name**, **size**, and **format**. This data is processed using **Cloud Run**, deployed from a **GitHub repository**, and finally published to **Pub/Sub**, with logs viewable in both Pub/Sub subscriptions and Cloud Logging.

---

## 🚀 Features

- Upload file to Cloud Storage
- Trigger Cloud Run service (via GCS event)
- Extract file metadata: name, size, format
- Publish metadata to a Pub/Sub topic
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

📁 your-project/
├── README.md           # Project documentation
├── index.js            # Core logic for metadata extraction & publishing
└── package.json        # Node.js project config & dependencies

## 🔧 Prerequisites
Make sure you have the following:
A Google Cloud Project
Billing enabled
Enabled APIs:
  Cloud Run
  Cloud Storage
  Cloud Pub/Sub
  Artifact Registry (if deploying from source)
GitHub repo with index.js and package.json
Node.js 18+ installed locally (for testing)

## Format of results in Pub/Sub subscriber or logs

  File name   File size (in bytes)   File format (extension)
  
This project is maintained by Vicky Pukale
GitHub: https://github.com/vickypukale

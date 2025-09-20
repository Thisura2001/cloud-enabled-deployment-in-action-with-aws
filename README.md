# Cloud Enabled Deployment In Action with GCP

This repository contains four projects:

* **course-service** (Spring Boot + MySQL)
* **student-service** (Spring Boot + MongoDB)
* **media-service** (Spring Boot + Local file storage, can be extended to GCS/MinIO)
* **frontend-app** (React + TypeScript)

---

## Backend Services

### 1. course-service

* **Entity:** Course(id, name, duration)
* **Endpoints:**

  * GET /courses
  * GET /courses/{id}
  * POST /courses
  * DELETE /courses/{id}
* **Default port:** 8081
* **Configure:** MySQL settings

### 2. student-service

* **Document:** Student(registrationNumber, fullName, address, contact, email)
* **Endpoints:**

  * GET /students
  * GET /students/{id}
  * POST /students
  * DELETE /students/{id}
* **Default port:** 8082
* **Configure:** MongoDB settings

### 3. media-service

* **Resource:** files
* **Endpoints:**

  * POST /files (multipart/form-data: file)
  * GET /files (list)
  * GET /files/{id} (fetch)
  * DELETE /files/{id} (delete)
* **Default port:** 8083
* **Storage:** Uses local disk storage at `./data/media` by default (override with env var `MEDIA_STORAGE_DIR`). Can be extended to **Google Cloud Storage (GCS)** or MinIO.

---

## Frontend (frontend-app)

* Built with **React + TypeScript + MUI + Axios + Vite**
* Contains 3 sections: **Courses, Students, Media**
* **Scripts:**

  * `npm run dev` → Vite dev server
  * `npm run build` → TypeScript build + Vite build
  * `npm run preview` → Preview built app

---

## Build

* **Backend:** run `mvn -q -e -DskipTests package` at repo root to build services.
* **Frontend:** run `npm install` then `npm run dev` inside `frontend-app`.

---

## Deployment

This project demonstrates **cloud-enabled deployment with Google Cloud Platform (GCP)**. Services can be deployed on **Cloud Run, GKE, or Compute Engine**, with MySQL on **Cloud SQL**, MongoDB on **Atlas/Compute**, and media storage on **Google Cloud Storage**.

Name:Thisura Liyanage
STID = 2301671024
email = thisuravimukthi123@gmail.com

---

## Demo Video

📺 Watch the full walkthrough here: [Project Demo Video](https://drive.google.com/file/d/1usDg9EKZZZIJxedxa0SNS-2QuzN1axZs/view?usp=sharing)

# 🏥 **Patient Management Domain**

## 📖 Description
The **Patient Management** domain is responsible for managing all patient-related information within the hospital system. Each CRUD action is designed as an independent microservice to ensure **modularity, scalability, and maintainability**.

---

## 🔹 Microservices

### ✅ **1. Create Patient**
- **📌 Description:** Registers a new patient in the system.
- **🔹 Method:** `POST`
- **🔗 Dependencies:** Encryption microservice 🔐
- **📥 Inputs:** Patient data (*name, date of birth, gender, address, phone number, username, and password*)
- **📤 Outputs:** Creation confirmation ✅

### 🔍 **2. Read Patient**
- **📌 Description:** Retrieves information about a specific patient.
- **🔹 Method:** `GET`
- **🔗 Dependencies:** Patient database 🗂️
- **📥 Inputs:** `Patient ID`
- **📤 Outputs:** Patient data 📄

### ✏️ **3. Update Patient**
- **📌 Description:** Modifies a patient's information.
- **🔹 Method:** `PUT`
- **🔗 Dependencies:** Patient database 🗄️, Encryption microservice 🔐 (to update the password if modified)
- **📥 Inputs:** `Patient ID` and updated data
- **📤 Outputs:** Update confirmation 🔄

### ❌ **4. Delete Patient**
- **📌 Description:** Removes a patient from the system.
- **🔹 Method:** `DELETE`
- **🔗 Dependencies:** Patient database 🗄️
- **📥 Inputs:** `Patient ID`
- **📤 Outputs:** Deletion confirmation 🗑️

---

## 🛠️ **Technologies Used**
- **⚙️ Backend:** Java, Spring Boot 💻
- **🗄️ Database:** PostgreSQL 🐘

---

## 🔗 **Integrations**
- **🩺 Medical Care Domain:** Patient data is used for scheduling medical appointments.
- **🩹 Clinical History Domain:** Patient data is used for recording their clinical history.

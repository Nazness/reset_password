# reset_password

This project demonstrates the automation of a password change process in an ITSM system using Ivanti Workflow and REST API.

## 📌 Use Case

Automate the process of changing a user password in an external system by triggering a REST API call from Ivanti workflow.

## 🔧 Technologies

* Ivanti ITSM Workflow
* REST API
* JSON
* Web Services

## 🔄 Process Overview

1. **User Request Initiation**
   A user creates a request via the Ivanti self-service portal (e.g. "Password Change").

2. **Workflow Execution**
   The Ivanti workflow is triggered based on the request and performs the following:

   * Sends a REST API request to the target system.
   * Passes the required parameters (username, new password) as a JSON payload.
   * Waits for a response (e.g., success or error message).

3. **API Request Format**

```http
POST /api/v1/change-password HTTP/1.1
Host: external-system.com
Content-Type: application/json

{
  "username": "useruser",
  "new_password": "NewStrongPassword123!"
}
```

4. **Response Handling**
   The workflow handles the API response:

   * On success: updates request status to "Completed".
   * On failure: logs error and sets status to "Failed".

## ✅ Outcome

* Fully automated password change process.
* Secure transfer via HTTPS.
* No manual interaction required after request submission.

---

## 📂 Files

* `README.md` – Project documentation
* `rest-api-spec.json` – Example payload structure
* `ivanti-workflow-diagram.png` – Visual of the Ivanti process (optional)

---




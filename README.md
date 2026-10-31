# 🤖 WhatsApp AI Agent for Executive Appointment Scheduling

An automated, AI-powered workflow built on [n8n](https://n8n.io/) that connects WhatsApp Business to Google Gemini, Google Calendar, and Gmail. It serves as an intelligent executive assistant that schedules appointments between clients and company representatives seamlessly over WhatsApp.

---

## 🌟 Features

* **💬 WhatsApp Integration**: Receives and responds to user messages via the 1MSG WhatsApp Business API Trigger.
* **🧠 Contextual AI Agent**: Powered by Google Gemini (`gemini-1.5-flash`) with conversation memory (`Simple Memory`).
* **📅 Google Calendar Scheduling**: Automatically checks availability and creates appointment events.
* **✉️ Gmail Confirmation**: Automatically dispatches formal confirmation emails to all meeting participants upon booking.
* **📊 Google Sheets Logging**: Reads/writes appointment and client records directly from a connected spreadsheet.

---

## 🏗️ Workflow Architecture

```text
[ WhatsApp Trigger ] ──► [ AI Agent ] ──► [ 1MSG WhatsApp Send ]
                             │
            ┌────────────────┼────────────────┬────────────────┐
            ▼                ▼                ▼                ▼
     [ Gemini Model ]  [ Memory ]    [ Google Calendar ] [ Gmail / Sheets ]

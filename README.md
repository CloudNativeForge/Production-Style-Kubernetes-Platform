Method
High-Level Architecture (Zero-Capital Startup)

To keep costs near zero while supporting web and mobile, the platform will use a Backend API + Web App + Mobile App architecture.

Key idea: one backend powers everything.

Components:
	1.	Frontend Web App
	2.	Mobile App
	3.	Backend API
	4.	Database
	5.	Notification Service
	6.	Restaurant Dashboard

Architecture Overview:
@startuml

actor Customer
actor RestaurantOwner

Customer --> WebApp
Customer --> MobileApp

WebApp --> BackendAPI
MobileApp --> BackendAPI

RestaurantOwner --> RestaurantDashboard
RestaurantDashboard --> BackendAPI

BackendAPI --> Database
BackendAPI --> NotificationService

NotificationService --> SMS
NotificationService --> Email

@enduml

Technology Stack (Free Tier Friendly)

Frontend

Web App
	•	React (Next.js)

Mobile App
	•	React Native (Expo)


Backend

Backend API
	•	Node.js
	•	NestJS framework


Database
	•	PostgreSQL


Hosting (Zero Cost)

Frontend Web
	•	Vercel free tier

Backend
	•	Render free tier
	•	Railway free tier

Mobile App Build
	•	Expo


Notifications

Email
	•	Resend
	•	SendGrid free tier

SMS
	•	Twilio free trial

⸻

Core System Modules

1 User Service

Handles:
	•	Registration
	•	Login
	•	Profile

Roles:
	•	Customer
	•	RestaurantOwner
	•	Admin

⸻

2 Restaurant Service

Handles:
	•	Restaurant listing
	•	Menu items
	•	Operating hours

⸻

3 Order Service

Handles:
	•	Create order
	•	Update order status
	•	Order tracking

This is a Healthcare Appointment Reservation API that acts as a central booking system for multiple hospitals.
Instead of patients calling each hospital individually, they can use this single API to book appointments across different healthcare providers.

How does it work?
1. Single Entry Point
Patients send one request to: POST /healthcare/categories/{category}/reserve
The {category} could be "cardiology", "surgery", "pediatrics", etc.

2. Smart Routing System
The service automatically routes requests to the correct hospital based on the hospital name:

Grand Oak Community Hospital → Dr. Thomas Collins, $7,000 fee
Clemency Medical Center → Dr. Anne Clement, $12,000 fee
Pine Valley Community Hospital → Dr. Seth Mears, $8,000 fee (with 20% discount)

3. Instant Confirmation
Returns a complete appointment confirmation with:

Unique appointment number (e.g., "AGO1234567890")
Doctor details and availability
Patient information
Appointment date
Fee information
Key Benefits
Unified Interface: One API for multiple hospitals
Instant Response: No waiting - immediate appointment confirmation
Standardized Format: Same response structure regardless of hospital
Error Handling: Clear error messages for invalid requests
Comprehensive Logging: Full audit trail of all requests
Technical Architecture
Built on WSO2 Synapse integration platform
Uses content-based routing to direct requests
Mock responses for demonstration (no actual hospital systems)
JSON-based communication
RESTful API design
Real-World Application
In a production environment, this would:

Connect to actual hospital booking systems
Validate doctor availability in real-time
Handle payment processing
Send confirmation emails/SMS
Integrate with electronic health records
This service demonstrates how integration platforms can simplify complex multi-system interactions into a single, user-friendly API.

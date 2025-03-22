## 📚 **InvestIQ Pro – Action Plan (Category-Wise)**  

---

## 🎯 **Goal:**  
To build a fully functional AI-powered goal-based investment platform that empowers users with:  

- **Goal-Based Smart Investment Suggestions**  
- **Family Investment Contribution Toward Shared Goals**  
- **Email Tracking for Unnecessary Expenses**  
- **Savings & Growth Dashboard with Real-Time Insights**  

---

## 🛠️ **Plan of Action (Category-Wise)**  

---

### 📝 **1. Frontend Development**

---

✅ **Tech Stack:**  
- **Framework:** React Native / Flutter for cross-platform compatibility.  
- **State Management:** Redux / MobX to manage application state.  
- **UI Library:** Tailwind / Bootstrap for consistent design.  
- **API Integration:** Axios / Fetch for backend communication.  

✅ **Core Modules:**  
- **Login & Registration:** OAuth 2.0 (Google, Facebook).  
- **Goal Management Dashboard:** Create, update, and track financial goals.  
- **Contribution Interface:** Multi-user contribution view for family goals.  
- **Expense Analysis Panel:** Real-time feedback on flagged expenses.  
- **Savings & Growth Graphs:** Dynamic visualizations of portfolio performance.  

✅ **Action Items:**  
- Setup project with required dependencies.  
- Design intuitive UI/UX for goal creation and contribution tracking.  
- Implement API calls for backend integration.  
- Add push notifications for goal contribution reminders.  

---

### 🎲 **2. Backend Development**

---

✅ **Tech Stack:**  
- **API Gateway:** Node.js with Express.js for routing and middleware.  
- **Authentication:** OAuth 2.0 + JWT for secure login.  
- **AI Model APIs:** Flask/Django to serve ML models via REST APIs.  
- **Microservices Communication:** RESTful APIs / gRPC.  

✅ **Core Modules:**  
- **User Management:** OAuth-based registration and login.  
- **Goal Engine API:** Goal creation, updates, and optimization.  
- **Email Parsing API:** Parses order confirmation emails to identify unnecessary expenses.  
- **Contribution Prediction API:** Predicts user contributions using LSTM models.  
- **Portfolio API:** Suggests optimal asset allocation using PyPortfolioOpt.  

✅ **Action Items:**  
- Setup API Gateway and route APIs securely.  
- Implement JWT-based session management.  
- Define microservices for goal management, expense tracking, and contribution prediction.  
- Validate API requests and ensure data integrity.  

---

### 📈 **3. Goal Engine & Portfolio API**

---

✅ **Tech Stack:**  
- **Framework:** Flask/Django  
- **Model:** PyPortfolioOpt  

✅ **Core Modules:**  
- **Goal Creation & Management:** Create, update, and delete goals.  
- **Portfolio Optimization:** Minimize risk and maximize returns using Markowitz MPT.  
- **Contribution Splitting:** Allocate contributions dynamically among multiple family members.  

✅ **Action Items:**  
- Implement API for goal creation and management.  
- Optimize portfolios using PyPortfolioOpt.  
- Integrate contribution prediction module to adjust asset allocation dynamically.  

✅ **Endpoints:**  
- `POST /goals/create` – Create new goal.  
- `GET /goals/list` – List active goals.  
- `PUT /goals/update` – Update goal progress.  
- `POST /portfolio/optimize` – Optimize portfolio.  

---

### 📧 **4. Email Parsing & Expense API**

---

✅ **Tech Stack:**  
- **Framework:** Flask  
- **Model:** BERT for email classification  
- **External API:** Gmail API for email fetching  

✅ **Core Modules:**  
- **Email Parsing:** Extract order information from Zomato, Swiggy, Myntra, and similar platforms.  
- **Expense Classification:** Classify emails as necessary/unnecessary using BERT.  
- **Expense Flagging:** Suggest reinvestment of flagged expenses into financial goals.  

✅ **Action Items:**  
- Setup Gmail API integration to fetch user emails.  
- Fine-tune BERT for email classification with relevant datasets.  
- Implement API to parse and classify emails.  

✅ **Endpoints:**  
- `POST /emails/parse` – Parse and classify order emails.  
- `GET /emails/flagged` – List flagged unnecessary expenses.  

---

### 🧠 **5. Contribution Prediction API**

---

✅ **Tech Stack:**  
- **Framework:** Flask  
- **Model:** RNN/LSTM for time-series prediction  
- **Database:** MongoDB for storing historical contributions  

✅ **Core Modules:**  
- **Contribution History:** Fetch historical contribution patterns.  
- **Future Prediction:** Use LSTM to predict upcoming contributions.  
- **Goal Progress Adjustment:** Dynamically adjust goal timelines based on predictions.  

✅ **Action Items:**  
- Train LSTM model with historical contribution data.  
- Implement Flask API for contribution predictions.  
- Store historical data and predictions in MongoDB.  

✅ **Endpoints:**  
- `POST /contributions/predict` – Predict future contribution patterns.  
- `GET /contributions/history` – Retrieve past contribution history.  

---

### 📊 **6. Savings & Growth Dashboard**

---

✅ **Tech Stack:**  
- **Frontend:** React Native / Flutter  
- **API Integration:** REST APIs for portfolio growth predictions  
- **Visualization Library:** Chart.js / D3.js for dynamic graphs  

✅ **Core Modules:**  
- **Goal Progress Dashboard:** Visualize goal contribution and completion status.  
- **Portfolio Growth Visualization:** Forecast asset growth over time.  
- **Expense Reduction Suggestions:** Visualize impact of reducing unnecessary expenses.  

✅ **Action Items:**  
- Design dynamic UI to display savings growth and goal status.  
- Connect frontend to backend APIs for real-time data.  
- Implement predictive alerts for underfunded goals.  

✅ **Endpoints:**  
- `GET /portfolio/projections` – Forecast future asset growth.  
- `GET /goals/list` – Fetch current goal progress and savings.  

---

### 🔐 **7. Authentication & Security**

---

✅ **Tech Stack:**  
- **Framework:** Node.js + OAuth 2.0 + JWT  
- **Database:** PostgreSQL for storing user credentials  
- **Encryption:** AES encryption for sensitive data  

✅ **Core Modules:**  
- **OAuth Login:** Secure login via Google/Facebook.  
- **Session Management:** JWT token-based session security.  
- **API Rate Limiting:** Prevent brute-force and DDoS attacks.  

✅ **Action Items:**  
- Implement OAuth 2.0 with Google API for authentication.  
- Generate JWT tokens to validate user sessions.  
- Add rate limiting and input sanitization for all APIs.  

✅ **Endpoints:**  
- `POST /auth/register` – User registration.  
- `POST /auth/login` – OAuth-based login.  
- `GET /auth/profile` – Retrieve user profile.  

---

### 📡 **8. API Gateway & Microservice Integration**

---

✅ **Tech Stack:**  
- **Framework:** Node.js with Express.js  
- **API Gateway:** Central routing for all microservices  
- **Security:** OAuth + JWT for session validation  

✅ **Core Modules:**  
- **Request Routing:** Route requests to respective APIs.  
- **Service Communication:** Microservices communicate via REST/gRPC.  
- **Error Handling:** Centralized error logging and response.  

✅ **Action Items:**  
- Implement API Gateway to route requests securely.  
- Integrate JWT validation for authorized routes.  
- Set up centralized error handling.  

✅ **API Gateway Routes:**  
- `/auth/*` → Auth Service  
- `/goals/*` → Goal Engine API  
- `/emails/*` → Email Parsing API  
- `/contributions/*` → Contribution Prediction API  

---

### 📦 **9. Database & Storage**

---

✅ **Tech Stack:**  
- **Structured Data:** PostgreSQL for users, goals, and transactions.  
- **Unstructured Data:** MongoDB for portfolio allocations and historical data.  

✅ **Core Modules:**  
- **User Management:** PostgreSQL to store user credentials.  
- **Goal Management:** PostgreSQL to manage goals and contributions.  
- **Email Storage:** MongoDB to store parsed email data.  

✅ **Action Items:**  
- Define schemas and models for PostgreSQL.  
- Set up MongoDB collections for dynamic data storage.  
- Create indexes for faster data retrieval.  

✅ **Database Tables/Collections:**  
- `users` – Stores user details and auth credentials.  
- `goals` – Stores goal progress and contributions.  
- `email_records` – Stores parsed email data for expense tracking.  

---

### 🧪 **10. Testing & Quality Assurance**

---

✅ **Core Modules:**  
- **Unit Testing:** Test goal creation, contribution predictions, and email parsing APIs.  
- **Integration Testing:** Validate end-to-end flow from frontend to backend.  
- **API Load Testing:** Use JMeter to simulate high user traffic.  

✅ **Action Items:**  
- Define unit test cases for Flask and Node.js APIs.  
- Perform integration tests to validate data flow.  
- Stress test API Gateway with 1000+ concurrent requests.  

---

### 🚀 **11. Deployment & Scaling**

---

✅ **Tech Stack:**  
- **Docker:** Containerize Flask and Node.js services.  
- **Kubernetes:** Orchestrate services for auto-scaling.  
- **AWS Lambda:** Deploy ML models as Lambda functions.  

✅ **Action Items:**  
- Create Docker images for all microservices.  
- Use Kubernetes for container orchestration.  
- Deploy Flask APIs to AWS Lambda for scaling.  

✅ **CI/CD Pipeline:**  
- Set up GitHub Actions for automated build and deployment.  
- Trigger deployment on successful PR merge.  

---

### 🎉 **Final Delivery**

✅ **MVP Features Complete:** Goal-based investment platform.  
✅ **Secure APIs & Scalable Architecture:** Ready for production.  
✅ **Demo Ready for Hackathon:** Live demo and presentation slide deck.  

# AWS Bedrock Multi-Agent System for Accommodation & Restaurant Recommendations

## 📌 Introduction
This project is a **Multi-Agent System (MAS)** built on **AWS Bedrock**, utilizing **Lambda functions** and **Amazon S3** to provide intelligent accommodation and restaurant recommendations.  
By leveraging AWS Bedrock Agents, we enable natural language interactions where user queries are dynamically processed and routed to specialized agents, each responsible for handling a different domain (e.g., hotels, Airbnbs, and restaurants).  

---

## 🔍 What is a Multi-Agent System (MAS)?
A **Multi-Agent System (MAS)** is an architecture where multiple autonomous agents collaborate to achieve a common goal.  
In this project, we designed multiple **AWS Bedrock Agents**, each with distinct responsibilities:  

- **Supervisor Agent:** Routes user requests to the appropriate action group.  
- **Accommodation Agent:** Handles hotel & Airbnb recommendations.  
- **Restaurant Agent:** Retrieves restaurant suggestions based on user preferences.  

Each agent has its own **Action Group**, which triggers **AWS Lambda functions** to process data, apply filtering logic, and return structured responses.  

---

## 🏗 Architecture Overview
The project follows a **modular and serverless architecture**, leveraging AWS services for scalability and efficiency:

1️⃣ **User Query**  
   - The user sends a request (e.g., *"Find a luxury hotel in New York with a pool."*).  

2️⃣ **AWS Bedrock Supervisor Agent**  
   - Analyzes the request and determines whether it relates to **accommodation** or **restaurants**.  
   - Routes the request to the correct **Action Group**.  

3️⃣ **AWS Lambda Execution**  
   - The Action Group triggers a **Lambda function**:
     - \`accommodation-action-group.py\` fetches hotel/Airbnb data from S3.
     - \`restaurant-action-group.py\` retrieves restaurant data.  
   - The Lambda function processes the request, filters data, and formats the response.  

4️⃣ **Response Generation**  
   - The processed response is returned to the **Bedrock Agent**.  
   - The agent then constructs a human-readable response for the user.  

---

## ⚡ Technologies Used
- **AWS Bedrock**: Orchestrates and manages the Multi-Agent System.  
- **AWS Lambda**: Serverless compute for executing data processing logic.  
- **Amazon S3**: Stores structured datasets (hotels, Airbnbs, restaurants).  
- **boto3**: AWS SDK for Python to interact with AWS services.  
- **Postman / API Gateway**: For testing the system's API endpoints.  

---

## 🌍 Real-World Applications
This system can be expanded and integrated into **real-world applications**, such as:
- Travel and hospitality chatbots.  
- AI-powered virtual assistants for trip planning.  
- Smart booking systems with natural language capabilities.  

With **AWS Bedrock’s foundation models**, it is possible to extend the system with **enhanced NLP capabilities**, making recommendations even more accurate and personalized.  

---


## 🔗 Conclusion
This project demonstrates the **power of AWS Bedrock Agents** in building an **intelligent, multi-agent recommendation system**.  
By integrating **serverless compute, structured data, and NLP-driven logic**, we enable a seamless conversational AI experience for accommodation and restaurant searches. 🚀  

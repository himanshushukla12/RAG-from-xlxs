# Solving Business Problems with AI

## Objective
Develop a proof-of-concept application to intelligently process email order requests and customer inquiries for a fashion store. The system should accurately categorize emails as either product inquiries or order requests and generate appropriate responses using the product catalog information and current stock status.

## Task Description

### Inputs

Google Spreadsheet **[Document](dataset/Solving%20Business%20Problems%20with%20AI.xlsx)** containing:

- **Products**: List of products with fields including product ID, name, category, stock amount, detailed description, and season.

- **Emails**: Sequential list of emails with fields such as email ID, subject, and body.

### Instructions

- Implement all requirements using advanced Large Language Models (LLMs) to handle complex tasks, process extensive data, and generate accurate outputs effectively.
- Use Retrieval-Augmented Generation (RAG) and vector store techniques where applicable to retrieve relevant information and generate responses.
- You are provided with a temporary OpenAI API key granting access to GPT-4o, which has a token quota. Use it wisely or use your own key if preferred.
- Address the requirements in the order listed. Review them in advance to develop a general implementation plan before starting.
- Your deliverables should include:
   - Code developed within this notebook.
   - A single spreadsheet containing results, organized across separate sheets.
   - Comments detailing your thought process.
- You may use additional libraries (e.g., langchain) to streamline the solution. Use libraries appropriately to align with best practices for AI and LLM tools.
- Use the most suitable AI techniques for each task. Note that solving tasks with traditional programming methods will not earn points, as this assessment evaluates your knowledge of LLM tools and best practices.

### Requirements

#### 1. Classify emails
    
Classify each email as either a _**"product inquiry"**_ or an _**"order request"**_. Ensure that the classification accurately reflects the intent of the email.

**Output**: Populate the **email-classification** sheet with columns: email ID, category.

#### 2. Process order requests
1.   Process orders
  - For each order request, verify product availability in stock.
  - If the order can be fulfilled, create a new order line with the status “created”.
  - If the order cannot be fulfilled due to insufficient stock, create a line with the status “out of stock” and include the requested quantity.
  - Update stock levels after processing each order.
  - Record each product request from the email.
  - **Output**: Populate the **order-status** sheet with columns: email ID, product ID, quantity, status (**_"created"_**, **_"out of stock"_**).

2.   Generate responses
  - Create response emails based on the order processing results:
      - If the order is fully processed, inform the customer and provide product details.
      - If the order cannot be fulfilled or is only partially fulfilled, explain the situation, specify the out-of-stock items, and suggest alternatives or options (e.g., waiting for restock).
  - Ensure the email tone is professional and production-ready.
  - **Output**: Populate the **order-response** sheet with columns: email ID, response.

#### 3. Handle product inquiry

Customers may ask general open questions.
  - Respond to product inquiries using relevant information from the product catalog.
  - Ensure your solution scales to handle a full catalog of over 100,000 products without exceeding token limits. Avoid including the entire catalog in the prompt.
  - **Output**: Populate the **inquiry-response** sheet with columns: email ID, response.


We look forward to seeing your solution and your approach to solving real-world problems with AI technologies.
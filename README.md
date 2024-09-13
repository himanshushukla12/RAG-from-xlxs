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



## Project Setup

### Prerequisites
Ensure you have Python installed on your machine. This guide assumes you have Python 3.8 or higher. You can check your Python version by running:
```bash
python --version
```

### Installation

1. **Clone the repository**
   Clone the project repository to your local machine using Git. Replace `your-repository-link` with the actual URL of your repository:
   ```bash
   git clone your-repository-link
   cd repository-folder
   ```

2. **Install required libraries**
   Install all required libraries listed in the `requirements.txt` file using pip:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Jupyter Notebook**
   Start the Jupyter Notebook server:
   ```bash
   jupyter notebook
   ```

   This command will open the Jupyter Notebook dashboard in your default web browser.

### Running the Notebook

- Once Jupyter Notebook opens in your browser, navigate to the directory containing your `.ipynb` file.
- Click on the `.ipynb` file to open it.
- Run the cells sequentially by clicking on each and pressing `Shift + Enter`, or use the "Run" button in the toolbar.

### Note
All operations are performed locally, and this guide utilizes Hugging Face models. Ensure that your `requirements.txt` includes the Hugging Face `transformers` library.

---

### Jupyter Notebook Guide

Here’s how to navigate and use the Jupyter Notebook for running the provided `.ipynb` file after following the README instructions:

1. **Open the Notebook:**
   - Launch Jupyter Notebook using the command `jupyter notebook` from your terminal.
   - Jupyter will open in your default web browser; typically it starts at `http://localhost:8888/tree`.
   - Navigate to the folder where your `.ipynb` file is located.

2. **Running Notebook Cells:**
   - Click on the `.ipynb` file to open it.
   - To run the cells, click on a cell to select it and then either:
     - Press `Shift + Enter` to run the cell and move to the next cell.
     - Press `Ctrl + Enter` to run the cell and remain on the same cell.
     - Use the "Run" button in the toolbar to execute the cell.

3. **Save and Checkpoint:**
   - To save your notebook, click on the "Save" icon in the toolbar or press `Ctrl + S`.
   - Jupyter automatically creates checkpoints, allowing you to revert to previous versions.

4. **Shut Down:**
   - When you are done, you can shut down the Jupyter server by closing the browser window and stopping the terminal process (usually with `Ctrl + C`).

By following these steps, you can effectively run and interact with your Jupyter Notebook locally using the Hugging Face models as specified in the setup guide.
# Solving Business Problems with AI

## Objective
Develop a proof-of-concept application to intelligently process email order requests and customer inquiries for a fashion store. The system should accurately categorize emails as either product inquiries or order requests and generate appropriate responses using the product catalog information and current stock status.

## Task Description

### Inputs

Google Spreadsheet **[Document](dataset/Solving%20Business%20Problems%20with%20AI.xlsx)** containing:

- **Products**: List of products with fields including product ID, name, category, stock amount, detailed description, and season.

- **Emails**: Sequential list of emails with fields such as email ID, subject, and body.


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
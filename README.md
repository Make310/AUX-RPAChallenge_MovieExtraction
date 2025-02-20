# 🎬 AUX-RPAChallenge_MovieExtraction

## 📌 Project Overview
This process automates the extraction of movie data using UiPath, following best practices and leveraging the **REFramework**.  
It searches for movie details on **Rotten Tomatoes** and extracts key information such as:
- 🎬 **Director**
- 🌟 **Protagonists**
- 🎭 **Genre**
- ⭐ **Rating**
- 📝 **Synopsis**

The extracted data is then stored in an **Excel report** and sent via **email**.

---

## 🚀 Features
✔ **Web Automation** → Uses browser automation to navigate Rotten Tomatoes and extract movie details.  
✔ **Excel Processing** → Reads movie names from an input file and writes extracted data to an output file.  
✔ **Structured Data Handling** → Uses a **DataTable** instead of Orchestrator Queues for better flexibility.  
✔ **Email Integration** → Sends the final extracted report automatically.  
✔ **Logging & Error Handling** → Implements best practices for debugging and troubleshooting.  

---

## 📌 How It Works

### **1️⃣ Initialization (`Init`)**
- **`InitAllSettings.xaml`** → Loads configuration data from `Config.xlsx`.
- **`InitAllApplications.xaml`** → Opens the browser and prepares the automation environment.
- **`I-1.MovieExtraction_OpenBrowser.xaml`** → Opens **Rotten Tomatoes** homepage.
- **`I-2.MovieExtraction_PrepareFileResults.xaml`** → Prepare the final file result.
- **`I-3.MovieExtraction_ExtractData.xaml`** → Get Movie table.

### **2️⃣ Get Transaction Data (`GetTransactionData`)**
- **Extracts each movie title as a transaction** to be processed.
- **Handles structured data extraction** to avoid duplicate searches.
- **`G-1.MovieExtraction_SendEmailResults.xaml`** → Sends the final report via email.

### **3️⃣ Process Transaction (`Process`)**
- **`P-1.MovieExtraction_ExtractMovieDetail.xaml`** → Searches each movie on Rotten Tomatoes.

### **4️⃣ End Process (`End Process`)**
- **`E-1.MovieExtraction_CloseBrowser.xaml`** → Closes the browser session after extraction.

---

## 🛠️ Setup Instructions

1️⃣ **Clone this repository**  
```bash
git clone https://github.com/Make310/AUX-RPAChallenge_MovieExtraction


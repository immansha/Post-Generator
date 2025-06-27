# **LinkedIn Post Generator with AI**  

🚀 **Generate engaging LinkedIn posts tailored to your writing style using AI!**  

This tool analyzes your past LinkedIn posts and generates new content matching your preferred **topic, length, and language** (English/Hinglish) using **Llama-3 via Groq API**.  

## **✨ Features**  
✅ **AI-Powered Post Generation** – Uses **few-shot learning** to mimic your writing style.  
✅ **Smart Post Analysis** – Extracts **tags, language, and length** from past posts.  
✅ **Customizable Output** – Control post **length (Short/Medium/Long)** and **language (English/Hinglish)**.  
✅ **Streamlit UI** – Simple, interactive interface for easy post generation.
# project-genai-post-generator
This tool will analyze posts of a LinkedIn influencer and help them create the new posts based on the writing style in their old posts  

<img src="resources/tool.jpg"/>

Let's say Mohan is a LinkedIn influencer and he needs help in writing his future posts. He can feed his past LinkedIn posts to this tool and it will extract key topics. Then he can select the topic, length, language etc. and use Generate button to create a new post that will match his writing style. 

## Technical Architecture
<img src="resources/architecture.jpg"/>


## **🛠️ Tech Stack**  
- **Backend**: Python, LangChain, Groq API (Llama-3)  
- **Frontend**: Streamlit  

## **🚀 Quick Start**  

### **1. Prerequisites**  
- Python 3.8+  
- Groq API Key ([Get it here](https://console.groq.com/keys))  

### **2. Installation**  
```bash
git clone https://github.com/yourusername/linkedin-post-generator.git
cd linkedin-post-generator
pip install -r requirements.txt
```

### **3. Configure API Key**  
Create a `.env` file and add your Groq API key:  
```env
GROQ_API_KEY=your_api_key_here
```

### **4. Run the App**  
```bash
streamlit run main.py
```
Visit `http://localhost:8501` to start generating posts!  

## **📂 Project Structure**  
```
├── data/  
│   ├── raw_posts.json          # Raw LinkedIn posts  
│   └── processed_posts.json    # Processed posts with metadata  
├── few_shot.py                 # Few-shot learning logic  
├── llm_helper.py               # Groq LLM integration  
├── post_generator.py           # Post generation logic  
├── preprocess.py               # Post metadata extraction  
├── main.py                     # Streamlit app  
└── requirements.txt            # Dependencies  
```

## **📈 How It Works**  
1. **Stage 1: Preprocessing**  
   - Extracts **tags, language, and line count** from raw posts.  
   - Unifies tags (e.g., "Job Search" = "Jobseekers" + "Job Hunting").  

2. **Stage 2: Post Generation**  
   - User selects **topic, length, and language**.  
   - AI generates a post using **similar past posts as examples**.  


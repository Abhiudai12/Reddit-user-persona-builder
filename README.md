# Reddit User Persona Builder

This project extracts and analyzes a Reddit user's profile to generate a detailed user persona using Large Language Models (LLMs).  
It scrapes a user's posts and comments and then uses the DeepSeek LLM via OpenRouter API to infer attributes like age group, interests, writing style, and beliefs — with citations from the user's Reddit activity.

## Project Files

| File                    | Description                                                              |
|-------------------------|--------------------------------------------------------------------------|
| `reddit_persona.py`     | Main executable script to scrape and generate persona                   |
| `Reddit_persona.ipynb`  | Jupyter notebook version with inline explanations                       |
| `kojied_persona.txt`    | Sample persona output for Reddit user `kojied`                          |
| `Hungry-Move-6603.txt`  | Sample persona output for Reddit user `Hungry-Move-6603`                |
| `README.md`             | Project instructions and documentation                                  |

## How It Works

1. Input: Reddit username (e.g., `kojied`)
2. Scraping: Uses PRAW to collect recent posts and comments
3. Prompt Building: Creates an intelligent profiling prompt
4. LLM Inference: Sends prompt to DeepSeek via OpenRouter API
5. Output: Saves detailed persona as a `.txt` file with citations

## Setup Instructions

### 1. Clone the Repository

git clone https://github.com/Abhiudai12/Reddit-user-persona-builder.git
cd reddit-user-persona-builder


### 2. Install Dependencies
!pip install praw python-dotenv

### 3. Set Up OpenRouter API Key

- Get a free key from: https://openrouter.ai/keys
- Copy the full key shown when you create it (it won’t be shown again)

### 4. Edit and Run the Script

Update your `reddit_persona.py` to include your API key:

```python
api_key = "sk-or-v1-xxxxxxxxxxxxxxxxxxxxxx"

Then run:
python reddit_persona.py

## Technologies Used

- Python  
- PRAW (Reddit API wrapper)  
- OpenRouter.ai (LLM Gateway)  
- DeepSeek LLM (`deepseek/deepseek-r1:free`)  
- Jupyter Notebook  

## Author

Abhiudai Shahi – bt22csd040@iiitn.ac.in

## License

This project is for academic and research purposes only. Attribution appreciated.

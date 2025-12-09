# Project 1: Simple Q&A Chatbot
* **Description**: Build a command-line chatbot using OpenAI/Claude API that answers general questions.
* **Skills**: API integration, environment variables, basic prompt design
* **Tech**: Python, requests/httpx, dotenv

## Steps for Implementation

### Steps 1: Set up your project structure

chatbot/
├── .env
├── .gitignore
├── requirements.txt
└── chatbot.py

### Step 2: Install Dependencies
* Create your ```requirement.txt```
```
anthropic
python-dotenv
```

* Then Install

``` bash

pip install -r requirement.txt
```

Create a `.env` file:
```

ANTHROPIC_API_KET=your-api-key-here
```

And a `.gitignore' to keep your key safe:
```

.env
__pycache__/
```

### Step 4: Build the Chatbot

```python
chatbot.py
```


### Step 5: Get Your API Key

* Go to console.anthropic.com
* Sign up or login in
* Navigate to API Keys and create a new key
* Copy the key into your ```.env``` file

### Step 6: Run your Chatbot

```bash

python chatbot.py
```

### How It Works

| **Component** | **Purpose** |
| ------------- | ----------- |
| ```dotenv```  | Loads API key from ```.env``` file securely |
| ```Anthropic``` client | Official SDK handles API requests and authentication |
| ```conversation_history``` | List of messages that maintains context across turns |
| System prompt | Sets the assitant's behaviour and personality |

### Key Concepts Demonstrated

* **API Integration**: The Anthropic SDK abstracts away HTTP requests, handling authentication, retries , and response parsing.
* **Environment variables**: Using  ```python-dotenv``` keeps secrets out of your code and version control.
* **Prompt Design**: The system prompt defines the assistant's role. You can customize it - fot example, making it a coding assistant or a creative writing helper.
* **Conversation Memory**: By appending each exchange to ```conversation_history```, the chatbot remembers previous message in the session.

## Next Steps to Explore

* Add streaming responses for real-time output
* Save/load conversation history to files
* Add different "personas" via system prompts
* Implement rate limiting and error retry logic
* Buisnf a simple GUI with ```tkinter``` or a web interface with flask



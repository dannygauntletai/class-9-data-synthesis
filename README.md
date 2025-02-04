# Class 8: Data Synthesis with AI

## Introduction

Use LLMs to create and augment data, enabling otherwise impossible applications and literally generating value.

## Prerequisites

- Docker (for containerized usage)
- Python 3.11.0 or greater (for local setup)
- LangSmith API Key [Here](https://smith.langchain.com/)
- OpenAI API Key [Here](https://platform.openai.com/api-keys)

## Class Materials
- [Link to Class Slides](https://docs.google.com/presentation/d/1jz7BkK6btdZdCXHiDbLXTQmH0EmJWjZ3Up7Gqdp2c0s/edit?usp=sharing)

## Docker
1. Start Jupyter to run the `.ipynb` file with a local notebook:
   ```
   docker compose up jupyter
   ```
Note: The Docker setup will automatically use the environment variables from your `.env` file.

## Running Different Scripts
You can use the provided `run.sh` script for easier execution.
Make sure to make the script executable with `chmod +x run.sh` in the CLI before using:
```
./run.sh jupyter #(runs jupyter notebook locally)
```

## Local Setup (Alternative to Docker)

If you prefer to run the examples locally:

1. Ensure you have Python 3.11.0 or greater installed.

2. Clone the repository:
   ```
   git clone [repository-url]
   cd [repository-name]
   ```

3. Set up the environment:
   ```
   python3 -m venv .venv
   source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
   pip install -r requirements.txt
   ```

4. Configure environment variables:
   ```
   cp .env.sample .env
   # Edit .env with your API keys
   ```
5. export your `.env` variables to the system:
(python-dotenv should handle this for you in each file, but in case you have env var issues)

   **Linux / Mac / Bash**
      ```
      export $(grep -v '^#' .env | xargs)
      ```
6. Run an example:
   ```
   python3 langsmith_demo.py
   ```

## Troubleshooting

- Ensure you're using a compatible Python version (3.11.0 or greater) for local setup
- For Docker issues, check your Docker installation and make sure the Docker daemon is running (open in desktop app)
- If you encounter package issues, try updating pip: `pip install --upgrade pip`

## Need Help?
Refer to the class materials or reach out to the course instructor or learning assistant
#### Install Package

```bash
pip install webapp_builder
```


### Example Usage

```python
# Importing the CodeGenerator and ImageProcessor classes
from webapp_builder import CodeGenerator, ImageProcessor

from dotenv import load_dotenv, find_dotenv
import os
import openai
load_dotenv(find_dotenv())
# OpenAI API Key
api_key = os.getenv("OPENAI_API_KEY")
openai.api_key = api_key
# Create instances of the classes
code_generator = CodeGenerator()
image_processor = ImageProcessor()
# Example usage of CodeGenerator
code_text = "searchbar at the top right corner, navigation menu at the header, company logo at the top left corner. "
generated_code = code_generator.generate_code(code_text)
print(generated_code)

# Example usage of ImageProcessor
image_path = '/path/to_your_web_image_here/'
image_description = image_processor.get_image_description(image_path, api_key)
print(image_description)
```

For running the Streamlit app, you can create a separate Python script (let's call it `app_runner.py`) with the following content:

```python
# app_runner.py
from webapp_builder import main
from dotenv import load_dotenv, find_dotenv
import os
import openai
load_dotenv(find_dotenv())
# OpenAI API Key
api_key = os.getenv("OPENAI_API_KEY")
openai.api_key = api_key
if _name_ == "_main_":
    main()
```

Then, you can run this script to launch the Streamlit app:

```bash
streamlit run app_runner.py
```


Ensure you have your OpenAI API key configured in your environment variables or pass it directly when calling methods that require it.


# web-app-builder--LLM
#### App Demo (Video Demo)
https://github.com/george-mountain/web-app-builder--LLM/assets/19597087/4541e5f5-844d-4862-8745-bac3436de6ec


# Web Builder App

Web Builder App is a Streamlit-based application that allows users to upload an image, generate code based on the contents of the image, and view the code implementation.

## Table of Contents
- [Data Flow Diagram](#data-flow-diagram)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Running the Application](#running-the-application)
- [License](#license)


## Data Flow Diagram
![dataFlow](https://github.com/george-mountain/web-app-builder--LLM/assets/19597087/827cfd54-ef13-4040-8184-8a93f097b5af)



## Getting Started

### Prerequisites

Make sure you have the following software installed on your machine:

- Python 3.8 or later
- Pytorch Cuda: CUDA Version >=11.8. Install from here - [Pytorch CUDA Installation](https://pytorch.org/)

### Installation From Github
---

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/web-builder-app.git
   cd web-builder-app
   ```

2. Create a virtual environment:

   ```bash
   python -m venv env
   ```

3. Activate the virtual environment:

   - For Windows:

     ```bash
     .\env\Scripts\activate
     ```

   - For Linux/Mac:

     ```bash
     source env/bin/activate
     ```

4. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Create .env file:
    Create .env file and place your API keys in the file. A sample of how to do this is seen on the .env file


6. Alternative installation from Github using pip:
    You can install the project using pip by running the command below:

   ```bash
   pip install git+https://github.com/george-mountain/web-app-builder--LLM
   ```


## Usage

### Running the Application

To run the application locally:

```bash
streamlit run main.py
```

Visit the provided URL in your web browser to interact with the application.


## License

This project is licensed under the MIT License - see the [LICENSE](https://opensource.org/license/mit/) file for details.
```

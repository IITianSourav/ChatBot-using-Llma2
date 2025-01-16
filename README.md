# End-to-End Medical Chatbot using Llama2

This project is an end-to-end medical chatbot built using the Llama2 model. It leverages LangChain for creating conversational AI and Pinecone for vector database management. The application runs on Flask, with Llama2 being used for generating medical-related responses.

## Tech Stack Used
- **Python**: Programming language for the backend.
- **LangChain**: Framework for building language model applications.
- **Flask**: Micro web framework for serving the chatbot application.
- **Meta Llama2**: Large language model used for generating medical responses.
- **Pinecone**: Vector database for storing and searching medical knowledge.

## Steps to Run the Project

### Step 1: Clone the Repository
Clone the repository to your local machine.

```bash
git clone https://github.com/yourusername/End-to-End-Medical-Chatbot-using-Llama2.git
cd End-to-End-Medical-Chatbot-using-Llama2
```

### Step 2: Create a Conda Environment
Create a new Conda environment with Python 3.8.

```bash
conda create -n mchatbot python=3.8 -y
conda activate mchatbot
```

### Step 3: Install Dependencies
Install all the required dependencies using the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

### Step 4: Configure Pinecone Credentials
Create a `.env` file in the root directory of the project and add your Pinecone credentials as follows:

```
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
PINECONE_API_ENV = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```

### Step 5: Download the Quantized Llama2 Model
Download the quantized model `llama-2-7b-chat.ggmlv3.q4_0.bin` from the following link:

[Download Llama2 Model](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main)

Once downloaded, place the model file in the `model` directory of the project.

### Step 6: Store the Index
Run the following command to store the model index:

```bash
python store_index.py
```

### Step 7: Run the Application
Start the Flask application by running the following command:

```bash
python app.py
```

### Step 8: Access the Chatbot
Open your web browser and navigate to `http://localhost:5000` to interact with the medical chatbot.

## Folder Structure
```
/End-to-End-Medical-Chatbot-using-Llama2
│
├── app.py                # Main Flask app file to serve the chatbot
├── store_index.py        # Script to store the index in Pinecone
├── requirements.txt      # List of required dependencies
├── model/                # Folder for storing the Llama2 model
├── .env                  # Configuration file for Pinecone credentials
└── README.md             # This README file
```

## Contributing
Feel free to fork the repository and contribute to the project. You can submit pull requests with new features, bug fixes, or improvements.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

### Explanation:
- **Tech Stack Used**: Lists the technologies and frameworks used in the project.
- **Steps to Run**: Provides detailed instructions for setting up and running the project.
- **Folder Structure**: Describes the file and directory structure for better understanding.
- **Contributing**: Encourages others to contribute to the project.
- **License**: Mentions the license under which the project is distributed.

Make sure to replace the placeholder values (like `xxxxxxxxxxxxxxxxxxxxxxxxxxxxx` for Pinecone credentials) with actual values before sharing the `README.md` publicly.

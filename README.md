Project: PrepPilot --- Interview Trainer Agent for Data Analyst and Data Scientist roles
Technology: Langflow, IBM Granite, IBM watsonx.ai, Retrieval-Augmented Generation (RAG)

Overview
PrepPilot is an AI-assisted interview practice workflow designed to help learners prepare for Data Analyst and Data Scientist interviews. It retrieves relevant interview material from a knowledge base and provides answer evaluation and improvement guidance.

Problem Statement
Learners preparing for technical interviews often need practice questions, structured feedback, and a clear explanation of what their answers are missing. PrepPilot brings these practice steps into a Langflow-based AI workflow.

Main Features
Retrieves interview questions and reference answers from the interview knowledge base.
Evaluates a user's response and provides a score out of 10.
Identifies missing concepts and explains inaccuracies.
Suggests an improved, interview-ready answer.
Provides examples for SQL and data-analysis concepts where relevant.
Workflow Components
Knowledge Base: Stores and retrieves relevant interview question-and-answer content from the supplied knowledge-base PDF.
PrepPilot Agent: Uses the retrieved context to answer interview-practice requests.
Answer Evaluation: Assesses the user's response, highlights missing points, and provides an improved answer.
Feedback / Coaching: Helps the learner understand how to strengthen an answer.
The exact behavior depends on the exported Langflow flow and the connected model/service configuration.

Technology Stack
Langflow --- visual workflow orchestration
IBM watsonx.ai --- model access
IBM Granite --- language model
Knowledge Base / vector retrieval --- retrieval of interview reference material
Python --- local environment for running Langflow
Repository Structure
PrepPilot-Interview-Trainer/
├── README.md
├── PrepPilot - Interview Trainer Agent.json
├── Interview_Knowledge_Base_Data_Analyst_Scientist.pdf
├── PrepPilot_Testing_Report.pdf
├── screenshots/
│   ├── 01_knowledge_retrieval.png
│   ├── 02_answer_evaluation.png
│   └── 03_incorrect_answer.png
├── presentation/
│   └── PrepPilot_Project_Presentation.pptx
└── demo/
    └── PrepPilot_Demo.mp4
Files shown as planned items above should only be included once they actually exist in the repository. Keep filenames consistent with the files you upload.

Setup and Run
Install a compatible Python version and create a virtual environment.
Install Langflow in that environment.
Activate the environment.
Start Langflow:
langflow run
Open the local Langflow address shown in the terminal (commonly http://localhost:7860).
Import the exported Langflow flow JSON, if needed.
Configure your own IBM watsonx.ai credentials and model access in Langflow.
Security: Do not upload API keys, access tokens, passwords, or credential-bearing environment files. Export the Langflow flow with API keys and secrets excluded.

Testing Evidence
The testing report documents three Playground tests:

Test Expected behavior Observed result

Knowledge Base Retrieve relevant Relevant definition, retrieval reference material for syntax, examples, and a question about SQL use case were returned window functions

Answer evaluation Evaluate a partially Score shown: 7/10, correct answer with missing points and an improved answer

Incorrect-answer Identify a Score shown: 2/10, evaluation misconception and with explanation, correct it missing concepts, and SQL examples
These results describe the supplied test screenshots; they are not a claim of comprehensive production validation.

Responsible Use
Intended for learning and interview practice, not as the sole basis for hiring decisions.
Users should verify important technical information.
Do not enter sensitive personal information.
Do not commit API keys, private credentials, or confidential candidate data.
Future Scope
Add more interview categories and role-specific question sets.
Improve multi-turn mock interview handling.
Add additional test cases and evaluation examples.
Refine retrieval quality and feedback consistency.
Project Status
The knowledge-base retrieval and two answer-evaluation scenarios have been tested in the Langflow Playground. Presentation and demo assets should be added when they are completed.

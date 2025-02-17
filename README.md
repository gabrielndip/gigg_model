# LLM model for resumé and cover letter generation

## Data Preparation
### Text in pdf and docx files to be converted as csv text and stored in a single folder.
### Text Extraction: Use python-docx (for .docx) and PyPDF2 (for .pdf) in Python to extract the text content.
### Cleaning: Remove irrelevant information like excessive whitespace, special characters, headers/footers that aren't part of the content, including personal ID information.
### Formatting Consistency: Standardizing CV structure. For example, ensure consistent section headings (e.g., "Experience," "Education," "Skills"). 
### Data Augmentation: Due to small data size, slightly rephrase sentences, creating variations of bullet points, or even generating synthetic examples based on existing CVs.

## Choose a Pre-trained LLM: Select a suitable pre-trained LLM.  Consider these factors:
### Accessibility and Cost: Use open-source model Llama 2/3 from Hugging Face.

## Fine-tuning
### Prepare the Training Data: Structure the data for fine-tuning; input-output pairs may be needed.
#### Input: This could be a prompt describing the type of document to generate (e.g., "Generate a CV for a software engineer with 5 years of experience"). Give keywords or a brief summary of the desired job.
#### Output: The corresponding CV from your dataset.
### Fine-tuning Process:
#### Platform/Library: Use a library like Hugging Face Transformers or Google Cloud Vertex AI to fine-tune the model.
#### Hyperparameter Tuning: Experiment with different hyperparameters (learning rate, batch size, etc.) to optimize the model's performance.
#### Evaluation: Regularly evaluate the model's generated outputs on a held-out portion of the data.

## Phase 3: Deployment and Usage
### Deploy the Model: Use Google Cloud Vertex AI to fine-tune the model and deploy.
### Create Prompts: Design effective prompts to guide the model. Experiment with different prompts to get the best results.  
### Iterate and Refine:  Continuously evaluate the model's output and refine prompts.  If you get new CVs, consider retraining the model periodically to keep it up-to-date.



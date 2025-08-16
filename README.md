🎨 AI Storybook Illustrator 🖌️
This project provides a simple yet powerful web application that generates children's storybook illustrations from a single line of text. Using the power of Natural Language Processing (NLP) and a state-of-the-art image generation model, it transforms your words into beautiful, whimsical art.

✨ Features
Intuitive Web Interface: A clean and simple UI built with Gradio, making it accessible to everyone.

Text-to-Image Generation: Simply type a sentence (e.g., "A brave knight confronts a friendly dragon") to create a unique illustration.

Customizable Art Styles: Choose from a variety of artistic styles to match the mood of your story, including:

Vibrant watercolor

Cute claymation

Japanese anime

Retro 8-bit pixel art

Indian Madhubani folk art

Smart Keyword Extraction: Automatically identifies the most important subjects and objects in your story line using spaCy for more accurate and relevant images.

Optimized for Performance: Utilizes GPU (CUDA) if available for fast image generation and uses fp16 precision to conserve memory.

⚙️ How It Works
The application follows a simple three-step process to generate an illustration:

Keyword Extraction: When you input a story line, the application uses the spaCy NLP library to parse the sentence. It intelligently identifies the main subjects (nouns and proper nouns) and any descriptive adjectives associated with them. For example, in "A brave little fox explores a magical forest," it would extract "brave little fox" and "magical forest."

Prompt Engineering: The extracted keywords are then combined with your chosen art style to construct a detailed prompt for the image generation model. A negative prompt is also used to prevent common undesirable elements like text, watermarks, or blurry results.

Example Prompt: award-winning children's storybook illustration of a brave little fox, a magical forest, Vibrant watercolor style, vibrant colors, detailed, beautiful, whimsical

Image Generation: The final prompt is sent to the Stable Diffusion v1.5 model. The model processes the text and generates a high-quality, unique illustration that visually represents the story line. The final image is then displayed on the web interface.

🛠️ Technologies Used
Image Generation: Diffusers library with the runwayml/stable-diffusion-v1-5 model.

NLP (Keyword Extraction): spaCy with the en_core_web_sm model.

Web Interface: Gradio

Core Library: PyTorch

🚀 Getting Started
You can run this project easily in a cloud environment like Google Colab or on your local machine.

Prerequisites
Python 3.8+

pip package manager

(Recommended) An NVIDIA GPU with CUDA support for fast performance.

1. Clone the Repository
Bash

git clone https://github.com/your-username/ai-storybook-illustrator.git
cd ai-storybook-illustrator
2. Set Up a Virtual Environment
It's recommended to create a virtual environment to manage dependencies.

Bash

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
3. Install Dependencies
Install the required Python libraries using the provided requirements.txt file or by running the commands directly.

Bash

pip install torch diffusers transformers accelerate gradio spacy
python -m spacy download en_core_web_sm
4. Run the Application
If you are using the provided .ipynb file, simply open it in Jupyter Notebook or Google Colab and run the single code cell.

The script will:

Download and load the necessary AI models (this may take a few minutes on the first run).

Start the Gradio web server.

Provide a public URL that you can open in your browser to use the app.

📖 Usage
Enter a Story Line: In the "Story Line" textbox, type a descriptive sentence for the illustration you want to create.

Choose an Artistic Style: Select your preferred style from the dropdown menu.

Generate: Click the "Generate Illustration" button.

View: The generated image will appear in the output box on the right.

Enjoy creating your own storybook worlds!# AI_StoryBook

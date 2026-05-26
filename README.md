Stable Diffusion Generator

A simple AI image generation project using Stable Diffusion. This project allows users to generate images from text prompts using Python and the Stable Diffusion model.

Features
Generate images from text prompts
Easy-to-use Python script
Supports custom prompts
Saves generated images automatically
Requirements

Install the following before running the project:

Python 3.8+
pip
Libraries Used
pip install torch diffusers transformers accelerate pillow
Project Structure
stable_diffusion_generator/
│── app.py
│── requirements.txt
│── README.md
│── outputs/
How to Run
1. Clone the Repository
cd stable_diffusion_generator
2. Install Dependencies
pip install -r requirements.txt
3. Run the Program
python app.py
Example Code
from diffusers import StableDiffusionPipeline
import torch

model_id = "runwayml/stable-diffusion-v1-5"

pipe = StableDiffusionPipeline.from_pretrained(
    model_id,
    torch_dtype=torch.float16
)

pipe = pipe.to("cuda")

prompt = "A futuristic city at sunset"

image = pipe(prompt).images[0]

image.save("outputs/generated_image.png")

print("Image generated successfully!")
Output

The generated image will be saved inside the outputs folder.

Example Prompt Ideas
A cyberpunk city at night
A cute cat astronaut
A fantasy castle in clouds
A realistic beach sunset
A futuristic robot warrior

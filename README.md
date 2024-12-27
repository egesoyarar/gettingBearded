# Image-to-Image Beard Addition using Stable Diffusion

This project utilizes Stable Diffusion pipelines to generate clean-shaven images and add realistic beards to them. It leverages `StableDiffusionPipeline`, `StableDiffusionImg2ImgPipeline`, and `StableDiffusionInpaintPipeline` to produce high-quality results.

## Features

- **Generate clean-shaven portraits**: Creates realistic images of clean-shaven individuals using text-to-image generation.
- **Add realistic beards**: Adds photorealistic, well-groomed beards using inpainting and image-to-image processing.
- **Custom beard mask creation**: Dynamically generates a mask for the lower face to ensure precise beard placement.

## Requirements

- Python 3.8+
- A CUDA-enabled GPU (strongly recommended for performance, otherwise the pc shutted down several times and I became insane.)

Install the required dependencies from `requirements.txt`:

```bash
pip install -r requirements.txt
```

## How It Works

1. **Clean-Shaven Image Generation**:
   - Uses the Stable Diffusion text-to-image pipeline to generate a clean-shaven portrait.

2. **Beard Mask Creation**:
   - Detects the lower face area using MediaPipe to define the beard region.
   - Creates a binary mask highlighting the beard placement area.

3. **Inpainting**:
   - Applies the mask to add light stubble or a realistic beard to the clean-shaven image.

4. **Refinement**:
   - Refines the beard details using the image-to-image pipeline for a seamless and photorealistic appearance.

## Usage

1. Clone the repository and navigate to the project directory.

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook file `gettingBearded.ipynb`.

4. Run the notebook cells step-by-step to:
   - Load the Stable Diffusion pipelines.
   - Define the beard mask creation logic.
   - Generate paired images (clean-shaven and bearded).

5. Save the generated images by running the provided utility function.

## Output

The notebook outputs:
- **Clean-Shaven Image**: The base portrait.
- **Inpainted Beard Image**: A light stubble or minimal beard addition.
- **Refined Beard Image**: A detailed, photorealistic beard.

## Example

Generated paired images will be saved in the `paired_dataset` directory with filenames like:

- `image_0_clean.png`: Clean-shaven portrait.
- `image_0_beard.png`: Portrait with beard.

## Credits

- [**Stable Diffusion**]([https://huggingface.co/docs/diffusers/main/en/api/pipelines/stable_diffusion/inpaint](https://huggingface.co/docs/diffusers/main/en/api/pipelines/stable_diffusion/overview))

---
For questions or suggestions, please feel free to reach out.


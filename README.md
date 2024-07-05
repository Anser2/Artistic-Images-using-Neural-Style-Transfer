# Artistic-Images-using-Neural-Style-Transfer
Using VGG-19 to apply style effect from style image to content image to genrate an artistic image

![WhatsApp Image 2024-07-05 at 00 12 02_d2d868d9](https://github.com/Anser2/Artistic-Images-using-Neural-Style-Transfer/assets/130187355/05d15e87-07ce-419b-bc17-2794358b63d6)

![WhatsApp Image 2024-07-05 at 00 13 55_2640e34f](https://github.com/Anser2/Artistic-Images-using-Neural-Style-Transfer/assets/130187355/948f18b1-70f4-4620-a460-4c71ae71221a)

# Artistic Images using Neural Style Transfer

This project demonstrates the use of Neural Style Transfer (NST) to create artistic images by combining the content of one image with the style of another image. The NST algorithm leverages the power of the VGG-19 neural network to apply the style of a given image to a content image, generating a new, stylized image.

## Overview

Neural Style Transfer (NST) is a technique that blends the content of one image (the content image) with the style of another image (the style image) to create a third image (the generated image) that maintains the recognizable content of the content image but appears to be painted in the style of the style image.

## Key Features

- **Content Representation**: Extracts the content features of the content image using the VGG-19 network.
- **Style Representation**: Extracts the style features of the style image using the VGG-19 network.
- **Combined Loss**: Minimizes a loss function that combines both content loss and style loss to generate the final stylized image.
- **Optimization**: Uses gradient descent to iteratively update the generated image.

## Requirements

- TensorFlow
- NumPy
- Matplotlib
- Scipy

## Usage

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/Artistic-Images-using-Neural-Style-Transfer.git
    cd Artistic-Images-using-Neural-Style-Transfer
    ```

2. **Install the required libraries**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the main script**:
    ```bash
    python main.py --content_image path_to_content_image --style_image path_to_style_image --output_image output_image_name
    ```

## How It Works

1. **Content and Style Extraction**:
    - Use the VGG-19 network pre-trained on the ImageNet dataset.
    - Extract features from intermediate layers to capture content and style representations.

2. **Loss Calculation**:
    - **Content Loss**: Measures how different the content of the generated image is from the content image.
    - **Style Loss**: Measures how different the style of the generated image is from the style image.
    - **Total Loss**: A weighted combination of content loss and style loss.

3. **Optimization**:
    - Initialize the generated image as a copy of the content image.
    - Use an optimizer (e.g., Adam) to minimize the total loss by updating the generated image.

## References

- [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576)
- [VGG-19 Architecture](https://arxiv.org/abs/1409.1556)

## License

This project is licensed under the MIT License - see the file for details.

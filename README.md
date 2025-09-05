# ai-styliser
Small app to apply one images style to another. I have quickly modded the original so the user can load the restyle image of choice, the original used random images from Upsplash but never worked for me after the first time. I want to eventually add this to minipaint as a restyle tool. 

WARNING - The sizing and layout are not right yet, but it works well wrt altering the images.   

Original - https://github.com/hemant467/AI-art-Generator

## How the original works

### Model Loading

- On start, it loads two TFLite models:
- Transfer model: Does the actual stylisation.
- Bottleneck model: Extracts style features from the chosen art image.

### Image Upload

- You upload a content image (your photo) via the UI.
- The system resizes and displays it.

### Style Selection

- You click "Generate new Art"—it fetches a random art image from Unsplash as the style reference.

### Stylisation

- Both images are preprocessed and fed to the models.
- The bottleneck model extracts style features.
- The transfer model applies these features to your photo, outputting a stylised canvas.

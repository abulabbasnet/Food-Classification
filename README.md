# Food-Classification
Developed a food classification system using pre-trained mobilenet.

For testing with external images the following code can be used once the model is trained.


# from google.colab import files
# uploaded = files.upload()
# import cv2
# image = cv2.imread('test_image.jpg')
# import numpy as np

# Preprocess the image (resize, normalize, etc.)
preprocessed_image = preprocess_image(image)  # Replace with your actual preprocessing function

# Reshape the image to match the input shape of the model
input_image = np.expand_dims(preprocessed_image, axis=0)

# Make predictions using the model
predictions = model.predict(input_image)

# Get the predicted class label
predicted_class = np.argmax(predictions)

# Print the predicted class label
print("Predicted class:", predicted_class)


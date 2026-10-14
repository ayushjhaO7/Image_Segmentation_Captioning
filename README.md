# 🧠 Image Segmentation and Captioning

This is a Deep Learning project I developed during an internship. It takes input images and automatically generates descriptive captions explaining what is happening in the scene, while also extracting precise segmentation masks for the subjects in the image.

## ✨ Features

- **Image Captioning:** Generate descriptive captions for images using a Transformer-based model.
- **Image Segmentation:** Segment objects in images using a U-Net or Mask R-CNN model.
- **Interactive Web Apps:** Upload or link images and get captions and segmentation masks instantly.
- **Pretrained Models:** Use provided weights for quick inference or train your own models.

---

## 🚀 Setup & Installation

This project requires **Python 3.8+**. You will need to install the required dependencies before running the application.

```bash
pip install streamlit tensorflow torch torchvision numpy pandas pillow matplotlib opencv-python requests tqdm scikit-image
```

---

## 🛠️ Guide to Use (Custom Segmentation Model)

To run the main application with your own custom-trained segmentation model, follow these steps:

1. **Train the Captioning Model:** Run `Image_Caption_train.ipynb` on Kaggle.
2. **Save Caption Weights:** Save the output model in a folder named `saved_models` as `image_captioning_coco_weights.h5`, and output the vocabulary file as `vocab_coco.file` in a folder named `saved_vocabulary`./kaggle/input/datasets/jeffaudi/coco-2014-dataset-for-yolov3 
3. **Train the Segmentation Model:** Run `image-segmentation.ipynb` on Kaggle.
4. **Save Segmentation Weights:** Save this model in the `saved_models` folder as `segmentation_model.h5`.
5. **Launch the App:** Run the following command in your terminal:
   ```bash
   streamlit run app.py
   ```

---

## 🖼️ Guide to Use (Pretrained ResNet50)

I have also created a separate version of the app that uses a pretrained **RESNET50** model for image segmentation out-of-the-box. It marks objects with bounding boxes and provides individual masks for each detected object.

1. **Train the Captioning Model:** Run `Image_Caption_train.ipynb` on Kaggle.
2. **Save Caption Weights:** Save the output model in a folder named `saved_models` as `image_captioning_coco_weights.h5`, and output the vocabulary file as `vocab_coco.file` in a folder named `saved_vocabulary`.
3. **Launch the ResNet App:** Run the following command in your terminal:
   ```bash
   streamlit run Pretrain_app.py
   ```

---

https://github.com/user-attachments/assets/20e409f0-ae28-4511-9da4-bb694d3c2c5a

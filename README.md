# 'estonian-ortofoto-to-ETAK' Project

This project aims to classify land use types in Estonian ortophotos and validate them against the ETAK vector database. The main goal is to develop a convolutional neural network (CNN) model that can accurately detect and classify various land use types, such as forests, urban areas, water bodies, and agricultural land, from high-resolution orthophotos obtained from the Estonian Land Board.

## Data

The project uses orthophotos obtained from the Estonian Land Board's WFS service and the corresponding ETAK vector database. The orthophotos are in GeoTIFF format and cover the entire territory of Estonia at a spatial resolution of 0.5 m. The ETAK vector database includes six thematic datasets - buildings, land use types, relief, utility facilities, transportation, and water bodies - in multiple file formats, including Esri SHP, Mapinfo TAB, Microstation DGN, and Autocad DXF.

## Methodology

The project uses a CNN-based approach for land use classification. The CNN model is trained on a set of labeled orthophoto patches and their corresponding ETAK vector polygons. The trained model is then used to classify the entire orthophoto mosaic into different land use types, which are represented as vector polygons in the output.

## Code

The code for this project is written in Python and uses various open-source libraries, including TensorFlow, Keras, and GeoPandas. The code is organized into multiple modules that perform different tasks, such as data preprocessing, model training, validation, and prediction.

## Usage

To use this project, follow these steps:

1. Clone the repository: `git clone https://github.com/<username>/estonian-ortofoto-to-ETAK.git`
2. Install the required packages: `pip install -r requirements.txt`
3. Run the data preprocessing script to download the orthophotos and the ETAK vector database: `python preprocess.py`
4. Run the model training script to train the CNN model: `python train.py`
5. Run the prediction script to classify the entire orthophoto mosaic: `python predict.py`
6. Validate the output against the ETAK vector database using the validation script: `python validate.py`

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

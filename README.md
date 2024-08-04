
Converting JPG to GeoTIFF

This Jupyter Notebook provides a step-by-step guide to converting JPG images with embedded GPS information into georeferenced GeoTIFF files. 
Additionally, it includes functionality to read and display TIFF files using OpenCV and resize images using PIL.
## Features

- Extract GPS information from image EXIF data.
- Convert GPS coordinates to degrees.
- Georeference images using extracted GPS information.
- Save georeferenced images as GeoTIFF files.
- Read and display TIFF images.
- Resize and save TIFF images.

## Requirements

- Python 3.x
- Jupyter Notebook
- Pillow
- OpenCV
- GDAL

## Installation

1. Clone the repository:
    ```bash
    git clone 
    ```

2. Create a virtual environment (optional but recommended):
    ```bash
    python3 -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

   4. Open the Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
   Then open `coverting jpg to geotiff.ipynb`.


## Usage

1. Prepare your input and output directories. Place your images with GPS data in the input directory.
   
2. Update the `input_directory` and `output_directory` variables in the script:
    ```python
    input_directory = "input_image"
    output_directory = "output_image"
    ```

3. Run the notebook cells sequentially to process the images, georeference them, and perform additional operations such as displaying and resizing the images.

4. To read and display a specific TIFF image:
    ```python
    import cv2

    image = cv2.imread('output_image/your_image.tif', cv2.IMREAD_UNCHANGED)
    cv2.imshow('TIFF Image', image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    ```

5. To resize a specific TIFF image:
    ```python
    from PIL import Image

    with Image.open('output_image/your_image.tif') as img:
        new_size = (2000, 1800)  # Width, Height
        resized_img = img.resize(new_size)
        resized_img.save('resized_your_image.tif')
        resized_img.show()
    



## Contact

For any questions or suggestions, please contact[raju.venkateshkumar@gmail.com](mailto:raju.venkateshkumar@gmail.com).


# Hindi and English Text Extractor

This Streamlit application allows users to extract text from images containing Hindi and English content. It uses Optical Character Recognition (OCR) technology to recognize and extract text from uploaded images.


## Features
1. Upload images containing Hindi and English text

2. Extract text from the uploaded images

3. Display the extracted text

4. Search for specific keywords within the extracted text

5. Highlight search results
## Requirements
Python 3.6+

Streamlit

Pytesseract

Pillow (PIL)

Tesseract OCR engine
## Installation
1. Clone this repository or download the source code.

2. Install the required Python packages: 

        pip install streamlit pytesseract Pillow

3. Install Tesseract OCR engine:


For Windows:

    1. Download and install from 
        https://github.com/UB-Mannheim/tesseract/wiki

    2. After installation, you need to add the Tesseract-OCR directory to your system's PATH environment variable:

        Right-click on 'This PC' or 'My Computer' and select 'Properties'

        Click on 'Advanced system settings'

        Click on 'Environment Variables'

        Under 'System variables', find and select 'Path', then click 'Edit'

        Click 'New' and add the path to your Tesseract-OCR installation (e.g., C:\Program Files\Tesseract-OCR)

        Click 'OK' to close all dialog boxes

    3. Set the TESSDATA_PREFIX environment variable:

        Follow the same steps as above to open Environment Variables

        Under 'System variables', click 'New'

        Set Variable name as 'TESSDATA_PREFIX'

        Set Variable value as the path to your Tesseract tessdata 
        directory (e.g., C:\Program Files\Tesseract-OCR\tessdata)

        Click 'OK' to save    
4. Restart your command prompt or IDE for the changes to take effect

For macOS: Use Homebrew: 

        brew install tesseract

For Linux: Use your package manager, e.g., 

        sudo apt-get install tesseract-ocr

5. Download the Hindi language data for Tesseract:

Download hin.traineddata from 

        https://github.com/tesseract-ocr/tessdata

Place the downloaded file in the Tesseract tessdata directory:

Windows:

        C:\Program Files\Tesseract-OCR\tessdata\ 
(or wherever you installed Tesseract)

macOS/Linux: 

        /usr/share/tesseract-ocr/4.00/tessdata/
    
(path may vary based on your installation)
## Usage
1 Run the Streamlit app:

        streamlit run app.py

2 Open your web browser and go to the URL displayed in the terminal (usually http://localhost:8501).

3 Use the file uploader to select an image containing Hindi and/or English text.

4 The app will display the uploaded image and the extracted text.

5 Enter a keyword in the search box to find and highlight specific text within the extracted content.
## Deployment

To make your application accessible online, you can deploy it to various platforms. Here's a guide to deploying your Streamlit app on Streamlit Cloud:

1. Create a GitHub repository with your application code, including:


        app.py (your main Streamlit application file)

        requirements.txt (list all required packages)

        Any other necessary files


2. Create a requirements.txt file in your repository root with the following content:

        streamlit

        pytesseract

        Pillow

3. Sign up for a free account on Streamlit Cloud.

4. From the Streamlit Cloud dashboard, click on "New app" and select your GitHub repository, branch, and the main file (app.py).

5. Advanced Settings:

You may need to add environment variables, particularly TESSDATA_PREFIX if required by your deployment.


6. Click "Deploy" and wait for the process to complete.

7. Once deployed, Streamlit Cloud will provide a URL where your app is accessible.



## Troubleshooting
1. If you encounter a TesseractError, ensure that Tesseract is properly installed and that the TESSDATA_PREFIX environment variable is set correctly.

2. Make sure the Hindi language data (hin.traineddata) is installed in the correct Tesseract data directory.

3. For deployment issues, check if the platform supports installing system libraries like Tesseract.
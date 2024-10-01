# NotYourOrdinaryOCR

This project combines Optical Character Recognition (OCR) using Tesseract with a KMP (Knuth-Morris-Pratt) string matching algorithm to detect and highlight specific words in images. Additionally, the project integrates text-to-speech (TTS) capabilities to vocalize detected text.

Features
OCR (Tesseract): Detects and extracts text from images.
KMP Algorithm: Efficient search for specific words within the detected text.
Highlight Keywords: Visual highlighting of the keyword on the image.
Text-to-Speech (gTTS): Converts the detected text to speech and saves it as an audio file.
Technologies Used
OpenCV: For image processing and visualization.
Tesseract-OCR: To extract words and their bounding boxes.
KMP Algorithm: For efficient string searching.
Google Text-to-Speech (gTTS): To convert detected text into speech.
mpg321: To play the audio file.
How It Works
Step 1: Detect Words in the Image
Using pytesseract, text is extracted from the image along with its bounding box positions. This allows the program to display and annotate the detected words on the image.

Step 2: Search Keyword with KMP Algorithm
The KMP algorithm is implemented to search for the occurrence of a specific word (e.g., "Saurabh") within the detected text, ensuring efficient string matching.

Step 3: Text-to-Speech
Using gTTS, the entire detected text is converted to speech and saved as an audio file. The system then plays the audio file using mpg321.

Step 4: Highlighting the Keyword
The program highlights the searched keyword by drawing a green rectangle around it on the image.

Installation
Install Tesseract-OCR:

bash
Copy code
sudo apt install tesseract-ocr
Install Required Python Packages:

bash
Copy code
pip install pytesseract gtts
sudo apt-get install mpg321
Usage
Run the Script:

Detect words, search for a specific keyword, highlight it, and convert the text to speech.
Example:

python
Copy code
highlight_word_in_image('test3.png', 'Saurabh')
The script will:

Extract and display the words detected in the image.
Search for the keyword using the KMP algorithm.
Highlight the keyword in green.
Convert the detected text into an audio file (detected_text.mp3) and play it.
Custom Input: Change image_path and word_to_find to customize the input image and keyword search.

Future Enhancements
Add support for multiple keyword searches.
Improve accuracy of OCR on complex images.
Add a web-based interface for easier use.

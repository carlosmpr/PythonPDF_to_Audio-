# PDF to Audio Speech

Python program that reads a pdf file, and convert the text to audio file
using the libraries pyttsx3 and PyPDF2.

> pyttsx3 library for Text to Speech
> 
> PyPDF2 It will help to the text from the PDF
 
## Install the libraries

    pip install pyttsx3
    pip install PyPDF2

## Code

1. import the libraries:
    
       import PyPDF2
       import pyttsx3
2. Open the Pdf File:

       path = open('file.pdf', 'rb')
3. Transform the file to Pdf Object:
   
       pdfReader = PyPDF2.PdfFileReader(path)
4. Select your page:

        from_page = pdfReader.getPage("#)
5. Extra the text of the page:
      
         text = from_page.extractText()
6. Run the code to read the text

         speak = pyttsx3.init()
         speak.say(text)
         speak.runAndWait()
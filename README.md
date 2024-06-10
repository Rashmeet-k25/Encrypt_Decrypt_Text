# Encrypt_Decrypt_Text
Demonstrated encryption and decryption of text using Caesar Cipher technique with GUI.<br>
This is a Python script that creates a graphical user interface (GUI) application using the Tkinter library. The application is a Caesar Cipher, a type of substitution cipher where each letter in the plaintext is 'shifted' a certain number of places down the alphabet.

Here's a breakdown of the code:

*Importing modules:*

The script starts by importing the tkinter module, which is used to create the GUI, and the sys module, which is used to determine the operating system.

*Defining the CaesarCipher class:*

The CaesarCipher class is defined, which inherits from tk.Frame. This class represents the main application window.

*Initialization:*

The __init__ method is called when an instance of the CaesarCipher class is created. It sets up the application window with a background color, creates a main frame, and calls the render_widgets method to create the GUI components.

*Rendering widgets:*

The render_widgets method creates the following GUI components:

1. A title label with the text "Caesar Cipher"
2. A text widget where the user can input the plaintext
3. A label and entry field for the user to input the key (shift value)
4. Two buttons: "Encrypt" and "Decrypt"
5. A container frame to hold the buttons and key entry field
   
*Encrypt and decrypt methods:*

The encrypt_decrypt method takes three arguments: text, mode, and key. It performs the Caesar Cipher encryption or decryption based on the mode parameter ('e' for encryption, 'd' for decryption). The method shifts each letter in the input text by the key value, wrapping around the alphabet if necessary.

*Key entry validation:*

The key_entry_validation method is called whenever the user inputs a value in the key entry field. It checks if the input is a valid integer between 1 and 25 (inclusive), and enables or disables the "Encrypt" and "Decrypt" buttons accordingly.

*Button command methods:*

The encrypt_command and decrypt_command methods are called when the user clicks the "Encrypt" or "Decrypt" buttons, respectively. They retrieve the input text and key, perform the encryption or decryption using the encrypt_decrypt method, and update the text widget with the result.

*Main script:*

The main script creates an instance of the CaesarCipher class, sets the window title, and configures the window size and resizability based on the operating system. Finally, it starts the GUI event loop using root.mainloop().

Overall, this script creates a GUI application that allows users to input plaintext and a key, and then encrypts or decrypts the text using the Caesar Cipher algorithm.

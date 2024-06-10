# Encrypt_Decrypt_Text
Demonstrated encryption and decryption of text using Caesar Cipher technique with GUI.<br>

This Python code creates a graphical user interface (GUI) application for encrypting and decrypting text using the Caesar Cipher technique. Following is the break down of the code step by step:<br>

*Importing Libraries:*<br>
- **tkinter** is imported for creating the GUI.
- **sys** is imported to check the platform (operating system).<br>

*Defining the `CaesarCipher` Class:*<br>
- The `CaesarCipher` class inherits from `tk.Frame`, which is a container widget in Tkinter.<br>

*Initialization:*<br>
def __init__(self, root):
- Initializes colors and letters for the cipher.
- Calls the parent class (`tk.Frame`) initializer with a background color.
- Sets up the main frame and calls `render_widgets` to create and place widgets.<br>

*Rendering Widgets:*<br>
def render_widgets(self):
- Creates and places all the widgets (labels, text area, buttons, and entry field) in the GUI.<br>

*Creating the Title Label:*<br>
self.title = tk.Label()
- A label with the text "Caesar Cipher" is created and placed at the top of the mainframe.<br>

*Creating the Text Widget:*<br>
self.text_widget = tk.Text()<br>
self.text_widget.grid(column=0, row=1, padx=100)
- A text widget for entering the text to be encrypted or decrypted.<br>

*Creating the Key Label:*<br>
self.key_label = tk.Label()<br>
self.key_label.grid(column=0, row=2, pady=(38, 10))
- A label for the key input with a description.<br>

*Creating the Buttons Container:*<br>
- A container to hold the Encrypt and Decrypt buttons along with the key entry field.<br>

*Creating Encrypt and Decrypt Buttons:*<br>
self.button_encrypt = tk.Button()<br>
self.button_encrypt.grid(column=0, row=0, ipadx=5, ipady=5)<br>
self.button_decrypt = tk.Button()<br>
self.button_decrypt.grid(column=2, row=0, ipadx=5, ipady=5)<br>
- Two buttons for encrypting and decrypting the text, initially disabled.<br>

*Creating the Key Entry Field:*<br>
self.key_entry_validation_command = self.buttons_container.register(self.key_entry_validation)<br>
self.key_entry = tk.Entry()<br>
self.key_entry.grid(column=1, row=0, ipady=9)<br>
- An entry field for the user to input the key, with validation to ensure it's within the correct range.<br>

*Caesar Cipher Logic:*<br>
def encrypt_decrypt(self, text, mode, key):
- Function to encrypt or decrypt the text based on the mode ('e' for encrypt, 'd' for decrypt) and the key.<be>

*Key Entry Validation:*<br>
def key_entry_validation(self, value):
- Validates the key entry and enables/disables the buttons accordingly.<br>

*Encrypt and Decrypt Commands:*<br>
def encrypt_command(self):<br>
def decrypt_command(self):
- Functions to handle encryption and decryption commands by getting the key and text, then updating the text widget with the result.<br>

*Running the Application:*<br>
operating_system = sys.platform<br>
root = tk.Tk()<br>
caesar_cipher_app = CaesarCipher(root)<br>
root.title = 'Caesar Cipher'
if 'win' in operating_system:<br>
    root.geometry('800x450')<br>
elif 'linux' in operating_system:<br>
    root.geometry('800x470')<br>
elif 'darwin' in operating_system:   <br>
    root.geometry('800x470')<br>
root.resizable(width=False, height=False)
root.mainloop()
- Detects the operating system and sets the window size accordingly.
- Creates the main application window and runs the main loop.

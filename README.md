# Encrypt-Decrypt
letters = "abcdefghijklmnopqrstuvwxyz"
letters_list = [] # add every letter to this list one by one

end = False
for letter in letters:
  letters_list.append(letter)

def encrypt(msg,shift): 
  output = ""

  for letter in msg:
    output +=  letters_list[(letters_list.index(letter) + shift) % 26]

  print("Encrypted message: ",output)
def decrypt(msg,shift): 
  output = ""

  for letter in msg:
    output +=  letters_list[(letters_list.index(letter) - shift) % 26]

  print("Decrypted message: ",output)


while not end:

  txt = input("Welcome to the Caesar Sipher! Coded by: vNxr aka Nor. Press enter to continue: ")

  pro = input("Would you like to encrypt or decrypt: ").lower()
  
  if pro == "encrypt":
    text = input("Enter the message you would like to encrypt: ")
    text = text.lower()
    encrypt(text, 80)
  else:
    text = input("Enter the message you would like to decrypt: ")
    text = text.lower()

    decrypt(text, 80)



  
  con = input("Would you link to encrypt/decrypt another message? y/n: ")

  if con == "n":
    end = True
  


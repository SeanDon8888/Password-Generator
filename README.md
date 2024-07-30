This is an explanation on how the code works
# Explaination guide 
# First we want to import our libraries 
#random imports the random moudle
# string imports the string module
import random
import string 
# now we create a function called generate_password
def generate_password(length: int = 10):
    alphabet = string.ascii_letters + string.digits + string.punctuation
    # we are creating an list of characters to generate
    #string.ascii_letters gives us the letters, string.digtis gives numbers, string.punctuation gives us punctuation
    password = ''.join(random.choice(alphabet) for i in range(length))
    # for i in range(lentgth) we are creaing a loop length times so it will stop at 10 characters sense we set it prior
    # the .join takes all the random characters from the loop and combines them into a single string
    return password
#return passowrd will save the value for us
password = generate_password()
# password = gnerate_password calls the generate_password function with the degault length of 10 
print(f"Generated Password: {password}")
# this prints our our password for us 

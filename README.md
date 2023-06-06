# Password-Generator
A password generator that generates passwords based on user input.

# Password Generator

This is a simple Python program that generates random passwords based on user preferences.

## How it Works

The program uses the `random` and `string` modules in Python to generate random passwords. It prompts the user for the desired length of the password and whether to include digits and symbols. Based on the user's preferences, the program generates a random password using a combination of letters, digits, and symbols.

## Usage

1. Run the program by executing the Python script: `python password_generator.py`.
2. Follow the prompts to specify the desired length of the password and whether to include digits and symbols.
3. The program will generate a random password based on the user's preferences and display it on the screen.

## Code Snippets

Here are some snippets of the code and their explanations:

### Generating a Random Password



def generate_password(length=8, include_digits=True, include_symbols=True):
    characters = string.ascii_letters
    if include_digits:
        characters += string.digits
    if include_symbols:
        characters += string.punctuation

    password = random.choices(characters, k=length)
    return ''.join(password)

This code defines a function generate_password that takes parameters for password length, whether to include digits, and whether to include symbols. It generates a random password by randomly selecting characters from a pool of letters, digits, and symbols.


    print("Welcome to the Password Generator!")
    length = int(input("Enter the desired length of the password: "))
    include_digits = input("Include digits? (y/n): ").lower() == 'y'
    include_symbols = input("Include symbols? (y/n): ").lower() == 'y'

    password = generate_password(length, include_digits, include_symbols)
    print("Generated Password:", password)

if __name__ == '__main__':
    main()

This code defines the main function that serves as the entry point of the program. It prompts the user for the desired length of the password and whether to include digits and symbols. It then calls the generate_password function with the user's preferences and displays the generated password.


import random
import string


def generate_random_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password


def main():
    password_length = input("Enter the desired password length: ")
    if(password_length.isnumeric()):
        generated_password = generate_random_password(int(password_length))

        print("Generated Password:", generated_password)

        user_input = input("Please enter the generated password to continue: ")

        if user_input == generated_password:
            print("Password entered correctly. Access granted.")
        else:
            print("Incorrect password. Access denied.")
    else:
        print("Invalid Number")


if __name__ == "__main__":
    main()

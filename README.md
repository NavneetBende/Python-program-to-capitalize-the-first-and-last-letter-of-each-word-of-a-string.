Capitalize the first and last letter of each word of a string
In this python program, we will be changing the case for the first and last character of the string. Changing case in the string doesn’t only change the look of the string but also changes its value in many ways like it change the ASCII value of the character and also changes its sensitivity because when we perform operations on string case sensitivity of a character changes many things like when you match a lowercase a with uppercase it will give false result.

Capitalize the first and last character of each word of a string
Algorithm
Step 1:- Start.
Step 2:- Take user input.
Step 3:- Slice string from 0 to 1 and convert its case to uppercase.
Step 4:- Concatenate the string from 1 to length of string – 1.
Step 5:- Concatenate last character after converting it to upper case.
Step 6:- Print the string.
Step 7:- End.

Python program to convert first and last letter of string to Upper-Case
Objective – Write a python program to capitalize the first and last character of each word in a string

#take user input
String = input('Enter the String :')
#start slicing the String
#take 1st character and convert it to upper case
#Concatinate the string with remaning-1 length
#take last character and change it to uppercase and concatinate it to string
String = String[0:1].upper() + String[1:len(String)-1] + String[len(String)-1:len(String)].upper()
#print the String
print(String)
Output
Enter the String :Prepinsta
PrepinstA
Method 2 (Capitalize the First and Last letter)
def FirstAndLast(string) :
    # Create an equivalent char array of given string
    ch = list(string);
    i = 0 ;
    while i < len(ch):
        # k stores index of first character and i is going to store index of last character.
        k = i;
        while (i < len(ch) and ch[i] != ' ') :
            i += 1;
        # Check if the character is a small letter If yes, then Capitalise
        if (ord(ch[k]) >= 97 and
            ord(ch[k]) <= 122 ):
            ch[k] = chr(ord(ch[k]) - 32);
        else :
            ch[k] = ch[k]
        if (ord(ch[i - 1]) >= 90 and
            ord(ch[i - 1]) <= 122 ):
            ch[i - 1] = chr(ord(ch[i - 1]) - 32);
        else :
            ch[i - 1] = ch[i - 1]
        i += 1
    return "" . join(ch);
if __name__ == "__main__" :
    string = "Prep insta";
    print("Input string "+string);
    print("String after Capitalize the first and last character of each word in a string:- "+FirstAndLast(string));
Output
Input string Prep insta
String after Capitalize the first and last character of each word in a string:- PreP InstA
Note
The time complexity of above method is o(n) as we are iterating over the string once in the for loop

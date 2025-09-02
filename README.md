# Programming Assignment #1

## Alphabet Soup Problem
```
#Create a function that takes a string and returns a string with its letters in alphabetical order.

def alphabet_soup(al_s):
    str_list = list(al_s)
    str_list.sort()
    sorted_string = "".join(str_list)

    return sorted_string

def main():
    al_s = input("Input a string to be arranged alphabetically: ")
    result = alphabet_soup(al_s)
    print(result)
```
## Emoticon Problem
```
main()

#Create a function that changes specific words into emoticons. 
#Given a sentence as a string, replace the words smile, grin, sad, and mad with their corresponding emoticon.

def emotify(string):

    string = string.replace("smile", ":)")
    string = string.replace("grin", ":D")
    string = string.replace("sad", ":((")
    string = string.replace("mad", ">:(")

    return string

def main():
    string = input("Write a sentence with either smile, grin, sad, or mad: ")
    result = emotify(string)
    print(result)
```
## Unpacking List Problem
```
main()


#Unpack the list into three variables, being first, middle, and last, with middle being everything in between the first and last element. 
#Then print all three variables.

def unpacking_list():
    packed_list = [1,2,3,4,5,6]
    
    first = packed_list[0]
    middle = packed_list[1:-1]
    last = packed_list[-1]

    print("First: " + str(first))
    print("Middle: " + str(middle))
    print ("Last: " + str(last))

unpacking_list()
```

# Experiment 1: Introduction to Python Programming

This is a repository that contains Jupyter Notebook code using the Python programming language. It is a set of three exercises that make use of basic Python coding and concepts.

## 1. Alphabet Soup Problem
This function takes an input from the user and outputs the characters of the input string into an alphabetically arranged version of the string. The function accomplishes this by converting the string into a list using ```list()```, then sorting the list using ```.sort()``` to sort it in alphabetical order, and turning the list back into the string using the ```.join()```.

• Example: "hacker" -> "acehkr"

## 2. Emoticon Problem
This function accepts user input for a sentence and replaces set words with the corresponding emoticons. The function accomplishes this by using ```.replace() ``` to replace select words with their emoticon variants.

**Conversion List:**

• "smile" -> ":)"

• "grin" -> ":D"

• "sad" -> ":(("

• "mad" -> ">:("

**Example:**

• "I am mad!" -> "I am >:(!"

## 3. Unpacking List Problem
This code divides a given list of numbers into a first part, a middle part, and a last part. The code accomplishes this by outputting the first element from the packed_list list, outputting the elements sliced from the first index to before the negative first index when counting from the end, and finally outputting the last element by finding the negative first index when counting from the end.

• Example: 1st = [1,2,3,4,5,6]

• First: 1, Middle: [2,3,4,5] Last: 6

### Requirements:

• Python v.3.8 or later versions

• Jupyter Notebook

### How to Run:

1. Download the repository or make a fork through Github.

2. Open Jupyter Notebook and upload the file (.ipynb) using the notebook.

3. Run the cells in order and input the desired user inputs in the blank boxes.

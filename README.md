# Experiment 1: Introduction to Python Programming v.1.1

This repository contains Jupyter Notebook code written in the Python programming language. It is a set of three exercises that utilize basic Python coding and concepts.

## 1. Alphabet Soup Problem
The first part of the code creates a user-defined function called `alphabet_soup()` that takes a parameter named `al_s`. It uses `list()` to convert whatever input is received by the alphabet soup parameter into a list.
```
def alphabet_soup(al_s): #Creates a user-defined function called alphabet_soup
    str_list = list(al_s) #Converts the given parameters into a list
```

This part of the code uses `.sort()` to sort the converted string in alphabetical order. It achieves this as each character or letter in a string is considered a separate element, which, when converted to list formatting, would convert a string 'string' into a list that separates each character, similar to ['s', 't', 'r', 'i', 'n', 'g']. Once it has been converted to a list data structure, `.sort()` rearranges the elements in the list. Once the elements are arranged, `.join()` converts the arranged list back into a string data structure, and the user-defined function returns the values of the rearranged and reconverted string.
```
    str_list.sort() #Sorts the list into alphabetical order
    sorted_string = "".join(str_list) #Converts the list back into a string

    return sorted_string #Returns the sorted string content
```

The main function prompts the user for input on the string they would like to arrange and stores the user's input in `string_input`. It then calls the alphabet_soup function and uses `string_input` in place of the parameter `al_s`, then runs the function to convert, sort, and return the rearranged string. It stores the value of the rearranged string to `result`, then outputs the result and calls the main function to run the whole code.
```
def main():
    string_input = input("Input a string to be arranged alphabetically: ") #Asks for user input on a string to be arranged by the alphabet_soup function
    result = alphabet_soup(string_input) #Calls the alphabet_soup function and assigns the result of the function to 'result'
    print(result) #Outputs the result of the function
main()
```
**Example:** 

• "hacker" -> "acehkr"

### Alphabet Soup Code:
```
def alphabet_soup(al_s): #Creates a user-defined function called alphabet_soup()
    str_list = list(al_s) #Converts the given parameters into a list
    str_list.sort() #Sorts the list into alphabetical order
    sorted_string = "".join(str_list) #Converts the list back into a string

    return sorted_string #Returns the sorted string content

def main():
    inp = input("Input a string to be arranged alphabetically: ") #Asks for user input on a string to be arranged by the alphabet_soup function
    result = alphabet_soup(inp) #Calls the alphabet_soup function and assigns the result of the function to 'result'
    print(result) #Outputs the result of the function
main()
```

## 2. Emoticon Problem
The first part of the code defines a user-defined function called `emotify()` that takes a single parameter, `string`. The function has respective replacements for the words 'smile', 'grin', 'sad', and 'mad' in emoticon form, which convert each word into its corresponding emoticon version when found in the user input. It then returns the converted input for printing.
```
def emotify(string): #Creates a user-defined function called emotify()
    string = string.replace("smile", ":)") #Converts any 'smile' found in the input into ':)'
    string = string.replace("grin", ":D") #Converts any 'grin' found in the input into ':D'
    string = string.replace("sad", ":((") #Converts any 'sad' found in the input into ':(('
    string = string.replace("mad", ">:(") #Converts any 'mad' found in the input into '>:('

    return string #Returns the converted string value
```
The main function first asks for user input in string format, containing the words that will be converted into emoticons, and stores the user input under `user_input`. It then calls the emotify function and uses `user input` as a `string` to replace any words detected in the conversion list with an emoticon. Once the string is returned from the `emotify()` function, it stores the result in `result` and outputs the converted string using `print()` before calling the main function to run.
```
def main():
    user_input = input("Write a sentence with either smile, grin, sad, or mad: ") #Asks for user input on a string that will have the given words converted to emoticon form
    result = emotify(user_input) #Stores the converted string value to result
    print(result) #Outputs the result of the function
main()
```

**Conversion List:**

• "smile" -> ":)"

• "grin" -> ":D"

• "sad" -> ":(("

• "mad" -> ">:("

**Example:**

• "I am mad!" -> "I am >:(!"

### Emoticon Code:
```
def emotify(string): #Creates a user-defined function called emotify()
    string = string.replace("smile", ":)") #Converts any 'smile' found in the input into ':)'
    string = string.replace("grin", ":D") #Converts any 'grin' found in the input into ':D'
    string = string.replace("sad", ":((") #Converts any 'sad' found in the input into ':(('
    string = string.replace("mad", ">:(") #Converts any 'mad' found in the input into '>:('

    return string #Returns the converted string value

def main():
    user_input = input("Write a sentence with either smile, grin, sad, or mad: ") #Asks for user input on a string that will have the given words converted to emoticon form
    result = emotify(user_input) #Stores the converted string value to result
    print(result) #Outputs the result of the function
main()
```

## 3. Unpacking List Problem
The first part of the code creates the user-defined function `unpacking_list()` and sets the given values into the list called `packed_list`, consisting of a list of numbers from 1 to 6.
```
def unpacking_list():
    packed_list = [1,2,3,4,5,6] #Sets the values of the packed list
```

The body of the code indexes the first element from the `packed_list` list by using `packed_list[0]` and stores the value in `first`. It then slices the list from the second element up to the element before the last using `packed_list[1:-1]` and stores the sliced values to `middle`. This is achievable due to the ordered property of the list data structure, which allows counting in a reverse sequence. The terminal value is not included in the slice, which means that only 2 to 5 are sliced rather than 2 to 6. Finally, it indexes the last value using `packed_list[-1]` and stores the value to `last.`
```
    first = packed_list[0] #Indexes the first element
    middle = packed_list[1:-1] #Slices the second element up till before the last element
    last = packed_list[-1] #Indexes the last element
```

The last part of the code uses `print()` to output the unpacked list into the first, middle, and last parts and calls the function to run the code.
```
    print("First: ", str(first)) #Outputs the indexed first element stored in 'first'
    print("Middle: ", str(middle)) #Outputs the sliced elements stored in 'middle'
    print ("Last: ", str(last)) #Outputs the indexed last element stores in 'last'

unpacking_list() #Calls the function
```
**Example:** 

• 1st = [1,2,3,4,5,6]

• First: 1, Middle: [2,3,4,5] Last: 6

### Unpacking List Code:
```
def unpacking_list():
    packed_list = [1,2,3,4,5,6] #Sets the values of the packed list
    
    first = packed_list[0] #Indexes the first element
    middle = packed_list[1:-1] #Slices the second element up till before the last element
    last = packed_list[-1] #Indexes the last element

    print("First: ", str(first)) #Outputs the indexed first element stored in 'first'
    print("Middle: ", str(middle)) #Outputs the sliced elements stored in 'middle'
    print ("Last: ", str(last)) #Outputs the indexed last element stores in 'last'

unpacking_list() #Calls the function
```

### Requirements:

• Python v.3.8 or later versions

• Jupyter Notebook

### How to Run:

**1.** Download the repository or make a fork through GitHub.

**2.** Open Jupyter Notebook and upload the file (.ipynb) using the notebook.

**3.** Run the cells in order and input the desired user inputs in the blank boxes.

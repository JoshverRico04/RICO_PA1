# ALPHABET SOUP PROBLEM
  Create a function that takes a string and returns a string with its letters
  in alphabetical order.

Example:
* alphabet_soup(“hello”) &rarr; ehllo
* alphabet_soup(“hacker”) &rarr; acehkr

### CODE

Create a function called "alphabet_soup" with a parameter called "word". Transform the input "word" into a sorted list with the `sorted()` function. Join the letters into a string with no spaces with the `join()`function.  
							
    def alphabet_soup(word):
        sort = sorted(word) 
        output = "".join(sort)
    
        return output


### OUTPUT

    print(alphabet_soup("hello"))
    print(alphabet_soup("hacker"))

> ehllo\
> acehkr

# EMOTICON PROBLEM:
  Create a function that changes specific words into emoticons. Given a sentence
  as a string, replace the words smile, grin, sad and mad with their corresponding emoticon:

<img width="307" height="196" alt="image" src="https://github.com/user-attachments/assets/b1f7123b-4c8f-4e00-8927-88f524c7c3cb" />

EXAMPLE:
* emotify("Make me smile") &rarr; Make me :)
* emotify("I am mad") &rarr; I am >:(


### CODE

Create a 2 dimensional list with the words to be replaced in the first column and the corresponding emoticons to the second column

    arr = [["smile",":)"], #create a 2 dimensional list
           ["grin",":D"],
           ["sad",":(("],
           ["mad",">:("]] 


Create a function called `emotify()` with one parameter called `sentence`. use `split()` to separate each words into an individual element in a list. create a for loop with the row length of `arr` as its range.

create a for loop within the for loop with the length of the number of words in the list `words` then 


The first loop will cycle through `arr` 
    
    def emotify(sentence):
        words = sentence.split()
        output = " "
        for i in range(len(arr)):
            for j in range(len(words)):
                if words[j].lower() in arr[i]:
                    words[j] = arr[i][1]
        output = output.join(words)
    
        return output



### OUTPUT

    print(emotify("Make me smIle"))
    print(emotify("Mad I am"))
    print(emotify("How sAD I am "))
    print(emotify("I cannot gRIn at you"))

> Make me :)
> >:( I am
> How :(( I am
> I cannot :D at you






# UPACKING LIST PROBLEM: 
  Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being
  everything in between the first and last element. Then print all three variables






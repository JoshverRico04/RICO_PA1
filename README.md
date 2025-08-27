# ALPHABET SOUP PROBLEM

### OVERVIEW

  A function that takes a string and returns a string with its letters in alphabetical order.

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

### OVERVIWE
  A function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad, and mad with their corresponding emoticon:

<img width="307" height="196" alt="image" src="https://github.com/user-attachments/assets/b1f7123b-4c8f-4e00-8927-88f524c7c3cb" />

EXAMPLE:
* emotify("Make me smile") &rarr; Make me :)
* emotify("I am mad") &rarr; I am >:(


### CODE

Create a 2 dimensional list with the words to be replaced in the first column and the corresponding emoticons to the second column.

    arr = [["smile",":)"], #create a 2 dimensional list
           ["grin",":D"],
           ["sad",":(("],
           ["mad",">:("]] 


Create a function called `emotify()` with one parameter called `sentence`. The `split()` will separate each words into an individual element in a list. create a for loop with the row length of `arr` as its range and create another for loop within it and let length of the list `words` as its range.

This for loop structure checks if each element on `words` has a similar word on `arr`. During comparison in the if statement, the elements on `words` are transformed into lowercase letters using the `lower()` function. This ensures that similar words are verified even if they have different letter cases.

Finally Join the elements in the list `words` using the `.join()` with a single space in between.

This structure also maintain the letter case of other words in the sentence.



    
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

> Make me :)\
> \>:( I am\
> How :(( I am\
> I cannot :D at you\






# UPACKING LIST PROBLEM: 

### OVERVIEW
  Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being
  everything in between the first and last element. Then print all three variables.

EXAMPLE:
* 1st = [1,2,3,4,5,6]
* Output: first: 1		middle: [2,3,4,5]		last: 6

### CODE

let `arr1` be the one dimensional list of values.

Since python counts starting in `0` we get the first element in the list by writing `arr1[0]`.

To get the last element, we use a negative index which counts from the final element of the list. `arr[-1]`.

To get the elements in between the first and last element, we write `arr1[1:-1]`. This starts counting from the second index to the index before the last element. This is because ranges in python does not include the final number when using a range. 

 
	arr1 = [2,4,6,8,9,10,12,14,16] #create a list
	first = arr1[0] #get the first element
	last = arr1[-1] #get the last element
	mid = arr1[1:-1] #get the elements between the first and last element



### OUTPUT

	print(first)
	print(last)
	print(mid)

> 2\
> 16\
> [4, 6, 8, 9, 10, 12, 14]


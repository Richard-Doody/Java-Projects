# Java Text Editor
This is a Java Text Editor I developed as part of the course Data Structures and Performance run by UCSD on Coursera. 
Over the course of the project I used a linkedlist, a binary search tree and a trie structure to represent the dictionary. I also compared the Big O performance of the linkedlist dictionary with the BST using a benchmarking class I wrote that took advantage of system nano time to time searches in both implementations and outputed the results into the eclipse console, which I then graphed in google docs.  

For the dictionary’s I implemented methods addWord, isWord and size. For the trie implementation I used a hashmap structure using a character as the key and a trienode as the value. To implement the auto-complete funtion I then traced down the trie and found the stem or if there wasn’t a stem I returned an empty list. Once I found the stem I performed a breath first search to generate all the valid completions. 

Finally I implmeneted a Suggestions method for when someone mis-spells a word. To do that I created a class that did single operation mutations on words so like changing his to this by adding the “t”. I created a method distanceOne that returned all words that were one mutation away (like a single character deletion or insertion or substitution) I used a boolean flag called isWord to ensure that the mutations were words before returning them. After that I created a method that took in the misspelled word as a string, and an int value that represented how many valid words to return based on the misspelled word. I then performed a breath first search looking for valid words that were a single mutation away from the string entered.

# French-test
There are two lists with the french words and the second with the correct translation in English we have to create a program to check English translation from french by the user and it should run until all are guessed right.
If the user guesses the wrong Frech word it should reapear at the end.


## Python code

#### if you want to enter list from user
    list_of_french_word = []
    
    list_of_correct_english_translation = []
    
    n = int(input("Enter the list size "))
    
    print("\n")
    for i in range(0, n):
 
      print("Enter French word at index", i, )
      item = input()
      list_of_french_word.append(item)
      print("Enter Correct English word at index", i, )
      word = input()
      list_of_correct_english_translation.append(word)
  
  
# for Test input
#### list_of_french_word = ["Chat","Chien","Poisson"]
#### list_of_correct_english_translation = ["Cat", "Dog", "Fish"]



    def guess_words_from_french (list_of_french_words, list_of_correct_english_translations):
    
    x= len(list_of_french_words)
    print(x)
    i=0
    k=0
    
    while i< x :
        listf =list_of_french_words
        liste = list_of_correct_english_translations
        print("What is English word for ",listf[k], " ?")
        y= input()
       
       if(y == liste [k]):
            listf.pop(k)
            liste.pop(k)
            i=i+1
            
        else:
            listf.append(listf[k])
            listf.pop(k)
            liste.append(liste[k])
            liste.pop(k)
        
    guess_words_from_french(list_of_french_word,list_of_correct_english_translation)



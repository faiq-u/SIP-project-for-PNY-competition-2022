while True:
    vowels = []
    no_vowels = 0
    punctuation = []
    no_punc = 0
    symbols = []
    no_sym = 0
    no_spaces = 0
    consonants = []
    no_conso = 0
    sentence = input("Enter a sentence to find the number of vowels and other information for: ").lower()

    for s in sentence:
        if s in "aeiou":
            vowels.append(s)
            no_vowels += 1
        elif s in ",.?\":;\'":
            punctuation.append(s)
            no_punc += 1
        elif s in "!@#$%^&*(){}_-+=|/<>"+"\\":
            symbols.append(s)
            no_sym += 1
        elif s == " ":
            no_spaces += 1
        elif s != "":
            consonants.append(s)
            no_conso += 1
    no_words = len(sentence.split())
    words = sentence.split()
    letters = no_conso + no_vowels
    if no_vowels == 1:
        print("There is", no_vowels, "vowel in your sentence.")
    else:
        print("There are", no_vowels, "vowels in your sentence.")
    if no_conso == 1:
        print("There is", no_conso, "consonant in your sentence.")
    else:
        print("There are", no_conso, "consonants in your sentence.")
    if letters == 1:
        print("There is", letters, "letter in your sentence.")
    else:
        print("There are", letters, "letters in your sentence.")
    if no_punc == 1:
        print("There is", no_punc, "punctuation mark in your sentence.")
    else:
        print("There are", no_punc, "punctuation marks in your sentence.")
    if no_sym == 1:
        print("There is", no_sym, "symbol in your sentence.")
    else:
        print("There are", no_sym, "symbols in your sentence.")
    if no_spaces == 1:
        print("There is", no_spaces, "space in your sentence.")
    else:
        print("There are", no_spaces, "spaces in your sentence.")
    if no_words == 1:
        print("There is", no_words, "word in your sentence.")
    else:
        print("There are", no_words, "words in your sentence.")

    print("The following are the vowels in your sentence:")
    for v in vowels:
        print(v)
    print("The following are the consonants in your sentence:")
    for v in consonants:
        print(v)
    print("The following are the punctuation marks in your sentence:")
    for v in punctuation:
        print(v)
    print("The following are the symbols in your sentence:")
    for v in symbols:
        print(v)
    print("The following are the words in your sentence:")
    for v in words:
        print(v)
    closer = input("Enter 'EXIT' as input to quit or anything else to continue: ").upper()
    if closer == "EXIT":
        break

# python-scripts
#My codes made with python. 
# The code has been made using italian words. Soon i'll publish the "translated" version
#scelta norm -> morse | morse -> norm
import math, shutil, os
print("Welcome in the worst made morse traslater ever. Pick an action below")
print("1. Morse to alpha\n2. Alpha to morse\n3. Chars list \n\n+To pick one just input the relative number")
scelta = input()
#wowie
while scelta != "1" and scelta != "2" and scelta != "3" and scelta != "4":
    print("Repeat!")
    scelta = input()
#MORSE TO ALPHA
if scelta == "1":
    oof = 0
    frase_tradotta = ""
    print("you've chosen morse => alpha. Put \"/\" between letters and \"/\" at word's end. hf")
    frase = input()
    nuova_frase = ""
    #print(f"input: \"{frase}\"")
    #array con i codici
    for carattere in frase:
        oof += 1
        if carattere == "." or carattere == "-" or carattere == "/" or carattere == " ":
            if carattere == "." or carattere == "-":
                nuova_frase = nuova_frase + carattere
            elif carattere == " ":
                nuova_frase = nuova_frase + "/"
            elif carattere == "/":
                nuova_frase = nuova_frase + carattere
            else:
                nuova_frase = nuova_frase
        
    frasi = nuova_frase.split("//")
    #print(frasi)
    #BUGG GROSSO QUANTO LA MADONNA E GESU' CRISTO
    for frase in frasi:
        parole = frase.split("/")
        for parola in parole:
######PAROLE

            if parola == ".-":
                frase_tradotta = frase_tradotta + "a"
            elif parola == "-...":
                frase_tradotta = frase_tradotta + "b"
            elif parola == "-.-.":
                frase_tradotta = frase_tradotta + "c"
            elif parola == "-..":
                frase_tradotta = frase_tradotta + "d"
            elif parola == ".":
                frase_tradotta = frase_tradotta + "e"
            elif parola == "..-.":
                frase_tradotta = frase_tradotta + "f"
            elif parola == "--.":
                frase_tradotta = frase_tradotta + "g"
            elif parola == "....":
                frase_tradotta = frase_tradotta + "h"
            elif parola == "..":
                frase_tradotta = frase_tradotta + "i"
            elif parola == ".---":
                frase_tradotta = frase_tradotta + "j"
            elif parola == "-.-":
                frase_tradotta = frase_tradotta + "k"
            elif parola == ".-..":
                frase_tradotta = frase_tradotta + "l"
            elif parola == "--":
                frase_tradotta = frase_tradotta + "m"
            elif parola == "-.":
                frase_tradotta = frase_tradotta + "n"
            elif parola == "---":
                frase_tradotta = frase_tradotta + "o"
            elif parola == ".--.":
                frase_tradotta = frase_tradotta + "p"
            elif parola == "--.-":
                frase_tradotta = frase_tradotta + "q"
            elif parola == ".-.":
                frase_tradotta = frase_tradotta + "r"
            elif parola == "...":
                frase_tradotta = frase_tradotta + "s"
            elif parola == "-":
                frase_tradotta = frase_tradotta + "t"
            elif parola == "..-":
                frase_tradotta = frase_tradotta + "u"
            elif parola == "...-":
                frase_tradotta = frase_tradotta + "v"
            elif parola == ".--":
                frase_tradotta = frase_tradotta + "w"
            elif parola == "-..-":
                frase_tradotta = frase_tradotta + "x"
            elif parola == "-.--":
                frase_tradotta = frase_tradotta + "y"
            elif parola == "--..":
                frase_tradotta = frase_tradotta + "z"
###########            NUMERI            
            elif parola == "-----":
                frase_tradotta = frase_tradotta + "0"
            elif parola == ".----":
                frase_tradotta = frase_tradotta + "1"
            elif parola == "..---":
                frase_tradotta = frase_tradotta + "2"
            elif parola == "...--":
                frase_tradotta = frase_tradotta + "3"
            elif parola == "....-":
                frase_tradotta = frase_tradotta + "4"
            elif parola == ".....":
                frase_tradotta = frase_tradotta + "5"
            elif parola == "-....":
                frase_tradotta = frase_tradotta + "6"
            elif parola == "--...":
                frase_tradotta = frase_tradotta + "7"
            elif parola == "---..":
                frase_tradotta = frase_tradotta + "8"
            elif parola == "----.":
                frase_tradotta = frase_tradotta + "9"
            elif parola == "-----":
                frase_tradotta = frase_tradotta + "0"
############            PUNTEGGIATURA
            elif parola == ".-.-.-":
                frase_tradotta = frase_tradotta + "."
            elif parola == "--..--":
                frase_tradotta = frase_tradotta + ","
            elif parola == "---...":
                frase_tradotta = frase_tradotta + ":"
            elif parola == "..--..":
                frase_tradotta = frase_tradotta + "?"
            elif parola == "-...-":
                frase_tradotta = frase_tradotta + "="
            elif parola == "-....-":
                frase_tradotta = frase_tradotta + "-"
            elif parola == "-.--.":
                frase_tradotta = frase_tradotta + "("
            elif parola == "-.--.-":
                frase_tradotta = frase_tradotta + ")"
            elif parola == ".-..-.":
                frase_tradotta = frase_tradotta + "\""
            elif parola == ".----.":
                frase_tradotta = frase_tradotta + "\'"
            elif parola == "-..-.":
                frase_tradotta = frase_tradotta + "/"
            elif parola == ".--.-.":
                frase_tradotta = frase_tradotta + "@"
        frase_tradotta = frase_tradotta + " "
    print(frase_tradotta)

elif scelta == "2":
    print('You\'ve chosen alpha => morse, the un-existing characters wwill be replaced with "#"')
    frase_tradotta_tomorse = ""
    frase_alpha = input()
    for char in frase_alpha:
        if char == "a" or char == "A":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".-"
        elif char == "b" or char == "B":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-..."
        elif char == "c" or char == "C":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-.-."
        elif char == "d" or char == "D":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-.."
        elif char == "e" or char == "E":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "."
        elif char == "f" or char == "F":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "..-."
        elif char == "g" or char == "G":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "--."
        elif char == "h" or char == "H":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "...."
        elif char == "i" or char == "I":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".."
        elif char == "j" or char == "J":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".---"
        elif char == "k" or char == "K":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-.-"
        elif char == "l" or char == "L":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".-.."
        elif char == "m" or char == "M":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "--"
        elif char == "n" or char == "N":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-."
        elif char == "o" or char == "O":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "---"
        elif char == "p" or char == "P":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".--."
        elif char == "q" or char == "Q":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "--.-"
        elif char == "r" or char == "R":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".-."
        elif char == "s" or char == "S":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "..."
        elif char == "t" or char == "T":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-"
        elif char == "u" or char == "U":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "..-"
        elif char == "v" or char == "V":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "...-"
        elif char == "w" or char == "W":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".--"
        elif char == "x" or char == "X":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-..-"
        elif char == "y" or char == "Y":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-.--"
        elif char == "z" or char == "Z":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "--.."
        elif char == "0":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-----"
        elif char == "1":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".----"
        elif char == "2":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "..---"
        elif char == "3":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "...--"
        elif char == "4":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "....-"
        elif char == "5":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "....."
        elif char == "6":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-...."
        elif char == "7":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "--..."
        elif char == "8":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "---.."
        elif char == "9":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "----."
        elif char == ".":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".-.-.-"
        elif char == ",":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "--..--"
        elif char == ":":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "---..."
        elif char == "?":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "..--.."
        elif char == "=":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-...-"
        elif char == "-":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-....-"
        elif char == "(":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-.--."
        elif char == ")":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-.--.-"
        elif char == "\"":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".-..-."
        elif char == "\'":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".----."
        elif char == "/":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "-..-."
        elif char == "@":
            frase_tradotta_tomorse = frase_tradotta_tomorse + ".--.-."
        elif char == " ":
            frase_tradotta_tomorse = frase_tradotta_tomorse + "/"
        else:
            frase_tradotta_tomorse += "#"
        #auto /
        if char != " ":
            frase_tradotta_tomorse += "/"
    print(frase_tradotta_tomorse)
elif scelta == "3":
    print("\nLetters: ")
    print("A = .-")
    print("B = -...")
    print("C = -.-.")
    print("D = -..")
    print("E = .")
    print("F = ..-.")
    print("G = --.")
    print("H = ....")
    print("I = ..")
    print("J = .---")
    print("K = -.-")
    print("L = .-..")
    print("M = --")
    print("N = -.")
    print("O = ---")
    print("P = .--.")
    print("Q = --.-")
    print("R = .-.")
    print("T = -")
    print("S = ...")
    print("U = ..-")
    print("V = ...-")
    print("W = .--")
    print("X = -..-")
    print("Y = -.--")
    print("Z = --..")

    print("\nNumbers: ")
    print("0 = -----")
    print("1 = .----")
    print("2 = ..---")
    print("3 = ...--")
    print("4 = ....-")
    print("5 = .....")
    print("6 = -....")
    print("7 = --...")
    print("8 = ---..")
    print("9 = ----.")

    print("\nPunctuation: ")
    print(". = .-.-.-")
    print(", = --..--")
    print(": = ---...")
    print("? = ..--..")
    print("= = -...-")
    print("- = -....-")
    print("( = -.--.")
    print(") = -.--.-")
    print("\" = .-..-.")
    print("\' = .----.")
    print("@ = .--.-.")



input()

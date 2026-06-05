# demo
This is my first repository




import random
import string

text = input("Enter your str: ")
words = text.split(" ")

code = int(input("Enter 1 to code & 0 to decode: "))

decode = True if(code == 1) else False

if decode == True:

    new = []

    for word in words:

        if len(word) >= 3:

            r1 = "".join(random.choices(string.ascii_lowercase, k=3))
            r2 = "".join(random.choices(string.ascii_lowercase, k=3))

            ncode1 = r1 + word[1:] + word[0] + r2

            new.append(ncode1)

        else:
            ncode2 = word[::-1]
            new.append(ncode2)

    print(" ".join(new))

else:

    new = []

    for word in words:

        if len(word) >= 3:

            ncode1 = word[-4] + word[3:len(word)-4]

            new.append(ncode1)

        else:
            ncode2 = word[::-1]
            new.append(ncode2)

    print(" ".join(new))

## Midterm 1
**Problem 1**
import string
str_ = "Hello World!"
def scramble(str_):
    letters = list(string.ascii_letters)
    new_str = []
    for x in str_:
        for i in range(len(letters)):
            if x == letters[i]:
                x = letters[i+1] if i < (len(letters) -1) else letters[0]
                new_str.append(x)
                break
            elif x not in letters:
                new_str.append(x)
                break
    return "".join(new_str)               # list -> string

scramble(str_)

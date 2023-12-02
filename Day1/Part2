# Part 1
from data import my_stuff 
# lines = my_stuff.split("\n")
# my_strings = []
# nums = []

# for string in lines:
#     num = ""

#     for char in string:
#         if char.isdigit():
#             num += char
#             break  

#     for char in reversed(string):
#         if char.isdigit():
#             num = num + char
#             break  

#     nums.append(int(num))
# print(sum(nums))
    

numbers = {    "one": "o1e",
    "two": "t2o",
    "three": "t3e",
    "four": "f4r",
    "five": "f5e",
    "six": "s6x",
    "seven": "s7n",
    "eight": "e8t",
    "nine": "n9e",
}

lines = my_stuff.split("\n")
my_strings = []

for line in lines:
    modified_line = line

    for k, v in numbers.items():
        modified_line = modified_line.replace(k, v)

    my_strings.append(''.join(modified_line.split()))

nums = []

for string in my_strings:
    num = ""

    for char in string:
        if char.isdigit():
            num += char
            break  

    for char in reversed(string):
        if char.isdigit():
            num = num + char
            break  

    nums.append(int(num))
print(sum(nums))
    

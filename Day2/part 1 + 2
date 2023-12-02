def check_if_possible(colour_list, data_lines):
    satisfied_lines = []
    min_colours = []

    for line_number, game in enumerate(data_lines, start=1):
        red, green, blue = (0, 0, 0)
        game_possible = True  

        for turn in game.split(': ')[1].split(';'):
            for quantity, color in (word.split() for word in turn.split(', ') if len(word.split()) == 2):
                quantity = int(quantity)
                if color == "red" and quantity > red:
                    red = quantity
                elif color == "blue" and quantity > blue:
                    blue = quantity
                elif color == "green" and quantity > green:
                    green = quantity

        min_colours.append(red * green * blue)
        if red > int(colour_list[0]) or green > int(colour_list[1]) or blue > int(colour_list[2]):
            game_possible = False

        if game_possible:
            satisfied_lines.append(line_number)

    return satisfied_lines, min_colours

colours = input("how many red, green and blue? (red, green, blue): ")
list_of_colours = [int(num.strip()) for num in colours.split(',')]

with open("gamedata.txt", "r") as data:
    my_lines = data.readlines()

satisfied_lines, min_colors = check_if_possible(list_of_colours, my_lines)
print(sum(satisfied_lines))
print(sum(min_colors))

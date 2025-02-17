# colour_language
A language based on the 7 colours of music
def convert_text_to_colors(text):
    # Define the color pattern
    color_pattern = {
        'a': 'red', 'b': 'orange', 'c': 'yellow', 'd': 'green',
        'e': 'blue', 'f': 'indigo', 'g': 'violet',
        'h': 'red', 'i': 'orange', 'j': 'yellow', 'k': 'green',
        'l': 'blue', 'm': 'indigo', 'n': 'violet',
        'o': 'red', 'p': 'orange', 'q': 'yellow', 'r': 'green',
        's': 'blue', 't': 'indigo', 'u': 'violet',
        'v': 'red', 'w': 'orange', 'x': 'yellow', 'y': 'green',
        'z': 'blue', 
        'A': 'red', 'B': 'orange', 'C': 'yellow', 'D': 'green',
        'E': 'blue', 'F': 'indigo', 'G': 'violet', 'H': 'red', 'I': 'orange', 'J': 'yellow', 'K': 'green',
        'L': 'blue', 'M': 'indigo', 'N': 'violet', 'O': 'red', 'P': 'orange', 'Q': 'yellow', 'R': 'green',
        'S': 'blue', 'T': 'indigo', 'U': 'violet',
        'V': 'red', 'W': 'orange', 'X': 'yellow', 'Y': 'green',
        'Z': 'blue', 
    }
 
    # Initialize variables
    color_names_output = []
    hexadecimal_color_codes_output = []
 
    # Convert each letter to color
    for letter in text:
        if letter in color_pattern:
            color_names_output.append(color_pattern[letter])
            # Convert color names to RGB values and then to hexadecimal color codes
            color_rgb = (255, 0, 0) if color_pattern[letter] == 'red' else \
                        (255, 165, 0) if color_pattern[letter] == 'orange' else \
                        (255, 255, 0) if color_pattern[letter] == 'yellow' else \
                        (0, 128, 0) if color_pattern[letter] == 'green' else \
                        (0, 0, 255) if color_pattern[letter] == 'blue' else \
                        (75, 0, 130) if color_pattern[letter] == 'indigo' else \
                        (238, 130, 238)  # 'violet'
            hexadecimal_color_codes_output.append('{:02x}{:02x}{:02x}'.format(*color_rgb))
        else:
            color_names_output.append('N/A')
            hexadecimal_color_codes_output.append('N/A')
 
    return color_names_output, hexadecimal_color_codes_output
 
# Test the function
text = "Hello World"
color_names, hexadecimal_color_codes = convert_text_to_colors(text)
print("Color Names Output:", color_names)
print("Hexadecimal Color Codes Output:", hexadecimal_color_codes)

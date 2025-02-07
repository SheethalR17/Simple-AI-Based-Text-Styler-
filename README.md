# Simple-AI-Based-Text-Styler-
Converts text into Shakespearean, Pirate, Futuristic AI, Old English, and Poetic styles. 
def shakespearean(text):
    words = {"you": "thou", "are": "art", "your": "thy", "hello": "hail", "friend": "comrade", "love": "affection"}
    return " ".join(words.get(word, word) for word in text.split())

def pirate_speak(text):
    words = {"hello": "ahoy", "my": "me", "friend": "matey", "is": "be", "are": "be", "you": "ye", "where": "whar"}
    return " ".join(words.get(word, word) for word in text.split())

def futuristic_ai(text):
    words = {"hello": "greetings", "friend": "unit", "I am": "this entity is", "love": "emotion synthesis"}
    return " ".join(words.get(word, word) for word in text.split()).upper()

def old_english(text):
    words = {"the": "ye", "is": "be", "have": "hath", "you": "thou", "do": "dost", "friend": "fellow"}
    return " ".join(words.get(word, word) for word in text.split())

def poetic(text):
    return " ".join(text.split()) + ", my heart sings free!"

# Get user input
text = input("Enter text: ")
print("\nAvailable Styles: Shakespearean, Pirate, Futuristic AI, Old English, Poetic")
style = input("Choose style: ").lower()

# Apply selected style
if style == "shakespearean":
    print("\nStyled Text:\n", shakespearean(text))
elif style == "pirate":
    print("\nStyled Text:\n", pirate_speak(text))
elif style == "futuristic ai":
    print("\nStyled Text:\n", futuristic_ai(text))
elif style == "old english":
    print("\nStyled Text:\n", old_english(text))
elif style == "poetic":
    print("\nStyled Text:\n", poetic(text))
else:
    print("\nInvalid style. Try again.")

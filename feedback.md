Nicole,
Your Hackathon project is great! I really like the idea and the final result.
You used all the topics and tools we learned in class, and your code is clean and readable.
A few points I’d like to highlight:
1. The connection to your database appears twice—once in your database file and once in the main file. It should only be in the database file.
2. Your project is a bit simple. Try to be more ambitious next time and think of additional features you could implement.
   For example, you could have added user recognition or a score system.
3. In your database file, instead of writing:
    cursor.execute('DROP TABLE IF EXISTS trivia')
    
    cursor.execute('''CREATE TABLE trivia
                (id SERIAL PRIMARY KEY, 
                question TEXT UNIQUE, 
                correct_answer TEXT)''')
    
    connection.commit()

  You can simplify it like this:
    cursor.execute('''CREATE TABLE IF NOT EXISTS trivia
                (id SERIAL PRIMARY KEY, 
                question TEXT UNIQUE, 
                correct_answer TEXT)''')
    
    connection.commit()
    
Really good job, keep going!
    

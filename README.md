![image_alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/Intro.jpg)
# Learn Regular Expression

---

## **What is Regular Expression?**

A **Regular Expression (RegEx)** is a sequence of characters that defines a search pattern. It is primarily used for searching, matching, and manipulating text in strings. Regular expressions are powerful tools that allow for complex string pattern recognition, including matching specific sequences, searching for particular types of characters, or validating formats like email addresses, phone numbers, or dates.

### What is sequence of characters in Regex ?

A **regular expression** consists of a series of characters (letters, digits, symbols) and special operators. These characters can be literal, meaning they match exactly as they appear, or they can be symbolic, representing a broader set of possible characters or patterns.

- **Literal characters:** Regular letters and numbers that stand for themselves in a pattern. For instance, in the regex pattern `"abc"`, each character represents itself, so it will only match the string "abc".

- **Special (Meta) characters:** These have a special meaning in regular expressions and allow for more flexible, dynamic pattern matching. For example, a period (`.`) in a regex means "match any character."

### What is **search pattern in Regex ?**

> A **search pattern within text data** refers to a specific set of rules or criteria defined to locate and match particular sequences of characters (words, numbers, symbols, etc.) in a block of text. This pattern helps identify whether the text contains certain elements or structures, based on the defined rules, rather than looking for exact matches.
> 

For example, a search pattern might say:

- "Find any text that starts with 'A' and ends with 'e'."
- "Find a sequence of exactly 5 digits."
- "Find all words that contain both 't' and 'e'."

### What is types of search pattern ?

### **Search Patterns Can Be Specific or General:**

- **Specific patterns** match very narrowly defined strings.
    - Example: The pattern `"apple"` only matches the exact word "apple".
    
- **General patterns** use special symbols (called **metacharacters**) to match a broader set of strings.
    - Example: The pattern `\d{3}` matches any sequence of three digits, like "123", "456", or "789".

           

         

---

## Fundamental element of  regular expressions :

## **Basic Matchers :**

> **Basic matchers** are fundamental elements that allow you to search for and match specific sequences of characters in text. Understanding these basic matchers is essential for constructing effective regular expressions.
> 

### 1. **Literals**

- **Definition:** Literal characters are the most straightforward type of matchers in regex. They match the exact character(s) as they appear in the text.

- **Example:**
    - Pattern: `cat`
    - Matches: The string "cat", but not "catalog" or "cater".

[Try another example by your hands .](https://regex101.com/r/dmRygT/1)

## **Meta Characters :**

> **Metacharacters** are special characters in regular expressions (RegEx) that have specific meanings and functionalities, allowing users to construct complex search patterns. Unlike regular characters, which represent themselves, metacharacters enable operations such as matching multiple characters, specifying the position of matches, defining repetitions, and grouping elements. They play a crucial role in text processing, pattern matching, and data validation.
> 

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/1.png)

## **The Full Stop :**

The full stop `.` is the simplest example of a meta character. The meta character `.`
matches any single character. It will not match return or newline characters.
For example, the regular expression `.ar` means: any character, followed by the
letter `a`, followed by the letter `r`.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/2.png)

>>[Test Regex Here](https://regex101.com/r/xc9GkU/1)<<

---

## **Character Sets :**

> **Character Sets** (also known as **character classes**) in regular expressions are a way to define a group of characters that can be matched at a specific position in a string. By enclosing characters in square brackets `[ ]`, you create a **character set**, allowing the regex engine to match any one of the characters inside the brackets. This provides greater flexibility for pattern matching because a single position in the pattern can match multiple characters.
> 

## **Basic Character Set :**

> Character sets are also called character classes. Square brackets are used to specify character sets. Use a hyphen inside a character set to specify the characters' range. The order of the character range inside the square brackets doesn't matter.
> 

For example, the regular expression `[Tt]he` means: an uppercase
`T` or lowercase `t`, followed by the letter `h`, followed by the letter `e`.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/3.png)

>>[Test Regex Here](https://regex101.com/r/2ITLQ4/1)<<

A period inside a character set, however, means a literal period. The regular
expression `ar[.]` means: a lowercase character `a`, followed by the letter `r`,
followed by a period `.` character.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/4.png)

>>[Test Regex Here](https://regex101.com/r/wL3xtE/1)<<

---

## Character Ranges :

> Ranges of characters can be specified using a hyphen (`-`) inside square brackets. This allows you to match any character within a defined range.
> 

- **Syntax:** `[a-z]` matches any lowercase letter from `a` to `z`.
    
    ### For Example :
    
    **Pattern:**
    
    ```
    [a-z]
    ```
    
    **Text:**
    
    ```
    "h3ll0 world"
    ```
    
    ### Steps:
    
    1. The first character in the text is "h" → it matches because "h" is a lowercase letter.
    2. The next character "3" is skipped since it's not a lowercase letter.
    3. "l", "l", and "o" are lowercase letters, so they match.
    4. After a space, "w", "o", "r", "l", and "d" also match because they are lowercase letters.

- Syntax:  `[A-Z]` m**atches:** any uppercase letter from `A` to `Z`.
    
    ### For Example :
    
    **Pattern:**
    
    ```
    [A-Z]
    ```
    
    **Text:**
    
    ```
    "Hello World, Welcome to 2024!"
    ```
    
    ### Steps:
    
    1. The text starts with "H" → it matches because "H" is an uppercase letter.
    2. "e", "l", "l", and "o" are lowercase, so they are skipped.
    3. "W" matches because it's uppercase.
    4. "o", "r", "l", and "d" are lowercase, so they are skipped.
    5. The uppercase "W" in "Welcome" matches.
    6. "e", "l", "c", "o", and "m" are skipped (lowercase letters).
    7. The uppercase "T" in "to" matches.
    8. The numbers and special characters like space and punctuation are skipped.

- **Syntax:** `[0-9]` matches any digit from `0` to `9`.
    
    ### For Example :
    
    **Pattern:**
    
    ```
    [0-9]
    ```
    
    **Text:**
    
    ```
    "Phone number: 123-456-7890"
    ```
    
    ### Steps:
    
    1. The text starts with "Phone number:" which has no digits, so they are ignored.
    2. The digits "1", "2", and "3" match.
    3. The digits "4", "5", and "6" match after the hyphen.
    4. Finally, "7", "8", "9", and "0" match after another hyphen.
    
    ### 
    

---

## Combining Ranges :

- Multiple ranges can be combined within a character set.

- **Syntax:** `[a-zA-Z0-9]` matches any letter (uppercase or lowercase) or digit.

### For example :

**Pattern:**

```
[a-zA-Z0-9]
```

- **Matches:** any letter or digit.
- **Text:** "H3ll0W0rld"
- It matches any single alphabetic or numeric character like "H", "3", "l", etc.

---

### **Negated Character Sets :**

> Negated character sets, also called **negative character classes**, allow you to match any character **except** those specified inside the square brackets. To define a negated character set, you use the caret (`^`) symbol as the **first character** inside the square brackets.
> 

### This feature is powerful when you want to exclude certain characters from a match, providing fine control over what gets matched.

## **Basic Syntax**:  [^characters]

- The `^` symbol **negates** the character set.
- **Example:** `[^abc]` matches any character **except** `a`, `b`, or `c`.

### For Example  :

- **Text:** `"Hello, world! How are you?"`
- **Pattern Explanation:** The regular expression `[^.,!?]` will match:
    - All alphabetic characters (`H`, `e`, `l`, `o`, `w`, `r`, `d`, `H`, `o`, `w`, etc.)
    - Spaces are also matched.
    - Punctuation marks `,`, `!`, and `?` are **skipped**.

---

### **Special Characters in Character Sets :**

> Some characters have special meanings in regex (e.g., `.`, `*`, `+`). Inside character sets, these characters are often treated as literals and lose their special meaning, except for a few exceptions like `-` (range indicator) and `^` (negation if placed at the beginning).
> 

- **Syntax:** `[.*+]` matches any of the characters `.`, ``, or `+` literally.
- **Example:**
    - **Pattern:** `[.*+]`
        - **Matches:** a literal period (`.`), asterisks (``), or plus (`+`).
        - **Text:** "a.b*c+"
        - The regex will match ".", "*", and "+".
        

### **Predefined Character Classes :**

Instead of defining a character set manually, regex provides predefined character classes to simplify matching common types of characters.

- **`\d`:** Matches any digit (equivalent to `[0-9]`).
- **`\D`:** Matches any non-digit character (equivalent to `[^0-9]`).
- **`\w`:** Matches any "word" character: alphanumeric and underscore (equivalent to `[a-zA-Z0-9_]`).
- **`\W`:** Matches any non-word character (equivalent to `[^a-zA-Z0-9_]`).
- **`\s`:** Matches any whitespace character (spaces, tabs, line breaks).
- **`\S`:** Matches any non-whitespace character.

### Magic of **Escape Sequences in Character Sets :**

- Certain characters have special meanings inside a character set, such as the caret `^`, hyphen ``, and closing bracket `]`. If you want to match these characters literally, they need to be **escaped** using a backslash `\`.

- **Example:**
    - **Pattern:** `[a\-z]`
        - **Matches:** a literal hyphen ``, or any lowercase letter between `a` and `z`.
        - **Text:** "a-z"
        - The regex will match "a", "-", and "z".

---

### **Repetitions Characters :**

> R**epetition characters** (also called quantifiers) define **how many times** a character, group, or pattern should appear in the text. They allow you to search for repeating occurrences of a pattern, making them a powerful tool for matching varying lengths of text.
> 

## **Types of Repetition Characters (Quantifiers) :**

- The Asterisk (`*`)
- **The Plus (`+`)**
- **The Question Mark (`?`)**
- **The Curly Braces (`{}`)**

### The Asterisk (`*`): Zero or More Repetitions :

> The `*` symbol matches zero or more repetitions of the preceding matcher. The
regular expression `a*` means: zero or more repetitions of the preceding lowercase
character `a`.
> 

 For example, the regular expression
`[a-z]*` means: any number of lowercase letters in a row.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/5.png)

>>[Test Regex Here](https://regex101.com/r/7m8me5/1)<<

For Example , The `*` symbol can be used with the meta character `.` to match any string of characters `.*`. The `*` symbol can be used with the whitespace character `\s` to match a string of whitespace characters. For example, the expression
`\s*cat\s*` means: zero or more spaces, followed by a lowercase `c`,
followed by a lowercase `a`, followed by a lowercase `t`,
followed by zero or more spaces.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/6.png)

>>[Test Regex Here](https://regex101.com/r/gGrwuz/1)<<

### The Plus (`+`): One or More Repetitions :

> The `+` symbol matches one or more repetitions of the preceding character. For
example, the regular expression
> 

For example, the regular expression `c.+t` means: a lowercase `c`, followed by
at least one character, followed by a lowercase `t`. It needs to be
clarified that`t` is the last `t` in the sentence.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/7.png)

>>[Test Regex Here](https://regex101.com/r/Dzf9Aa/1)<<

### **The Question Mark (`?`): Zero or One Repetition :**

> The meta character `?` makes the preceding character
optional. This symbol matches zero or one instance of the preceding character, That mean  Match **zero or one** occurrence of the preceding element.
> 

For example, the regular expression `[T]?he` means: Optional uppercase
`T`, followed by a lowercase `h`, followed by a lowercase `e`.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/8.png)

>>[Test Regex Here](https://regex101.com/r/cIg9zm/1)<<

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/9.png)

>>[Test Regex Here](https://regex101.com/r/kPpO2x/1)<<

### **The Curly Braces (`{}`): Specific Number of Repetitions:**

> Curly braces allow you to specify **exactly how many times** you want to match the character. You can specify an exact number or a range.
> 

 For example, the regular expression `[0-9]{2,3}` means: Match at least
2 digits, but not more than 3, ranging from 0 to 9.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/10.png)

>>[Test Regex Here](https://regex101.com/r/juM86s/1)<<

We can leave out the second number. For example, the regular expression
`[0-9]{2,}` means: Match 2 or more digits. If we also remove the comma,

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/11.png)

>>[Test Regex Here](https://regex101.com/r/Gdy4w5/1)<<

The regular expression `[0-9]{3}` means: Match exactly 3 digits.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/12.png)

>>[Test Regex Here](https://regex101.com/r/Sivu30/1)<<

---

## **Capturing Groups :**

> A capturing group is a group of subpatterns that is written inside parentheses
`(...)`. As discussed before, in regular expressions, 
Capturing groups allow you to treat a part of your regex pattern as a 
single unit. This is especially useful when you want to apply 
quantifiers or modifiers to multiple characters or subpatterns. For 
example, `(abc)+` matches one or more repetitions of "abc" as a whole.
> 

- **Basic Syntax for Capturing Groups**:  `(pattern)`
- Parentheses `()` create a **capturing group**.
- The pattern inside the parentheses is what gets captured when matched.

### **How Capturing Groups Work :**

When you surround a part of a regular expression with parentheses, the part inside the parentheses becomes a **capturing group**. Each time the regex matches text that corresponds to the group, that portion is saved and can be referenced later.

### **What Does "Group" Mean in Regex? :**

> A **group** in regex is a way to treat multiple characters or a sub-pattern as a single unit. Groups are created by surrounding part of a regular expression with parentheses `( )`. These parentheses help organize your regex pattern, making it more flexible and powerful.
> 

## **Purpose of Grouping:**

### **Organize Complex Patterns**:

You can group several characters together so that they can be quantified or repeated as a single unit.

- **Example**: The regex pattern `(ab)+` means "find one or more occurrences of the sequence `ab`." Without parentheses, `ab+` would mean "find `a` followed by one or more `b`s," which is different.

### **Apply Quantifiers to the Group**:

 By using a group, you can apply quantifiers (like `+`, `*`, or `{n}`) to multiple characters at once.

- **Example**: In the regex `(abc){2}`, the group `(abc)` is treated as a single unit, and `{2}` specifies that it should match **exactly twice**, meaning the text `"abcabc"` will match, but `"abc"` will not.

### **Improve Readability**:

Grouping helps make your regular expressions easier to read and understand. For example, `(\d{4})-(\d{2})-(\d{2})` clearly shows that you're looking for a date with a year, month, and day, separated by dashes.

### **What Does "Capture" Mean in Regex? :**

> The **"capture"** part of a capturing group means that when the regular expression matches text, the text that matches the pattern inside the group (the part inside the parentheses) is **saved**. This "captured" text can then be used later in your program or within the regex itself.
> 

### **Purpose of Capturing:**

### **Extract Matched Data**:

When a group captures text, it saves that part of the match so you can use it later in the code. For example, if you're searching for dates in a document, you can capture the year, month, and day from each date and store them for later processing.

- 

### **Accessing Captured Data**:

 Once the regex finds a match, you can access the captured parts of the text using programming functions. Each capture is assigned an index, starting from `1`. In some languages, you can refer to captured groups by their index, such as `group(1)` or `group(2)`.

**Example**

: In the regex

```
(\d{4})-(\d{2})-(\d{2})
```

applied to the text

```
"2024-10-06"
```

, the capturing groups store:

- Group 1: `"2024"` (the year)
- Group 2: `"10"` (the month)
- Group 3: `"06"` (the day)

### **Reuse Captured Data (Backreferences)**:

Captured data can also be reused inside the same regex using **backreferences**. Backreferences allow you to refer to a previously captured group and enforce that the same value appears again.

- **Example**: In the regex `(\w+)\s+\1`, the `\1` refers back to the text captured by the first group `(\w+)`. This ensures that the same word appears twice in a row, like `"hello hello"`.

### **Key Differences Between Grouping and Capturing**:

1. **Grouping**: Organizes parts of a regex into a single unit so you can treat them together (e.g., applying quantifiers). 

1. **Capturing**: When a group is used to actually save the matched part of the text, so you can reference or manipulate it later.

## Example :

Suppose you have a set of IDs like `x1y2z3`, `a5b6c7`, `abcdef`, `g1h2i3`, `123456`, `m7n8o9`, `p0q1r2`, `s3t4u5`, `1a2b3c`, `y9z0a1`, and you want to find out which of them follow the pattern `letter number letter number letter number`. There are two ways to do that:

- Without using grouping: `[a-z]\d[a-z]\d[a-z]\d`

- Using grouping, you can make the pattern shorter by grouping the `[a-z]\d` sequence and applying an exact quantifier of `3`to it: `([a-z]\d){3}`
    
    ![1_l3V5k0_9R2dZNn8664XnGw.webp](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/13.webp)
    
    Let’s say we want to extract the day, month, and year from birthday dates in the format `dd-mm-yyyy`, we can use this regex:
    
    ```
    (\d{1,2})-(\d{1,2})-(\d{4})
    ```
    
    ![1_l3V5k0_9R2dZNn8664XnGw.webp](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/14.webp)
    
  [Try by your self >>](https://regex101.com/r/qQB3oy/1)
    
    ---
    
    ## **Backreferences :**
    
    > Backreferences are a feature that allows you to reference and reuse the text captured by a capturing group within the same regex pattern. They provide a powerful way to search for repeated patterns and validate complex text structures.
    > 
    
    - In a regex pattern, you can reference a capturing group by using a 
    backslash followed by the group number. Group numbers are assigned based
     on the order of opening parentheses in the regex pattern, starting from
     1. For example, `\1` refers to the text captured by the first capturing group, `\2` to the second, and so on.
    
    - Let’s explore backreferences with an examples:
        - `(abc)\1` matches `abcabc`. In which, `(abc)` is a capturing group, and `\1` is a backreference that matches the same text as captured by the capturing group, so, `\1` matches `abc` too.
        - `(a|b|cd)\1` matches `aa`, `bb` or `cdcd`
        - `(\d)(.+)\1+\2?` matches `1a1`, `1a1a`, `1a11`, `1a11a1`
            
    ![1_l3V5k0_9R2dZNn8664XnGw.webp](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/15.webp)
            
   Suppose we need to search for duplicated words in this article, such as 
        “the the regex” or “hello hello world”. Imagine how challenging this 
        task would be if you were to use the regular search. However, we can 
        easily accomplish it with the regex `\b([A-Za-z]+) +\1\b`
            
![1_l3V5k0_9R2dZNn8664XnGw.webp](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/16.webp)
            
        
   [Try by your self >>](https://regex101.com/r/qQB3oy/1)
        

---

## **Alternation :**

> **Alternation** is a fundamental concept in regular expressions that allows you to match one of several different patterns. It works similarly to a logical OR operator, meaning that if any of the specified patterns match, Now, you may be thinking that character sets and alternation work the same way. But the big difference between character sets and alternation is that character sets work at the character level but alternation works at the expression level.
> 

### **Syntax of Alternation :**

- The syntax for alternation uses the pipe symbol (`|`), which separates different options.
- **Basic Syntax**:  `pattern1 | pattern2 | pattern3`

### **How Alternation Works :**

When you use alternation in a regular expression:

- The engine evaluates each option in the order they appear.
- It stops as soon as it finds the first match.
- If a match is found, the engine captures the matched text according to the specified capturing groups.

### For example:

The regular expression `(T|t)he|car` means: either (an uppercase `T` or a lowercase
`t`, followed by a lowercase `h`, followed by a lowercase `e`) OR
(a lowercase `c`, followed by a lowercase `a`, followed by
a lowercase `r`). Note that I included the parentheses for clarity, to show that either expression in parentheses can be met and it will match.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/17.png)


### [Try by your self >>](https://regex101.com/r/fBXyX0/1)

---

## **Escaping Special Characters :**

> In regular expressions, certain characters have special meanings and functions. These **metacharacters** allow for complex pattern matching but can also create confusion when you want to match them literally. To use these characters in a regex pattern as literal characters, you must **escape** them.
> 

- **What Are Special Characters?**
    
    Special characters, also known as **metacharacters**, have unique roles in regex. Here are some of the most common ones:
    
![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/18.png)
    

- **Why Escape Special Characters?**
    - When you want to include these characters in a regex pattern without invoking their special meanings, you must escape them with a backslash (`\`). This tells the regex engine to treat the character literally rather than as a command or modifier.
    - **escaping** refers to the practice of using a backslash (`\`) to indicate that the character following it should be treated literally rather than as a special metacharacter.
- **How to Escape Special Characters ?**
    - A backslash `\` is used in regular expressions to escape the next character. This
    allows us to include reserved characters such as `{ } [ ] / \ + * . $ ^ | ?` as matching characters. To use one of these special character as a matching character, prepend it with `\`.

## For example:

 the regular expression `.` is used to match any character except a
newline. Now, to match `.` in an input string, the regular expression
`(f|c|m)at\.?` means: a lowercase `f`, `c` or `m`, followed by a lowercase
`a`, followed by a lowercase `t`, followed by an optional `.`
character.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/19.png)

### [Try by your self >>](https://regex101.com/r/DOc5Nu/1)

---

## **Practical Examples :**

### Pattern:

### To match the string "hello (world)" literally, use:

<aside>
➡️

### hello\s\(world\)

</aside>

---

1. **Finding File Extensions**: If you want to match file names ending with `.jpg`, you can write:

<aside>
➡️

### \.jpg$

</aside>

---

1. **Text Replacement**: In a text editor, you might want to find all instances of `*` to replace them with something else:

    
    <aside>
    ➡️
    
    ### \*
    
    </aside>
    

---

1. **Matching Parentheses**: To search for text in parentheses, such as `(example)`:

    
    <aside>
    ➡️
    
    ### \((.*?)\)
    
    </aside>
    

---

## Anchors in Regular Expressions :

> **Anchors** are special characters in regular expressions that allow you to specify the position of a match within a string rather than matching a specific character. They help define the boundaries or locations within the string where a pattern should be matched. Anchors do not consume characters in the string; they simply assert that a particular position exists.
> 

### Types of Anchors :

There are two primary types of anchors in regex:

1. **Start Anchor (`^`)**
2. **End Anchor (`$`)**

### Start Anchor (`^`) :

- **Definition**: The caret symbol (`^`) is used to ensures that a match must occur at the **beginning** of a line or string.
- **Functionality**: If a regex pattern starts with `^`, it ensures that the pattern matches only if it appears at the start of the input string.

### **Example:**

- **Pattern**: `^Hello`
- **Text**:
    - `"Hello world!"` ➔ **Matches**: `"Hello"`
    - `"Say Hello to the world!"` ➔ **Does Not Match**: The word "Hello" does not occur at the start.
    - `"Hello again!"` ➔ **Matches**: `"Hello"` at the beginning.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/sa1.png)

### [Try by your self >>](https://regex101.com/r/5ljjgB/1)

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/sa2.png)

### [Try by your self >>](https://regex101.com/r/jXrKne/1)

### End Anchor (`$`) :

- **Definition**: The dollar sign (`$`) is used to assert that a match must occur at the **end** of a line or string.
- **Functionality**: If a regex pattern ends with `$`, it ensures that the pattern matches only if it appears at the end of the input string.

### **Example**:

- **Pattern**: `world!$`
- **Text**:
    - `"Hello world!"` ➔ **Matches**: Ends with `"world!"`
    - `"world! is beautiful"` ➔ **Does Not Match**: "world!" is not at the end.
    - `"Say hello to the world!"` ➔ **Does Not Match**: "world!" is not at the end.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/20.png)

### [Try by your self >>](https://regex101.com/r/y4Au4D/1)

---

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/21.png)

### [Try by your self >>](https://regex101.com/r/y4Au4D/1)

---

### Combining Anchors :

### **Example**:

- **Pattern**: `^Hello world!$`
- **Text**:
    - `"Hello world!"` ➔ **Matches**: The entire string matches.
    - `"Hello world! Extra text"` ➔ **Does Not Match**: There’s extra text.
    - `"Say Hello world!"` ➔ **Does Not Match**: The string does not start with "Hello".

You can combine start and end anchors to match an entire string or line.

---

## **Shorthand Character Sets :**

> **Shorthand character sets** in regular expressions provide a concise way to match common character classes without having to explicitly list all the characters. They are predefined shortcuts that simplify the regex syntax and improve readability.
> 

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/22.png)

## **`.` (Dot) :**

- **Description**: Matches any character **except for a newline** (`\n`).
- **Usage**: This is one of the most commonly used shorthand characters in regex. It is used when you want to match **any character** in a particular position in a string.
- **Example**:
    - **Pattern**: `a.b`
    - **Text**: `"acb"`, `"a1b"`, `"a!b"`
    - **Matches**: All three examples because `.` matches any character between `a` and `b`.

## `\w` (Word Character) :

- **Description**: Matches any **alphanumeric** character: `[a-zA-Z0-9_]`.
    - **Lowercase letters** (`a-z`).
    - **Uppercase letters** (`A-Z`).
    - **Digits** (`0-9`).
    - The **underscore** (`_`).
- **Usage**: Useful when you want to match words, variable names, or alphanumeric sequences.
- **Example**:
    - **Pattern**: `\w+`
    - **Text**: `"Hello_World 123"`
    - **Matches**: `"Hello_World"`, `"123"`.

## `\W` (Non-Word Character) :

- **Description**: Matches any character that is **not alphanumeric**, i.e., it is the **opposite** of `\w`.
    - **Equivalent**: `[^a-zA-Z0-9_]`.
- **Usage**: Useful for matching punctuation, spaces, or other non-alphanumeric characters.
- **Example**:
    - **Pattern**: `\W`
    - **Text**: `"Hello, World!"`
    - **Matches**: `","` (comma), `" "` (space), `"!"` (exclamation mark).

## `\d` (Digit) :

- **Description**: Matches any **digit**: `[0-9]`.
- **Usage**: Commonly used for matching numbers, phone numbers, or dates.
- **Example**:
    - **Pattern**: `\d+`
    - **Text**: `"Price is 100 dollars"`
    - **Matches**: `"100"`.

## **`\D` (Non-Digit) :**

- **Description**: Matches any **non-digit** character, i.e., it is the **opposite** of `\d`.
    - **Equivalent**: `[^0-9]`.
- **Usage**: Useful for matching letters, punctuation, and whitespace when you want to avoid matching numbers.
- **Example**:
    - **Pattern**: `\D+`
    - **Text**: `"123abc"`
    - **Matches**: `"abc"` (since it's not a digit).

## **`\s` (Whitespace) :**

- **Description**: Matches any **whitespace** character, including:
    - Space ( ``).
    - Tab (`\t`).
    - Newline (`\n`).
    - Carriage return (`\r`).
    - Form feed (`\f`).
    - Unicode space characters (`\p{Z}`).
- **Usage**: Useful for matching spaces, tabs, and other separators in a string.
- **Example**:
    - **Pattern**: `\s+`
    - **Text**: `"Hello World"`
    - **Matches**: `" "` (the space between `"Hello"` and `"World"`).

## **`\S` (Non-Whitespace) :**

- **Description**: Matches any character that is **not whitespace**, i.e., it is the **opposite** of `\s`.
    - **Equivalent**: `[^ \t\r\n\f\p{Z}]`.
- **Usage**: Useful for matching any character except spaces, tabs, and line breaks.
- **Example**:
    - **Pattern**: `\S+`
    - **Text**: `"Hello World"`
    - **Matches**: `"Hello"`, `"World"`.

## Practical Examples :

- **Matching a Phone Number**:
    - **Pattern**: `\d{3}-\d{3}-\d{4}`
    - **Text**: `"Call me at 123-456-7890"`
    - **Matches**: `"123-456-7890"`.
    
- **Extracting Words**:
    - **Pattern**: `\w+`
    - **Text**: `"Regex is cool!"`
    - **Matches**: `"Regex"`, `"is"`, `"cool"`.
    
- **Finding Whitespace**:
    - **Pattern**: `\s+`
    - **Text**: `"Hello World"`
    - **Matches**: `" "` (space between words).

---

## **Lookarounds** in Regular Expressions **:**

> Lookarounds allow you to assert conditions about what appears before or after a certain position in the text **without consuming characters**. In other words, lookarounds check for conditions without including the matched part in the final match.
> 

### Explanation of each type of lookaround:

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/23.png)

### **Positive Lookahead `(?=...)` :**

- **Description**: Asserts that what follows the current position in the text **must match** the pattern inside the lookahead.
- **How it works**: The regular expression engine checks if the part of the text after the current position matches the lookahead expression, but it **doesn't include** that matched portion in the overall result.
- **Syntax**: `X(?=Y)`
    - Matches `X` only if it is followed by `Y`.
- **Example**:
    - **Pattern**: `\d(?=px)`
    - **Text**: `"100px 200px"`
    - **Matches**: `1`, `2` (it finds digits only if they are followed by `"px"`, but `"px"` is not part of the match).
    
    **Explanation**: The `\d` matches a digit, and `(?=px)` asserts that `"px"` must immediately follow, but `"px"` isn't included in the match.
    

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/24.png)

 [Try by your self >>](https://regex101.com/r/IDDARt/1)

### Negative Lookahead `(?!...)` :

- **Description**: Asserts that what follows the current position in the text **must not match** the pattern inside the lookahead.
- **How it works**: The regular expression engine checks if the part of the text after the current position does **not** match the lookahead expression.
- **Syntax**: `X(?!Y)`
    - Matches `X` only if it is **not followed** by `Y`.
- **Example**:
    - **Pattern**: `\d(?!px)`
    - **Text**: `"100px 200em"`
    - **Matches**: Any digit from 0→9 (it finds digits that are **not** followed by `"px"`).
    
    **Explanation**: The `\d` matches a digit, and `(?!px)` asserts that `"px"` must **not** follow. So, digits followed by `"px"` are excluded.
    

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/25.png)

 [Try by your self >>](https://regex101.com/r/V32Npg/1)

### **Positive Lookbehind `(?<=...)` :**

- **Description**: Asserts that what precedes the current position in the text **must match** the pattern inside the lookbehind.
- **How it works**: The regular expression engine checks if the part of the text before the current position matches the lookbehind expression, but it **doesn't include** that portion in the overall result.
- **Syntax**: `(?<=Y)X`
    - Matches `X` only if it is preceded by `Y`.
- **Example**:
    - **Pattern**: `(?<=\$)\d+`
    - **Text**: `"$100 €200"`
    - **Matches**: `100` (finds numbers that are preceded by `"$"`, but `"$"` is not included in the match).
    
    **Explanation**: The `\d+` matches one or more digits, and `(?<=\$)` asserts that a dollar sign `"$"` must precede the digits.
    
![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/26.png)
    
    ### [Try by your self >>](https://regex101.com/r/avH165/1)
    

### Negative Lookbehind `(?<!...)` :

- **Description**: Asserts that what precedes the current position in the text **must not match** the pattern inside the lookbehind.
- **How it works**: The regular expression engine checks if the part of the text before the current position does **not** match the lookbehind expression.
- **Syntax**: `(?<!Y)X`
    - Matches `X` only if it is **not preceded** by `Y`.
- **Example**:
    - **Pattern**: `(?<!\$)\d+`
    - **Text**: `"$100 200"`
    - **Matches**: `200` (finds numbers that are **not** preceded by `"$"`).
    
    **Explanation**: The `\d+` matches one or more digits, and `(?<!\$)` asserts that the digits must **not** be preceded by a dollar sign `"$"`.
    

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/27.png)

### [Try by your self >>](https://regex101.com/r/8Efx5G/1)

---

## **Flags**  in Regular Expressions **:**

> Flags are also called modifiers because they modify the output of a regular expression. These flags can be used in any order or combination, and are an integral part of the RegExp.
> 

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/28.png)

### **`i` - Case Insensitive Matching**:

- **Function**: This flag tells the regular expression engine to ignore the case when matching the pattern to the input string.

- **Details**: By default, regular expressions are case-sensitive, meaning that `"a"` does not match `"A"`. The `i` flag overrides this behavior, allowing both uppercase and lowercase characters to be matched interchangeably.
    - **Example**:
        - Without the `i` flag: `/apple/` would match `"apple"` but not `"Apple"`.
        
        - With the `i` flag: `/apple/i` would match both `"apple"` and `"Apple"`.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/29.png)

### [Try by your self >>](https://regex101.com/r/dpQyf9/1)

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/30.png)

### [Try by your self >>](https://regex101.com/r/ahfiuh/1)

### **`g` - Global Search:**

- **Function**: This flag tells the RegEx engine to find **all** matches in the input string, not just the first match.
- **Details**: By default, most regular expression engines stop after finding the first match. When the `g` flag is set, the engine continues searching for more matches even after finding the first one.
    - **Example**:
        - Without the `g` flag: `/cat/` would stop after matching the first occurrence of `"cat"` in `"cat cat cat"`.
        - With the `g` flag: `/cat/g` would find and match all three occurrences of `"cat"` in `"cat cat cat"`.

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/32.png)

### [Try by your self >>](https://regex101.com/r/jnk6gM/1)

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/33.png)

### [Try by your self >>](https://regex101.com/r/dO1nef/1)

### **`m` - Multiline Mode**:

- **Function**: This flag changes the behavior of the `^` (start of line) and `$` (end of line) anchors so that they match at the start or end of **each line** within a string, rather than just at the start or end of the entire string.
- **Details**: By default, the `^` and `$` characters only match the beginning and end of the entire input string. However, if the input string contains multiple lines (separated by newline characters), the `m` flag allows these anchors to match the beginning or end of each individual line.
    - **Example**:
        - Without the `m` flag: `/^cat/` would only match `"cat"` at the beginning of the entire string.
        - With the `m` flag: `/^cat/m` would match `"cat"` at the beginning of each line in a multi-line string like:

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/34.png)

These flags can be combined for more powerful pattern matching. For example, `/cat/gim` would find all occurrences of `"cat"`, ignoring case, across multiple lines

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/35.png)

### [Try by your hand >>](https://regex101.com/r/hoGMkP/1)

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/36.png)

### [Try by your hand >>](https://regex101.com/r/E88WE2/1)

---

## Greedy vs Lazy Matching in Regular Expressions :

> In regular expressions, **greedy** and **lazy (or non-greedy)** matching refer to how much text a quantifier (like `*`, `+`, `?`, `{n,m}`) will match when there are multiple possible matches in a string.
> 
- **Greedy matching** will always try to match **as much text as possible**.
- **Lazy (or non-greedy) matching** will try to match **as little text as possible** while still satisfying the pattern.

## **Greedy Matching** (Default Behavior) :

By default, most quantifiers in regular expressions are **greedy**. This means they will match **the longest possible string** that still satisfies the pattern.

### Greedy Quantifiers:

- `*`- Match 0 or more times.
- `+` - Match 1 or more times.
- `?` - Match 0 or 1 time.
- `{n,m}` - Match between `n` and `m` times.

## Example (Greedy):

- **Pattern**: `/<b>.*<\/b>/`
    - `.*` means "0 or more of any character (greedy)."
- **String**: `"This is <b>bold</b> and <b>another bold</b> tag"`
- **Output**: `"<b>bold</b> and <b>another bold</b>"`

![image alt](https://github.com/0XAl3aref/Regullar-Expresion-/blob/main/Images/37.png)

## [Try by your self >>](https://regex101.com/r/AyAdgJ/1)

## **Lazy Matching** (Non-Greedy Matching) :

### Lazy Quantifiers:

- `*?` - Match 0 or more times, as few as possible.
- `+?` - Match 1 or more times, as few as possible.
- `??` - Match 0 or 1 time, as few as possible.
- `{n,m}?` - Match between `n` and `m` times, as few as possible.

## Example (Lazy):

- **Pattern**: `/<b>.*?<\/b>/`
    - `.*?` means "0 or more of any character (lazy)."
- **String**: `"This is <b>bold</b> and <b>another bold</b> tag"`
- **Output**: `"<b>bold</b>"`


## [Try by your self>>](https://regex101.com/r/AyAdgJ/2)

---

---

<aside>
🧑🏻‍💻

Creator : Mohamed Saber 

</aside>

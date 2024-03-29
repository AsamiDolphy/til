# What/how I am learning daily as an absolute beginner in Japan

## 9 Feb, 2024
* [paizaラーニング](https://paiza.jp/ "paiza")
  - Python体験編1: Pythonをはじめよう(chapter 1 to 9)
  - スキルチェック(Ruby: 2)
* [PERSONAL MIRAIZ](https://miraiz-persol.jp/learning)
  - Python入門: chapter 1, 2


 So far so good.
 It looks quite similar to Ruby. I think both are pretty readable.

  ##### Python
  ```python
  print("Hello world") # -> Hello world
  print(1 + 1) # 2
  print("1 + 1") # 1 + 1
  ```
   ##### Ruby
  ```ruby
  puts "Hello world" # -> Hello world
  puts 1 + 1 # 2
  puts "1 + 1" # 1 + 1
  ```


 Also, `variable` (変数) is used similarly.

  ##### Python
  ```python
  message = "Hello world"
  print(message) # -> Hello world
  ```

   ##### Ruby
  ```ruby
  message = "Hello world"
  puts message # -> Hello world
  ``````


  Taking `input` (代入) is like..
  
  ##### Python
  ```python
  name = input()
  print("Hello " + name)  # Yamada -> Hello Yamada
  ```
   ##### Ruby
  ```ruby
  name = gets.chomp
  puts "Hello #{name}"  # Yamada -> Hello Yamada
  ```


  Not too similar but memorable.

  ##### Python
  ```python
  number = int(input())
  print(number * 10)  # 12 -> 120
  ```

   ##### Ruby
  ```ruby
  number = gets.chomp.to_i
  puts number * 10  # 12 -> 120
  ``````


  As well as..

  ##### Python
  ```python
  number = int(input())
  print("日給" + str(number * 1000) + "円")  # 8 -> おこづかい：8000円
  ```

   ##### Ruby
  ```ruby
  number = gets.chomp.to_i
  puts "日給：#{number * 1000}円"  # 8 -> 日給：8000円
  ```

  `int()` is like `to_i` of Ruby and `str()` is like `to_s` of that.

---

### 10 Feb, 2024
* [paizaラーニング](https://paiza.jp/ "paiza")
 - Python体験編1: Pythonをはじめよう(chapter 10 to 11)
  - スキルチェック(Python: 2, Ruby: 2)
* [PERSONAL MIRAIZ](https://miraiz-persol.jp/learning)
  - Python入門: chapter 3

 Because the logic and structure of the code are similar between Python and Ruby, but the syntax differs a little, I keep forgetting to add `:` and `(  )` for Python code and `end` for Ruby.

 ## `if` statement

  ##### Python
  ```python
  name = input()

  if name == "python":
    print("Welcome")
  ```
   ##### Ruby
  ```ruby
  name = gets.chomp

  if name == "python"
    puts "Welcome"
  end
  ```

    ##### Python
  ```python
  number = input()

  if number >= 50: # =-> if number is less than and equal to 50
    print(number) # -> If true, print the number
  ```
   ##### Ruby
  ```ruby
  number = gets.chomp.to_i

  if number >= 50 # =-> if number is less than and equal to 50
    puts number # -> If true, print the number
  end
  ```

## `if` `else` `elif` (`elsif` for Ruby)
    ##### Python
  ```python
  name = input()
  print("Hello " + name)

  if name == "python":
    print("Welcome")
  elif name == "PYTHON":
    print("Good morning")
  else:
    print("Goodbye")
  ```
   ##### Ruby
  ```ruby
  name = gets.chomp

  if name == "python"
    puts "Welcome"
  elsif name == "PYTHON"
    puts "Good morning"
  else
    puts "Goodbye"
  end
  ```

  MIRAIZ: `operators`
  ```python
  x = 12 # assignment
  y = 2 # assignment
  z = x > y and y% 2 == 0
  print(z) # <- true!
  ```
  I was surprized to know that in Python, I don't need to explicitly declare the data type of a variable when I create it! Instead, Python determines the data type of a variable dynamically based on the values assigned to it. 
  This should be one reason why Python is said to be a readable and faster development language compared to many other languages, I assume.

  So I can confirm the type as below:
  ```python
  x = 3.1492
  print(type(x))
  ```
  then it prints
  ```python
  <class 'int'>
  ```


  ## 12 Feb, 2024
* [paizaラーニング](https://paiza.jp/ "paiza")
  - Python体験編1: Pythonをはじめよう(chapter 12)
  - スキルチェック(Python: 9, Ruby: 1)
* [PERSONAL MIRAIZ](https://miraiz-persol.jp/learning)
  - Python入門: chapter 4

  Classify numbers.
  It's a good to review Ruby by comparing with Python. This reminded me of the usage of string interpolation `#{}` to insert the value.

    ##### Python
  ```python
  number = int(input())

  if number < 100:
    print(str(number) + "は100より小さい")
  elif number < 200:
    print(str(number) + "は100以上200より小さい")
  else:
    print(str(number) + "は200以上")
  ```

    ##### Ruby
  ```ruby
  number = gets.chomp.to_i

  if number < 100
    puts "#{number} は100より小さい"
  elsif number < 200
    puts "#{number} は100以上200より小さい"
  else
    puts "#{number} は200以上"
  end
  ```



Something new I learnt today through the skill check drills.

* To remove `substrings`, use string manipulation methods
(not '-')
* `gsub` method, "global substitution" is to replace all occurrences of a specified pattern within a string with another substring.

    ##### Ruby
  ```ruby
  S = gets.chomp.to_s

  if S.include?("の秋")      # 「の秋」が含まれている場合
    puts S.gsub("の秋", "")  # 「の秋」を「」と置き換える
  else
    puts S
  end
  ```

 MIRAIZ: `google Colaboratory`, `for` roop, `range` function
  ```python
  for x in [3, 4]:   # input 3 and 4 for x
    print(x * 5)
    print(x * 10)
    print(x * 15)

  # output
  15    # <- 3 * 5
  30    # <- 3 * 10
  45    # <- 3 * 15
  20    # <- 4 * 5
  40    # <- 4 * 10
  60    # <- 4 * 15
  ```

`range` function: it generates a sequence of numbers, but it __does not include the upper bound specified__ in the function call.
range(3, 5) generates a sequence of numbers starting from 3 up to (but not including) 5. So, the sequence generated by range(3, 5) is [3, 4]. 

  ```python
  for x in range(3, 5):   # input from 3 to 4 for x 
    print(x * 5)
    print(x * 10)
    print(x * 15)

  # output
  15    # <- 3 * 5
  30    # <- 3 * 10
  45    # <- 3 * 15
  20    # <- 4 * 5
  40    # <- 4 * 10
  60    # <- 4 * 15
  ```

Now I wanted to know there in Ruby. It made me a little confused. 

    ##### Python
  ```python
  for x in [3, 4]:
  ```

Thins in Ruby can be as below.

    ##### Ruby
  ```ruby
  for x in [3, 4]
  end
  ```
  ```ruby
  [3, 4].each do |x| 
  end
  ```
  
And `range` function is like this below.

    ##### Python
  ```python
  for x in range(3, 5):  # 3, 4 (not including 5)
  ```

    ##### Ruby
  ```ruby
  for x in 3..4          # range '3..4' includes 3 and 4!
  end
  ```

    ## 13 Feb, 2024
* [paizaラーニング](https://paiza.jp/ "paiza")
  - Python体験編1: Pythonをはじめよう(chapter 13 to 15)
  - スキルチェック(Ruby: 1)
* [PERSONAL MIRAIZ](https://miraiz-persol.jp/learning)
  - Python入門: chapter 4

  I found the `loop` logic interesting to compare between Python and Ruby. 

    ##### Python
  ```python
  greeting = "Hello world"
  for i in range(5):        # <- "i" is a variable. "range(5)" repeats 5 times
    print(greeting)

  # output
  Hello world
  Hello world
  Hello world
  Hello world
  Hello world
  ```

    ##### Ruby
  ```ruby
  greeting = "Hello world"
  5.times do |i|
    puts greeting
  end

  # output
  Hello world
  Hello world
  Hello world
  Hello world
  Hello world
  ```

Variable "i" holds the current iteration index. Therefore..

    ##### Python
  ```python
  greeting = "Hello world"
  for i in range(5):
    repeats 5 times
    print(greeting + str(i))  # <- added "str(i)" to show current iteration index

  # output
  Hello world0                # <- iteration index is added after "Hello world"
  Hello world1
  Hello world2
  Hello world3
  Hello world4
  ```

    ##### Ruby
  ```ruby
  greeting = "Hello world"
  5.times do |i|
    puts greeting + i.to_s
  end

  # output
  Hello world0
  Hello world1
  Hello world2
  Hello world3
  Hello world4
  ```

Receive a variable to loop for.

    #### Python
  ```python
  greeting = "Hello world"
  count = int(input())

  for i in range(count):
    print(greeting)
  ```

    ##### Ruby
  ```ruby
  greeting = "Hello world"
  count = gets.chomp.to_i

  count.times do |i|
    puts greeting
  end
  ```

    #### Python
  ```python
  count = int(input())

  for i in range(count):
    name = input()
    print("Hello " + name)

  # input
  3
  world
  Yamada
  python

  # output
  Hello world
  Hello Yamada
  Hello python
  ```

    ##### Ruby
  ```ruby
  count = gets.chomp.to_i

  count.times do |i|
    name = gets.chomp
    puts "Hello " + name
  end

  # input
  3
  world
  Yamada
  python

  # output
  Hello world
  Hello Yamada
  Hello python
  ```
Receive multiple variables and classify.

    #### Python
  ```python
  count = int(input())

  for i in range(count):
    number = int(input())
    print(number)

    if number == 10:
        print(str(number) + "は10に等しい")
    elif number > 10:
        print(str(number) + "は10より大きい")
    else:
        print(str(number) + "は10未満")
  ```

    #### Ruby
  ```ruby
  count = gets.chomp.to_i

  count.times do |i|
    number = gets.chomp.to_i
    puts number

    if number == 10
        puts "#{number}は10に等しい"
    elsif number > 10
        puts "#{number}は10より大きい"
    else
        puts "#{number}は10未満"
    end
  end
  ```

And this was the last lesson of paiza learning. It was very fun and easy to understand as they explain "variable" etc. every time. I think that's very important for the beginners. 

In the skill check on paiza, I have learnt something new.

In Ruby, to see if there are the same characters in a string:

  #### Ruby
  ```ruby
  s = gets.chomp

  if s.chars.uniq.length < s.length
    puts "NG"                 # <- 文字数が減った = 重複があった
  else
    puts "OK"
  end
  ```

## `.chars` method
`.chars` method is used to split a string into an array of its individual characters. Here's how it works:

  ```ruby
  string = "Hello"
  characters = string.chars
  puts characters.inspect     # Output: ["H", "e", "l", "l", "o"]
  ```
The `.chars` method converts each character of the string into an element of an array, allowing to access and manipulate individual characters more easily.

## `.uniq` method
`.uniq` method is used to remove duplicate elements from an array. Here's how it works:

  ```ruby
  array = [1, 2, 2, 3, 3, 3, 4, 5]
  unique_elements = array.uniq
  puts unique_elements.inspect  # Output: [1, 2, 3, 4, 5]
  ```

`.uniq` method returns a new array with duplicate elements removed, preserving only the unique elements in the original array. It does not modify the original array.

## `length` method
length method (or size method, which is an alias of length) is used to determine the number of elements in various data structures. Here are a few examples:

  * For strings: Returns the number of characters in the string.
  * For arrays, hashes, and other collections: Returns the number of elements in the collection.

  ```ruby
  string_length = "Hello".length         # string_length is 5
  array_length = [1, 2, 3, 4, 5].length  # array_length is 5
  ```


Then the same thing in Python:

  #### Python
  ```python
  s = input()

  if len(set(s)) < len(s):
    print("NG")
  else:
    print("OK")
```

## len` function
`len()` function returns the number of elements in a sequence or collection. Here are a few examples:

  * For strings: Returns the number of characters in the string.
  * For lists, tuples, sets, and dictionaries: Returns the number of elements in the collection.

  ```python
  string_length = len("Hello")        # string_length is 5
  list_length = len([1, 2, 3, 4, 5])  # list_length is 5
  ```

## `set` function
`set()` function and data type represent an unordered collection of unique elements. Here's an overview of set() in Python:

Creating a Set:
Creating a set by passing an iterable (such as a list, tuple, or string) to the set() function, or by using curly braces {} with comma-separated elements:

  ```python
  # Using set() function
  my_set1 = set([1, 2, 3, 4, 5])

  # Using curly braces
  my_set2 = {1, 2, 3, 4, 5}
  ```

Properties of Sets:
Sets are unordered collections, meaning the elements are not stored in any particular order.
Sets contain only unique elements. If you try to add an element that already exists in the set, it will not be added again.
Sets can only contain immutable (hashable) elements. This means you cannot have lists or other sets as elements of a set, but you can have tuples since they are immutable.

Common Operations on Sets:
* Adding elements: Use the add() method to add a single element to the set, or use the update() method to add multiple elements from another set or iterable.
* Removing elements: Use the remove() or discard() methods to remove specific elements from the set.
* Set operations: Sets support various set operations such as union, intersection, difference, and symmetric difference.
Here's a basic example of using sets:

  ```python
  my_set = {1, 2, 3, 4, 5}

  # Adding elements
  my_set.add(6)
  print(my_set)  # Output: {1, 2, 3, 4, 5, 6}

  # Removing elements
  my_set.remove(3)
  print(my_set)  # Output: {1, 2, 4, 5, 6}

  # Set operations
  other_set = {4, 5, 6, 7, 8}
  intersection = my_set.intersection(other_set)
  print(intersection)  # Output: {4, 5, 6}
  ```

      ## 12 Mar, 2024
* [paizaラーニング](https://paiza.jp/ "paiza")
  - スキルチェック(Ruby: 1)
* [PERSONAL MIRAIZ](https://miraiz-persol.jp/learning)
  - Python入門: chapter 4

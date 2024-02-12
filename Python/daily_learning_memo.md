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
# What I am learning daily as an absolute beginner in Japan

### 9 Feb, 2024
#### * paizaラーニング [(リンク)](https://paiza.jp/ "paiza")
　Python体験編1: Pythonをはじめよう(chapter 1 to 9)

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


 Also, variable (変数) is used similarly.

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


  Taking input is like..
  
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

  `int()` is like `to_i` of Ruby.
  `str()` is like `to_s` of Ruby.

  
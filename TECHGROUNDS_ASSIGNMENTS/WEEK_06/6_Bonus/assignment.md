# [6/ Bonus]

You might have seen a folder in the drive named ‘Pls fix’. This folder contains 16 very small Python scripts that are somehow broken. Your job is to fix the mistake by changing only 1 or 2 small things within the script. The expected result for each script is written in the multi-line comment at the top of the script.

This exercise is meant as a little fun puzzle, but also to help you learn to troubleshoot existing code, so even though they are optional, they are recommended to do.

Of course, you can get to the expected results by simply deleting all the code and using a print function, but that would defeat the purpose of this exercise.

The exercises are approximately ordered based on difficulty level, but you might want to skip one if you get stuck and go back to that one later

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Assignment

Exercise:

- Fix the 16 broken Python scripts
- 1
  
  ```
  '''
  The output should be:
  hello Casper
  hello Floris
  hello Esther
  '''
  foo = 'hello'
  ls = ['Casper', 'Floris', 'Esther']
  for name in ls:
  	print(loo,name)
  
  ```
  
  
- 2
  
  ```
  '''
  The output should be:
  100
  '''
  foo = 20
  bar = '80'
  print(foo + bar)
  ```
  
  
- 3
  
  ```
  '''
  The output should be:
  30
  '''
  foo = 20
  for i in range(10):
  	foo -= 1
  
  print(foo)
  ```
  
  
- 4
  
  ```
  
  ```
  
  
- 5
  
  ```
  '''
  The output should be:
  Star Wars
  '''
  ls = ['Lord of the rings', 'Star Trek', 'Iron Man', 'Star Wars']
  print(ls[4])
  ```
  
  
- 6
  
  ```
  '''
  The output should be:
  80
  '''
  foo = 80
  if foo < 30:
  	print(foo)
  else:
  	print('big number wow')
  elif foo < 100:
  	print(foo)
  ```
  
  
- 7
  
  ```
  '''
  The output should be:
  ['Dog', 'Cat', 'Fly']
  '''
  ln = ['Dog', 'Cat', 'Elephant', 'Fly', 'Horse']
  short_names = []
  
  for animal in ln:
  	if len(animal) == 3:
  		short_names.append(animal)
  	short_names = []
  
  print(short_names)
  ```
  
  
- 8
  
  ```
  '''
  The output should be:
  20
  '''
  foo = 10
  bar = 2
  print(foo**bar)
  ```
  
  
- 9
  
  ```
  '''
  The output should be:
  0
  1
  2
  3
  4
  8
  9
  '''
  for i in range(10):
  	if i < 5:
  		print(i)
  	elif i < 8:
  		break
  	else:
  		print(i)
  ```
  
  
- 10
  
  ```
  '''
  The output should be:
  the number is 20
  '''
  print('the number is' + 20)
  ```
  
  
- 11
  
  ```
  '''
  The output should be:
  IT LIVES!
  '''
  dev monster():
  	print('IT LIVES!')
  
  monster()
  ```
  
  
- 12
  
  ```
  '''
  The output should be:
  4
  16129
  '''
  def square(x):
  	return x**2
  
  nr = square(2)
  print(nr)
  
  big = square(foo)
  print(big)
  
  foo = 127
  ```
  
  
- 13
  
  ```
  '''
  The output should be:
  Your random number is: <insert random number here>
  '''
  import random
  
  random.randint(1,100)
  print("Your random number is:")
  ```
  
  
- 14
  
  ```
  '''
  The output should be:
  True
  '''
  def rtn(x):
  	return(x)
  
  foo = rtn(3)
  
  if foo > rtn(4):
  	print(True)
  else:
  	print(False)
  ```
  
  
- 15
  
  ```
  '''
  The output should be:
  a5|||5|||5|||a5|||5|||5|||a5|||5|||5|||
  '''
  foo = ''
  for i in range(3):
  	foo += 'a'
  	for j in range(3):
  		foo += '5'
  	for k in range(3):
  		foo += '|'
  
  print(foo)
  ```
  
  
- 16
  
  ```
  '''
  The output should be:
  A playable game 
  '''
  import random
  
  # generate random int
  goal = random.randint(1,100)
  
  win = False
  tries = 1
  
  while win == False and tries < 7:
  	try:
  		# ask for input
  		inpt = int(input("Please input a number between 1 and 100: "))
  		# count attempt as a try
  		tries += 1
  
  		# check for match
  		if inpt == goal:
  			win = True
  			print("Congrats, you guessed the number!")
  			print("It took you", tries, "tries")
  		# give hints
  		elif inpt < goal:
  			print("The number should be higher")
  		else:
  			print("The number should be lower")
  
  	except:
  		print("Please type an integer")
  
  # 
  if win == False:
  	print("Game over! You took more than seven tries")
  ```
  
  
- 

### Used sources

- The Techgrounds ‘Pls fix’ folder ,which contains 16 very small Python scripts that are somehow broken.

- 

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

Exercise:

- Fix the 16 broken Python scripts

- 1
  
  ![1.png](1.png)

- 2
  
  ![2.png](2.png)

- 3
  
  ![3.png](3.png)

- 4
  
  ![4.png](4.png)

- 5

- 6

- 7

- 8

- 9

- 10

- 11

- 12

- 13

- 14

- 15

- 16
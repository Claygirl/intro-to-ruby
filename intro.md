Intro to Ruby
=============

Meet Mr. Turtle! Apart from being a legitimate turtle, he's a Ruby object. And he has some pretty serious artistic talent. Thanks to Mr. Turle will learn how to interact with objects in Ruby (yes! this means programming stuff!) and how to draw some clever shapes.

The very basic concept in Ruby is that everything is an object. We will learn what this means exactly in a little while, but for now it's important to keep in mind that _everything_ is an object here. 

Every object has some properties - talents and Mr. Turtle here draws. They all also have a way of communicating with us and are very prone to suggestions of what should they do. So, let's see how to persuade Turtle to do something for us - In the mean time we'll also learn basic concepts of computer programming.

First step
-------------
Mr. Turtle will cooperate eagerly and draw whatever you want, but only if you command him in a very precise and specific way. This applies to all programming activities - your programme will run great as far as you follow basic rules.

Here, the proper way to say something to Mr. Turtle is to put it inside the following block:

```ruby
Turtle.start do
  // your code goes here
end
```

Everything in the block will be executed by the turtle. For the first example, let's just draw 100 pixels of a straight line. Type in the code into the editor and hit "Run" at the bottom.

```ruby
Turtle.start do
  forward 100
end
```

Neat, huh?! But we can certainly do better than that. Square would be even better. We will need to make some turns in the process, let's see how this looks like.

```ruby
Turtle.start do
  forward 100
  turnright 90
  forward 100
  turnright 90
  forward 100
  turnright 90
  forward 100
end
```

For the record - yes, Mr. turtle also turns left if you wish to.

Square was ok, but can you make a triangle?

Variables
-------------
Good job on your first triangle! You're definitely ready to take the next step.

```ruby
Turtle.start do
  i = 0
  40.times do
    forward 10
    forward i
    turnright 90
    i += 10
  end
end
```

Loop
-------------
Greek-like pattern.

```ruby
Turtle.start do
  5.times do
    forward 10
    turnleft 90
    forward 10
    turnright 90
    forward 10
    turnright 90
    forward 20
    turnright 90
    forward 20
    turnleft 90
    forward 20
    turnleft 90
  end
end
```

Conditionals
-------------
And some randomness.

```ruby
Turtle.start do
  100.times do |i|
    ang = rand(360)
    turnright ang
    len = rand(40)
    forward len
    goto width/2, height/2 if(i % 10 == 0)
  end
end
```

Everything together
-------------
Turtle will draw the Earth.

```ruby
Turtle.start do
  goto width/4, height/2
  360.times do |i|
    forward 2
    turnright 1
  end
  
  pencolor blue
  r = 120
  30.times do
    goto rand(width), rand(height)
    goto width/2, height/2
    penup
    turnright rand(360)
    forward r + rand(100)
    len = 5 + rand(30)
    pendown
    5.times do
      forward len
      turnleft 180-360/10
    end
  end
  
  goto width/2, height/2
end
```

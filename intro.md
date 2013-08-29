Intro to Ruby
=============

Meet Mr. Turtle! Apart from being a legitimate turtle, he's a Ruby object. And he has some pretty serious artistic talent. Thanks to Mr. Turle will learn how to interact with objects in Ruby (yes! how to program stuff!) and draw some clever shapes.

The very basic concept in Ruby is that everything is an object. We will learn what this means exactly in a little while, but for now it's important to keep in mind that _everything_ is an object here. 

Every object has some properties - talents and Mr. Turtle here draws. They all also have a way of communicating with us and are very prone to suggestions of what should they do. So, let's see how to persuade Turtle to do something for us - In the mean time we'll also learn basic concepts of computer programming.

First step
-------------

Variables
-------------
Turtle will draw a spiral.

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

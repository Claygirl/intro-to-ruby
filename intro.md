Intro to Ruby
=============

Zmienne
-------------
Żółw rysuje spiralę.

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

Pętla
-------------
Grecki wzorek.

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

Instrukcje warunkowe
-------------
I losowość.

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

Wszystko połączone
-------------
Żółw rysuje ziemię.

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

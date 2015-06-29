# The Times Construct

The next construct is `times`. There are two important distinctions to be mindful of when using `times`. The first one is that it has to be called on an Integer (like 1 or 10000). The second is that it executes the block a certain number of times, which is dependent on the number that it's called on. Let's look at the example below:

```ruby
5.times do
  puts "Penguins like to jump off icebergs!"
end
```

This outputs `Penguins like to jump off icebergs!` five times in your Terminal.

## Examples

### Basic Times Example: Dinner Party

Let's take a look at some more complex examples: 

You just has a wildly successfull dinner party with seven of your very best friends. Then they went home and left you with all of the dishes. They will not be invited back. 

Let's clean those dishes using the `times` method:

```ruby
7.times do 
  puts "I am doing the dishes for my former friends"
end

# => "I am doing the dishes for my former friends"
# => "I am doing the dishes for my former friends"
# => "I am doing the dishes for my former friends"
# => "I am doing the dishes for my former friends"
# => "I am doing the dishes for my former friends"
# => "I am doing the dishes for my former friends"
```

### Intermediate Times Example: Crime Spree

Okay, that's fine but all we did was print text––what if we wanted to change the value of a variable within a loop? Let's see how that works: 

You are a jewel thief who has stolen 960 very valuable jewels (you are a really good jewel thief). But now you need to unload your stolen jewels from your bag into the safe in your secret hideout.  

```ruby
jewels_in_bag = 100

3.times do 
  puts "Hiding stolen jewels"
  jewels_in_bag = jewels_in_bag - 10
end

puts "We have #{jewels_in_bag} jewels still to hide"


# => "Hiding stolen jewels"
# => "Hiding stolen jewels"
# => "Hiding stolen jewels"

# => "We have 70 jewels still to hide

```

#### Advanced Times Example

This is fun and all but so far we've only printed text within the block of code within the loop. What if we wanted to do something more, say keep track of the number of jewels we are hiding *as we hide them*? 

```ruby
jewels_in_bag = 960

3.times do 
  puts "Hiding stolen jewels"
  jewels_in_bag = jewels_in_bag - 250
  puts "Now there are only #{jewels_in_bag} jewels left to hide!"
end

puts "We have #{jewels_in_bag} still to hide"


# => "Hiding stolen jewels"
# => "Now there are only 90 jewels left to hide!"
# => "Hiding stolen jewels"
# => "Now there are only 80 jewels left to hide!"
# => "Hiding stolen jewels"
# => "Now there are only 70 jewels left to hide!"

# => "We have 70 still to hide"

```

%%%

## Using the `times` method

We're still struggling to master that levitation charm. Since we need to keep praciticing, let's write somd code that allows us to puts out the phrase "Wingardium Leviosa" seven times. This time, we want to achieve that result by writing fewer lines of code. With the `loop` keyword, we needed to write `puts "Wingardium Leviosa" seven times`. With the `times` keyword, we can do it with far fewer lines. 

Fill out the content of the `using_times` method so that calling it will puts out the desired phrase seven times by using the `times` keyword. 

```ruby
def using_times
	#your code here
end

~~~solution

def using_times 
	7.times do
		puts "Wingardium Leviosa"
	end
end

using_times

~~~validation
looping_string = "Wingardium Leviosa\nWingardium Leviosa\nWingardium Leviosa\nWingardium Leviosa\nWingardium Leviosa\nWingardium Leviosa\nWingardium Leviosa\n"

expect{ using_times }.to output(looping_string).to_stdout

```

%%%

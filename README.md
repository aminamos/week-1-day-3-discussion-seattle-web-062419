# Week 1, Day 3 Discussion Questions

## Instructions

Take 30 minutes and answer the following questions together with your group. Take turns playing around with the code provided in Pry or IRB.

## Questions

1 . If the `Animal` class is defined like this:

```ruby
class Animal

  def species
    "cat"
  end

end
```

How would you 

a. Make a new instance of `Animal`?
  Animal.new
b. `puts` out to the terminal, the species of that new `Animal` instance?
  Animal.species

2 . Although we all know that cats are the best species, not all animals are cats (unfortunately). How could you change the `Animal` class so that an instance of `animal` can have its species set to any species at all?
  # attr_accessor :species

  # OR

  # def species=(species)
  #  @species = species
  # end


3 . We have the following class, and the following two instances of that class:

```ruby
class Animal

  def species
    "cat"
  end
end

maru = Animal.new
hanna = Animal.new
```

Given the above, what will the following return? Why?

```ruby
maru == hanna
```

# false because the object IDs are not the same

4 . Given the following class:

```ruby
class Animal
  
  def species 
    my_species = "cat"
  end

  def say_species
    puts "Hi! I'm a #{my_species}"
  end
end
```

What will happen when we invoke the following code?

```ruby
maru = Animal.new
maru.say_species
```
# should puts Hi! I'm a cat

Is it broken? Why? How can you fix it?

# it is broken, trying to directly access my_species instead
# of getting it from species method. delete my from my_species

5 . Reverse engineer this code (i.e., write the class that will make the code work as invoked below):

```ruby
frederick = Animal.new("bull")
frederick.species
# => "bull"
```

**Hint:** How can you instantiate, or *initialize*, an instance of a class with a given value? What kind of variable would you use so that that value can be shared across instance methods within a class?

# class Animal
#     attr_accessor :species
# 
#     def initialize(species)
#         @species = species
#     end
# end

6 . Given the following code:

```ruby
class Animal
  
  def initialize(species)
    @species = species
  end

end

lil_bub = Animal.new("cat")
```

What is the relationship between `lil_bub` and the `Animal` class? 

# it's initializing a new animal with the species of "cat" and assigning
# that to variable lil_bub












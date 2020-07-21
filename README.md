# create_a_better_world
Playing around with python to make the world a better place.

Feel free to fork the code and write the necessary packages for dependencies.  :)
Also, in order to properly grow the codebase, we will need some documentation.
Oh, and in the event that my code is not "pythonic" I welcome you to lend a hand. 
This is not my day job.  


"""
Created on Mon Jul 20 17:50:25 2020
@author: ericervin
"""

from emotions import love, compassion, gratitude
from wisdom import reason, critical_thinking, teach

gifts = [love(), compassion(), gratitude()] # Create list of gifts to apply to the people

# Build function to create a better world
def create_a_better_world(people, gifts):
    for person in people:
        for gift in gifts:
            person.apply(gift)
            teach(person, gift)
            teach(person, critical_thinking)
            teach(person, reason)
        if person.goodwill_to_all != True:
            while person.goodwill_to_all  == False:
                love(person)
                teach(person, love)

# Run the function in an endless loop
while True:
    create_a_better_world(people, gifts)

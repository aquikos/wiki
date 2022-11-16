---
title: "Générémós"
---

The Générémós, or, more specifically, the Générémós Liré, is the highest legislative body in the Liran Republic. 
It functions similarly to a national parliament, though there are some notable differences. 
It consists of a 144 member legislative body, with 8 parties represented as of the 3660 parliamentary elections.

<!---
History
Powers/Functions
Elections
Membership
Organization (within the Chamber)
--->

## History

The Générémós was created alongside the Liran Republic, and has lasted ever since.

## Election Procedures

Each Généjé serves a three year term, and is limited to four terms in total. 
Because of how elections are structured, every seat technically goes up for election every three years.
                
Instead of voting for individual candidates at a lower level, each state is 
alotted a certain amount of seats in direct proportion to its population.

To determine how many members each state gets, the total population is divided by 144, giving the population threshold required for one seat.
Each state's population is then divided by this number, giving the amount of seats they ought to receive.
Because this number is unlikely to be an integer, and because only so many seats remain, whichever states are closest to receiving another seat receive priority. 

|         | Population | Overflow | Seats | Extra Seat? |
|:-------:|:----------:|:--------:|:-----:|:-----------:|
|  Kenemo |   31.56m   |   0.450  |   34  |      No     |
| State 2 |   22.43m   |   0.484  |   24  |      No     |
| State 3 |   17.10m   |   0.666  |   19  |     Yes     |
| State 4 |   14.99m   |   0.363  |   16  |      No     |
| State 5 |   12.01m   |   0.110  |   13  |      No     |
| State 6 |   10.55m   |   0.516  |   12  |     Yes     |
| State 7 |    9.06m   |   0.890  |   10  |     Yes     |
| State 8 |    8.25m   |   0.005  |   9   |      No     |
| State 9 |    5.97m   |   0.517  |   7   |     Yes     |

The algorithm to generate this data is found below (in Python):
<pre>
import math

# Function to get each state's overflow.
def get_overflow(val):
    return val - math.floor(val)

# Stores the population of each state. It does not technically have to be ordered from greatest to least, but it can be.
populations = [31.56, 22.43, 17.1, 14.99, 12.01, 10.55, 9.06, 8.25, 5.97]

# Stores the national population.
nat_pop = sum(populations)

# Get the population threshold required for a member.
T = round((nat_pop / 144), 6)

# Gives the total amount of members, including overflow value, for every state.
state_totals = [(populations[k] / T) for k, v in enumerate(populations)]

# Gives just the decimal value of each state's member amount.
state_overflows = [get_overflow(state_totals[k]) for k, v in enumerate(state_totals)]

# Gives the total number of spare seats in the house.
spare_seats = 144 - sum([math.floor(state_totals[k]) for k, v in enumerate(state_totals)])

# Gives the total amount of members assigned to each state.
assgnd_seats = [math.floor(state_totals[k]) for k, v in enumerate(populations)]

# Documents which states received an extra member.
assgnd_extras = [0] * 9

# Documents the overflow of those states which received an extra member.
overflows = [0] * 9

# Eventually stores tuples holding all of the data for each state.
state_data = []

# Assigns each spare seat to the proper state.
for i in range(spare_seats):
    mv = max(state_overflows)
    ind = state_overflows.index(mv)
    overflows[ind] = state_overflows[ind]
    state_overflows[ind] = 0
    assgnd_seats[ind] += 1
    assgnd_extras[ind] += 1

# Compiles all of the data generated into state_data
for k, v in enumerate(populations):
    if assgnd_extras[k] >= 1:
        data = (populations[k], round(overflows[k], 3), "Yes", assgnd_seats[k])
        state_data.append(data)

    else:
        data = (populations[k], round(state_overflows[k], 3), "No", assgnd_seats[k])
        state_data.append(data)

print(f"National Population: {round(nat_pop, 3)}m")
print(f"Member Threshold: {T}")
print(f"Spare Seats: {spare_seats}\n")

for k, v in enumerate(state_data):
    print(f"State {k+1}:")
    print(f"Population: {state_data[k][0]}m")
    print(f"Overflow: {state_data[k][1]}")
    print(f"Received Overflow Seat? {state_data[k][2]}")
    print(f"Seats: {state_data[k][3]}\n")
</pre>

## Organization

### Current Membership
![3660 Election Results](/wiki/images/3660_liran_national_parliament_makeup.svg)

{{< article link="/wiki/government/liran_political_parties/" >}}





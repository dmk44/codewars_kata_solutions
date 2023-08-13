# Two fighters, one winner

Create a function that returns the name of the winner in a fight between two fighters.

Each fighter takes turns attacking the other and whoever kills the other first is victorious. Death is defined as having `health <= 0`.

Each fighter will be a `Fighter` object/instance. See the Fighter class below in your chosen language.

Both `health` and `damagePerAttack` (`damage_per_attack` for python) will be integers larger than 0. You can mutate the `Fighter` objects.

Your function also receives a third argument, a string, with the name of the fighter that attacks first.

**Example:**
```
declare_winner(Fighter("Lew", 10, 2), Fighter("Harry", 5, 4), "Lew") => "Lew"
  
Lew attacks Harry; Harry now has 3 health.
Harry attacks Lew; Lew now has 6 health.
Lew attacks Harry; Harry now has 1 health.
Harry attacks Lew; Lew now has 2 health.
Lew attacks Harry: Harry now has -1 health and is dead. Lew wins.
```

```python
class Fighter(object):
    def __init__(self, name, health, damage_per_attack):
        self.name = name
        self.health = health
        self.damage_per_attack = damage_per_attack
        
    def __str__(self): return "Fighter({}, {}, {})".format(self.name, self.health, self.damage_per_attack)
    __repr__=__str__
```

## Solution

```python
def declare_winner(a, b, c):

    if c == b.name: b, a = a, b
    while True:
        b.health -= a.damage_per_attack
        if b.health > 0: 
            print(f"{a.name} атакует {b.name}. У {b.name} осталось {b.health}")
        if b.health <= 0:
            print(f"{a.name} атакует {b.name}. {b.name} погибает с {b.health}")
            print(a.name, "Победил!")
            return a.name
            break

        a.health -= b.damage_per_attack
        if a.health > 0: 
            print(f"{b.name} атакует {a.name}. У {a.name} осталось {a.health}")
        if a.health <= 0:
            print(f"{b.name} атакует {a.name}. {a.name} погибает с {a.health}")
            print(b.name, "Победил!")
            return b.name
            break
```
# Grasshopper - Terminal game combat function
**DESCRIPTION:**

Create a combat function that takes the player's current health and the amount of damage recieved, and returns the player's new health. Health can't be less than 0.


## Solution
```C++
int combat(int health, int damage) {
return (damage <= health) * (health - damage);
}
```
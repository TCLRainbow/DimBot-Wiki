# PP: Sword fighting minigame
> Please note that at the current stage, all pp-related data will reset once the bot restarts!

> This is a global context command: You can either send the commands in a server or DM

## Fundamental command: d.pp
The very first thing that you should do when starting is to send `d.pp`. This initialises your pp. You can also send this again to reroll your pp, or `d.pp <user>` to set the target's pp.

Each `d.pp` command call will perform the following actions on the target's pp:
* Sets the size to a random integer between 0-69 inclusive
* 25% chance to generate viagra
* 10% chance to generate sesami oil **if the target doesn't have it**

This means that `d.pp` always rerolls viagra even if it is already available/activated; if the target has sesami oil, `d.pp` does NOT affect it in any way.

## Combat command: d.pp sf
The next command is `d.pp swordfight` *(`sf`)*, allowing you to use your pp as a weapon and sword fight. If you just send `d.pp sf`, you will fight against a random person, **including yourself**. You can specify your target by `d.pp sf <user>`.


Provided that both sides have a valid pp, the following will happen, the bot will award you a score:
```
score = target's size - your size
```
This will be added into your total score as well.

In cases where your target's size is actually larger, the awarded score will be negative, and your score will simply be deducted.

> Note: This command has a cooldown of 10 seconds per user.
## Other commands
### d.pp info
Displays your pp statistics without modifying it. This command also displays the size of your pp in integer unlike other commands which simply draw it.
### d.pp leaderboard
Shows the score of every person. You will occasionally see a lot of persons with 0. This is usually due to people initialising others' pp but they haven't `d.pp sf` for once.

------------------
## Items
### Viagra
When your pp has `Viagra available!` under it, it means you can activate viagra by `d.pp viagra`. Doing so will double your current pp size for 3 rounds during sword fight.

Please note that your opponent can still change your pp size even if you have viagra available/activated.
### Sesami oil
Sesami oil is a **passive** item. When obtained, you can completely absorb the next attack targetting you. However, you can't decide when to activate this item.
## Abilities
If your items fit certain scenarios, you can use abilities to do powerful moves.
### Zenitsu
Zenitsu is the name of a character in Demon Slayer, basically like Thor but holding a katana instead.

When you have **both** ``Viagra available`` **and** ``Sesami oil``, you can send `d.pp zen <user>` to stun a user for 2 rounds. Simply sending `d.pp zen` stuns a random person, **including yourself**.

If you are stunned, you must send `d.pp sf` twice to remove the effect.
+++
title = "0 - Brainstorming"
date = 2019-11-27
template = "article.html"
+++

## Prelude

I'm trying to design a tcg.  I enjoy playing tcg's with friends, and I find tcg's to be a very
creative hobby, not just for deck building (which in a lot of cases I don't find creative), but
for the systems exploration aspect.  It's like a less dangerous form of chemistry mixing cards
to see what reactions form.  Eventually though, you get bored of seeing various chemical formulas
for creating infinite energy and start to look for the formulas that create the illusive 'fun' and 'deep' energies that tickle the brain beyond big numbers and tables that look more like spilled cards than a game of creatures fighting.  When you get to that point, you either start looking into
developing a curated set of cards that generate that crunchy thinky fun environment (cubing) or you start trying to develop custom cards that are crunchy and thinky in and of themselves.

However, there are limits to deck making, cubing, and card making, and that's the system itself, sometimes you just want a new system to explore, and that's what I want at this moment.  

Seperately, my YouTube algorithm has been reccommending WolfeyVGC videos, so I've been learning about competitive Pokemon again.  I also started playing the Pokemon tcg a bit on my phone.  I think it's a badly designed game that is kind of fun because of how absolutely busted it is.  I can't take it seriously when either my or my opponet spends 5 minutes cycling through 40 cards in their deck and locking down the board in one turn, but I still have fun doing it when I get to.
The very obvious thing I noticed is that the Pokemon tcg is nothing like the game... and I'd like to use that as an oppurtunity for something new and sick.

As of writing this, I already have some cards that I've been mocking up using the wonderful tool [Dexterous](https://www.dextrous.com.au/), but before showing those bad card designs, I'd like to show my work for getting there.

## Drawing Inspiration

I think most people have played Pokemon, but if you haven't, it's a game about dog fighting with magical dogs that are sometimes dragons or bridges or ice cream.  There's a lot of layers to it, especially in the competitive world, but at it's core it's a turn based battler with rock/paper/scissor elements.  Already, we have a nice starting point because card games can be a form of turn based battler, and the rock/paper/scissor element is pretty easy add on.

So what are the cards in this game? Well, looking at the Pokemon tcg, probably the Pokemon, or in this copyright respecting game, ***Monsters*** (I'm very creative).  However, our first point of differentiation is that Monsters don't have attacks or actions on them, they act more like bundles of stats with a type (which we'll call ***Aspects***) and an ***Ability*** or two.  ***Abilities*** will work similarly to how they do in the tcg: passive or triggered effects that help give identities to the attached ***Monsters***.

So what about the moves?  I already decided they're not going directly on the ***Monster*** cards... but if I make them their own cards, where do they go?  In the video games, the answer is simple, they're attached to the Pokemon.  In a physical card game, this is a pretty bad idea for three reasons.

1. It's pretty unreasonable to maintain a move list for ***Monsters*** in a physical card game, so every monster could learn every move, or only moves of matching ***Aspects*** (or some other siloing system).  This either gives way too much freedom, or way too little freedom.
2. A lack of randomness can lead toxic strategies and extremely hard counters forming with no real counter play or chance for failure.  Pokemon has this, but can alleviate this with bluffing, we won't have that luxury (I'll explain why later).
3. It means each player will have 4 to 6 mini decks that they can't mix but also need to look at two at a time... this can lead to some pretty bad mistakes or cheating oppurtunities, along with being extremely unergonomic (inergonomic? I'm not really spell checking this).

So, I guess attacks are going in the deck, and you'll have a hand of cards.  Oh, and there's more than just attacks, so we'll use the umbrella term ***Actions***.  Also, ***Monsters*** will live on the battlefield or the bench, just like the vidya games.

I'm not really sure what other card types would be needed at this point, I'm sure I'll end up having subtypes like ***Action - Attack*** or permanents on the field... I don't want to use the term Aura since it's used by so many other games... I'll think of something.

Anyway, I mentioned ***Aspects*** before, and I have some conflicting feelings about it.  I love the rock/paper/scissor element to it and it's thematic feeling, it's so exciting hitting a fire type with water and knocking it out in one go.  It works really well in video games when the game looks up the table in an instant and you just need a rough memory of type interactions.  In table top games, that look up has to be manual.  The Pokemon tcg approaches this issue by putting a few weaknesses on the Pokemon themselves that are mostly related to their types, although not entirely consistent.  This is fine, but what if I want to add another type? Is it just going to be inherently weaker against older cards which weren't designed around it? Also, how many weaknesses and resistances can I realistically fit on a card? Also, what if I don't just want elemental types? I like dragon type, but if I have a ***Dragon Aspect*** then there's no way I'm not going to have a ***Goblin Aspect*** that shits everything up.

I think for now, I'm going to do the inadvisable move and have ***Aspects*** utilize reminder cards with either a table or other form of communicating an ***Aspects*** specific interactions.  To alleviate the pressure of trying to remember too many ***Aspect*** interactions, I think I'll make thinks like Goblin and Dragon into creature sub types.  I'll also use both the creature type and ***Aspect*** when calculating STAB.

For those unaware, in the Pokemon games, your moves get empowered if they share a type with the Pokemon using it.  So Charmander's Flamethrower will be stronger than Squirtles (although there's something to be said for the element of surprise).  This is something I want to bring into my game as a form of soft siloing, but I don't want it to be too wordy or ugly.  For instance, imagine we had a fire type attack named Flamethrower:

```
(F) Flamethrower
Action - Attack

Deal 3 damage to target monster.  If this shares an aspect with the user, deal 5 damage instead.
```

Nearly doubles it's word count just for the mechanic.  However, I think I have a solution that also allows me to include the beloved element of accuracy into the game.  (That's not a joke, I think accuracy and miss mitigation are really interesting to play around and give a knob of risk and reward to certain moves.)  

The design element I'm thinking of is based on **Star Wars: Destiny**, a really wacky Trading Dice Game that got discontinued a few years ago.  The game had unique dice per character card that you would roll to deal damage, gain resources, etc.  Having dice also opened up the effect of managing dice: selecting specific sides, rerolling dice, using rolled dice as a resource, etc. 

<img src="https://images-cdn.fantasyflightgames.com/filer_public/74/2c/742c9f57-4e44-4128-9ba0-9aeb77f401d9/swd14-16_pl_cardfan_1.png" alt="Star Wars Destiny" width="250"/>

It was a cool system and I'd like to take the idea of using dice in that manner, but instead of attaching them to the characters, attach dice to the ***Action*** cards.  I'm also going to avoid using specific dice, since having a dice per card in your deck is insane.  Instead, all the cards will use d6's.  Now I can introduce accuracy and aspects in a pretty straight forward way, let's look at the beginnings of a card idea:

*(the slashes are supposed to look like down arrows)*
```
(F) Flamethrower
Action - Attack

\2/ - Deal 3 damage to target monster.
\7/ - Deal 5 damage to target monster.
```

It's less wordy than the original card text, and a bit more intuitive to read.  If you roll a 1, you miss, if you roll a 2 to 6, you deal 3 damage, and if you roll a 7, you deal 5.  So by introducing the dice, we've clearly introduced a way to miss and have a knob to turn for accuracy, and can even add critical hits on 6's and... wait that says 7... on a d6? Good eye.  I think this is actually a pretty cool way to have STAB work: add 1 to your roll if the ***Monster*** shares a type with the ***Action***.  Also, because each clause is independent, we can have moves that don't just scale damage, perhaps something like this?

```
(W) High Tide
Action - Attack

\1/ - Deal 3 damage to target monster.
\4/ - Deal 2 damage to 2 target monsters.
```

Lots of possibilities I think.

Okay, time for one more thing to think about: Turn structure and dead cards.  In the video games, you select the moves your Pokemon will use and how they will use them simultaneously and secretly, then things get revealed at the same time.  This works because the game can easily keep track of that, but once again, we do not have that luxury.  If you're targeting a grass ***Monster*** with a one hit ko fire move, when both players reveal moves and they revealed they were going to switch, you could just say that you were going to target the other ***Monster***.  This removes a lot of the tension from the game and allows for some bad sportsmanship.  I don't really want to leave this up to the good graces of players and want the turn structure to enforce a fun game loop.

Instead of picking everything simultaneously, players will pick things one at a time, back and forth.  So the first player will pick a move, then the second, then the first, then the second, then the moves happen.  Pretty straightforward.  However, there's an issue here: very low card velocity.  Know what's fun about card games? Using your cards! No one likes seeing the same card or cards sit in there hands not doing anything for a full game, they'd much rather play it or cycle it, but how can we do that with only two ***Actions*** per turn?

Well, this is where I'm going to draw some inspiration from Flesh and Blood (specifically, but also other any cards as resources systems).  I'd like each card in your hand to have the functionality of an ***Action*** or the ability to ***Support*** an action.  I don't want to actually have a resource system, it moves too far away from the inspiration for this game, but ***Supporting*** will fill a similar job.  To describe the idea, let's ammend our **Flamethrower** example to include an important part of Pokemon: stats.

```
(F) Flamethrower
Action - Attack

\2/ - Deal 3 + (pow) damage to target monster.
\7/ - Deal 5 + (pow) damage to target monster.
```

This should be pretty straightforward, a high powered ***Monster*** will do more damage with it's attacks.  Does that mean the low powered monsters are out of luck? No, this is where your left over cards in hand come into play, let's ammend the above again to show how ***Supporting*** will work:

*(I'm just going to go with three stats for now to keep the initial design of the system simpler, I don't want to deal with physical/special splits.)*
```
(F) Flamethrower
Action - Attack

\2/ - Deal 3 + (pow) damage to target monster.
\7/ - Deal 5 + (pow) damage to target monster.

(Pow): +2
(Def): -1
(Spd): 0
```

The above card can be played as an attack during your turn, or it can be attached to a ***Monster***.  The attached monster will have their stats changed by the listed amount, in this case they'll get stronger but frailer.  With a hand size of 5 cards (just to pick a number), this will mean a player has to choose two ***Actions*** to use and which to have ***Support***, which ***Monsters*** to use them, and how to distribute their ***Supporting***.  At the end of the turn, ***Supporting*** cards will go on the bottom of the deck, and used ***Actions*** will go to the discard, then players will draw back up.  This will provide high card velocity, more choices to make, more knobs to turn, and is just something I'm really excited to see how it plays.

Now we've touched on types, card types, and turn structure, we really have most of the basics down for a really shitty play test, there's just one more thing I want to add before talking about card layouts: I hate prize cards.  Prize cards are a win more mechanic and are dumb.  I want to have a loose rubber banding mechanic, and for this system I think it's going to be by making ***Monstes*** double faced: when one of your monsters is knocked out, they're flipped and added to your hand as a special ***Action***.  We'll see if this is too much or kind of cool.

## Basic Rules

So to tie all the above together into some basic rules for how this will play for play testing:

1. Each player comes to the table with 6 monsters and a 60 card deck (or 4 and 40 for small games).
2. Each player chooses two of their monsters seceretly to start on the field, the others start on the bench face down.
3. The players randomly choose the first player, each draw 5 cards, then start playing rounds until a winner is decided.

A round plays out as follows:

1. Action Phase: Players take 1 action per turn back and forth until both pass:
    * Commit an action in hand for a monster.
    * Support a monster with a card in hand.
    * Discard a card to switch a monster out with a benched monster (revealing it if it hasn't been revealed yet.) (All counters on the monster are removed, and all supporting cards immediately go to the bottom of your deck.)
    * Passing.
2. Draw Phase: Once both players have passed, they draw back up to 5 cards.
3. Roll Phase: Roll a dice for each acting monster.
4. Resolution Phase: In order of the monsters speed, each monster carries out their actions.
    * Speed ties between players are decided by turn order.
    * Speed ties between a players own monster are decided by the player.
    * Damage dealt to a monster is calculated by subtracting the monsters defense from the damage being dealt.  If the damage is reduced to 0 at this stage, instead deal 1 damage.  Once the amount of damage being dealt is calculated, apply any aspect bonuses or penalties.  After a monster is dealt damage, if it has more damaged marked on it than it does health, it is knocked out and the owner returns it to their hand flipped.
5. After all monsters have carried out their actions, put any supporting cards on the bottom of their owners deck.

## Initial Layout

Okay, I'm tired of just typing things that I've been thinking about for a while instead of showing the card layouts I was playing around in conjunction with coming up with the ideas (I want to see how much is reasonable to put on a card).  Also, yes I am using AI art for this: I want something that can allow me to quickly recognize a card while I'm prototyping and playtesting, and this is already incredibly time consuming and iterative, if this ever moves on from being a shitter side project I'll upgrade all the assets used.

***Monsters*** are pretty straight forward, they have a name, a type, an aspect, an ability, and some stats:

<img src="/images/fire_lord.png" alt="Silly Monster Design" width="250"/>

***Actions*** are a bit more complex given they have multiple potential clauses, a name, a type, an aspect and supporting stats that need to be layed out in a distinct way to make an intuitive distinction from the other mode of play.  I've decided to go with a form of the flip card design from old Kamigawa sets, it's a bit ugly, but it's also very distinct and clearly seperates the play mode from the support mode:

<img src="/images/pounce.png" alt="Silly Attack Design" width="250"/>

Don't take the assets and colors too seriously, I'm just looking for a reasonably good layout to start.

This article has taken me longer than expected to do me being a slow writer, needing to set up the site, and having a job/hobbies/wife/workouts... so the next article could be a while, but when and if it happens, it will be about a first play test with some friends and will include a full print and play pdf of rules and starting deck.  I would put that in this article, but I need to actually design the cards and write the rules, not just the general ideas for the rules.
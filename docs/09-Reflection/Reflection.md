---
title: Reflection
---

## Module

Overall this subsystem was a success. 
It senses, temperature and humidity, and it communicates with all other boards in the system. 
It should have been calibrated better, and it needs some smoothing to attenuate the noise that ends up in the data lines both on the board and through out the system. 
To remake this I would choose higher tolerance capacitors and resistors for the on board data lines and perhaps filter the signal more.

## Start Up Tips
Come up with an Idea first very general, I Know I'm making a land based rover for primarily agriculture exploration, what should a rover have, then start throwing ideas at the wall. It doesn't matter if they seem dumb in the moment, write them all down the useful obvious ones, the cool ones, the funny ones and the dumb ones. Once you have about 100 start narrowing them down. When you decide on what you want start researching how those systems work. Once you know how they work it is only a matter of selecting components, meeting the budget and other requirements, designing the circuit, and building the thing.

## Lessons

- Read datasheets carefully
- Don't bet on components remaining in stock have backup options in your price range preselected.
- Make sure all of your design checkers pass
- Make sure you know how your circuit works, in and out. Know why each component exists.
- Take your time with soldering, do not rush, it will cost you more time.
- Be excited about what you are creating.

## Top 5 Recomendations

1. Use VSCode for everything, mpremote for python, and platformio for C.
2. Triple check your connection headers match your teammates.
3. LEDs are very important for debugging the need to be on your board, Not optional.
4. Debug your code with more code. Add lines to make your code reply simply in serial in trouble areas to help identify where the code is breaking.
5. If you can somehow go back in time and become very proficient in coding before this class do that.

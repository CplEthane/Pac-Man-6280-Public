Pac-Man implementation for the 6280 FPGA

Started by Ethan Forsythe, 13 September 2024

This is the starter code for an arcade-accurate port of Pac-Man to the 6280 FPGA. The current version is far advanced from what you see here -- for instance, I replaced all the ghost's AI routines recently as to implement the ghost "look-ahead" feature (which telegraphs to the player which direction the ghost plans to turn before they actually turn at an intersection.) This version is bare-bones and has Pac-Man going around the maze, eating dots, and being chased solo by Pinky. There's a lot of other things in here you might consider wasteful it terms of space, but I'm currently almost done with the entire implementation and even with the title screen, Pac-Man here only weighs in at 128Kb (1 whole megabit!)

If you've never programmed for a legacy hardware, especially one that's limited to 8 kilobytes of RAM as this is here, you'll likely question why some functions aren't written more elegantly such as using recursion. That's because recursion eats up memory and if you saw the current version of my code, you'll ask why I unrolled many of my loops and didn't partner my evaluations with &&'s.

Despite the deficiency in memory, the 6280 is a VERY fast 8-bit CPU so cycling through each of the ghosts in the up-to-date version -- including keeping score, fruit bonuses, ghost-fright-modes, etc -- is still running at a rock-solid 60fps.

I more or less report my updates via my X/Twitter if you're curious as to where Pac-Man port sits at the moment; so if you want to see them, just go to https://x.com/11975MHz and check my media tab for screenshots.

-Ethan Forsythe Dec 18, 2024

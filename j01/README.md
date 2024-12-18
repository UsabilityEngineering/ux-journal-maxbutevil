# GoblinCon
**Max van der Veen, 11/22/2024**

This journal is written from the perspective of a group of people who are unfamiliar with GoblinCon, but familiar with the similar JackBox series of games. In reality, I made the game, so I'm having to pretend a bit, and incorporating feedback received while testing the game with my friends.
## User Experience
Our goal was to successfully start a game of GoblinCon and play one full round.
### Landing Page
We started by going to the link, which brought us to this page:
![image](https://github.com/user-attachments/assets/f50d9bc9-7afa-4338-846f-28c0a99f0c43)
We didn't run into any issues here, because we knew going into it that the game had a structure similar to the JackBox series of games. In JackBox games, a non-mobile device is the "host", and displays a join code. Players then join the game on their phone by entering the code. However, if we didn't already have that knowledge, this screen probably would've been confusing to us. This page could benefit from improved **Help and Documentation**; some kind of mechanism to explain how the game works to players who are confused. For example, a button or a link that provides information about how the game works would go a long way.

### Hosting
The host page looks like this:
![image](https://github.com/user-attachments/assets/8ef75649-3af9-4956-8526-9d00f641111f)
This is where we encountered the biggest issues. The settings occupy a lot of the screen, but it's not clear at a glance how you change them. We were able to figure out fairly quickly that you change the settings by clicking them, but then we encountered a bigger problem. The settings changed with each click, but they changed in unpredictable ways. When we clicked a setting, it felt like it randomly decided whether to increase or decrease.

After some more experimentation, we figured out that clicking on the right side of a setting would increase the value, while clicking the left side would decrease it. This was made more confusing by the fact that the values "loop around". If you click the right side of the "Number of Rounds" setting while it's already at the maximum 8 rounds, it would loop around to the minimum of 1, which made it harder for us to figure out what was going on.

A final, smaller issue is that the "Game Mode" setting doesn't change when clicked. It appears to only have one option, making us wonder why it was even visible at all. Having a setting that does not respond to user input is another potential source of confusion, and makes it even less obvious that the other settings *do* respond to user input.

This is an issue with **Consistency & Standards**. Where possible, the interface should be consistent with users' previous experiences with similar tools. Here, there are buttons that do not look like buttons, defying user expectations. To make matters worse, they're invisibly split in half, doing opposite things depending on where you click.

On the other hand, using the system wasn't a bad experience once we understood how it worked. If the settings more obviously functioned as buttons, and were visually split in half in some way, the interface would be much better. We set the "Number of Rounds" to 1, reset the other settings to their defaults, and moved on.

### Starting
The players were familiar with JackBox, so they didn't have any issues joining the game from their phone. Once everybody was in and we were ready to start, we ran into another small issue. In JackBox, a specific player is chosen to be the "VIP", and they start the game when everybody is ready. However, it was not clear to us that GoblinCon worked the same way. Unlike JackBox, GoblinCon has settings that you change from the host, so in our minds, it made sense that the game would be started from the host. Fortunately, the player who was able to start the game noticed fairly quickly that this was not the case, but it still led to a bit of friction that could have been avoided.

### Drawing
Once the game started, the players were greeted with a page that looks like this.
![image](https://github.com/user-attachments/assets/e063c41d-0efb-4d67-95e0-e5f2c4fc154d)

Here, we encountered some more problems. It's not clear what "Mr. Smooch" means without seeing the additional context on the host screen, which says to "draw a creature named Mr. Smooch".

A bigger issue was that the "submit" button is large and easy to accidentally click, and once you submit, your drawing is locked in for the round. This is a frustrating experience, and a major issue with both **User Control/Freedom** and **Error Recovery**. Users should ultimately have as much control over their experience as possible, and when they make a mistake, they should be able to reverse it with minimal negative consequences. Here, users can easily "lock in" their intent by mistake without any opportunity to go back or recover from the issue. Fortunately, I have a proposed solution. Currently, if a player runs out of time without pressing the "submit" button, their drawing will be automatically submitted anyway. I think the best solution would be to have _all_ submissions work this way. Rather than pressing the "Submit" button, a player would have the option to "Lock In" their drawing. They wouldn't be able to edit their drawing while it's "Locked In", but they would be able to press the same button again to "Unlock" their drawing if they want to go back and change something.

Another issue is that it was not clear what all the buttons do. Changing colors by using the buttons at the top was intuitive, but it wasn't immediately obvious that the top-right button with the is for erasing, though the dotted circle did help us eventually figure it out. Also, the buttons at the bottom left are "Undo", "Redo", and "Toggle Line Weight" respectively, which is not at all clear (though the "Toggle Line Weight" button icon changes when the line weight is thick, which helped). Again, this was something that wasn't too difficult to figure out through experimentation, but it could've been more clear.

The first round was a bit rocky, but by talking to each other as we played, we were able to figure out how the game's drawing pad worked. When we were done, we had the impression that a second round would have gone fairly smoothly (as long as nobody submitted early by mistake).

### Voting
We didn't run into any issues with voting for others' submissions; the UI was much simpler and did its job well. Since we had made the game only have one round, it ended after we voted.

### Conclusion
The long list of issues above makes the UI look pretty ineffective, but in my (completely unbiased) opinion, it's actually decent overall. There were several screens that I didn't comment on because I didn't find any significant problems with them. Also, the UI is fairly learnable - once you are sufficiently familiar with it, many of the issues go away. If the game was more intuitive to new users and easier to learn, it could be very effective.

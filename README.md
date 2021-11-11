## Welcome to Thomas Gorman's Homepage

### Projects

## FAME - A Tycoon Adventure Game

# Start your journey

In FAME, you start your journey to become a music star with nothing but $20 and an old acoustic guitar. You must amass one million followers over the course of your journey. Perform, record, and survive the journey of being a musician! Good luck!

# The more fans you have... the more you gain!

Specialized mathematical formulas help provide a smooth experience and allows for an increase of the rate of growth as you play the game.

```code example

else if (selectedItem.Name == "Perform")
                {
                    Random rnd = new Random();
                    double moneyEarned = rnd.Next(20 * (timesPerformed + 1) * (epsReleased / 3 + 1) * ((albumsReleased + 1)) * (showmanship + 1));
                    int fansGained = rnd.Next(20 * ((timesPerformed / 4) + 1) * (((5 ^ albumsReleased + (epsReleased / 2))) + 1) * (showmanship * 3 + 1));
                    numberOfFans = numberOfFans + fansGained;
                    playerMoney = moneyEarned + playerMoney;
                    string moneyEarnedStr = moneyEarned.ToString();
                    WriteLine($"You performed a concert and earned ${moneyEarned} and gained {fansGained} fan(s).");
                    timesPerformed++;
                }
```

You can use the [editor on GitHub](https://github.com/tmgorman23/tmgorman23.github.io/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).


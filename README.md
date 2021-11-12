# Welcome to Thomas Gorman's Homepage V1.0

# Projects

## FAME - A Tycoon Adventure Game

### Start your journey

In FAME, you start your journey to become a music star with nothing but $20 and an old acoustic guitar. You must amass one million followers over the course of your journey. Perform, record, and survive the journey of being a musician! Good luck!

![Image](https://github.com/tmgorman23/tmgorman23.github.io/blob/main/images/famehome.PNG?raw=true)
![Image](https://github.com/tmgorman23/tmgorman23.github.io/blob/main/images/famelocations.PNG?raw=true)

### The more fans you have... the more you gain!

Specialized mathematical formulas help provide a smooth experience and allows for an increase of the rate of growth as you play the game.


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


### Random Events

Being a musician has its challenges, so the game reflects this through random chances. Your guitar strings can break! But it isn't all bad, once you're popular enough, you may also be invited to come onto a late night talk show, festival, or more!

                    code example 2
                    Random rnd1 = new Random();
                    Random rnd2 = new Random();
                    if (rnd2.Next(16) == rnd1.Next(16))
                    {
                        //Find the guitar string in user's inventory using built in LINQ function.
                        Item guitarStrings = CurrentPlayer.Inventory.FirstOrDefault(x => x.Name == "Guitar Strings");
                        //Remove guitar string from the inventory.
                        CurrentPlayer.Inventory.Remove(guitarStrings);

                        WriteLine("Your guitar strings broke!");
                        Utility.DelayUser();
                        ViewLocations();
                    };

![Image](https://github.com/tmgorman23/tmgorman23.github.io/blob/main/images/famerandom.PNG?raw=true)

                    public void RandomEvent()
                    {
                        //random events to speed up gameplay
                        Random rnd = new Random();
                        int randomValue = rnd.Next(1000);
                        //Award!
                        if (randomValue >= 0 && randomValue <= 10 && numberOfFans > 50000)
                        {
                            Random rnd1 = new Random();
                            int fansGained = rnd1.Next(1000, 25000);
                            numberOfFans = numberOfFans + fansGained;

                            WriteLine($"Congrats! You won an award! You gained {fansGained} fans from the exposure.");

                            Utility.DelayUser();
                        }
                        //Late Night Show
                        else if (randomValue >= 100 && randomValue <= 150 && numberOfFans > 75000)
                        {
                            Random rnd1 = new Random();
                            int fansGained = rnd1.Next(1000, 25000);
                            numberOfFans = numberOfFans + fansGained;
                            Random rnd2 = new Random();
                            int moneyEarned = rnd2.Next(1000, 2500);
                            playerMoney = playerMoney + moneyEarned;

                            WriteLine($"Congrats! You were invited onto a late night show to perform! You gained {fansGained} fans from the exposure and were payed ${moneyEarned}.");

                            Utility.DelayUser();
                        }
                        //Festival
                        else if (randomValue >= 200 && randomValue <= 300 && numberOfFans > 25000)
                        {
                            Random rnd1 = new Random();
                            int fansGained = rnd1.Next(1000, 25000);
                            numberOfFans = numberOfFans + fansGained;
                            Random rnd2 = new Random();
                            int moneyEarned = rnd2.Next(1000, 2500);
                            playerMoney = playerMoney + moneyEarned;

                            WriteLine($"Congrats! You were invited to perform at a music festival! You gained {fansGained} fans from the exposure and were payed ${moneyEarned}.");

                            Utility.DelayUser();
                        }

                    
## Tip Calculator

### A concise tip calculator that doesn't waste your time.

![Image](https://github.com/tmgorman23/tmgorman23.github.io/blob/main/images/tipcalchome.PNG?raw=true)

Enter the total bill amount and the desired tip percentage and quickly get an answer.

![Image](https://github.com/tmgorman23/tmgorman23.github.io/blob/main/images/tipcalcexample.PNG?raw=true)

And don't worry about any mistakes, we'll let you know.

![Image](https://github.com/tmgorman23/tmgorman23.github.io/blob/main/images/tipcalcerror.PNG?raw=true)

            bool billSuccess = double.TryParse(BillAmountTextBox.Text, out billAmount);
            if (billSuccess)
            {
                Console.WriteLine($"Converted {BillAmountTextBox.Text} to {billAmount}");
            }
            else
            {
                ErrorTextBoxBill.Text = "Error: Please enter a number without any symbols or letters.";
                InitializeComponent();
            }

            bool tipSuccess = double.TryParse(TipAmountTextBox.Text, out tipPercentage);
            if (tipSuccess)
            {
                Console.WriteLine($"Converted {TipAmountTextBox.Text} to {tipPercentage}");
            }
            else
            {
                ErrorTextBoxTip.Text = "Error: Please enter a number without any symbols or letters.";
                InitializeComponent();
            }

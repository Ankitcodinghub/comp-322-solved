# comp-322-solved
**TO GET THIS SOLUTION VISIT:** [COMP 322 Solved](https://www.ankitcodinghub.com/product/comp-322-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;110753&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP 322 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Assignment 3: Object Oriented Design.

Before you start:

● Collaboration and research for similar problems on the internet are recommended. However, your submission should reflect individual work and personal effort.

● Submit two files called assignment3-part1.cpp and assignment3-part2.cpp containing all the declarations of your classes, together with their implementation and a main() function to run your code.

Make sure your code is clear and readable. Readability of your code as well as the quality of your comments will be graded.

● No submission by email. Submit your work to mycourse.

● If your code does not compile successfully it will not be graded.

● Be happy when working on your assignment, because a happy software developer has more inspiration than a sad one :).

Part One [70 points]

In this assignment we will tackle the implementation of a very simplified version of the famous BlackJack card game. We will drop all the complicated rules and we will consider that the game is played by one player against the computer.

The simplified rules are like this:

● Each card has a numerical value.

○ Numbered cards are counted at their face value (two counts as 2 points, three, 3 points, and so on)

○ An Ace count as either 1 point or 11 points (whichever suits the player best)

○ Jack, queen and king count 10 points each

● The player will compete against the computer which represents the casino.

● The goal of the player is to try to reach a total point sum of 21 without exceeding it. Whoever exceeds 21 first loses (technically known as busting).

● At the beginning of each round, the player is dealt two open cards and the computer is dealt one open card. The cards are open, meaning that the values are known for both the player and the computer (no hidden cards).

● The player will see the sum of the points from his 2 open cards and decide whether or not to draw an additional card.

● When the player decides that he won’t draw anymore and he is happy with whatever total amount he got, the computer will draw and open an additional card.

● The computer will keep on drawing additional cards, one at a time as long as the sum of its cards is less or equal 16.

● If the computer busts, the player wins.

● If the computer doesn’t bust (total sum is less or equal 21), then the total values are compared between the computer and the player. Whomever has a higher value wins the round.

● If the two totals are the same, no one wins the round (technically called a push).

We will add a twist to the rules to give the casino a higher probability of winning. To do so, we need to keep track of the history of all the rounds to know how many rounds the player has won VS the casino. When we find that the casino is losing more rounds than the player (casino is winning less than 55% of the time), we need to trick the randomness of the cards in order to give the casino a tiny push and maintain a percentage of winning around 55% for the casino.

Here is a list of all the needed classes to code the game:

● Card: represents a card. Each card has a rank and a type which can be easily represented via enums.

○ Rank is one of the following {ACE = 1, TWO, THREE, FOUR, FIVE, SIX, SEVEN,

EIGHT, NINE, TEN, JACK, QUEEN, KING}

○ Type is one of the following {CLUBS, DIAMONDS, HEARTS, SPADES} ○ Card class must have the following methods:

■ getValue that would return the numerical value of a card

■ displayCard that would print to the screen the card information. For example 1H means ace of hearts, 2D means two of diamonds, QS means queen of spades and so on.

● Hand: represents the set of cards that the player or the computer holds. This class should contain a list of cards that can be implemented as an array or a vector or any data structure that you prefer. It should also have the following methods:

○ add that would add a card to the hand

○ clear that would clear all the cards from a hand (removing them)

○ getTotal that would get the total sum of the cards numerical values

Deck should implement the following methods:

○ Populate will create a standard deck of 52 cards

○ shuffle will shuffle the cards

○ deal will deal one card to a hand

● AbstractPlayer: represents a generic abstract player that can be a human or the computer. This is an abstract class meaning that it has a pure virtual method. The methods that this class have are:

○ virtual bool isDrawing() const = 0; which is a pure virtual method that indicates whether a player wants to draw another card.

○ isBusted that returns true if a player has busted (sum of cards exceeds 21).

● HumanPlayer: represents the human player. This class inherits AbstractPlayer and should have the following methods:

○ isDrawing implements the inherited method that indicates whether a player wants to draw another card

○ announce a method that prints information about whether the player wins, loses or has a push situation.

● ComputerPlayer: represents the computer (the casino). This class inherits

AbstractPlayer and should have the following method:

○ isDrawing implements the inherited method that indicates whether the computer should be drawing another card. Remember that the rules for the computer are different. The computer should keep on drawing an additional card as long as the sum of its cards is less or equal 16. This method should take the percentage of winning into consideration. If the percentage is less than 55%, then you need to implement some logic to make sure that the casino gets better chances of winning.

● BlackJackGame: a class representing the overall game. This class must have the following data members:

○ A Deck data member m_deck

○ A ComputerPlayer member m_casino

It should also implement the following method:

○ play that plays the game of blackjack

Use the following main function to run the game:

int main()

{ cout &lt;&lt; ” Welcome to the Comp322 Blackjack game!” &lt;&lt; endl &lt;&lt; endl;

BlackJackGame game;

// The main loop of the game bool playAgain = true; char answer = ‘y’; while (playAgain)

{ game.play();

// Check whether the player would like to play another round cout &lt;&lt; “Would you like another round? (y/n): “; cin &gt;&gt; answer; cout &lt;&lt; endl &lt;&lt; endl; playAgain = (answer == ‘y’ ? true : false);

}

cout &lt;&lt;“Gave over!”; return 0;

}

The output while playing the game should be something similar to this:

Welcome to the Comp322 Blackjack table!

Casino: 8S [8]

Player: 4C 9D [13]

Do you want to draw? (y/n):y Player: 4C 9D 7C [20]

Do you want to draw? (y/n):n

Casino: 8S 2H [10] Casino: 8S 2H 9S [19] Player wins.

Would you like another round? (y/n):y

Casino: 1S [11]

Player: 1C 2H [13]

Do you want to draw? (y/n):y Player: 1C 2H 10D [13]

Do you want to draw? (y/n):y

Player: 1C 2H 10D KH [23]

Player busts. Casino wins.

Would you like another round? (y/n):y

Casino: QS [10]

Player: 4C 4H [8]

Do you want to draw? (y/n):y Player: 4C 4H 3S [11]

Do you want to draw? (y/n):y

Player: 4C 4H 3S JC [21]

Casino: QS 1C [21] Push: No one wins.

Would you like another round? (y/n):n Gave over!

Grading scheme:

● Proper calculation of the Ace value (1 vs 11) as per the instructions: 3 points

● Rank and type implemented properly as enum: 2 points

● Card::getValue() and Card::displayCard(): 10 points (5 each)

● Hand:: add, clear, getTotal: 12 points (4 each)

● Deck:: populate, shuffle, deal: 12 points (4 each)

● AbstractPlayer::isBusted: 4 points

● AbstractPlayer::isDrawing pure virtual and const: 4 points

● HumanPlayer::isDrawing , annouce : 8 points (4 each)

● ComputerPlayer::isDrawing: 5 points

● BlakJackGame::play(): 6 points

● Keeping track of winning history and maintaining a 55% chance of winning to the casino: 4 points

Part Two [30 points]

Modify your implementation to accommodate for a multi-hand game. This means that the same player can have 1, 2 or 3 hands at the same table. The maximum number of hands that a player can have at the same time is 3.

If the player chooses to have 3 hands, this means that the player will act as if he (or she) were 3 different players. The player can win some hands and lose some others. The player will be drawing for the 3 different hands one after the other.

Clone your code from part 1 and modify it to accommodate the new requirements. Please make sure to submit the versions separately.

Same rules apply as before. Modify the output to reflect the new reality.

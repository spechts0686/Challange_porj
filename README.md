# Challange_porj

//virtual black jack

//Card.h

//looks at current cards and suit for cards
class Card(){
public: Card(int rank, suit)
getRank();
getSuit();
int getValue()

private:
int rank
string suit;
};

// number of cards in deck, hand and to give.
class Deck{
public:
  Deck();
  void shuffle();
  Card dealCard();

private:
  vector<Card> cards;
  int curIndex;

};

//checks players hands and adds cards to hand
class Player{
public:
    Player();
    void addCard(const Card& card);
    int getHandValue() const;

private:
  vector<Card> hand;
};

// main function that keeps track of score, player or dealers turn, outcome of each hand.
class Game{
public:
  Game();
void start();

private:
Deck deck;
Player player;
int playerScore;
void dealInitialCards();
void playerTurn();
void dealerTurn();
void determineOutcome();
};



Банковский аккаунт



\#include <iostream>

using namespace std;



class BankAccount {

private:

&nbsp;   int accountNumber;

&nbsp;   double balance;



public:

&nbsp;   BankAccount(int number, double bal) {

&nbsp;       accountNumber = number;

&nbsp;       balance = bal;

&nbsp;   }



&nbsp;   int getAccountNumber() {

&nbsp;       return accountNumber;

&nbsp;   }



&nbsp;   double getBalance() {

&nbsp;       return balance;

&nbsp;   }



&nbsp;   void deposit(double amount) {

&nbsp;       if (amount > 0)

&nbsp;           balance += amount;

&nbsp;   }



&nbsp;   void withdraw(double amount) {

&nbsp;       if (amount > 0 \&\& amount <= balance)

&nbsp;           balance -= amount;

&nbsp;   }

};



int main() {

&nbsp;   BankAccount acc(12345, 1000);



&nbsp;   acc.deposit(500);

&nbsp;   acc.withdraw(300);



&nbsp;   cout << acc.getAccountNumber() << endl;

&nbsp;   cout << acc.getBalance() << endl;



&nbsp;   return 0;

}



Игровой персонаж



\#include <iostream>

using namespace std;



class Character {

private:

&nbsp;   int health;



public:

&nbsp;   Character(int h) {

&nbsp;       health = h;

&nbsp;   }



&nbsp;   int getHealth() {

&nbsp;       return health;

&nbsp;   }



&nbsp;   void takeDamage(int damage) {

&nbsp;       if (damage > 0 \&\& health - damage >= 0)

&nbsp;           health -= damage;

&nbsp;   }



&nbsp;   void heal(int amount) {

&nbsp;       if (amount > 0)

&nbsp;           health += amount;

&nbsp;   }

};



int main() {

&nbsp;   Character hero(100);



&nbsp;   hero.takeDamage(30);

&nbsp;   hero.heal(20);



&nbsp;   cout << hero.getHealth() << endl;



&nbsp;   return 0;

}



Точка на плоскости и цветная точка



\#include <iostream>

\#include <string>

using namespace std;



struct Point {

&nbsp;   int x;

&nbsp;   int y;

};



class ColoredPoint : public Point {

public:

&nbsp;   string color;



&nbsp;   ColoredPoint(int x, int y, string c) {

&nbsp;       this->x = x;

&nbsp;       this->y = y;

&nbsp;       color = c;

&nbsp;   }

};



int main() {

&nbsp;   ColoredPoint p(3, 4, "red");



&nbsp;   cout << p.x << " " << p.y << " " << p.color << endl;



&nbsp;   return 0;

}



Точка на плоскости 



\#include <iostream>

\#include <string>

using namespace std;



struct Point {

&nbsp;   int x;

&nbsp;   int y;

};



class ColoredPoint : public Point {

public:

&nbsp;   string color;



&nbsp;   ColoredPoint(int x, int y, string c) {

&nbsp;       this->x = x;

&nbsp;       this->y = y;

&nbsp;       color = c;

&nbsp;   }

};



int main() {

&nbsp;   ColoredPoint p(3, 4, "red");



&nbsp;   cout << p.x << " " << p.y << " " << p.color << endl;



&nbsp;   return 0;

}



Человек и сотрудник



\#include <iostream>

\#include <string>

using namespace std;



class Human {

protected:

&nbsp;   string name;

&nbsp;   int age;



public:

&nbsp;   Human(string n, int a) {

&nbsp;       name = n;

&nbsp;       age = a;

&nbsp;   }

};



class Employee : public Human {

private:

&nbsp;   string position;



public:

&nbsp;   Employee(string n, int a, string p) : Human(n, a) {

&nbsp;       position = p;

&nbsp;   }



&nbsp;   void show() {

&nbsp;       cout << name << " " << age << " " << position << endl;

&nbsp;   }

};



int main() {

&nbsp;   Employee e("Ivan", 25, "Engineer");

&nbsp;   e.show();



&nbsp;   return 0;

}






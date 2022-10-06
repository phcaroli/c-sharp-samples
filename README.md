# C#
// Declarando variaveis

int jogada1;
int jogada2;
int jogada3;
int total;

// instaciando o objeto dado usando biblioteca de classes do .net System.Random 

Random dado = new Random();
jogada1 = dado.Next(1,7);
jogada2 = dado.Next(1,7);
jogada3 = dado.Next(1,7);

total = jogada1 + jogada2 + jogada3;

Console.WriteLine("Dado 1 = " + jogada1);
Console.WriteLine("Dado 2 = " + jogada2);
Console.WriteLine("Dato 3 = " + jogada3 + "\n");
Console.WriteLine("Total = " + total + "\n");

// Condição para indicar o bonus por jogada. Se conter 3 numeros iguais, bonus +6 senão, bonus +2.

if ((jogada1 == jogada2) || (jogada2 == jogada3) || (jogada1 == jogada3))
{   
    if ((jogada1 == jogada2) && (jogada2 == jogada3)) 
    {
    Console.WriteLine("You rolled triples! +6 bonus to total!");
    total += 6;
    Console.WriteLine("Total = " + total + "\n");
    }
    else
    {
    Console.WriteLine("You rolled doubles! +2 bonus to total!");
    total += 2;
    Console.WriteLine("Total = " + total + "\n");
    }
}

// Condição para indicar se jogador ganhou ou perdeu de acordo com o valor total.
if (total > 14)
{
    Console.WriteLine("You win!");
}
else 
{
    Console.WriteLine("Sorry, you lose.");
}


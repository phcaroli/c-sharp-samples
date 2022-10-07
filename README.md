# C#

<h2>Exemplos C#</h2>

<p>Jogo de Dados: Usando Random e IF </p>
<div class="highlight highlight-source-shell"><pre> 
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

</div></prev>

<p>Gerador de Números da Megasena: Usando Random e While </p>
<div class="highlight highlight-source-shell"><pre> 

// Gerador de numeros Mega Sena:

int num1;
int num2;
int num3;
int num4;
int num5;
int num6;
int bolao = 0;

while (bolao < 101) {

Random numeros = new Random();
num1 = numeros.Next(1,10);
num2 = numeros.Next(10,21);
num3 = numeros.Next(21,31);
num4 = numeros.Next(3,41);
num5 = numeros.Next(41,51);
num6 = numeros.Next(51,61);

Console.WriteLine("Números: " + num1+ ", " + num2+ ", " + num3+ ", " + num4+ ", " + num5+ ", " + num6+ "\n ");
bolao++;
}

</div></pre>

<p>Criando Matriz Simples </p>
<div class="highlight highlight-source-shell"><pre> 


/*
string[] fraudulentOrderIDs = new string[3];

fraudulentOrderIDs[0] = "A123";
fraudulentOrderIDs[1] = "B456";
fraudulentOrderIDs[2] = "C789";
// fraudulentOrderIDs[3] = "D000";
*/

string[] fraudulentOrderIDs = { "A123", "B456", "C789" };

Console.WriteLine($"First: {fraudulentOrderIDs[0]}");
Console.WriteLine($"Second: {fraudulentOrderIDs[1]}");
Console.WriteLine($"Third: {fraudulentOrderIDs[2]}");

fraudulentOrderIDs[0] = "F000";

Console.WriteLine($"Reassign First: {fraudulentOrderIDs[0]}");

// Verificando tamanho da matriz
Console.WriteLine($"There are {fraudulentOrderIDs.Length} fraudulent orders to process.");
</div></pre>

<p>Criando Matriz e usando função Foreach para Loop </p>
<div class="highlight highlight-source-shell"><pre> 

int[] inventory = { 200, 450, 700, 175, 250 };
int sum = 0;
int bin = 0;

foreach (int items in inventory)
{
    sum += items;
    bin++;
    Console.WriteLine($"Bin {bin} = {items} items (Running total: {sum})");
}
Console.WriteLine($"Total: {sum}");
</div></prev>

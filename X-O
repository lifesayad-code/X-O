using System;

class Program

{

static char[] board = { '1', '2', '3', '4', '5', '6', '7', '8', '9' };

static char currentPlayer = 'X';



static string playerX = " X بازیکن";

static string playerO = "  O بازیکن";







static void Main()

{

    Console.OutputEncoding = System.Text.Encoding.UTF8;



    int moves = 0;



    while (true)

    {

        Console.Clear();

        DrawBoard();



        string name = currentPlayer == 'X' ? playerX : playerO;

        Console.WriteLine($"نوبت شماست {name}:");









        int choice;

        if (!int.TryParse(Console.ReadLine(), out choice))

        {

            Console.WriteLine("لطفا یدونه از اعداد رو انتخاب کنید");

            Console.ReadKey();

            continue;

        }



        if (choice < 1 || choice > 9)

        {

            Console.WriteLine("لطفا عددی بین یک تا نه از اعداد موجود در جدول وارد کنید");

            Console.ReadKey();

            continue;

        }













        if (board[choice - 1] == 'X' || board[choice - 1] == 'O')

        {

            Console.WriteLine("این خونه قبلا پر شده!");

            Console.ReadKey();

            continue;

            }



        board[choice - 1]  = currentPlayer;

        moves++;



        if ( CheckWin() )

            {

            Console.Clear() ;

            DrawBoard() ;



            Console.WriteLine($" {currentPlayer} بازی رو برد!") ;



            break;

             }



        if (moves == 9)

        {

            Console.Clear() ;

              DrawBoard();

              Console.WriteLine("...بازی مساوی شد...") ;

            break ;

                 }



        currentPlayer = (currentPlayer == 'X') ? 'O' : 'X';

        }

        }



static void DrawBoard() 



   { 

    Console.WriteLine($"{board[0]} |  {board[1]} | {board[2] }") ;

    Console.WriteLine("--+---+--");

    Console.WriteLine($"{board[3]} | {board[4]} | {board[5] }") ;

    Console.WriteLine("--+---+--");

    Console.WriteLine($"{board[6]} | {board[7]} | {board[8] }");

    }



static bool CheckWin()

{

    int[,] winPositions =

        {

        {0,1,2} , {3,4,5} , {6,7,8},

        {0,3,6} , {1,4,7} , {2,5,8},

        {0,4,8} , {2,4,6}

    } ;



    for (int i = 0; i < 8; i++)

    {

        if (board[winPositions[i, 0]] == currentPlayer &&

            board[winPositions[i, 1]] == currentPlayer &&

            board[winPositions[i, 2]] == currentPlayer)

        {

            return true;

        }

             }

    return false;

     }

}

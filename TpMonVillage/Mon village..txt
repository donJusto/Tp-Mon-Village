using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace TpMonVillage
{
    class Program
    {
        enum mention { nul, passable, assezBien, bien, excellent, parfait };
        static string[,] tableauQuestion = new string[5, 9];
        static void Main(string[] args)
        {
            Console.Clear();

            drawTriangle();
            drawRectangle();
            drawDoor();
            //Console.Clear();
            pseudo();
            string monVillage = null;
            int score = 0, succes = 0, echec = 0;
            drawPlayArea();
            Console.ReadKey();
        }

        private static void drawPlayArea()
        {
            Console.Clear();
            int ConsoleMilieu = Console.WindowWidth / 2;
            Console.SetCursorPosition(ConsoleMilieu, 2);
            Console.WriteLine("Il s'agit d'un QCM");

         }

        private static void drawTriangle()
        {
            Console.BackgroundColor = ConsoleColor.White;
            //Console.SetWindowPosition(0, 0);
            //Console.WindowWidth = Console.LargestWindowWidth;
            //Console.WindowHeight = Console.LargestWindowHeight;
            int maxWidth = Console.LargestWindowWidth;
            int maxHeight = Console.LargestWindowHeight;
            Console.SetWindowSize(maxWidth, maxHeight);
            int XmilieuEcran = Console.LargestWindowWidth / 2; //Milieu écran moins 1

            Console.SetCursorPosition(XmilieuEcran - 10, 1);
            //Console.ForegroundColor = ConsoleColor.;
            Console.BackgroundColor = ConsoleColor.DarkGray;
            Console.ForegroundColor = ConsoleColor.DarkGray;
            Console.WriteLine("_____/\\____");
            Console.SetCursorPosition(XmilieuEcran - 6, 2);
            Console.WriteLine("/  \\");
            Console.SetCursorPosition(XmilieuEcran - 7, 3);
            Console.WriteLine("/    \\");
            Console.SetCursorPosition(XmilieuEcran - 8, 4);
            Console.WriteLine("/      \\");
            Console.SetCursorPosition(XmilieuEcran - 9, 5);
            Console.WriteLine("/        \\");
            Console.SetCursorPosition(XmilieuEcran - 10, 6);
            Console.WriteLine("/          \\");
            Console.SetCursorPosition(XmilieuEcran- 11, 2);
            Console.WriteLine("/           \\");
            Console.SetCursorPosition(XmilieuEcran - 12, 3);
            Console.WriteLine("/             \\");
            Console.SetCursorPosition(XmilieuEcran - 13, 4);
            Console.WriteLine("/               \\");
            Console.SetCursorPosition(XmilieuEcran - 14, 5);
            Console.WriteLine("/                 \\");
            Console.SetCursorPosition(XmilieuEcran - 15, 6);
            Console.WriteLine("/                   \\");
            Console.SetCursorPosition(XmilieuEcran - 16, 7);
            Console.WriteLine("/                     \\");
            Console.SetCursorPosition(XmilieuEcran - 17, 8);
            Console.WriteLine("/                       \\");
            Console.SetCursorPosition(XmilieuEcran - 18, 9);
            Console.WriteLine("/                         \\");
            Console.SetCursorPosition(XmilieuEcran - 19, 10);
            Console.WriteLine("/                           \\");
            Console.SetCursorPosition(XmilieuEcran - 20, 11);
            Console.WriteLine("/                             \\");
            Console.SetCursorPosition(XmilieuEcran - 21, 12);
            Console.WriteLine("/                               \\");
            Console.SetCursorPosition(XmilieuEcran - 22,13);
            Console.WriteLine("/                                 \\");
            Console.SetCursorPosition(XmilieuEcran - 23, 14);
            Console.WriteLine("/                                   \\");
            Console.SetCursorPosition(XmilieuEcran - 24, 15);
            Console.WriteLine("/                                     \\");
            Console.SetCursorPosition(XmilieuEcran - 25, 16);
            Console.WriteLine("/                                       \\");
            Console.SetCursorPosition(XmilieuEcran - 26, 17);
            Console.WriteLine("/                                         \\");
            Console.SetCursorPosition(XmilieuEcran - 27, 18);
            Console.WriteLine("/                                           \\");
            Console.SetCursorPosition(XmilieuEcran -28, 19);
            Console.WriteLine("/_____________________________________________\\");

        }

        private static void drawRectangle()
        {   
            Console.ForegroundColor = ConsoleColor.DarkRed;
            Console.BackgroundColor = ConsoleColor.DarkRed;
            int XmilieuEcran = Console.WindowWidth / 2; //Milieu écran moins 1
            //Console.SetCursorPosition(XmilieuEcran -28, 19);
            //Console.WriteLine("  _________________  ");
            Console.SetCursorPosition(XmilieuEcran - 26, 20);
            Console.WriteLine("|                                         |");
            Console.SetCursorPosition(XmilieuEcran - 26, 21);
            Console.WriteLine("|                                         |");
            Console.SetCursorPosition(XmilieuEcran - 26, 22);
            Console.WriteLine("|                                         |");
            Console.SetCursorPosition(XmilieuEcran - 26, 23);
            Console.WriteLine("|                                         |");
            Console.SetCursorPosition(XmilieuEcran - 26, 24);
            Console.WriteLine("|                                         |");
            Console.SetCursorPosition(XmilieuEcran - 26, 25);
            Console.WriteLine("|                                         |");
            Console.SetCursorPosition(XmilieuEcran - 26, 26);
            Console.WriteLine("|                                         |");
            Console.SetCursorPosition(XmilieuEcran - 26, 27);
            Console.WriteLine("|             _______________             |");
            Console.SetCursorPosition(XmilieuEcran - 26, 28);
            Console.WriteLine("|             |             |             |");
            Console.SetCursorPosition(XmilieuEcran - 26, 29);
            Console.WriteLine("|             |             |             |");
            Console.SetCursorPosition(XmilieuEcran - 26, 30);
            Console.WriteLine("|             |             |             |");
            Console.SetCursorPosition(XmilieuEcran - 26, 31);
            Console.WriteLine("|_____________|_____________|_____________|");
            Console.ForegroundColor = ConsoleColor.DarkGreen;
            Console.BackgroundColor = ConsoleColor.White;
            Console.SetCursorPosition(XmilieuEcran - 32, 30);
            Console.WriteLine("\\//\\/\\");
            Console.SetCursorPosition(XmilieuEcran + 19, 30);
            Console.WriteLine("\\/\\///");
            Console.SetCursorPosition(XmilieuEcran - 32, 31);
            Console.WriteLine("\\//\\/\\");
            Console.SetCursorPosition(XmilieuEcran + 19, 31);
            Console.WriteLine("\\/\\///");

            Console.SetCursorPosition(XmilieuEcran -26, 32);
           // Console.WriteLine("\\/\\/\\//\\//\\//\\//\\\\//\\\\////\\\\//\\\\\\///\\///");
           // Console.SetCursorPosition(XmilieuEcran -26, 33);
            //Console.WriteLine("\\/\\/\\//\\//\\//\\//\\\\//\\\\////\\\\//\\\\\\///\\///");



        }

        private static void drawDoor()
        {
            Console.BackgroundColor = ConsoleColor.White;
            Console.ForegroundColor = ConsoleColor.White;
            int XmilieuEcran = Console.WindowWidth / 2; //Milieu écran moins 1
            Console.SetCursorPosition(XmilieuEcran - 12, 28);
            Console.WriteLine("|             |");
            Console.SetCursorPosition(XmilieuEcran - 12, 29);
            Console.WriteLine("|           O |");
            Console.SetCursorPosition(XmilieuEcran - 12, 30);
            Console.WriteLine("|             |");
            Console.SetCursorPosition(XmilieuEcran - 12, 31);
            Console.ForegroundColor = ConsoleColor.DarkRed;
            Console.WriteLine("_______________");

           
        }
        private static void pseudo()
        {

            Console.WriteLine("Entrez votre pseudo");
            string pseudo = Console.ReadLine();
            Console.WriteLine(pseudo);

        }
        //Question 1
        
        static void TableauV1()
        {
            ///Avrankou

            tableauQuestion[0, 0] = "Quel est le nom de ton village ?";
            tableauQuestion[1, 0] = "Cotonou";
            tableauQuestion[2, 0] = "Avrankou";
            tableauQuestion[3, 0] = "Porto Novo";
            tableauQuestion[4, 0] = "2";
            //Question 2
            tableauQuestion[0, 1] = "Quel est le nom du chef du village ?"; ;
            tableauQuestion[1, 1] = "Gaspard";
            tableauQuestion[2, 1] = "Amen";
            tableauQuestion[3, 1] = "Zoro";
            tableauQuestion[4, 1] = "3";
            //Question3
            tableauQuestion[0, 2] = "Quel est le nom du Pere,du Fils du chef quartier ?";
            tableauQuestion[1, 2] = "Jesus";
            tableauQuestion[2, 2] = "Pas de nom";
            tableauQuestion[3, 2] = "Samson";
            tableauQuestion[4, 2] = "1";
            //Question4
            tableauQuestion[0, 3] = "Quel est la distance qui sépare cotonou de ton village ?";
            tableauQuestion[1, 3] = "50 Km";
            tableauQuestion[2, 3] = "120 Km";
            tableauQuestion[3, 3] = "43 Km";
            tableauQuestion[4, 3] = "3";
            //Question5
            tableauQuestion[0, 4] = "Quel est la distance qui sépare allada de ton village ?";
            tableauQuestion[1, 4] = "34 Km";
            tableauQuestion[2, 4] = "93 Km";
            tableauQuestion[3, 4] = "99 Km";
            tableauQuestion[4, 4] = "2";

        }
        static void TableauV2()
        {
           //GRAND POPO

            tableauQuestion[0, 0] = "Quel est la distance qui sépare allada de ton village ?";
            tableauQuestion[1, 0] = "'41 Km";
            tableauQuestion[2, 0] = "76 Km";
            tableauQuestion[3, 0] = "90 Km";
            tableauQuestion[4, 0] = "2";
            //Question 2
            tableauQuestion[0, 1] = "Quel est la distance qui sépare AVRANKOU de ton village";
            tableauQuestion[1, 1] = "40 Km";
            tableauQuestion[2, 1] = "5 Km";
            tableauQuestion[3, 1] = "80 Km";
            tableauQuestion[4, 1] = "3";
            //Question3
            tableauQuestion[0, 2] = "Quel est la distance qui sépare KETOU de ton village";
            tableauQuestion[1, 2] = "143 KM";
            tableauQuestion[2, 2] = "230 KM";
            tableauQuestion[3, 2] = "32 KM";
            tableauQuestion[4, 2] = "1";
            //Question4
            tableauQuestion[0, 3] = "Quel est la distance qui sépare LOKOSSA de ton village";
            tableauQuestion[1, 3] = "90 KM";
            tableauQuestion[2, 3] = "123 KM";
            tableauQuestion[3, 3] = "59 KM";
            tableauQuestion[4, 3] = "3";
            //Question5
            tableauQuestion[0, 4] = "Quel est la distance qui sépare GLAZOUE de ton village";
            tableauQuestion[1, 4] = "95 KM";
            tableauQuestion[2, 4] = "65 KM";
            tableauQuestion[3, 4] = "543 KM";
            tableauQuestion[4, 4] = "1";

        }
        static void TableauV3()
        {

            //DJOUGOU
            tableauQuestion[0, 0] = "Quel est la distance qui sépare allada de ton village ?";
            tableauQuestion[1, 0] = "'41 Km";
            tableauQuestion[2, 0] = "396 Km";
            tableauQuestion[3, 0] = "90 Km";
            tableauQuestion[4, 0] = "2";
            //Question 2
            tableauQuestion[0, 1] = "Quel est la distance qui sépare AVRANKOU de ton village";
            tableauQuestion[1, 1] = "40 Km";
            tableauQuestion[2, 1] = "5 Km";
            tableauQuestion[3, 1] = "489 Km";
            tableauQuestion[4, 1] = "3";
            //Question3
            tableauQuestion[0, 2] = "Quel est la distance qui sépare KETOU de ton village";
            tableauQuestion[1, 2] = "393 KM";
            tableauQuestion[2, 2] = "230 KM";
            tableauQuestion[3, 2] = "32 KM";
            tableauQuestion[4, 2] = "1";
            //Question4
            tableauQuestion[0, 3] = "Quel est la distance qui sépare LOKOSSA de ton village";
            tableauQuestion[1, 3] = "98 KM";
            tableauQuestion[2, 3] = "568 KM";
            tableauQuestion[3, 3] = "422 KM";
            tableauQuestion[4, 3] = "3";
            //Question5
            tableauQuestion[0, 4] = "Quel est la distance qui sépare GLAZOUE de ton village";
            tableauQuestion[1, 4] = "249 KM";
            tableauQuestion[2, 4] = "65 KM";
            tableauQuestion[3, 4] = "543 KM";
            tableauQuestion[4, 4] = "1";

        }
        static void TableauV4()
        {

            //DOGBO
            tableauQuestion[0, 0] = "Quel est la distance qui sépare allada de ton village ?";
            tableauQuestion[1, 0] = "'115 Km";
            tableauQuestion[2, 0] = "396 Km";
            tableauQuestion[3, 0] = "90 Km";
            tableauQuestion[4, 0] = "1";
            //Question 2
            tableauQuestion[0, 1] = "Quel est la distance qui sépare AVRANKOU de ton village";
            tableauQuestion[1, 1] = "246 Km";
            tableauQuestion[2, 1] = "245 Km";
            tableauQuestion[3, 1] = "489 Km";
            tableauQuestion[4, 1] = "2";
            //Question3
            tableauQuestion[0, 2] = "Quel est la distance qui sépare KETOU de ton village";
            tableauQuestion[1, 2] = "149 KM";
            tableauQuestion[2, 2] = "230 KM";
            tableauQuestion[3, 2] = "32 KM";
            tableauQuestion[4, 2] = "1";
            //Question4
            tableauQuestion[0, 3] = "Quel est la distance qui sépare LOKOSSA de ton village";
            tableauQuestion[1, 3] = "98 KM";
            tableauQuestion[2, 3] = "20 KM";
            tableauQuestion[3, 3] = "422 KM";
            tableauQuestion[4, 3] = "2";
            //Question5
            tableauQuestion[0, 4] = "Quel est la distance qui sépare GLAZOUE de ton village";
            tableauQuestion[1, 4] = "180 KM";
            tableauQuestion[2, 4] = "65 KM";
            tableauQuestion[3, 4] = "543 KM";
            tableauQuestion[4, 4] = "1";
            

        }
        static void TableauV5()
        {

            //DASSA
            tableauQuestion[0, 0] = "Quel est la distance qui sépare allada de ton village ?";
            tableauQuestion[1, 0] = "'115 Km";
            tableauQuestion[2, 0] = "150 Km";
            tableauQuestion[3, 0] = "90 Km";
            tableauQuestion[4, 0] = "2";
            //Question 2
            tableauQuestion[0, 1] = "Quel est la distance qui sépare AVRANKOU de ton village";
            tableauQuestion[1, 1] = "246 Km";
            tableauQuestion[2, 1] = "243 Km";
            tableauQuestion[3, 1] = "489 Km";
            tableauQuestion[4, 1] = "1";
            //Question3
            tableauQuestion[0, 2] = "Quel est la distance qui sépare KETOU de ton village";
            tableauQuestion[1, 2] = "149 KM";
            tableauQuestion[2, 2] = "230 KM";
            tableauQuestion[3, 2] = "392 KM";
            tableauQuestion[4, 2] = "3";
            //Question4
            tableauQuestion[0, 3] = "Quel est la distance qui sépare LOKOSSA de ton village";
            tableauQuestion[1, 3] = "98 KM";
            tableauQuestion[2, 3] = "176 KM";
            tableauQuestion[3, 3] = "422 KM";
            tableauQuestion[4, 3] = "2";
            //Question5
            tableauQuestion[0, 4] = "Quel est la distance qui sépare GLAZOUE de ton village";
            tableauQuestion[1, 4] = "24 KM";
            tableauQuestion[2, 4] = "65 KM";
            tableauQuestion[3, 4] = "543 KM";
            tableauQuestion[4, 4] = "1";

        }


    }
}



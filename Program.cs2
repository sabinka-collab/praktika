using System;
using System.IO;

class Program
{
    static void Main(string[] args)
    {
        string file = "C:\\Users\\alina\\OneDrive\\Рабочий стол\\2 курс\\системка\\zxy.txt";

        try
        {
            string content;
            using (StreamReader sr = new StreamReader(file))
            {
                content = sr.ReadToEnd();
            }
            int chet = 0;
            int max = 0;
            foreach (char c in content)
            {
                if (c == 'X')
                {
                    chet++;
                }
                else
                {
                    if (chet > max)
                    {
                        max = chet;
                    }
                    chet = 0;
                }
            }
            if (chet > max)
            {
                max = chet;
            }

            Console.WriteLine($"samaya dlinnaya posledovatelnost = {max}");
        }
        catch (Exception ex)
        {
            Console.WriteLine($"Ошибка при чтении файла: {ex.Message}");
        }
    }
}
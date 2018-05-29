# KDZ1
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace TOI
{
    class Program1
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Первый файл");
            byte[] p = File.ReadAllBytes(@"C:\Users\Анастасия\Desktop\TOI.doc");

            int[] t = new int[256];
            for (int i = 0; i < p.Length; i++)
            {
                int count = p[i];
                t[count] += 1;
            }
            FileStream f = new FileStream("dx.txt", FileMode.Create);
            foreach (var a in t)
            {
                Console.WriteLine(a);
            }

            Console.ReadKey();
        }
    }
    
   
}

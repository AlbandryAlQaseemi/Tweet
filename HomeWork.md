
```
using System;
using System.Collections.Generic;
namespace Homework
{
    class Program
    {
        static void Main(string[] args)
        {
            string tweet = "Ramadan Kareem #Twuaiq @bandry #رمضان #programming #DeepCoding @BQ";
            List<string> found = new List<string>();
            foreach (var item in tweet.Split(' '))
            {
                if (item.StartsWith("#") || item.StartsWith("@"))
                {
                    found.Add(item);
                }

            }
            foreach (var item in found)
            {
                Console.WriteLine(item);
            }
            countTweet(found);
        }

        static void countTweet(List<string> arr)
        {
            int count_h = 0;
            int count_m = 0;

            foreach (var item in arr)
            {
                if (item.StartsWith("#"))
                {
                    count_h++;
                }
                else if (item.StartsWith("@"))
                {
                    count_m++;
                }
            }
            Console.WriteLine("Number of hashtags: " + count_h);
            Console.WriteLine("Number of mentions: "+ count_m);
            
        }

    }

}
```

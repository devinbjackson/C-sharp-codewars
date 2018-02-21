# C-sharp-codewars


# Remove the minimum

using System;
using System.Collections.Generic;
using System.Linq;

public class Remover
{
  public static List<int> RemoveSmallest(List<int> numbers)
  {
    if(numbers.Count == 0){
    return new List<int>();
    }
    // Good Luck!
    List<int> sorted = new List<int>(numbers);
    sorted.Sort();
    List<int> noMin = new List<int>(numbers);
    int minIndex = noMin.IndexOf(sorted[0]);
    noMin.RemoveAt(minIndex);
    
    return noMin;
  }
}

#String cleaning

using System;

public class Kata
{
  public static string StringClean(string s)
        {
            string noInts = "";
            for(var i = 0; i < s.Length; i++)
            {
                if (!Char.IsDigit(s[i]))
                {
                    noInts += s[i];
                }
            }
            
            return noInts;
        }
}

#Remove first and last char

using System;

        public class Kata
        {
            public static string Remove_char(string s)
            {    
                if(s.Length == 2){
                return "";
                }
                s = s.Substring(1);
                s = s.Substring(0, s.Length-1);
                return s;
            }
        }
       
#   Enumerable Magic #2 - True for Any?

using System;
using System.Linq;

public class Kata
{
  public static bool Any(int[] arr, Func<int,bool> fun)
  {
    
    for(var i = 0; i < arr.Length; i++){
    if(fun(arr[i])){
      return true;
    }
    }
    return false;
  }
}

# Number of People in the Bus
     
     
using System;
using System.Collections.Generic;

public class Kata
    {
        public static int Number(List<int[]> peopleListInOut)
        {
          var total = 0;
          for(var i = 0; i < peopleListInOut.Count; i++){
            total += peopleListInOut[i][0] - peopleListInOut[i][1];
          }
          return total;
        }
    }

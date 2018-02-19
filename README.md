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

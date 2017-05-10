```c#
using System;
using System.Text;
			
public class Program
{
  public static void Main()
  {
    string text = "Hello World";   
    
    // Encode
    byte[] b1 = Encoding.UTF8.GetBytes(text);
    string encodeText = Convert.ToBase64String(b1);
    
    //-- Decode
    byte[] b2 = Convert.FromBase64String(encodeText);
    string decodeText = Encoding.UTF8.GetString(b2);    
    
    Console.WriteLine("Original text: {0}", text);
    Console.WriteLine("  Encode text: {0}", encodeText);
    Console.WriteLine("  Decode text: {0}", decodeText);    
  }  
}
```

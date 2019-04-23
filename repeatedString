import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the repeatedString function below.
    static long repeatedString(String s, long n) {
        long sizeOfString = (long) s.length();
        long baseAmount = 0;
        long lastSubCount = 0;
        char find = 'a';
        long extraChar = n%sizeOfString;
        if(s.indexOf(find) <0){
            System.out.print("no a's");
            return 0;
        }
        for(int i=0;i<sizeOfString;i++){
            if(s.charAt(i) == find){
                baseAmount++;
                if (i<extraChar)
                    lastSubCount++;
            }
        }
        long subCount = n/s.length();
        long result = baseAmount * subCount + lastSubCount;

        return result;
    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) throws IOException {
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        String s = scanner.nextLine();

        long n = scanner.nextLong();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        long result = repeatedString(s, n);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedWriter.close();

        scanner.close();
    }
}

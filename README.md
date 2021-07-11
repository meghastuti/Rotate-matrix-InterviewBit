import java.util.Arrays;
public class Rotate {
    public static void rotate(int[][] A)
    {
        int N = A.length;
 
        // Transpose 
        for (int i = 0; i < N; i++)
        {
            for (int j = i; j < N; j++)
            {
                int temp = A[i][j];
                A[i][j] = A[j][i];
                A[j][i] = temp;
            }
        }
 
        // swap 
        for (int i = 0; i < N; i++)
        {
            for (int j = 0; j < N / 2; j++)
            {
                int temp = A[i][j];
                A[i][j] = A[i][(N - 1)- j ];
                A[i][N - j - 1] = temp;
            }
        }
    }
 
    public static void main(String[] args)
    {
        int[][] A =
        {
            { 3,1 },
            {4,2 },
            
        };
 
        rotate(A);
 
        for (var r: A) {
            System.out.println(Arrays.toString(r));
        }
    }
}
  

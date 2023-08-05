# SPIRALmatrix
public class Main {
    public static void sss(int matrix[][]){
        int StartRow=0;
        int StartCol=0;
        int EndRow=matrix.length-1;
        int EndCol=matrix[0].length-1;
        for(int j=StartCol;j<=EndCol;j++){
            System.out.println(matrix[StartRow][j]+" ");
        }
        for(int i=StartRow+1;i<=EndRow;i++){
            System.out.println(matrix[i][EndCol]+" ");
        }
        for(int j =EndCol-1;j>=StartCol;j--) {
            if (StartRow == EndRow) {
                break;

            }System.out.println(matrix[EndRow][j] + " ");
        }
        for(int i=EndRow-1;i>=StartRow;i--){

            if(StartCol==EndCol){
                break;
            }

            System.out.println(matrix[i][StartCol]+" ");
        }
        StartCol++;
        StartRow++;
        EndCol--;
        EndRow--;
    }
    public static void main(String[] args) {
        int matrix[][] =  {{1, 2, 3, 4},
                          {5, 6, 7, 8},
                          {9, 10, 11, 12},
                          {13, 14, 15, 16}};
        sss(matrix);
    }
}

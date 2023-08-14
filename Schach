public class Schach {
        public static int row = 8;
        public static int col = 8;
        public static int[][] ma = new int [row][col];
        public static Pad pad = new Pad("Schach");
        public static char figuren[][] = new char [row][col];
        public static boolean matt = false;

        public static void main(String[] args) {
            printBoard();
            startGame();
        
        }

        public static void startGame(){
            setfiguren();

            while(matt == false){
                printfigurenOnBoard();
                matt = true;
            }


        }
    public static void printfigurenOnBoard() {
        for (int i = 0; i < row; i++) {
            for (int j = 0; j < col; j++) {
                if (figuren[i][j] == '\0') {
                    System.out.print("0\t");
                } else {
                    System.out.print(figuren[i][j]+"\t");
                }
            }
            System.out.println();
        }
    }
        public static void setfiguren(){
            //Schwarze Figuren
            figuren[0][0] = 't';
            figuren[0][1] = 'p';
            figuren[0][2] = 'l';
            figuren[0][3] = 'k';
            figuren[0][4] = 'q';
            figuren[0][5] = 'l';
            figuren[0][6] = 'p';
            figuren[0][7] = 't';

            //Schwarzen Bauern
            figuren[1][0] = 'b';
            figuren[1][1] = 'b';
            figuren[1][2] = 'b';
            figuren[1][3] = 'b';
            figuren[1][4] = 'b';
            figuren[1][5] = 'b';
            figuren[1][6] = 'b';
            figuren[1][7] = 'b';
          
            //weise Figuren
            figuren[row-1][0] = 'T';
            figuren[row-1][1] = 'P';
            figuren[row-1][2] = 'L';
            figuren[row-1][3] = 'Q';
            figuren[row-1][4] = 'K';
            figuren[row-1][5] = 'L';
            figuren[row-1][6] = 'P';
            figuren[row-1][7] = 'T';  

            // Weise Bauern
            figuren[row-2][0] = 'B';
            figuren[row-2][1] = 'B';
            figuren[row-2][2] = 'B';
            figuren[row-2][3] = 'B';
            figuren[row-2][4] = 'B';
            figuren[row-2][5] = 'B';
            figuren[row-2][6] = 'B';
            figuren[row-2][7] = 'B';

        }

    public static void printBoard(){  
        fillMatrix();
        printMatrix();
        padSetup();
        padOutput();

    }

    public static void fillMatrix() {
        int num = 0;

        for (int i = 0; i < ma.length; i++) {
            for (int j = 0; j < ma[i].length; j++) {
                if ((i + j) % 2 == 0) {
                    ma[i][j] = 1;
                } else {
                    ma[i][j] = 0;
                } 
            }
        }
    }

    public static void printMatrix() {
        for (int i = 0; i < ma.length; i++) {
            for (int j = 0; j < ma[i].length; j++) {
                System.out.print(ma[i][j]);
            }
            System.out.println();
        }
    }

    public static void padSetup() {
        pad.setPadSize(row*100, col*100);
        pad.setVisible(true);
    }

    public static void padOutput() {
        for (int i = 0; i < ma.length; i++) {
         for (int j = 0; j < ma[i].length; j++) {
            if (ma[i][j] == 1) {
               pad.setColor(Pad.black);
               pad.fillRect(j*100, i*100, 100, 100);
            } else {
               pad.setColor(Pad.white);
               pad.fillRect(j*100, i*100, 100, 100);
            }
            pad.redraw();
         }
      }
    }
}

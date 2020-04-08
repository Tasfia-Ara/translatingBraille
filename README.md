# translatingBraille
This program translated braille characters into english letters.
package com.src;

public class Braille4 {
        static char[][] a = {{'x', 'o'},
                {'o', 'o'},
                {'o', 'o'}};

        static char[][] b = {{'x', 'o'},
                {'x', 'o'},
                {'o', 'o'}};

        static char[][] c = {{'x', 'x'},
                {'o', 'o'},
                {'o', 'o'}};

        static char[][] d = {{'x', 'x'},
                {'o', 'x'},
                {'o', 'o'}};

        static char[][] e = {{'x', 'o'},
                {'o', 'x'},
                {'o', 'o'}};

        static char[][] f = {{'x', 'x'},
                {'x', 'o'},
                {'o', 'o'}};
        static char[][] g = {{'x', 'x'},
                {'x', 'x'},
                {'o', 'o'}};
        static char[][] h = {{'x', 'o'},
                {'x', 'x'},
                {'o', 'o'}};
        static char[][] i = {{'o', 'x'},
                {'x', 'o'},
                {'o', 'o'}};
        static char[][] j = {{'o', 'x'},
                {'x', 'x'},
                {'o', 'o'}};
        static char[][] k = {{'x', 'o'},
                {'o', 'o'},
                {'x', 'o'}};
        static char[][] l = {{'x', 'o'},
                {'x', 'o'},
                {'x', 'o'}};
        static char[][] m = {{'x', 'x'},
                {'o', 'o'},
                {'x', 'o'}};
        static char[][] n = {{'x', 'x'},
                {'o', 'x'},
                {'x', 'o'}};
        static char[][] o = {{'x', 'o'},
                {'o', 'x'},
                {'x', 'o'}};
        static char[][] p = {{'x', 'x'},
                {'x', 'o'},
                {'x', 'o'}};

        static char[][] q = {{'x', 'x'},
                {'x', 'x'},
                {'x', 'o'}};
        private static char[][] r = {{'x', 'o'},
                {'x', 'x'},
                {'x', 'o'}};
        static char[][] s = {{'o', 'x'},
                {'x', 'o'},
                {'x', 'o'}};
        static char[][] t = {{'o', 'x'},
                {'x', 'x'},
                {'x', 'o'}};

        static char[][] u = {{'x', 'o'},
                {'o', 'o'},
                {'x', 'x'}};
        static char[][] v = {{'x', 'o'},
                {'x', 'o'},
                {'x', 'x'}};
        static char[][] w = {{'o', 'x'},
                {'x', 'x'},
                {'o', 'x'}};
        static char[][] x = {{'x', 'x'},
                {'o', 'o'},
                {'x', 'x'}};
        static char[][] y = {{'x', 'x'},
                {'o', 'x'},
                {'x', 'x'}};
        static char[][] z = {{'x', 'o'},
                {'o', 'x'},
                {'x', 'x'}};
        static char[][] space = {{'o', 'o'},{'o','o'},{'o','o'}};

    /**
     * iterates through the given braille to see if the characters match with the characters in the letters
     * @param braille
     * @param letter
     * @return boolean
     */
        public static boolean arraysAreEqual(char[][] braille, char[][] letter){
            for(int i = 0; i<braille.length; i++){
                for(int j = 0; j<braille[0].length; j++){
                    if(braille[i][j] != letter[i][j]){
                        return false;
                    }
                }
            }
            return true;
        }

    /**
     * Translates braille characters into english letters.
     * @param braille
     * @return
     */
    public static char brailleTranslator(char[][]braille){


            //break down the larger braille into a smaller 3x2 matrix
            //store each character in another 2d array

            char[][] smallerMatrix = new char[3][2];
            int col = 0;
            int row = 0;

            smallerMatrix[0][0] = braille[row][col];
            smallerMatrix[1][0] = braille[row+1][col];
            smallerMatrix[2][0] = braille[row+2][col];
            smallerMatrix[0][1] = braille[row][col+1];
            smallerMatrix[1][1] = braille[row+1][col+1];
            smallerMatrix[2][1] = braille[row+2][col+1];

            char let = ' ';
            if(arraysAreEqual(smallerMatrix, a)){
                let = 'a';

            }
            else if(arraysAreEqual(smallerMatrix, b)){
                let = 'b';

            }
            else if(arraysAreEqual(smallerMatrix, c)){
                let = 'c';

            }
            else if(arraysAreEqual(smallerMatrix, d)){
                let = 'd';

            }
            else if(arraysAreEqual(smallerMatrix, e)){
                let = 'e';

            }
            else if(arraysAreEqual(smallerMatrix, f)){
                let = 'f';

            }
            else if(arraysAreEqual(smallerMatrix, g)){
                let = 'g';

            }
            else if(arraysAreEqual(smallerMatrix, h)){
                let = 'h';

            }
            else if(arraysAreEqual(smallerMatrix, i)){
                let = 'i';

            }
            else if(arraysAreEqual(smallerMatrix, j)){
                let = 'j';

            }else if(arraysAreEqual(smallerMatrix, k)){
                let = 'k';

            }else if(arraysAreEqual(smallerMatrix, l)){
                let = 'l';

            }else if(arraysAreEqual(smallerMatrix, m)){
                let = 'm';

            }else if(arraysAreEqual(smallerMatrix, n)){
                let = 'n';

            }else if(arraysAreEqual(smallerMatrix, o)){
                let = 'o';

            }else if(arraysAreEqual(smallerMatrix, p)){
                let = 'p';

            }else if(arraysAreEqual(smallerMatrix, q)){
                let = 'q';

            }else if(arraysAreEqual(smallerMatrix, r)){
                let = 'r';

            }else if(arraysAreEqual(smallerMatrix, s)){
                let = 's';

            }else if(arraysAreEqual(smallerMatrix, t)){
                let = 't';

            }else if(arraysAreEqual(smallerMatrix, u)){
                let = 'u';

            }else if(arraysAreEqual(smallerMatrix, v)){
                let = 'v';

            }else if(arraysAreEqual(smallerMatrix, w)){
                let = 'w';

            }else if(arraysAreEqual(smallerMatrix, x)){
                let = 'x';

            }else if(arraysAreEqual(smallerMatrix, y)){
                let = 'y';
            }
            else if(arraysAreEqual(smallerMatrix, z)){
                let = 'z';
            }
            else{
                let = ' ';
            }
            return let;
        }

    /**
     * splices the large matrix into smaller matrix to put into the brailleTranslator method
     * @param args
     */

    public static void main(String[] args) {
            // use a loop to iterate through every second column, and store that value in a temporary variable.
            // use that variable as a parameter to call the splicedMatrix method
            // splice the matrix , and then use the new matrix as a parameter for the method
            // Read a file, code adapted from https://stackoverflow.com/questions/4716503/reading-a-plain-text-file-in-java

            String allBrailleLinesText = "oxxoxooxoooxoxoooxxoxoooxooxxoooxoxxooxoooxoxoxoxo\n" +
                    "xxxxooxxooxoxoooxxxxoxooooxooxoooxxoooooooxooxoxoo\n" +
                    "oxooooxoooooxoooxoooooooxxxoooooxoooooooooooxoxoxo\n" +
                    "oxoxoxxoxoxooxooxxoxxxoxxoxoxooxooxoxoooxxxoxxxoxoxooxxooxoxxoxxox\n" +
                    "xxxoxxxxoxooxxooxoxoooxxooxxoxxooooxxxoooooxoxxooxxxxoooxxxooxoxxo\n" +
                    "oxooxoooxoxxxoooxoooooxoxxxoooxoooxoxoooooxoxoxxooxoxoooxoooxoxoxo\n" +
                    "xoxoooxxxxooxoxoxooxooxoxxxxoooxxooxoxxoxoxooxoo\n" +
                    "oxxxoooooxoooxooxxxooooooxoxooxxxxxoxooooxxxxooo\n" +
                    "xoooooxoxxooooooxoxoooooxooooooxooooxoxoooxoxooo\n" +
                    "xoxooxooxoxooxxooooxoxoxooxxxooxoxoxxxxx\n" +
                    "xxoxxxooxoooxxoxooxoxxxoooxxoxxxxxxooxxx\n" +
                    "ooxooxooxoooxoooooooxoxoooooooxoxoooxooo\n" +
                    "xxxoxooxxoxooxxoxoooxoxxxxooxxxoxooxxoxooxxoxo\n" +
                    "ooooxxxooxooxooxxxoooooxoxooooooxxxooxooxooxxx\n" +
                    "ooxxxoooxoxxxoooxoooooxoooooooxxxoooxoxxxoooxo\n";

            String[] brailleLines = allBrailleLinesText.split("\n");
            String translatedSentences = "";

            //making a smaller array out of the string
            for(int line=0; line<brailleLines.length; line += 3) {
                char[][] singleSentenceLargeMatrix = new char[3][brailleLines[line].length()];
                for(int j=0; j<brailleLines[line].length(); j++) {
                    singleSentenceLargeMatrix[0][j] = brailleLines[line].charAt(j);
                    singleSentenceLargeMatrix[1][j] = brailleLines[line+1].charAt(j);
                    singleSentenceLargeMatrix[2][j] = brailleLines[line+2].charAt(j);
                }


                char[][] smallerMatrix = new char[3][2];
                String sentence = "";
                for(int col = 0; col < singleSentenceLargeMatrix[0].length-1; col += 2){

                    int smallerCol = 0;
                    for(int row = 0; row < 3; row++) {
                        smallerMatrix[row][smallerCol] = singleSentenceLargeMatrix[row][col];
                        smallerMatrix[row][smallerCol+1] = singleSentenceLargeMatrix[row][col+1];
                    }

                    // smallerMatrix contains a single Braille char
                    char translatedLetter = brailleTranslator(smallerMatrix);
                    sentence += translatedLetter;
                }
                translatedSentences += sentence + "\n";
            }
            System.out.println(translatedSentences);
            //use a new temporary variable to store smallerMatrix and use it as a parameter to call the splicedMatrix method
            //print it out before the loop reiterates
            // smallerMatrix will be restored to its initial value
            //use a loop to assign the value of each element

        }
    }



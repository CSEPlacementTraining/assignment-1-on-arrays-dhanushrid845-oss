class Assignment1 {

    public int[] findLeapYears(int year) {
        int[] leapYears = new int[15];
        int count = 0;

        while (count < 15) {
            if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
                leapYears[count] = year;
                count++;
            }
            year++;
        }

        return leapYears;
    }
}

class Tester {
    public static void main(String[] args) {

        Assignment1 obj = new Assignment1();
        int startYear = 2000;

        int[] result = obj.findLeapYears(startYear);

        for (int year : result) {
            System.out.print(year + " ");
        }
    }
}

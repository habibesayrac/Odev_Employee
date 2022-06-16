# Odev_Employee

public class Employee {
    String name;
    double salary;
    int workHours;
    int hireYear;

    Employee (String name,double salary, int workHours,int hireYear){
        this.name = name;
        this.salary =salary;
        this.workHours = workHours;
        this.hireYear = hireYear;

    }

    public double tax(){

        if (this.salary<1000){

            double tax= this.salary*(0.0);
            return salary;

        }else if (this.salary>=1000){

            double tax= this.salary*(0.03);
            return tax;
        }
        return 0.0;
    }

    public int bonus(){
        if (workHours>40){
            int overTime = this.workHours - 40;
            int bonus = (overTime*30);

            return bonus;
        }
        return 0;
    }

    public double raiseSalary(){
        int farkYil=2021-this.hireYear;
        double zam;

        if ((farkYil)<10){
           zam = this.salary*(0.05);
            return zam;

        }else if ((farkYil)>9 && (farkYil)<20){
           zam = this.salary * (0.10);
            return zam;


        }else if ((farkYil)>=20 ){
            zam= this.salary * (0.15);
           return zam;
        }
        return 0;
    }


    public String toString(){

        double total = salary - tax() + bonus() + raiseSalary();
        double tot = salary + bonus() - tax();

        System.out.println("Adı:  " + this.name);
        System.out.println("Maaşı:  "+ this.salary);
        System.out.println("Çalışma Saati: " + this.workHours);
        System.out.println("Başlangıç Yılı: " + this.hireYear);
        System.out.println("Vergi:  " + tax());
        System.out.println("Bonus: " + bonus());
        System.out.println("Maaş Artışı: " + raiseSalary() );
        System.out.println("Vergi ve Bonuslar ile Birlikte Maaş: " + tot );
        System.out.println("Toplam Maaş: " + total);

       return null;
    }
}

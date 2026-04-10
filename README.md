class Student{
    String name;
    int marks;
    void setdetails(String n,int m){
        name=n;
        marks=m;
    }

    void display(){
        System.out.println("Name:"+name+" ,Marks:"+marks);
    }

    void checkResult(){
        if(marks>=50){
            System.out.println("Result: Pass");
        }
        else{
            System.out.println("Result: Fail");
        }
    }

    void grade(){
        if(marks>=90){
            System.out.println("Grade: A");
        }
        else if(marks>=75 && marks<90){
            System.out.println("Grade: B");
        }
        else if(marks>=50 && marks<75){
            System.out.println("Grade: C");
        }
        else{
            System.out.println("Grade: F");
        }
    }

    void compare(Student other){
        if(this.marks>other.marks){
            System.out.println(this.name+" scored higher than "+other.name);
        }
        else if(this.marks<other.marks){
            System.out.println(other.name+" scored higher than "+this.name);
        }
        else{
            System.out.println("Both scored equal marks");
        }
    }
}
class Main{
    public static void main(String[] args){
        Student s1=new Student();
        Student s2=new Student();
        s1.setdetails("Surya",95);
        s1.display();
        s1.checkResult();
        s1.grade();
        s2.setdetails("Allen",45);
        s2.display();
        s2.checkResult();
        s2.grade();
        s1.compare(s2);
    }

}

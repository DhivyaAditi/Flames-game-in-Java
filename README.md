public class Dcoder
 {
   Dcoder(String S,String K){
    char Name1[]=S.toCharArray();
    char Name2[]=K.toCharArray();
    int c=0;int d=0;
    for(int i=0;i<Name1.length;i++)
    {
      for(int j=0;j<Name2.length;j++)
      {
        if(Name1[i]==Name2[j])
        {
          c++; 
          Name2[j]--;
           break;
        }
        else
        d++;
      }
      continue;
    }
    c=c*2;
    int M=Name1.length+Name2.length;
    int luck_num=M-c;
  if(luck_num==1||luck_num==8||luck_num==9||luck_num==17){
    System.out.print("Sister and brother relationship");
  }
  if(luck_num==2||luck_num==4||luck_num==7){
    System.out.print("Enemy");
  }
  if(luck_num==3||luck_num==5||luck_num==16||luck_num==14||luck_num==18){
    System.out.print("Friends");
  }
  if(luck_num==6||luck_num==10||luck_num==19){
    System.out.print("Love");
  }
  if(luck_num==15||luck_num==11){
    System.out.print("Marraige");
  }
  if(luck_num==12||luck_num==13||luck_num==20){
    System.out.print("Affection");
  }
     }
   
   
   
  
   public static void main(String args[])
   { 
    Scanner sc=new Scanner(System.in);
    System.out.println("Enter your good name:");
    String S=sc.nextLine();
    System.out.println("Enter your partner name:");
    String K=sc.nextLine();
    Dcoder obj=new Dcoder(S,K);
   }
 }

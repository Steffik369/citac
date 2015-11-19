package citac;

public class log {
    private int cislo1 = 0;
    private int cislo2 = 0;
    private int max1 = 5;
    private int max2 = 3;
    
    
    
    ////////////////////////////////////////////////////////////////////////////
    
    public void setMax1(int cislo){
        this.max1 = cislo;
    }
    
    public void setMax2(int cislo){
        this.max2 = cislo; 
    }
    
    public int getCislo1(){
        return this.cislo1;
    }
    
    public int getCislo2(){
        return this.cislo2;
    }
    
    public int getMax1(){
        return this.max1;
    }
    
    public int getMax2(){
        return this.max2;
    }
    
    ////////////////////////////////////////////////////////////////////////////
    
    
    public void inkrementuj(){
        if(cislo1 + 1 <= max1){
            cislo1++;
        }else{
            cislo1 = 0;
            if(cislo2 + 1 <= max2){
                cislo2++;
            }else{
                cislo2 = 0;
            } 
        }
    }
    public void reset(){
        cislo1 = 0;
        cislo2 = 0;
    }
    
    public void tisk(){
        System.out.println("--- " + max2 + " - " + max1 + " ---");
        System.out.println("----- " +cislo2+":"+cislo1+" -----");
    }
    
    
}

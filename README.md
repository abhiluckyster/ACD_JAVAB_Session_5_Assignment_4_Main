# ACD_JAVAB_Session_5_Assignment_4_Main


public class Bank {
	//Parent class attribute-rate
	protected double rate;
	//Parent class constructor 
	public Bank(double rate) {
		this.rate = rate;
	}
	//Parent class Method-getRateOfInterest
	protected void getRateOfInterest()
		{		
		System.out.println("Overriden getRateOfInterest Bank");
		}
}


public class SBI extends Bank {
	//Child class SBI constructor
	public SBI(double rate) {
		super(rate);
	}
	//Child class SBI method-getRateOfInterest
	protected void getRateOfInterest()
	{
		System.out.println("welcome to SBI Bank");
		System.out.println("The rate of interest is "+ rate);
	}
}



public class ICICI extends Bank{
	//Child class ICICI constructor
	public ICICI(double rate) {
		super(rate);
	}
	//Child class ICICI method-getRateOfInterest
	protected void getRateOfInterest()
	{
		System.out.println("welcome to ICICI Bank");
		System.out.println("The rate of interest is "+ rate);		
	}
}



public class Axis extends Bank{
	//Child class Axis constructor
	public Axis(double rate) {
		super(rate);
	}
	//Child class Axis method-getRateOfInterest
	protected void getRateOfInterest()
	{
		System.out.println("welcome to Axis Bank");
		System.out.println("The rate of interest is "+ rate);
	}
}


public class Mainclass {
	public static void main(String[] args) {
		//Create object of SBI and Call constructor to initialize SBI rate
		SBI sb= new SBI(8);	
		//Create object of ICICI and Call constructor to initialize ICICI rate
		ICICI ic=new ICICI(7);
		//Create object of Axis and Call constructor to initialize Axis rate
		Axis ax= new Axis(9);
		//Call child Class-SBI method to override parent class-Bank method "getRateOfInterest"
		sb.getRateOfInterest();
		//Call child Class-ICICI method to override parent class-Bank method "getRateOfInterest"
		ic.getRateOfInterest();
		//Call child Class-Axis method to override parent class-Bank method "getRateOfInterest"
		ax.getRateOfInterest();	
	}
}

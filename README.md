# CIST4B1_AdvJava
A repository to document my Java learning journey

About Me
Hi! I'm Nimisha, a Biomedical Engineering student passionate about the biotechnology sector of healthcare. I aspire to leverage my programming skills, AI experience, and medical background to advance medical innovation.

Goals for This Course
- Strengthen my understanding of advanced Java concepts
- Become proficient in several data structures and their applications
- Learn to code more efficiently and effectively
- Be able to code during technical interviews

In-Class Java Coding Warm Up file
```java
// 2/2/2026 In Class Problem
abstract class Animal {
    String name;
    String foodType;
    public Animal() {
    	name = "John Doe";
    	foodType = "Human Food";
    	}
    public Animal(String name, String foodType) {
    	this.name = name;
    	this.foodType = foodType;
    }
    public abstract String noise();
}

class Panda extends Animal {
    int blackSpotCount;
    int waveCount;
    public Panda(String name, String foodType, int blackSpotCount, int waveCount) {
    	super(name, foodType);
    	this.blackSpotCount = blackSpotCount;
    	this.waveCount = waveCount;
    }
    public Panda() {
    	name = "Po";
    	foodType = "bamboo";
    	}
    public void addWaveCount() {
    	waveCount += 5;
    }
    public void addstain() {
    	blackSpotCount ++;
    }
    public String noise() {
        return "blah";
    }
}

class Tiger extends Animal {
    int stripeCount;
    int teethCount;
    public Tiger(String name, String foodType, int stripeCount, int teethCount) {
    	super(name, foodType);
    	this.stripeCount = stripeCount;
    	this.teethCount = teethCount;
    }
    public void addTeethCount() {
    	teethCount += 5;
    }
    public void addStripe() {
    	stripeCount ++;
    }
    public String noise() {
        return "Rah";
    }
}

public class Zoo {
    public static void main(String[] args) {
        Panda p1 = new Panda("Dodo", "bamboo", 10, 35);
        Tiger t1 = new Tiger("Mufasa", "deer", 15, 50);
        Panda p2 = new Panda();
        Animal[] Zoo1 = {p1, t1, p2};
        
        for (Animal animal:Zoo1) {
        	if (animal instanceof Panda) {
        		Panda newPanda = (Panda) animal;
        		newPanda.addWaveCount();
        		newPanda.addstain();
        		System.out.println("My name is " + newPanda.name + " and I love to eat " 
        		+ newPanda.foodType + ". I will wave to you " + newPanda.waveCount + 
        		" times and you will see me with " + newPanda.blackSpotCount + " black spots");
        		newPanda.noise();
        	}
        	else if (animal instanceof Tiger) {
        		Tiger newTiger = (Tiger) animal;
        		newTiger.addStripe();
        		newTiger.addTeethCount();
        		System.out.println("My name is "+ newTiger.name + " and I love to eat " + 
        		newTiger.foodType + ". I will have " + newTiger.stripeCount + 
        		" stripes and " + newTiger.teethCount+ " teeth count");
        		newTiger.noise();       		
        		}
        }
    }
}
```

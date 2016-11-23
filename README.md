# Oscript
This is a proposed object orient language. Java wouldn't be Java without out its OO paradiam. But one problem with Java is the fact that it is quite verbose. Oscript attempts to remedy this in a similar way how [CoffeeScript](http://coffeescript.org/) tries to make Javascript more Javascript and less like Java syntax. Below shows how a class would be declared in Oscript with its Java quivalent. 

```java
	type Rocket {
    	float fuelVol; 
        String name; 
        public static float consumeRate = 42f;
        
    	(String name) {
        	fuelVol = 0;
            this.name = name;
        }
        
        public:
          setFuel(float num) {
          	if(num > 0)
          		fuel = num;
          }
        
          getName() String return name;
          
          launch() {
          	while(sufficentFuel())
            	fuel -= 42f;
          }
          
          static main(String[] args) {
          	Rocket f9("Falcon 9 v1.2");
            f9.launch();
          }
        private:
        	sufficentFuel() boolean return (fuel-consumeRate) > 0;
        	
    }
```
VS.
```java
    public class Rocket {
    	private float fuelVol;
		private String name;
        public static float consumeRate = 42f;
        	
        public Rocket(String name) {
        	fuelVol = 0;
            this.name = name;
        }
        
        public void setFuel(float num) {
        	if(num > 0)
          		fuel = num;
        } 
        
        public float getName() {
        	return name;
        }
        
        public void launch() {
          	while(sufficentFuel())
            	fuel -= 42f;
        }
        
        public static void main(String[] args) {
        	Rocket f9 = new Rocket("Falcon 9 v1.2");
            f9.launch();
        }
        
        private boolean sufficentFuel() {
        	return (fuel-consumeRate) > 0;
        }
    }
```

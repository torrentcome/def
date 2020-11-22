# Android
## Version & Name

| CodeName | Version | Api level |
| ----- | ------ | ------ |
| R | 11 | API 30 |
| Android10 | 10 | API 29 |
| Pie | 9 | API 28 |
| Oreo | 8 | API 26-27 |
| Nougat | 7 | API 24-25 |

Ideally, the relationship would look more like this in the steady state:
```
minSdkVersion (lowest possible) <= targetSdkVersion == compileSdkVersion (latest SDK)
```
You’ll hit the biggest audience with a low minSdkVersion and look and act the best by targeting and compiling with the latest SDK — a great way to #BuildBetterApps

## Best practice & Writing clean code
#### Nested If's
I hate this, I seriously do, you have statements which require multiple checks like this below code and it goes so deep really deep, In coding which is bad actually.
```java
	if (vehicle != null) {
		if (vehicle.getCar() != null) {
			if (vehicle.getCar().getModel() != null) {
				int price = vehicle.getCar().getModel().getPrice();
			}

		}
	}
```

And the thing is, It can be avoided, you totally can, like this. As you see below one is more readable and easy to understand.
```java
if (vehicle == null || vehicle.getCar() == null || vehicle.getCar().getModel() == null) return;

int price = vehicle.getCar().getModel().getPrice();
```

#### Cognitive complexity
**Definition**: It's a psychological characteristic or psychological variable that indicates how complex or simple is the frame and perceptual skill of a person

In programming a method with nested if else's and larger size causes high cognitive complexity means less understandability.
 
So better to split large methods into logically separated smaller ones and use above **Nested If's** trick to reduce it.
 
Also SonarLint a static code analysis tool calculates this for you in realtime in android studio you can use sonar to see how you doing.

#### Region
Use regions to separate your code fragments in big classes like britisher's did with divide and rule policy, very effective ask indians.
```
//region meaningful name of your logically separated region
do your work here.
//endregion
```

#### Naming
Short names for short living variables and good and meaningful names for long living ones because they'll be with you for a long-long time. They are family.
```
For e.g. index variable within for loop can be 'i' but as class variable should be 'index'
```

#### [Parameter Object pattern](https://refactoring.guru/introduce-parameter-object)
There is no restriction to number of paramters passed in methods but it's a bad practice to pass more than 3 or 4, So if your methods contains a repeating group of parameters which are passed among several methods. We can avoid that by replacing these parameters with an object.

#### No comments
"Code never lies, comments sometimes do." - **Ron Jeffries**
* Always try to explain yourself in code because you're a coder not a commenter.
* Don't add obvious noise.
* Add comments for Public APIs.
* Use it where necessary as time passes by code will change comment wouldn't.
* You're being paid for coding not commenting.

#### Use Abstract classes
Create abstract classes to implement only those callbacks which you need. As `SimpleTabSelectedListener` below, No need to add onTabReselected, onTabUnselected if you don't need it.

```
public abstract class SimpleTabSelectedListener implements TabLayout.OnTabSelectedListener {

	@Override
		public void onTabReselected(TabLayout.Tab tab) {
		}

	@Override
		public void onTabUnselected(TabLayout.Tab tab) {
		}
}
```

## Must follow rules

#### Horizontal and vertical formatting rule
It's not a constraint but a formatting rule that should be followed to keep your code vertically and horizontally small so with just one glance you can read it all.

#### Boy Scout rule
**Definition**: Leave the campground cleaner than you found it

#### Consistency
If you do something in one way then do it the same way everywhere- **Uncle Bob**

#### Keep it simple rule
Keep it simple stupid. Simpler is always better. Reduce complexity as much as possible - **Uncle Bob**

## Must have Android tools

#### Android Lint
Please, guy's, it must/have to be MANDATORY for EVERYBODY. The Android Lint utility is probably one of the most powerful tools in your arsenal that you are not using. I could come up with many reasons why developers don’t seem to take full advantage of it, it's a shame. Lint even say when you have a miss spelling.

#### SonarLint
It's interesting to have,  i have been using it and i got to know about this from a colleague, sometimes they can be helpful, kidding. It has several features best one to just scan the modified classes and it'll automatically criticise you for your bad code and how ugly you can be sometimes. BTW **Cognitive complexity** we talked earlier it helps.

#### FindBugs
It's a program that uses static code analysis to find bugs in java code just like SonarLint. To know more about FindBug check this. Flip a coin or whatever but pick one of these tools.

## Stupid mistakes by Developers

#### Not using parcelable
If you're not using it then you're making a mistake. 

* Parcelable is designed for android.
* Parcelable is faster than serializable interface
* Parcelable interface takes more time for implemetation compared to serializable interface but there are plugins to automate it.
* Serializable interface is easier to implement
* Serializable interface create a lot of temporary objects and cause quite a bit of garbage collection
* Parcelable array can be pass via Intent in android

#### Directly accessing variables
If you're accessing another class variables using dot operator it'll become ugly with time. There is a reason why we have access modifiers keep your variables private and se getters to access those variables.

This'll reduce code coupling. People who code in activity and fragments might know what i'm talking about.

#### Creating too many class variables
If you still remember class as in OOPs concept class represents an entity a noun. A class has attributes which define it's states and methods it's behavior.

I have a totally different understanding from my experience I believe attributes are the real deal and methods they just work on it. So try to keep attributes which are relevant to class and trim those extra global variables(mostly booleans) you added for whatever reason.

Parameter object pattern can be of some help her.

## The coding principles

#### SOLID
It's a mnemonic acronym that helps define the five basic object-oriented design principles

 * Single Responsibility Principle
 * Open-Closed Principle
 * Liskov Substitution Principle
 * Interface Segregation Principle
 * Dependency Inversion Principle

#### DRY principle
Never ever write same piece of code twice make it your ironclad rule and strictly prohibit this in your kingdom.

#### The Critics principle
Okay it's totally made up but it's very logical. When you're reviewing code of your teammates don't be a friend, Be their arch enemy, don't let them make mistakes that you might have to clean someday. Cleaning other's shit will make your hand dirty. Enforce good practices in code reviews.

## Must have Android Libraries

#### [Android Debug Database](https://github.com/amitshekhariitbhu/Android-Debug-Database)

Android Debug Database allows you to view databases and shared preferences directly in your browser in a very simple way.

#### What can Android Debug Database do?
* See all the databases.
* See all the data in the shared preferences used in your application.
* Run any sql query on the given database to update and delete your data.
* Directly edit the database values.
* Directly edit the shared preferences.
* Directly add a row in the database.
* Directly add a key-value in the shared preferences.
* Delete database rows and shared preferences.
* Search in your data.
* Sort data.
* Download database.
* Debug Room inMemory database.

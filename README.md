### Android Interview Questions



### 1. Object-Oriented

- **What is an Object?**

  An object is an instance of a class that has states and behaviors. A Class
  can be defined as a template that describes the behavior/state that the object
  of its type support.

<br>

- **What is the main feature of OOP ?**

    `Encapsulation`, `Polymorphism`, `Inheritance`, `Abstraction`

<br>

- **What is encapsulation?**

  Encapsulation is one of the four fundamental OOP concepts. It is a mechanism of wrapping the data (variables) and code acting on the data (methods) together as a single unit. In encapsulation, the variables of a class will be hidden from other classes, and can be accessed only through the methods of their current class. Therefore, it is also known as *data hiding*. To achieve encapsulation in Java:
    - Declare the variables of a class as private.
    - Provide public setter and getter methods to modify and view the variables values.

  Benefits of Encapsulation:
    - The fields of a class can be made read-only or write-only.
    - A class can have total control over what is stored in its fields.

<br>


- **Difference between abstract and interface?**

  | Interface     | Abstract class     |
  | :------------- | :------------- |
  | Support multiple inheritances | Does not support multiple inheritances |
  | Can extends another interfaces only | Can extends another class and implement multiple interfaces |
  | Does not contain data member | Contains data member |
  | Does not contains constructors | contains constructors  |
  | In Java Contains only incomplete member (signature of member) | Contains both signature (abstract) of method and member functions |
  | Cannot have access modifiers by default and everything is assumed as public | Can has access modifiers for subs, methods and fields |


- **What is Polymorphism?**

  The word polymorphism means having many forms. In simple words, we can define polymorphism as the ability of a message to be displayed in more than one form. In Java polymorphism is mainly divided into two types: compile-time and runtime polymorphism.

- **What is the difference between static and dynamic Polymorphism?**

  *method overloading* represents a *static* form of polymorphism. method overloading means using two or more functions with same name but with the different parameters. Static polymorphism is resolved on compile-time and that is why it's called static. An example of this would be as follow:



  *method overriding* represents a *dynamic* form of polymorphism. It is a process in which a function call to the overridden method is resolved at Runtime. It is also known as *Dynamic Method Dispatch*. dynamic polymorphism is resolved at runtime. An example of this would be as follow:


- **Can Interfaces to be extended?**

  Yes, an interface can extend other interfaces. it supports multiple
  inheritances, which means it can extend more than one interface. But every
  class which wants to use an interface must add it by keyword `implements`
  and using the keyword `extends` for interfaces in classes is illegal and
  cause compile error.

- **What is the difference between overriding and overloading?**

  | Method Overloading      | Method Overriding     |
  | :-------------   | :------------- |
  | Method overloading is a compile time polymorphism.         | Method overriding is a run time polymorphism.       |
  | It help to rise the readability of the program. | While it is used to grant the specific implementation of the method which is already provided by its parent class or super class. |
  | It is occur within the class.	 | 	While it is performed in two classes with inheritance relationship. |
  | Method overloading may or may not require inheritance. | While method overriding always needs inheritance. |
  | In this, methods must have same name and different signature. | While in this, methods must have same name and same signature. |
  | In method overloading, return type can or can not be be same, but we must have to change the parameter. | While in this, return type must be same or co-variant. |

<br>

- **What is the use of the finalize method?**

  `finalize()` method is a protected and non-static method of java.lang.Object
  class. This method will be available in all objects you create in java. This
  method is used to perform some final operations or clean up operations on an
  object before it is removed from the memory. you can override the `finalize()`
  method to keep those operations you want to perform before an object is
  destroyed. Here is the general form of `finalize()` method.


- **What is a static variables in Java?**

  static is a non-access modifier in Java which is applicable for the following:
    - blocks
    - variables
    - methods
    - nested classes

  When a variable is declared as static, then a single copy of variable is created and shared among all objects at class level. Static variables are, essentially, global variables. All instances of the class share the same static variable.


- **Overriding for static method, possible?**

  quick response: no!

  Inheritance comes from object-oriented principles, all of OOP principles needs
  objects to apply on. when we talk about inheritance, it means we deal with some
  objects which have relationships with each other. Besides, "overriding" is a
  feature of OOP principle which is related to run-time polymorphism. The
  implementation to be executed is decided at run-time and the decision is made
  according to the object used for the call.

  On the other hand, static methods belong to the class not object. So we use
  static methods without the need for creating an instance of a class. Besides,
  static methods are resolved in compile-time. Hence the answer is 'NO'.


- **What is an abstract class? Benefits?**

  According to the official document, An abstract class is a class that is declared `abstract`. It may or may not include abstract methods. Abstract classes cannot be instantiated, but they can be subclassed. Also, An abstract method is a method that is declared without an implementation (without braces, and followed by a semicolon), If a class includes abstract methods, then the class itself must be declared `abstract`.
 
  We use abstraction when we want to enforce base functions a have base
  properties. Although we could use an interface for this, sometimes the
  functionality of such classes may overlap or it needs some objects which
  are shared in whole class scope, then we use abstraction.

- **What is an object cloning? can you use clone() method of every object ?**

  Object cloning refers to creation of exact copy of an object. It creates a new instance of the class of current object and initializes all its fields with exactly the contents of the corresponding fields of this object. Every class that implements `clone()` methods should call super.clone() to obtain the cloned object reference. Also it must implement java.lang.Cloneable interface otherwise it will throw CloneNotSupportedException when clone method is called on that class’s object.
  ```java
  protected Object clone() throws CloneNotSupportedException
  ```

- **Multiple inheritances? Possible? How can we do that?**

  Multiple inheritance in Java programming is achieved or implemented using interfaces. Java does not support multiple inheritance using classes. In simple term, a class can inherit only one class and multiple interfaces in a java programs.

- **Object scopes?**

  `public` , `protected` , default (no modifier) , `private`

  | Modifier     | Package     | Subclass     | World     |
  | :------------- | :------------- | :------------- | :------------- |
  | Public       | Yes       | Yes       | Yes       |
  | protected       | Yes      | Yes       | No       |
  | Default (no modifier)       | Yes       | No       | No       |
  | private       | No       | No       | No       |


- **Override private methods, possible?**

  No, a private method cannot be overridden since it is not visible from any other class.

- **why access to the non-static variable is not allowed from static method in Java?**

  because non-static variable are associated with a specific instance of an object while static is not associated with any instance.

- **What is the difference between int and Integer?**

  `int` is a primitive type, while `Integer` is class with a single field of type `int`. Variables of type `int` store the avtual binary value for the integer. Variables of type `Integer` store references to `Integer` objects, just as with any other reference (object) type. The `Integer` class is used where you need an `int` to be treated like any other object, such as in generic types or situations where you need nullability.

- **What are Autoboxing and unboxing?**

  - **Autoboxing:** Converting a primitive value into an object of the corresponding wrapper class is called autoboxing. For example, converting `int` to `Integer` class.
  - **Unboxing:**  Converting an object of a wrapper type to its corresponding primitive value is called unboxing. For example conversion of `Integer` to `int`.

- **What is the difference between initialization and instantiation?**

  - **Instantiation** is when memory is allocated for an object. This is what the `new` keyword is doing. A reference to the object that was created is returned from the `new` keyword.

  - **Initialization** is when values are put into the memory that was allocated. This is what the Constructor of a class does when using the `new` keyword. A variable must also be initialized by having the reference to some object in memory passed to it.


- **How does a static block work?**

  Run once when class is loaded, used for initializing static members.

- **What does the keyword `synchronized` mean?**

  A `synchronized` block in Java is synchronized on some object. All synchronized blocks synchronized on the same object can only have one thread executing inside them at a time. All other threads attempting to enter the synchronized block are blocked until the thread inside the synchronized block exits the block.


- **What is the difference between `==` and `.equal`?**
  - The `equals()` method compares two strings, character by character, to determine equality.
  - The `==` operator checks to see whether two object references refer to the same instance of an object

- **What is the `hashCode()` used for?**

  `hashcode()` returns the hashcode value as an Integer. Hashcode value is mostly used in hashing based collections like HashMap, HashSet, HashTable….etc. According to the official documentation, The general contract of `hashCode()` is:
    - Whenever it is invoked on the same object more than once during an execution of a Java application, the hashCode method must consistently return the same integer, provided no information used in equals comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
    - If two objects are equal according to the equals(Object) method, then calling the hashCode method on each of the two objects must produce the same integer result.

    - It is not required that if two objects are unequal according to the equals(java.lang.Object) method, then calling the hashCode method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hashtables.

- **What is thread-safe mean? How we can make our code thread-safe?**

  Thread safety in java is the process to make our program safe to use in multithreaded environment, there are different ways through which we can make our program thread safe.
    - Synchronization
    - Use of Atomic Wrapper, For example AtomicInteger.
    - Use of locks from java.util.concurrent.locks package.
    - Using thread safe collection classes
    - Using volatile keyword.

  Note that if two threads are both reading and writing to a shared variable, then using the volatile keyword for that is not enough. You need to use a synchronized in that case to guarantee that the reading and writing of the variable is atomic. Reading or writing a volatile variable does not block threads reading or writing. For this to happen you must use the synchronized keyword around critical sections.

- **what is the difference between `throw` and `throws`?**

  Keyword `throw` is used to explicitly throw as an exception in the body of function, while `throws` is utilized to handle checked exceptions for re-intimating the compiler that exceptions are being handled. The throws need to be used in the function’s signature and also while invoking the method that raises checked exceptions.

<br>

### 4. Android

- **What is `Application` class?**

  The `Application` class in Android is the base class within an Android app that contains all other components such as activities and services. The Application class, or any subclass of the Application class, is instantiated before any other class when the process for your application/package is created.

- **Difference between `Activity` and `Service`?**

  - **Activity:** An activity is the entry point for interacting with the user. It represents a single screen with a user interface.

  - **Service:** A service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. It is a component that runs in the background to perform long-running operations or to perform work for remote processes. A service does not provide a user interface.

- **Why do android apps need to ask permission like `INTERNET` or `LOCATION`?**

  The Android platform takes advantage of the Linux user-based protection to identify and isolate app resources called sandbox. This isolates apps from each other and protects apps and the system from malicious apps. If an app needs to use some system resources (like internet, or location sensor,..) or needs to connect other apps (like IAB library), it should request this access. Then android OS give this request and get permission to access the resource. If you want to use system resources, request the permission under the `<uses-permission>` tag in the `android-manifest.xml` file.

- **Differences between `serializable` and `Parcelable`?**

  Serializable is a standard java interface but not a part of the Android SDK. Just by implementating this interface your POJO will be ready to jump from one activity to another. So what's the problem with Serializable? Serializable use reflection during the process and lots of additional temp objects created along the way and it may cause garbage collection to occue more often. That is why the serializable is more than 10x slower than Parcelable.

- **Why `serializable` body is empty? How is it doing?**

  Yes, It's empty because the Java reflection API is performed for marshaling operations (by JVM). This helps identify the Java object's member and behavior but also ends up creating a lot of garbage objects.

- **Which method in `fragment` runs only once?**

  According to the [documentation](https://developer.android.com/guide/components/fragments#Creating), the `onCreate()` method is called once a fragment is created. Within your implementation, you should initialize essential components of the fragment that you want to retain when the fragment is paused or stopped, then resumed.

- **How does the activity respond when orientation is changed?**

  According to the [documentation](https://developer.android.com/guide/topics/resources/runtime-changes), Some device configurations can change during runtime (such as screen orientation, keyboard availability, and when the user enables multi-window mode). When such a change occurs, Android restarts the running `Activity` ( `onDestroy()` is called, followed by `onCreate()`). The restart behavior is designed to help your application adapt to new configurations by automatically reloading your application with alternative resources that match the new device configuration.

- **How to know `configChange` happens in `onDestroy()` function?**

  Once an activity is in the process of finishing then `isFinishing()` method is returned `true` value, otherwise `false` when the system is temporarily destroying the instance of the activity.

- **How to prevent the data from reloading when orientation is changed?**

  The most basic approach would be to use a combination of `ViewModels` and `onSaveInstanceState()`. A `ViewModel` is LifeCycle-Aware. In other words,
  a `ViewModel` will not be destroyed if its owner is destroyed for a
  configuration change (e.g. rotation). The new instance of the owner will
  just re-connected to the existing `ViewModel`. So if you rotate an `Activity`
  three times, you have just created three different `Activity` instances, but
  you only have one `ViewModel`. So the common practice is to store data in the
  `ViewModel` class (since it persists data during configuration changes) and
  use `OnSaveInstanceState()` to store small amounts of UI data.

- **How to handle multiple screen sizes?**

  It's a long debate but in a very nutshell, you can do it in these ways:
    - Use flexible layout like `ConstraintLayout` unless create alternative layout in different layout folders. (e.g. layout-sw480, layout-sw600, layout-sw720 ...)    
    - Provide different bitmap drawables for different screen densities or use vector assets.
    - Be aware of the screen orientation change approach in your application.
      If you don't want to handle it enforce to use just one orientation (portrait or landscape) through declaring it in the manifest file.

 for complete reading, see the [official documentation](https://developer.android.com/training/multiscreen/screensizes).

- **What is the difference between margin and padding?**

   - **Padding** will be space added inside the container, for instance,
    if it is a button, padding will be added inside the button.       

  - **Margin** will be space added outside the container.

- **What is `sw` keyword in `layout-sw600` folder meaning?**

  The `sw` keywrod which stands on "smallest width" is an screen size qualifier that allow you to provide alternative layouts for screens that have a minimum width measured in dp.
  The smallest width qualifier specifies the smallest of the screen's two sides, regardless of the device's current orientation, so it's a simple way to specify the overall screen size available for your layout. Here is some useful values:

    - **320dp:** a typical phone screen (240x320 ldpi, 320x480 mdpi, 480x800 hdpi, etc).
    - **480dp:** a large phone screen ~5" (480x800 mdpi).
    - **600dp:** a 7” tablet (600x1024 mdpi).
    - **720dp:** a 10” tablet (720x1280 mdpi, 800x1280 mdpi, etc).

  Figure below provides a more detailed view of how different screen dp widths generally correspond to different screen sizes and orientations.

  ![](/assets/images/layout-adaptive-breakpoints_2x.png)

- **What is the difference between `sw` and `w` and `h` as postfix in order to define the resources folder?**

    - `sw`: The smallest width qualifier specifies the smallest of the screen's two sides, regardless of the device's current orientation,
    - `w`: The width qualifier specifies the available width. For example, if you have a two-pane layout, you might want to use that whenever the screen provides at least 600dp of width, which might change depending on whether the device is in landscape or portrait orientation. Notice that this qualifier is orientation related.
    - `h`: The height qualifier specifies the available height. This is equivalent to `w` qualifier but is used when the available height is a concern.

  The major difference between these qualifiers is responding to orientation change. The `sw` isn't orientation sensitive but the two others are orientation sensitive. It means that if the screen is 480*800 in dp, then in `sw` always `layout-sw480` folder is loaded but in `w`, for portrait mode, `layout-w480`, and landscape mode, `layout-w800` folder is loaded.

- **What are the major differences between `ListView` and `RecyclerView`?**

  - **ViewHolder Pattern**: `Recyclerview` implements the ViewHolders pattern
    whereas it is not mandatory in a ListView. A `ViewHolder` object stores
    each of the component views inside the tag field of the Layout, so you can
    immediately access them without the need to look them up repeatedly.
    In `ListView`, the code might call `findViewById()` frequently during the
    scrolling of `ListView`, which can slow down performance. Even when the
    `Adapter` returns an inflated view for recycling, you still need to look up
    the elements and update them. A way around repeated use of `findViewById()`
     is to use the "view holder" design pattern.

  - **LayoutManager**: In a `ListView`, the only type of view available is
    the `vertical` ListView. A `RecyclerView` decouples list from its container
    so we can put list items easily at run time in the different containers
    (linearLayout, gridLayout) by setting LayoutManager.

  - **Item Animator**: `ListViews` are lacking in support of good animations,
    but the `RecyclerView` brings a whole new dimension to it.

- **Difference between `Intent` and `IntentService`?**
  - `Service` is the base class for Android services that can be extended to
    create any service. A class that directly extends `Service` runs on the main
    thread so it will block the UI (if there is one) and should therefore either
    be used only for short tasks or should make use of other threads for longer
    tasks.

  - `IntentService` is a subclass of `Service` that handles asynchronous requests
   (expressed as `Intents`) on demand. Clients send requests through
   `startService(Intent)` calls. The service is started as needed, handles each
   `Intent` in turn using a worker thread, and stops itself when it runs out of
   work. [Read More on Mindorks's blog]("https://blog.mindorks.com/service-vs-intentservice-in-android")

- **What is `Fragment`?**

  A `Fragment` is a piece of an activity which enable more modular activity design. A fragment has its layout, its behavior, and its life cycle callbacks. You can add or remove fragments in an activity while the activity is running. You can combine multiple fragments in a single activity to build a multi-pane UI. A fragment can also be used in multiple activities. The fragment life cycle is closely related to its host activity which means when the activity is paused, all the fragments available in the activity will also be stopped.

- **How to pass items to `fragment`?**

  Using `Bundle` you can pass items to the fragment.

- **How would you communicate between two `fragments`?**

  There are several ways to communicate two fragments. Using `interfaces` are a common way to do that. You can connect two fragments through interfaces that are implemented in the parent activity.

- **Difference between adding/replacing `fragment` in `backstack`?**
  - `replace` removes the existing `fragment` and adds a new `fragment`.
    This means when you press back button the fragment that got replaced will
    be created with its onCreateView being invoked.

  - `add` retains the existing fragments and adds a new `fragment` that means
    existing fragment  will be active and they wont be in 'paused' state hence
    when a back button is pressed onCreateView is not called for the existing
    fragment(the fragment which was there before new fragment was added).

    In terms of fragment’s life cycle events `onPause()`, `onResume()`,
    `onCreateView()` and other life cycle events will be invoked in case of
    `replace` but they wont be invoked in case of `add`.

- **What is the difference between `dialog` and `dialogFragment`?**

  THe `dialog` is a small window that prompts the user to make a decision or enter additional information. Instead, `dialogFragment` is a fragment that displays a dialog windows and contains a dialog object.

  DialogFragment does various things to keep the fragment's lifecycle driving it, instead of the Dialog. Dialogs are generally autonomous entities -- they are their own window, receiving their own input events, and often deciding on their own when to disappear. DialogFragment needs to ensure that what is happening with the Fragment and Dialog states remains consistent. To do this, it watches for dismiss events from the dialog and takes care of removing its own state when they happen.

- **What is the difference between `Thread` and `AsyncTask`?**

- **What is the relationship between the life cycle of an `AsyncTask` and an `Activity`? What problems can this result in? How can these problems be avoided?**

  An AsyncTask is not tied to the life cycle of the Activity that contains it.
  So, for example, if you start an AsyncTask inside an Activity and the user
  rotates the device, the Activity will be destroyed (and a new Activity
  instance will be created) but the AsyncTask will not die but instead goes
  on living until it completes.

  Then, when the AsyncTask does complete, rather than updating the UI of the
  new Activity, it updates the former instance of the Activity (i.e., the one
  in which it was created but that is not displayed anymore!). This can lead to
  an Exception (of the type java.lang.IllegalArgumentException: View not attached
  to window manager if you use, for instance, findViewById to retrieve a view
  inside the Activity).

  There’s also the potential for this to result in a memory leak since the
  AsyncTask maintains a reference to the Activity, which prevents the Activity
  from being garbage collected as long as the AsyncTask remains alive.

  For these reasons, using AsyncTasks for long-running background tasks is
  generally a bad idea . Rather, for long-running background tasks, a different
  mechanism (such as a service) should be employed.

- **What is `Lopper` and how it works?**
- **What are Handlers?**

    Handlers are objects for managing threads. It receives messages and writes
    code on how to handle the message. They run outside of the activity’s
    lifecycle, so they need to be cleaned up properly or else you will have
    thread leaks. Handlers allow communicating between the background thread
    and the main thread.

- **What is the difference between `Foreground` and `Background` and `Bounded` service?**
  - __Foreground Service:__ A foreground `service` performs some operation that
  is noticeable to the user. For example, we can use a foreground service to
  play an audio track. A `Notification` must be displayed to the user.

  - __Background Service:__ A background `service` performs an operation that
  isn’t directly noticed by the user. In Android API level 26 and above, there
  are restrictions to using background services and it is recommended to use
  WorkManager in these cases

  - __Bound Service:__ A `service` is bound when an application component binds
  to it by calling `bindService()`. A bound service offers a client-server
  interface that allows components to interact with the `service`, send requests,
  receive results. A bound service runs only as long as another application
  component is bound to it. [Read More](https://developer.android.com/guide/components/services)

- **What are the limitations of using `Services` in android 8 and higher?**
- **What is `JobScheduling`?**
- **What is `contentProvider` and what is typically used for?**

  A `ContentProvider` provides data from one application to another, when
  requested. It manages access to a structured set of data. It provides mechanisms for defining data security. [Learn more]("https://medium.com/@sanjeevy133/an-idiots-guide-to-android-content-providers-part-1-970cba5d7b42" "An idiot guide to android content providers").
  For further reading see the [official android documentation]("https://developer.android.com/guide/topics/providers/content-provider-basics" "Android official documentation")

  ![Conent Provider diagram](/assets/images/content-provider-diagram.png)

- **What is the difference between `apply()` and `commit()` in `sharedPreferences`?**
  - `commit()` writes the data **synchronously** and returns a boolean value of
    success or failure depending on the result immediately.

  - `apply()` is **asynchronous** and it won’t return any boolean response. Also
    if there is an `apply()` outstanding and we perform another `commit()`,
    The `commit()` will be blocked until the `apply()` is not completed.

- **How you load your `Bitmaps`? What do you do for loading large bitmaps?**
[Loading Large Bitmaps Efficiently in Android](https://android.jlelse.eu/loading-large-bitmaps-efficiently-in-android-66826cd4ad53 "Loading Large Bitmaps Efficiently in Android")

- **How Android apps compiled and run?**
  1. First step involves compiling the resources folder (/res) using the aapt
    (android asset packaging tool) tool. These are compiled to a single class
    file called R.java. This is a class that just contains constants.

  2. Second step involves the java source code being compiled to .class files
    by javac, and then the class files are converted to Dalvik bytecode by the
    “dx” tool, which is included in the sdk ‘tools’. The output is classes.dex.

  3. The final step involves the android apkbuilder which takes all the input
    and builds the apk (android packaging key) file.

- **Do you know any about how `Dalvik` is working?**
- **What are the benefits of `ART` in comparison to `Dalvik`?**
- **What is `AAPT` ?**
- **What is Doze mode?**

<br>

### 5. Architecture And Coding

- **What is MVVM stands for?**

- **What are the differences between MVP and MVVM?**
- **Explain SOLID programming principle?**
- **What is Dependency Inversion?**
- **What is Dependency Injection?**
- **What is repository pattern?**
- **What is android clean architecture?**


<br>

### 6. Tools and libraries

- **What is android DataBinding?**

- **Explain `scope` concept in dagger2**
- **What is marble diagram?**
- **Explain different types of Observables**
- **How to implement instant search with RxJava?**


<br>

### 7. Gradle

- **What is buildType?**

- **What do you do if you want to publish different versions of an APK with the same codabase?**

    *using product flavor.* [What is flavor?]("https://android.jlelse.eu/product-flavors-for-android-library-d3b2d240fca2")

- **How to add a dependency only on a certain build of the app?**

  Flavor dependency. What? don't worry, [read this link]("https://developer.android.com/studio/build/dependencies#dependency-configurations")

- **What is the difference between `implementation` and `api`?**

  These two keywords work the same when you want to add a new library but the main difference occurs when using it in the internal library. Let's explain it with an example. Consider your app has a library called 'libraryA'. This library is also dependant on another library called 'libraryB'. the dependency flow will be : `app -> libraryA -> libraryB` . If the libraryB is declared in libraryA with keyword `implementation`, so your app module does not know anything about the classes of libraryB. So you can't access and use any classes of libraryB. If you want to do that, you must declare libraryB in the libraryA Gradle file with keyword `api`. For more information read [this medium link]("https://medium.com/mindorks/implementation-vs-api-in-gradle-3-0-494c817a6fa").


- **What do you mean by Gradle wrapper?**

  The Gradle wrapper is the most suitable way to initiate a Gradle build. A Gradle wrapper is a Window’s batch script which has a shell script for the OS (operating system). Once you start the Gradle build via the wrapper, you will see an auto download which runs the build.

<br>

### 8. Design patterns

- **When to use Adapter pattern? (Not for RecyclerView or ListView)**

  Use Adapter pattern when you need to make two class work with incompatible interfaces. Adapter pattern can also be used to encapsulate third party code so that your application only depends upon Adapter, which can adapt itself when third party code changes or you moved to a different third party library.

- **In singleton pattern whether it is better to make the whole `getInstance()` method synchronized or just critical section is enough? Which one is preferable?**

  Synchronization of whole `getInstance()` method is costly and is only needed during the initialization on singleton instance, to stop creating another instance of Singleton.  Therefore it is better to only synchronize critical section and not the whole method.


- **What are the drawbacks of using singleton design pattern?**

  - **Testability issue:** The bad thing with singletons is that the
  `getInstance()` method is globally accessible. That means that you usually
  call it from within a class, instead of depending on an interface you can
  later mock. That's why it's impossible to replace it when you want to test
  the method or the class.

  - **Tight Coupling:** The singleton object is exposed globally and is
  available to a whole application. Thus, classes using this object become
  tightly coupled. So any change in the global object will impact all other
  classes using it.

  - **Violation issues:** Singleton principle can be violated by techniques such
  as cloning. If an application is running on multiple JVM’s, then, in this case,
  Singleton might be broken.

- **How can you prevent creating another instance of singleton using `clone()` method?**

  The preferred way to prevent creating another instance of a singleton is by not implementing Cloneable interface and if you do just throw an exception from `clone()` method "_not to create a clone of singleton class_".

- **When will you prefer to use a Factory Pattern?**

  The factory pattern is preferred in the following cases:
    - A class does not know which class of objects it must create

    - Factory pattern can be used where we need to create an object of any one of sub-classes depending on the data provided

    - you can use factory pattern where you have to create an object of any one of sub-classes depending on the given data



2. #### Which Android Libraries are you familiar with?

   * Android Jetpack
   * Retrofit2
   * RxJava / RxAndroid
   * Dagger2
   * Timber
   * Koin
   * Picasso / Glide
   * Gson

3. #### What is an **ORM**?

   * Object-relational mapping is a technique (a.k.a. design pattern) of accessing a relational database from an object-oriented language

4. #### Which **ORMs** are you familiar with?

   * Room
   * DBFlow
   * OrmLite
   * Realm

5. #### What is RxJava / RxAndroid?

   * A library for reactive programming
   * Works like wireframe between different layers and creates pipelines of data

6. #### What is the difference between `FlatMap`, `SwitchMap`, `ConcatMap` in RxJava?

7. #### Have you used Mockito?

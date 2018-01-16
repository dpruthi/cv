---
layout: page
title: Daily Dairy
date: 2017-06-19 16:31
author: tacitusdeep
comments: true
categories: []
---
<h2></h2>
<h2><span style="text-decoration:underline;color:#00ccff;">DD(6 months Industrial Training)</span></h2>
<h2><span style="text-decoration:underline;color:#00ccff;">June, 2017</span></h2>
I am doing six months training at<strong> Auribises Technologies Pvt Ltd</strong>, Ludhiana.

Whatever I am doing in the training, I briefly explaining here as Daily diary

<strong>First week: From 5th June, 2017 to 9th June, 2017</strong>
<h3 class="entry-title">DAY 1 (5/6/17)</h3>
On the first day I came to know about the company rules and regulations and the staff members give me introduction about the company like in which of the fields they are working on.

After that, my teacher introduced me to the Course Contents of my Training like what are the modules on which i will be working on.
<h3 class="entry-title">DAY 2 (6/6/17)</h3>
<h4>History of JAVA</h4>
Java language project initially started in June 1991 by James Gosling, Mike Sheridan, and Patrick Naughton. An oak tree stood outside Gosling’s office at that time and java named as oak initially. It later renamed as Green and was later renamed as java from java coffee.

<strong>A brief description of OOPS(Object-oriented programming style) &amp; JAVA</strong>

Java is a widely used programming language designed for use in the distributed environment of the internet. It is a popular language for Android applications.
Java programs are found in desktops, servers, mobile devices, smart cards and Blu-ray Discs (BD).
<h4>Features of java -</h4>
<ul>
	<li>Platform Independent: Write once, run anywhere (WORA)</li>
	<li>Object-Oriented</li>
	<li>Robust</li>
	<li>Secure</li>
	<li>Distributed</li>
	<li>Portable</li>
	<li>Architecture neural</li>
	<li>Multithreading</li>
</ul>
<h3 class="entry-title">DAY 3 (7/6/17)</h3>
<h4>Installing Java Development Kit (JDK)</h4>
JDK can be downloaded from http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
<h4>Installing Eclipse(IDE) &amp; Setting Path of JDK</h4>
Eclipse can be download from https://www.eclipse.org/downloads/?
<h4>First Syntax of JAVA using Eclipse IDE</h4>
FILE NAME : first.java
INPUT :

public class first {
public static void main(String[] args) {
System.out.println(“ My first java program :) ”);
}
}

OUTPUT :

My first java program :)
<h4>Operators, Conditional Statements, Loops.</h4>
Learnt about different types of operators (arithmetic, shift, conditional, bitwise, logical, increment and decrement ), conditional statements (if else, switch), loops (while, do while, for) and where they can be used in software.

Also practice it and implement to see how they works.
<h3 class="entry-title">DAY 12 (20/6/17)</h3>
<h4>Exception Handling</h4>
The <b>exception handling in java</b> is one of the <i>mechanism to handle the runtime errors</i> so that normal flow of the application can be maintained.
<h4 class="h2">Types of Exception</h4>
<ol>
	<li>Checked Exception</li>
	<li>Unchecked Exception</li>
	<li>Error</li>
</ol>
<h4 class="h2">Java Exception Handling Keywords</h4>
There are 5 keywords used in java exception handling.
<ol>
	<li>try ( try block must be followed by either catch or finally block)</li>
	<li>catch ( It is used to handle the Exception and must be used after the try block only)</li>
	<li>finally ( finally block is always executed whether exception is handled or not and follows try or catch block)</li>
	<li>throw ( throw keyword is used to explicitly throw an exception. Thrown by developer itself)</li>
	<li>throws ( )</li>
</ol>
Example code  -
<pre>/**
 * Created by deep on 20/6/17.
 */


public class Excp {
    public static void main(String[] args) {

        System.out.println("-----Main Started-----");

        int arr[] = {10, 30, 50, 40};
        //System.out.println( arr[20] );//exception


        int a = 10;
        int b = 0 ;


        try {

            int c = a/b;

        }catch (Exception e) {

            System.out.println("Some Exception :"+e);

        }


       try {

            System.out.println(arr[20]);


        } catch (ArrayIndexOutOfBoundsException ae) {

            System.out.println("Some Exception : "+ae);

        }


        finally{

            System.out.println("This must be Executed");//
        }

        System.out.println("-----Main Finished-----");
    }
}

</pre>
Output -

-----Main Started-----
Some Exception :java.lang.ArithmeticException: / by zero
Some Exception : java.lang.ArrayIndexOutOfBoundsException: 20
This must be Executed
-----Main Finished-----
<h3 class="entry-title">DAY 13 (21/6/17)</h3>
<h4>File Handling</h4>
Java uses the concept of stream to make I/O operation fast. The java.io package contains all the classes required for input and output operations.

We can perform <strong>file handling in java</strong> by Java I/O API.
<h4 class="h2">Stream(flow of data)</h4>
A stream is a sequence of data.In Java a stream is composed of bytes. It's called a stream because it is like a stream of water that continues to flow.

Binary data is write and read by:
<ul>
	<li> Output Stream (write)</li>
	<li> Input Stream(read)</li>
</ul>
Textual data is write and read by:
<ul>
	<li>Writer</li>
	<li>Reader</li>
</ul>
<h4>Keypoints:</h4>
<ul>
	<li>Java File API throw checked exception.</li>
	<li>File is file also directory is file in java file handling.</li>
</ul>
Example code -
<pre>package com.pratice;

import java.io.*;
import java.nio.file.Files;
import java.nio.file.FileSystems;
import java.nio.file.Path;
import java.nio.file.StandardCopyOption;


/**
 * Created by deep on 22/6/17.
 */

public class copyFile {

    void readFromFile() {

        FileReader reader = null;
        BufferedReader buffer = null;
        File file = null;

        try {
            file = new File("/home/deep/Desktop/demo.txt");
            reader = new FileReader(file);
            buffer = new BufferedReader(reader);
            String line = "";
            while ((line = buffer.readLine()) != null) {
                System.out.println(line);
            }

        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                reader.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }

    void writeIntoFile() {

        FileWriter writer = null;
        File file = null;


        try {
            file = new File("/home/deep/Desktop/demo.txt");
            writer = new FileWriter(file);
            String ftext = "This is text of demo.txt file";
            writer.write(ftext);
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                writer.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }


    //copy data from one file to another
    void copyFromota() {

        FileInputStream instream = null;
        FileOutputStream outstream = null;
        File infile = null;
        File outfile = null;

        try {

            infile = new File("/home/deep/Desktop/demo.txt");
            outfile = new File("/home/deep/Desktop/demo2.txt");

            instream = new FileInputStream(infile);
            outstream = new FileOutputStream(outfile);

            byte[] buffer = new byte[1024];

            int length;
           /*copying the contents from input stream to
            * output stream using read and write methods
            */
            while ((length = instream.read(buffer)) &gt; 0) {
                outstream.write(buffer, 0, length);
            }

            System.out.println("data of file demo.txt copied to demo2.txt file successfully!!");

        } catch (IOException ioe) {
            ioe.printStackTrace();
        } finally {
            //Closing the input/output file streams
            try {
                instream.close();
                outstream.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }

    }


    public static void main(String[] args)

    {
        try {

            File file1 = new File("/home/deep/Desktop/demo.txt");
            File file2 = new File("/home/deep/Desktop/demo2.txt");

            file1.createNewFile();
            System.out.println("demo file created!!");
            file2.createNewFile();//file created
            System.out.println("empty demo2 file created!!");

        } catch (Exception e) {
            System.out.println(e);
        }
        copyFile fref = new copyFile();
        fref.writeIntoFile();//writing into file
        System.out.println();
        fref.readFromFile();//read from file
        System.out.println();
        fref.copyFromota();//copy demo file data to demo2 file

        System.out.println();

        File file = new File("/home/deep/Desktop/Demodir");
        file.mkdir();//Demodir created
        System.out.println("empty Demodir created!!");

        Path movefrom = FileSystems.getDefault().getPath("/home/deep/Desktop/demo2.txt");
        Path target = FileSystems.getDefault().getPath("/home/deep/Desktop/Demodir/demo2.txt");
        Path target_dir = FileSystems.getDefault().getPath("/home/deep/Desktop/Demodir");
try {

    Files.move(movefrom, target, StandardCopyOption.REPLACE_EXISTING);
    System.out.println();
    System.out.println("demo2.txt moved to directory Demodir...!");
}catch (Exception e){
    System.out.println(e);
      }
        
    }
}</pre>
Output -
demo file created!!
empty demo2 file created!!

This is text of demo.txt file

data of file demo.txt copied to demo2.txt file successfully!!

empty Demodir created!!

demo2.txt moved to directory Demodir...!

Process finished with exit code 0

&nbsp;
<h3 class="entry-title">(26/7/17)  -   (30/7/17)</h3>
<h4>COLLECTION CLASSES :</h4>
Java provides a set of standard collection classes that implement Collection interfaces.

The standard collection classes are:
<ul>
	<li>LIST : ARRAYLIST, VECTOR</li>
	<li>SET : HASH SET, TREE SET</li>
	<li>QUEUE</li>
	<li>MAP</li>
	<li>HASH TABLE</li>
</ul>
&nbsp;
<pre>import java.util.ArrayList;
import java.util.Collections;
import java.util.Enumeration;
import java.util.HashMap;
import java.util.HashSet;
import java.util.Hashtable;
import java.util.Iterator;
import java.util.List;
import java.util.ListIterator;
import java.util.Map;
import java.util.PriorityQueue;
import java.util.Set;
import java.util.TreeSet;
import java.util.Vector;

public class CollectionsDemo {

void listDemo(){
 
//List list = new ArrayList(); // Polymorphic Statement
 
// Raw Type
ArrayList list1 = new ArrayList(); // Direct Object Construction
 
// Generic Type
ArrayList&lt;String&gt; list2 = new ArrayList&lt;String&gt;();
 
ArrayList&lt;Student&gt; list3 = new ArrayList&lt;Student&gt;();
 
// Adding data to the list
//list1.add(0,"John"); //0
list1.add("John"); //0
list1.add("Jennie");
list1.add("Jack");
list1.add(100); // list1.add(new Integer(100));
list1.add(2.2); // list1.add(new Double(100));
Student s = new Student(101,"George");
CollectionsDemo cdRef = new CollectionsDemo();
 
list1.add(s);
list1.add(cdRef);
list1.add("Jennie"); //n-1
 
// listing the data
System.out.println(list1);
 
// Read the element
System.out.println(list1.get(4));
 
// delete the element
list1.remove(0);
 
// update the data
list1.set(0, "Jennie JJ");
System.out.println(list1);
 
list2.add("John");
list2.add("Jennie");
list2.add("Jack");
list2.add("Jim");
list2.add("Joe");
//list2.add(10); err
//list2.add(2.2); err
 
Student s1 = new Student(101,"Ben");
Student s2 = new Student(101,"Fionna");
Student s3 = new Student(101,"George");
 
list3.add(s1);
list3.add(s2);
list3.add(s3);
//list3.add(10); err
//list3.add(2.2); err
 
// Read the entire list.
//1. For Loop
System.out.println("----------For Loop----------");
for(int i=0;i&lt;list2.size();i++){
String nm = list2.get(i);
System.out.println(nm);
}
 
//2. Enhanced For Loop
System.out.println("----------Enhanced For Loop----------");
for(String str : list2){
System.out.println(str);
} 
 
System.out.println("----------Enhanced For Loop Student----------");
for(Student stu : list3){
System.out.println(stu);
} 
 
System.out.println("----------Enhanced For Loop Raw Type----------");
for(Object o : list1){
System.out.println(o);
} 
 
//3. Iterator | Design Pattern
System.out.println("----------Iterator----------");
Iterator&lt;String&gt; itr1 = list2.iterator();
while(itr1.hasNext()){
String nm = itr1.next();
System.out.println(nm);
 
//if(nm.equals("Jim"))
// itr1.remove();
}
 
//4. Iterator | Design Pattern
System.out.println("----------ListIterator----------");
ListIterator&lt;String&gt; itr2 = list2.listIterator();
while(itr2.hasNext()){ //itr2.hasPrevious()
String nm = itr2.next(); //itr2.previous()
System.out.println(nm);
 
//if(nm.equals("Jim"))
// itr2.remove();
} 
System.out.println("----------ListIterator navigating back----------");
while(itr2.hasPrevious()){ //itr2.hasPrevious()
String nm = itr2.previous(); //itr2.previous()
System.out.println(nm);
 
//if(nm.equals("Jim"))
// itr2.remove();
} 
 
//2.Enumerations
System.out.println("----------Enumeration----------");
Enumeration&lt;String&gt; eRef = Collections.enumeration(list2);
while(eRef.hasMoreElements()){
String nm = eRef.nextElement();
System.out.println(nm);
}
 
list2.add("John");
System.out.println(list2);
 
// Methods
System.out.println(list2.size());
if(list2.contains("John"))
System.out.println("John is in the list");
 
int idx = list2.lastIndexOf("John");//list2.indexOf("John");
System.out.println(idx);
//list2.clear(); -&gt; remove all
 
ArrayList&lt;String&gt; list4 = new ArrayList&lt;String&gt;();
list4.add("Ben");
list4.add("Harry");
list4.add("George");
System.out.println("****************");
System.out.println(list2);
System.out.println(list4);
 
list2.addAll(list4);
System.out.println(list2);
 
list2.addAll(list1);
System.out.println(list2);
 
Object oRef = list2.get(13);
Student sRef = (Student)oRef;
System.out.println(sRef);
 
// THREAD SAFE OR SYNCHORNIZED
//Vector vector = new Vector(); // Raw Type
Vector&lt;String&gt; vector = new Vector&lt;String&gt;(); // Generic type
vector.add("Ben");
vector.add("Harry");
vector.add("George");
 
System.out.println(vector);
System.out.println(vector.get(1));
 
 
for(String str : vector){
System.out.println(str);
}
 
Iterator&lt;String&gt; itr3 = vector.iterator();
}
 
void setDemo(){
 
// Polymorphic Statement
//Set&lt;String&gt; set = new HashSet&lt;String&gt;();
 
// Direct Statement
//HashSet&lt;String&gt; set1 = new HashSet&lt;String&gt;(); // Generic
TreeSet&lt;String&gt; set1 = new TreeSet&lt;String&gt;(); // Generic
//HashSet set2 = new HashSet(); // Raw

set1.add("John");
set1.add("Jennie");
set1.add("Jack");
set1.add("Jim");
set1.add("Jennie");
set1.add("Joe");
 
System.out.println(set1);
 
// Iterate in a set
Iterator&lt;String&gt; itr = set1.iterator();
while(itr.hasNext()){
String nm = itr.next();
System.out.println(nm);
}
 
//set1.remove("John");
//set1.clear();
//set1.addAll(set2);
 
if(set1.contains("Jennie")){
System.out.println("Jennie is in the set");
}
}
 
void queueDemo(){
 
PriorityQueue&lt;Integer&gt; pq = new PriorityQueue&lt;Integer&gt;();
for(int i=10;i&gt;0;i--){
pq.add(i);
}
System.out.println(pq);
//System.out.println(pq.peek());
//System.out.println(pq.peek());
System.out.println(pq.poll());
System.out.println(pq.poll());
System.out.println(pq.poll());
System.out.println(pq);
}
 
void mapDemo(){
//Map&lt;Integer, String&gt; map = new HashMap&lt;Integer, String&gt;();
HashMap&lt;Integer, String&gt; map1 = new HashMap&lt;Integer, String&gt;();
HashMap map2 = new HashMap();
 
map1.put(101, "John");
map1.put(301, "Jennie");
map1.put(141, "Jack");
map1.put(178, "Jim");
map1.put(238, null);
 
map1.put(301, "Ben"); // We are updating the key 301
map1.put(null, null);
 
map1.put(null, "Joe");
 
System.out.println(map1);
System.out.println(map1.size());
System.out.println(map1.get(301));
 
//map1.clear();
 
// Iterate
// Extract all the keys
Set&lt;Integer&gt; set = map1.keySet();
Iterator&lt;Integer&gt; itr = set.iterator();
while(itr.hasNext()){
Integer key = itr.next();
String value = map1.get(key);
System.out.println(key+" - "+value);
}
 
// THREAD SAFE OR SYCHRONIZED
// ACCEPTS NO NULL KEY OR NULL VALUE
Hashtable&lt;Integer, String&gt; table = new Hashtable&lt;Integer, String&gt;();
}
 
public static void main(String[] args) {
 
CollectionsDemo cd = new CollectionsDemo();
//cd.listDemo();
//cd.setDemo();
//cd.queueDemo();
cd.mapDemo();
}

}</pre>
&nbsp;

&nbsp;
<h4>MULTITHREADING :</h4>
<b>Multithreading in java</b> is a process of executing multiple threads simultaneously.
Thread is basically a lightweight sub-process, a smallest unit of processing.
There is one main thread and any number of child threads in a process.
Main Thread handles many jobs and the job which consumes a lot of time is assigned to Child Thread. One Child Thread can also handle any number of jobs.
Main Thread does each and every job sequencially, that is why multithreading is used,jobs are performed parallelly.

Jobs in main thread are written in main method.

&nbsp;
<h4>THREAD METHODS :</h4>
We have various methods which can be called on Thread class object. These methods are very useful when writing a multithreaded application.

<img class="alignnone size-full wp-image-883" src="https://birjotsingh17.files.wordpress.com/2017/07/blog14.png?w=1000" alt="BLOG14" />

&nbsp;
<h4>SYNCHRONISATION :</h4>
Synchronization in java is the capability <em>to control the access of multiple threads to any shared resource</em>.
Java Synchronization is better option where we want to allow only one thread to access the shared resource.
<h4></h4>
<h4>AWT :</h4>
Java AWT (Abstract Window Toolkit) is <em>an API to develop GUI or window-based applications</em> in java.

Java AWT components are platform-dependent i.e. components are displayed according to the view of operating system. AWT is heavyweight i.e. its components are using the resources of OS.

The java.awt package provides classes for AWT api such as TextField, Label, TextArea, RadioButton, CheckBox, Choice, List etc.

<img class="alignnone size-full wp-image-891" src="https://birjotsingh17.files.wordpress.com/2017/07/017-07-14-232019.png?w=1000" alt="017-07-14 23:20:19.png" />

&nbsp;
<h4>SWINGS :</h4>
Java Swing tutorial is a part of Java Foundation Classes (JFC) that is <em>used to create window-based applications</em>. It is built on the top of AWT (Abstract Windowing Toolkit) API and entirely written in java.

Unlike AWT, Java Swing provides platform-independent and lightweight components.

The javax.swing package provides classes for java swing API such as JButton, JTextField, JTextArea, JRadioButton, JCheckbox, JMenu, JColorChooser etc.

&nbsp;
<h4>JDBC :</h4>
Java JDBC is a java API to connect and execute query with the database. JDBC API uses jdbc drivers to connect with the database.
Before JDBC, ODBC API was the database API to connect and execute query with the database. But, ODBC API uses ODBC driver which is written in C language (i.e. platform dependent and unsecured). That is why Java has defined its own API (JDBC API) that uses JDBC drivers (written in Java language).

<img class="alignnone size-full wp-image-901" src="https://birjotsingh17.files.wordpress.com/2017/07/jdbc.png?w=1000" alt="JDBC" />

&nbsp;
<h3 class="entry-title">(3/7/17)  -   (5/7/17)</h3>
<h4>DEFINE ANDROID?</h4>
<b>Android</b> is a software package and linux based operating system for mobile devices such as tablet computers and smartphones.

It is developed by Google and later the OHA (Open Handset Alliance). Java language is mainly used to write the android code even though other languages can be used.

The goal of android project is to create a successful real-world product that improves the mobile experience for end users.

There are many code names of android such as Lollipop, Kitkat, Jelly Bean, Ice cream Sandwich, Froyo, Ecliar, Donut etc.
<h4 class="h2">Features of Android</h4>
After learning what is android, let's see the features of android. The important features of android are given below:

1) It is open-source.

2) Anyone can customize the Android Platform.

3) There are a lot of mobile applications that can be chosen by the consumer.

4) It provides many interesting features like weather details, opening screen, live RSS (Really Simple Syndication) feeds etc.

It provides support for messaging services(SMS and MMS), web browser, storage (SQLite), connectivity (GSM, CDMA, Blue Tooth, Wi-Fi etc.), media, handset layout etc.
<div></div>
<h4>COMPONENTS OF ANDROID</h4>
<ol>
	<li>ACTIVITY (USER INTERFACE)</li>
	<li>SERVICE (BACKGROUND)</li>
	<li>CONTENT PROVIDER (DATABASE)</li>
	<li>BROADCAST RECEIVER</li>
</ol>
<h4> LIFECYCLE METHODS :</h4>
<ol>
	<li>onCreate</li>
	<li>onStart</li>
	<li>onResume</li>
	<li>onPause</li>
	<li>onStop</li>
	<li>onDestroy</li>
	<li>onRestart</li>
</ol>
<h4> LOG I:</h4>
Function of “log.i”  in Android is same as “system.out.println” in JAVA.
i stands for information.

SYNTAX:    <strong> log.i (key,”value”);</strong>
<h4>TOAST:</h4>
It is a message that comes for a few seconds when performed some action.

SYNTAX:
<strong>Toast.makeText (this, “This is a Toast message”,Toast.LENGTH_LONG).show();</strong>

<img class="alignnone size-full wp-image-806" src="https://birjotsingh17.files.wordpress.com/2017/07/y2js4.png?w=1000" alt="Y2JS4" />
<h4></h4>
<h4>NAVIGATION :</h4>
Navigation is used to navigate from one activity to another.
There are many methods for navigation
<ol>
	<li>IMPLICIT</li>
	<li>EXPLICIT (it is the best method to be used)</li>
</ol>
SYNTAX FOR EXPLICIT:
<strong>Intent intent = new intent (source, destination.class);</strong>
<strong>startActivity</strong>
<h4> finish() :</h4>
It is method that destroys the activity.When one have to go back to previous activity then “finish()” method is called.
Using navigation method to go back to previous activity is not a good practice because navigation method makes new object everytime it is called so it covers alot of memory whereas finish method destroys the activity.
Therefore using finish method to go to previous activity is a good practice.
<h4>NOTE:</h4>
<ul>
	<li>INTENT – which helps compinents to interact.</li>
	<li>icons/photos are kept in mipmap folder or in drawing folder.</li>
	<li>application name can be changed from string.xml file.</li>
	<li>We don’t make objects of Activity, Android Container makes object on its own.</li>
	<li>Activity works on stack i.e. last in first out.</li>
	<li>editText in ANDROID is same as Textfield as in JAVA.</li>
</ul>
<h2>Installing Android Studio in Ubuntu 16.04</h2>
Download link -  <a href="https://developer.android.com/studio/index.html?gclid=Cj0KEQjwv_fKBRCG8a3ao-OQuZ8BEiQAvpHp6CaSi4num65EW6gIwhp80a02kIjhhUUT3TkStQ8ufgwaAm6E8P8HAQ">Android Studio</a>
<pre><code>sudo unzip android-studio-ide-162.4069837-linux.zip -d /opt</code></pre>
To launch Android Studio, navigate to the <code>/opt/android-studio/bin</code> directory in a terminal and execute <code>./studio.sh</code>.
<h4>Things Done</h4>
Analysing the Activity life cycle i.e how one activity create, start, resume and pause, stop, delete.

Created two activities and pass data from to another using various Forward passing methods.

Code - <a href="https://github.com/dpruthi/Android_project">https://github.com/dpruthi/Android_project</a>

&nbsp;
<h3 class="entry-title">(6/7/17)  -   (14/7/17)</h3>
<h4>Menus in Android.</h4>
Menus are a common user interface component in many types of applications. To provide a familiar and consistent user experience, you should use the <code><a href="https://developer.android.com/reference/android/view/Menu.html">Menu</a></code> APIs to present user actions and other options in your activities.

<strong>Options menu and app bar</strong>

<img class="alignnone size-full wp-image-181" src="https://tacitusdeep.files.wordpress.com/2017/06/actionbar.png" alt="actionbar" width="428" height="215" />

<strong>Context menu and contextual action mode</strong>

<img class="alignnone size-full wp-image-183" src="https://tacitusdeep.files.wordpress.com/2017/06/menu-context-1.png" alt="menu-context (1)" width="420" height="356" />

<strong>Popup menu</strong>

<img class="alignnone size-full wp-image-184" src="https://tacitusdeep.files.wordpress.com/2017/06/popupmenu.png" alt="popupmenu" width="200" height="143" />
<h4>Views In Android.</h4>
The <code>View</code> class is a superclass for all GUI components in Android. For instance, the <code>TextView</code> class which is used to display text labels in Android apps is a subclass of <code>View</code>. Android contains the following commonly used <code>View</code> subclasses:
<ul>
	<li><code>TextView</code></li>
	<li><code>EditText</code></li>
	<li><code>ImageView</code></li>
	<li><code>ProgressBar</code></li>
	<li><code>Button</code></li>
	<li><code>ImageButton</code></li>
	<li><code>CheckBox</code></li>
	<li><code>DatePicker</code></li>
</ul>
These are only some of the many, many subclasses of the <code>View</code> class.
<h4>ViewGroup</h4>
The <code>ViewGroup</code> class is a subclass of the <code>View</code> class. <code>ViewGroup</code> instances work as containers for <code>View</code>instances to group <code>View</code> instances together. Android contains the following commonly used <code>ViewGroup</code>subclasses:
<ul>
	<li><code>LinearLayout</code></li>
	<li><code>RelativeLayout</code></li>
	<li><code>ListView</code></li>
	<li><code>GridView</code></li>
	<li>CardView</li>
	<li>WebView</li>
</ul>
These are not the only <code>ViewGroup</code> subclasses Android contains. There are others but which are less used.

Simple example, how we can use these views
<ul>
	<li><a href="https://github.com/dpruthi/ChalisaSangrah">ChalisaSangrah</a></li>
	<li><a href="https://github.com/dpruthi/News_Aggregator">News Aggregator</a></li>
</ul>
<h4 class="api-title">LocationManager</h4>
<code class="api-signature">public class LocationManager </code>
<code class="api-signature">extends Object</code><code class="api-signature"></code>

This class provides access to the system location services. These services allow applications to obtain periodic updates of the device's geographical location, or to fire an application-specified Intent when the device enters the proximity of a given geographical location.

You do not instantiate this class directly; instead, retrieve it through <code><a href="https://developer.android.com/reference/android/content/Context.html#getSystemService(java.lang.Class&lt;T&gt;)">Context.getSystemService(Context.LOCATION_SERVICE)</a></code>.

Unless noted, all Location API methods require the <code><a href="https://developer.android.com/reference/android/Manifest.permission.html#ACCESS_COARSE_LOCATION">ACCESS_COARSE_LOCATION</a></code> or <code><a href="https://developer.android.com/reference/android/Manifest.permission.html#ACCESS_FINE_LOCATION">ACCESS_FINE_LOCATION</a></code> permissions. If your application only has the coarse permission then it will not have access to the GPS or passive location providers. Other providers will still return location results, but the update rate will be throttled and the exact location will be obfuscated to a coarse level of accuracy.


<div class="dac-nav-sidebar"></div>

<div id="body-content" class="wrap clearfix">
<div class="jd-descr ">
<div id="jd-content" class="api apilevel-1">
<h4 class="api-title">NotificationManager</h4>
<code class="api-signature">public class NotificationManager </code>
<code class="api-signature">extends <a href="https://developer.android.com/reference/java/lang/Object.html">Object</a> </code>

Notifications can take different forms:
<ul>
	<li>A persistent icon that goes in the status bar and is accessible through the launcher, (when the user selects it, a designated Intent can be launched),</li>
	<li>Turning on or flashing LEDs on the device, or</li>
	<li>Alerting the user by flashing the backlight, playing a sound, or vibrating.</li>
</ul>
Each of the notify methods takes an int id parameter and optionally a <code><a href="https://developer.android.com/reference/java/lang/String.html">String</a></code> tag parameter, which may be <code>null</code>. These parameters are used to form a pair (tag, id), or (<code>null</code>, id) if tag is unspecified. This pair identifies this notification from your app to the system, so that pair should be unique within your app. If you call one of the notify methods with a (tag, id) pair that is currently active and a new set of notification parameters, it will be updated. For example, if you pass a new status bar icon, the old icon in the status bar will be replaced with the new one. This is also the same tag and id you pass to the <code><a href="https://developer.android.com/reference/android/app/NotificationManager.html#cancel(int)">cancel(int)</a></code> or <code><a href="https://developer.android.com/reference/android/app/NotificationManager.html#cancel(java.lang.String, int)">cancel(String, int)</a></code> method to clear this notification.

You do not instantiate this class directly; instead, retrieve it through <code><a href="https://developer.android.com/reference/android/content/Context.html#getSystemService(java.lang.Class&lt;T&gt;)">getSystemService(Class)</a></code>.

<img class="alignnone size-full wp-image-185" src="https://tacitusdeep.files.wordpress.com/2017/06/mobile-computing-12.png" alt="mobile-computing-12" width="578" height="254" />

</div>
</div>
</div>
<h4></h4>
<h4 class="api-title">SensorManager</h4>
<code class="api-signature">public abstract class SensorManager </code>
<code class="api-signature">extends <a href="https://developer.android.com/reference/java/lang/Object.html">Object</a> </code><code class="api-signature"></code>

SensorManager lets you access the device's <code><a href="https://developer.android.com/reference/android/hardware/Sensor.html">sensors</a></code>. Get an instance of this class by calling <code><a href="https://developer.android.com/reference/android/content/Context.html#getSystemService(java.lang.String)">Context.getSystemService()</a></code> with the argument<code><a href="https://developer.android.com/reference/android/content/Context.html#SENSOR_SERVICE">SENSOR_SERVICE</a></code>.

Always make sure to disable sensors you don't need, especially when your activity is paused. Failing to do so can drain the battery in just a few hours. Note that the system will <i>not</i> disable sensors automatically when the screen turns off.
<h4>ProgressManager</h4>
<h4>SmsManager</h4>
<code class="api-signature">public final class SmsManager </code>
<code class="api-signature">extends <a href="https://developer.android.com/reference/java/lang/Object.html">Object</a></code>

<code class="api-signature"></code>Manages SMS operations such as sending data, text, and pdu SMS messages. Get this object by calling the static method <code><a href="https://developer.android.com/reference/android/telephony/SmsManager.html#getDefault()">getDefault()</a></code>.

For information about how to behave as the default SMS app on Android 4.4 (API level 19) and higher, see <code><a href="https://developer.android.com/reference/android/provider/Telephony.html">Telephony</a></code>.

Simple example, how we can use these API -
<ul>
	<li><a href="https://github.com/dpruthi/LocationSender">LocationSender</a></li>
</ul>
<h4>Fragment</h4>
<h4>Broadcast Receiver</h4>
&nbsp;

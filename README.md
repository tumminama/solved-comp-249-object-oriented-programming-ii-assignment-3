Download Link: https://assignmentchef.com/product/solved-comp-249-object-oriented-programming-ii-assignment-3
<br>
<strong><u>Purpose:</u></strong> The purpose of this assignment is to allow you practice Inheritance, Polymorphism, Exception Handling, and File I/O, as well as other previous object oriented concepts.

There are two independent parts in this assignment, Part I and Part II.

<h1>Part I</h1>

<strong> </strong>

Post Canada is not happy with their current software that keeps track of activities of a delivery truck transporting packages from one city to another for subsequent local delivery by other trucks. You accepted to take the challenge as a programmer. Your first project is to write a new software application. Certain simplifying assumptions have been made to allow you to concentrate on OOP concepts rather than the complete realism of the simulation.




<h2>Implementation</h2>

<strong> </strong>

Implement the following classes: Truck, Package, Letter, Box, Crate, Metal Crate and Wood Crate, and CargoTest to simulate the long-distance transportation of packages by a truck.




Your solution must conform to the following:

<ul>

 <li>A set of classes, corresponding to Truck, Package, Letter, Box, Crate, Metal Crate and Wood Crate, must be designed, declared and implemented.</li>

 <li>The Truck class should contain the driver’s name, the originating and destination cities, its gross and unloaded weight, the number of packages and additional information about each package that it carries. You must use an array of type Package. You may assume that trucks can carry a maximum of 200 packages.</li>

</ul>

Trucks will be assigned a driver, loaded, weighed before and after loading, driven and unloaded. In addition, each truck has a gross income equal to the total shipping costs of the packages.




<ul>

 <li>The Package class is the abstract base class for a ‘packages’ hierarchy. Each package has a tracking number, weight and shipping cost, based on its weight. The tracking number encodes the originating and destination cities as well as the type of package. If the least significant digit of the tracking number is a 0, the package is a letter whose weight is given in ounces. Similarly if the unit’s digit is a 1, 2 or 3 then the package is a box, wooden crate or metal crate, respectively, whose weight is given in pounds. We are not concerned with the source and destination information for each package, so we will not examine the tracking number for this information.</li>

</ul>




<ul>

 <li>Shipping costs are computed as follows.

  <ul>

   <li>Letters cost $.05/ounce up to a maximum of 32 ounces (2 pounds).</li>

   <li>Boxes cost $2/lb up to a maximum of 40 pounds. o Wooden crates cost $2.50/lb up to a maximum of 80 pounds. o Metal crates cost $3.00/lb up to a maximum of 100 pounds.</li>

  </ul></li>

</ul>




<ul>

 <li>Your load method must check for packages that are too heavy. If so, then throw an exception and print out that package’s information (package type, tracking number, weight). Of course, don’t load</li>

</ul>

that package. If the package is ok to load, “get some space” for it and load it. NOTE: All Exceptions thrown will be of your own type – PackageException.




<ul>

 <li>If you determine a package is not one of the ones your truck is allowed to carry, throw an exception and print out the information (unknown package, tracking number, weight). NOTE: All Exceptions thrown will be of your own type –</li>

</ul>




<ul>

 <li>If the truck is full, throw an exception and then printout the information (package type, tracking number, weight) along with the fact that it was not loaded because the truck is full. NOTE: All Exceptions thrown will be of your own type –</li>

</ul>




<ul>

 <li>When packages are unloaded the package information is printout, and deducted from the truck load.</li>

</ul>




<ul>

 <li>You must handle weight conversion in two ways:

  <ul>

   <li>For package:</li>

  </ul></li>

</ul>

This can be implemented using two methods toOunces and toPounds, that will accept a double as a parameter. You will implement them in Package, or the subclasses, it is entirely up to you.

<ul>

 <li>For truck</li>

</ul>

This can be implemented using two methods toKilograms and toPounds, that will accept a double as a parameter. You must print out the weight of the vehicle in kilograms and in pounds.




To test your program you are to write the CargoTest code class which behaves in the following way:




<ul>

 <li>Instantiate a truck, with its driver, unloaded weight and both the originating and destination cities  Load the truck with packages.</li>

 <li>Determine the gross income earned by shipping of the cargo.</li>

 <li>Weigh the truck (AFTER it has been completely loaded).</li>

 <li>Drive the truck to its destination – this will simply be nice output to the screen that states the truck and its driver is driving from originating city to destination city.</li>

 <li>Unload the truck.</li>

</ul>




         Presents the following menu to the user, hence possible actions:




<table width="552">

 <tbody>

  <tr>

   <td width="552">What would you like to do?1.       Start a cargoa.       Driver nameb.       Unload weight(kg; lb)c.       Originating cityd.       Destination city2.       Load the truck with packagesa.       Package tracking numberb.       Package weight(oz; lb)c.       Package shipping cost3.       Unload a package4.       The number of packages loaded5.       The gross income earned by shipping of the cargo6.       Weight the truck(after it has been completely loaded)7.       Drive the truck to destination0. To quitPlease enter your*the sub-menus come after user confirms the choice but not with the ma choice and press &lt;Enter&gt;:                                                                      in menu.</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h3>Part I Evaluation</h3>




You will be evaluated mostly on the implementation of the classes, the relationship (is-a vs has-a) between the classes, abstract classes, methods’ implementation, methods’ overriding and the access, rights of the class members, as well as exception handling.




<h3>Required documents                                                      </h3>




<ul>

 <li>UML diagram. o Source code in Java.  o Javadoc file in HTML.</li>

 <li>Test cases for all the functionalities of the menu options.</li>

</ul>

Note- you need to hard code the array of packages, to validate when you try to load more than the allowed 200 packages.







<h1>Part II</h1>










Warships ….

<strong> </strong>

<em> </em>

The <strong>Warship</strong> class has the following attributes: a <em>serial number</em> (long type), a <em>name</em> (String type), a <em>creation</em> <em>year</em> (int type), an <em>owner country</em> (String type), a <em>price</em> (double type) and a <em>speed</em> (int type). It is assumed that both the name and the owner country are recorded as continuous strings with “_” to separate the different words if any (i.e. a name can be Royal_Fighter, and country can be United_Kingdom).




The file <strong><em>Initial_Warship_Info.txt</em></strong>, which one of its versions is provided with this assignment, has the information of various warships that take part of an internationl mission. However, this file is always created manually by a 3<sup>rd</sup> party firm, which is histroically known to lack pricision and so    errors in the serial numbers are expected to exist in this file. In specific, due to a cut-and-paste practice by employees of this firm, some serial numbers are mistakenly re-recorded later in the file as the serial numbers of other following warrships in that file. Consequently, a serial number can either appears once in the file, which is the correct case, or appears multiple times, in which case the second, and following, appearances are in error.




You must notice that the file <em>Initial_Warship_Info.txt </em>changes regularly, and it may have many records, or no records at all, depending on the current participants in the mission. The file provided with this assignment is only one version of the file, and must not be considered as the general case when writing your code.




<u>For part II, you are required to:</u>

<ol>

 <li>Write the implementation of the <strong>Warship</strong>class according to the above given specification.</li>

 <li>Write the implementation of an exception class called <strong>DuplicateSerialNumberException</strong>, which extends the <strong>Exception</strong> Should a duplicate serial number is detected at any point, an object from this class will be thrown. More details will follow below.</li>

 <li>Write the implementation of a public class, called <strong>WarshipInventory1</strong>, which will utilize the <strong>Warship</strong> class and the <em>txt</em>, as explained below. The class has a static array of warships, called <em>wsArr[]</em>, and few methods. Beside the main() method, the class must have the following methods:

  <ol>

   <li>A method called <strong><em>fixInventory()</em></strong>, which accepts two parameters, an input file stream name and an output file stream name. The first parameter is the stream related to the <em>txt</em>. The second parameter is related to an output file name, which will be entered by the user prior to calling this method (at the main() method). This output file will eventually store a correct version of the inventory. More information on that will follow below.</li>

   <li>A method called <strong><em>displayFileContents()</em></strong>, which accepts an input file stream name, then displays the contents of this file to the standard output (the screen).</li>

   <li>You can add any other methods to that class if you wish to.</li>

  </ol></li>

</ol>




<u>Here are the details of how your program must behave:</u>

<ul>

 <li>In the main() method, your program must prompt the user to enter the name of the output file that will be created to hold the modified/correct inventory. This output file is theoretically a copy of the <em>txt</em>, but with all the duplicate serial numbers corrected.</li>

 <li>If the entered file name by the user matches the name of an existing file, then the program must reject that name indicating to the user that a file with that name already exists, display the size of this existing file (in bytes) to the user, then prompt the user to enter a new name. This process would repeat <a href="https://www.google.com/search?hl=en&amp;rls=com.microsoft:en-us&amp;ei=q0V9S83MFYPElAftnuTNBQ&amp;sa=X&amp;oi=spell&amp;resnum=0&amp;ct=result&amp;cd=1&amp;ved=0CAQQBSgA&amp;q=define%3A+indefinitely&amp;spell=1">indefinitely,</a> until the user finally enters a name for a non-existing file. See Figure1 for illustration.</li>

 <li>Once the user finally enters a correct file name for the output file, the program will attempt to establish an input and output streams for the <em>txt </em>and that output file accordingly. This process may surely throw specific exceptions, and your program must handle all these exceptions properly.</li>

 <li>The <em>fixInventory()</em> method (see details below) will utilize the <em>wsArr[]</em> array as follows: All warship objects recorded in the <em>txt</em> file must first be copied into that array. All detections and corrections of the serial numbers will be conducted on that array. Once the array has finally all correct information, the objects will be recorded to the output file. However since it is always unknown at the time the program starts how many records are in the <em>Initial_Warship_Info.txt</em> file, you must first find this information. You may, and should, add a private helping method to the <strong>WarshipInventory1</strong> class to do so. Once the number of records is know, the array must be set to that size.</li>

 <li>If the number of records in the <em>txt </em>was detected to be zero or one; the case when the file is empty or has only one record, then the program must display a message indicating that, performs any needed operations (such as closing files), then exits, since there is nothing to be fixed.</li>

 <li>If the <em>txt </em>has more than one record, then finally the <em>fixInventory()</em> method will be called to create a the new output file with the correct information. The exact details of this method are as follows:

  <ul>

   <li>The method will accept two stream names for the input and output files, o The method must read each warship record from the input file and creates a warship object in the array <em>wsArr[]</em> based on that record,</li>

   <li>Once the entire input file is read into the array (notice that the array has real warship objects, and not just information), the method starts to trace that array from start to end looking for any serial number duplicates,</li>

   <li>If a serial number duplicate is detected, then the method displays a message to the user indicating that, and prompt the user to enter a new serial number,</li>

   <li>You should notice that this new number must not be a duplicate of any other existing record, and your program must guarantee that. Should the user enters a serial number that is still a duplicate, the program must throw a <strong>DuplicateSerialNumberException</strong>, which must be catched to display a message indicating that, then the user must be prompted again to enter a new serial number. Further bad entries will result in the same action; that is throwing of the</li>

  </ul></li>

</ul>

<strong>DuplicateSerialNumberException</strong> object, catching it to display the message, and the user is prompted again. Effectively, this process will repeat indefinitely until the user enters a correct serial number. Again, you may, and should, create a private helping method to find if a duplicate exists in the array. See Figure 2 for illustration.  o Finally, once all the duplicate serial numbers are removed, the new information of the objects in the <em>wsArr[]</em> must be copied to the output file. This output file has now the correct information.

<ul>

 <li>Upon the return of the <em>fixInventory() </em>call in the main() method, the program must use the <em>displayFileContents()</em> method to display the information of both the</li>

</ul>

<em>Initial_Warship_Info.txt</em> file, as well as the created output file. See Figure 3 for illustration.  Hint: You must carefully keep track of the opening and closing of these files.




Below are sample snapshots of the program behavior for further illustrations:




Figure 1: Detecting Existing Files













Figure 2: Detecting Existing Serial Numbers




Figure 3: Displaying File Contents (<em>partial image</em>)







<strong><u>Assignment Submission</u> </strong>

<strong> </strong>

<ul>

 <li>Create <strong>one </strong>zip file, containing the two parts: I, and II separately, where each part contains the files (.java and .html and test cases).</li>

 <li>Naming convention for the zip file:

  <ul>

   <li>If the work is done by 1 student: Your file should be called <em>a#_studentID_Part#</em>, where a# is a3 for assignment3, <em>studentID </em>is your student ID number, and <em>Part# </em>PartI, PartII or PartIII.</li>

   <li>If the work is done by 2 students: The zip file should be called <em>a#_studentID1_studentID2</em>, where a<em># </em>is a3 for assignment3, <em>studentID1 </em>and <em>studentID2 </em>are the student ID numbers of each student, and <em>Part# </em>PartI, PartII or PartIII.</li>

  </ul></li>

 <li>Assignments must be submitted in the right folder of the assignments. Upload your zip file at the URL: <a href="https://fis.encs.concordia.ca/eas/">https://fis.encs.concordia.ca/eas/</a> as <em>Programming Assignment </em> <strong>Assignments uploaded to an incorrect folder will not be marked and result in a zero mark. No resubmissions will be allowed. </strong></li>

</ul>

<em> </em>
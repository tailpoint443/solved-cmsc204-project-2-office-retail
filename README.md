Download Link: https://assignmentchef.com/product/solved-cmsc204-project-2-office-retail
<br>
<h2>Project 2</h2>

Office Depo, an office supply retailing company, donates its surpluses to colleges at the end of each year. Volunteers will help deliver packages of supplies to representatives of colleges (Recipient of supplies).

Create a Java application that will simulate the delivering packages from the container of packages by the volunteers to recipients.

<strong>Academic Honesty Policy Reminder</strong> | <strong>Do your own work</strong> – each submitted project will be compared against other submissions from current and previous semesters.

<strong>Data Element</strong>

<ul>

 <li><strong>Volunteer</strong>

  <ul>

   <li>Holds the relevant information for a Volunteer: <em>name</em></li>

  </ul></li>

 <li><strong>DonationPackage</strong>

  <ul>

   <li>Holds the information of the package to be donated: <em>description, weight</em></li>

  </ul></li>

 <li><strong>Recipient</strong>

  <ul>

   <li>Holds the information of the recipients: <em>name</em></li>

  </ul></li>

</ul>

<strong>Data Structure</strong>

<ul>

 <li>Create a generic queue class called <strong>MyQueue</strong> that implements the <strong>QueueInterface</strong> given to you</li>

 <li>Create a generic stack class called <strong>MyStack</strong> that implements the <strong>Stack</strong> <strong>Interface</strong> given to you</li>

 <li>Create a class <strong>VolunteerLine</strong> that implements <strong>VolunteerLineInterface</strong>

  <ul>

   <li>This class contains a queue of Volunteers and simulates queuing and dequeuing volunteers to and from the volunteers’ line</li>

  </ul></li>

 <li>Create a class <strong>RecipientLine</strong> that implements <strong>RecipientLineInterface</strong>

  <ul>

   <li>This class contains a queue of Recipients and simulates queuing and dequeuing Recipients to and from the recipients’ line</li>

  </ul></li>

 <li>Create a class <strong>Container</strong> that implements <strong>ContainerInterface</strong>

  <ul>

   <li>This class contains a stack of <strong>DonationPackage</strong> and simulates adding and removing package from the container’s stack</li>

  </ul></li>

 <li>Assumptions

  <ul>

   <li>When a volunteer enters a queue they will stay in the queue and every time that the volunteer is removed from the line they will be go back to the end of the line</li>

   <li>When a recipient receives a donation package they will leave their queue</li>

  </ul></li>

</ul>

<strong>Data Manager</strong>

<ul>

 <li>The <strong>DonationManager</strong> class will manage adding a new package to the container, a new volunteer to the volunteer queue line, a new recipient to the recipient queue and donating package by the volunteer to the recipient. The three methods named <strong>managerArrayPackage, managerArrayRecipient, </strong>and <strong>managerArrayVolunteer </strong>place their data elements in an array.  They all call the methods in the<strong> container, volunteer line, and recipient line </strong>respectively, named toArrayPackage, toArrayVolunteer, and toArrayRecipient.  Each of those methods calls toArray in MyStack or MyQueue.

  <ul>

   <li>Notice that because of type erasure in the generic MyStack and MyQueue, if their toArray methods return an array of type T, i.e., T[], they are actually returning Object[]. But since the individual elements of the array are still Packages, Recipients, or Volunteers, we can copy them one by one into a new array of the appropriate type and cast each one to the appropriate type.</li>

  </ul></li>

 <li><strong>DonationManager</strong> will implement the interface <strong>DonationManager Interface</strong></li>

</ul>

<strong>Exception Classes</strong>

<ul>

 <li>RecipientException:</li>

</ul>

<strong>public</strong> <strong>class</strong> <u>RecipientException</u> <strong>extends</strong> RuntimeException {

<strong>public</strong> RecipientException(){};

RecipientException(String message) {

<strong>super</strong>(message);

}

If the user attempts to add new Recipient and the recipient line is full, throw RecipientException(“Recipient Queue is full”).  If user attempts to remove a recipient and the recipient is empty, throw RecipientException(“Recipient Queue is empty”);

<ul>

 <li>VolunteerException – similar to RecipientException except throws VolunteerException when the Volunteer Queue is full or empty</li>

 <li>ContainerException – similar to RecipientException except throws ContainerException when the Volunteer Stack is full or empty</li>

</ul>

<strong>You may add additional methods and attributes to your classes, however, they cannot impact (or interfere with) any of the provided public test cases</strong>

<strong>The GUI (Provided for You)</strong>

<ul>

 <li>Initially there is no package on the container stack, or any volunteers or recipients on the queue</li>

 <li>Allows the user to load new packages to the container and add new volunteers to volunteer’s line and new recipient to recipients’ line</li>

 <li>Allows the user to simulate the process of donating a package from the container by the volunteer on the front of the Volunteer queue to the recipient on the front of the Recipient queue. When a volunteer finishes donating the package to the recipient, he/she will be placed at the back of the queue of volunteers to continue the process of donation. <strong>Each volunteer takes one package at a time to deliver to the recipient</strong></li>

</ul>

<strong>Programming Concepts</strong>

This project utilizes the following concepts:

<ul>

 <li>Previously learned materials</li>

 <li>Generic Queue</li>

 <li>Generic Stack</li>

 <li>Exception handling</li>

 <li></li>

</ul>

<strong>GitHub</strong>

<ul>

 <li>As you are working on your project, utilize your GitHub repro to manage your work. You will need to submit a screenshot of your repro.</li>

</ul>

<strong>Testing </strong>

<ul>

 <li>As a typical user, I should be able to utilize your program without running into too much difficulties!  Thoroughly test your project</li>

</ul>

<ul>

 <li>Think about the public and private test cases which your instructor will test your project against</li>

</ul>
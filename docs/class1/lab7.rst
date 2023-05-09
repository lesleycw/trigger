Lab 7: Introduction to MCN
==================================

This lab will make use of F5 Distributed Cloud Simulators to emulate the process of setting up two different sites (one in AWS, one on premises)


F5 provides "simulations" of its services via "F5 Simulators".  We will use the 
Distributed Cloud Simulator to familiarize you with the MCN concept.

Task 1: Creating a Site
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Please visit: https://simulator.f5.com/s/cloud2cloud_via_httplb/nav/sim1/020/0


Note that you will need to pay attention for fields that are highlighted.  Some of them like "Show Advanced Fields" 
may appear on the bottom right of the screen.

|lab007-1|

You can opt to fill in the form fields or you can click on the "Next" button to allow the simulator to fill-in 
the fields as required.  Note that all of these actions can also be performed via the Distributed Cloud API.

|lab007-2|

Stop when you reach the step of clicking on "Apply" after creating your AWS Site.

|lab007-3|

Congratulations you just simulated deploying your AWS Site via the Distributed Cloud Console.  If you like you can complete
running the simulator to deploy an Azure Site and create an HTTP Load Balancer.  In the next Lab Exercise we will
be creating Load Balancer resources in the "Live" lab environment.



.. |lab007-1| image:: _static/lab7-001.png
.. |lab007-2| image:: _static/lab7-002.png
.. |lab007-3| image:: _static/lab7-003.png

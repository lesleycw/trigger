Lab 6: Introduction to Content Delivery Networks (CDN)
=====================================================

F5 Distributed Cloud CDN (Content Delivery Network) provides integrated security with support for content caching and containerized edge-based workloads for richer digital experiences. Built on a high-performance, secure global private network, F5 Distributed Cloud CDN enables rich digital experiences for end users. Distributed Cloud CDN integrates with critical app security services to empower your organization as it pursues multi-cloud and edge-based initiatives. 

This lab provides an introduction to CDN services available within Distributed Cloud. The following steps will demonstrate the process of configuring CDN features within F5 Distributed Cloud Console. These steps will outline the process of creating CDN Distribution, and the steps involved for CDN Verification & viewing the Dashboard.

Task 1: Create CDN Distribution
~~~~~~~~~~~~~~~~~~~~~~~~

#. Login as SecOps, NetOps, or DevOps User

#. Select ‘Content Delivery Network’ from Common Services.

   .. image:: _static/lab6-001.PNG
	    :width: 75%
			
You can also select it from the left drop-down menu.		
						
	 .. image:: _static/lab6-002.PNG
			
#. Select Manage > Distributions > Add Distribution

   .. image:: _static/lab6-003.PNG
	    :width: 75%
			
#. Enter the following variables:

   ================================= =====
   Variable                          Value
   ================================= =====
   Name                              <namespace-cdn>
   Domains                           <namespace-cdn.lab-sec.f5demos.com>
   ================================= =====
	 
       .. image:: _static/lab6-004.PNG
	 
   ================================= =====
   Variable                          Value	
   ================================= =====
   Type of CDN Distribution          HTTP
   ================================= =====
	 
       .. image:: _static/lab6-005.PNG
			
   ================================= ==============
   Variable                          Value	
   ================================= ==============
   Automatically Manage DNS Records  Enabled/Checked
   ================================= ==============
	 
      .. image:: _static/lab6-006.PNG
	 
#. Under 'CDN Origin Pool' select 'Configure'.

      .. image:: _static/lab6-007.PNG
      
#. Enter the following variables under 'Origin Host Header'

   ================================= =====
   Variable                          Value	
   ================================= =====
   DNS Name:                         demo-app.amer.myedgedemo.com
   Enable TLS for Origin Servers     No TLS
   ================================= =====
   
      .. image:: _static/lab6-008.PNG
      
#. Select 'Add Item' under the 'List of Origin Servers'. 

      .. image:: _static/lab6-009.PNG
      
   ================================= =====
   Variable                          Value	
   ================================= =====
   Type of Origin Server:            Public DNS Name of Origin Server
   DNS Name                          demo-app.amer.myedgedemo.com
   ================================= =====
   
      .. image:: _static/lab6-010.PNG
      
#. Select 'Apply' > 'Apply' > 'Save and Exit'.

      .. image:: _static/lab6-011.PNG
      
#. The CDN Distribution will take a few moments to deploy. You can click the 'Refresh' button to monitor the status as it goes from ‘Pending’ to ‘Active’.
     
      .. image:: _static/lab6-012.PNG

#. Once the CDN Distribution is active you can launch a new browser window and navigate to <namespace-cdn.lab-sec.f5demos.com

   Note: It may take 1-2 minutes before the site loads
 
     .. image:: _static/lab6-013.png
       
#. In chrome, right click on the screen and navigate to developer tools (Inspect). Then click on the "Network' tab before refreshing the page a few times. You can see that the static content is being presented from cache.

#. Select the upper lefthand menu and navigate to the various sub-pages to generate some traffic. 

      .. image:: _static/lab6-014.PNG
      
   Congratuations!! You successfully deployed a CDN Distribution within F5XC.

#. Now you will see monitoring/performance statistics within the F5XC dashboard. 

#. Naviate to the Monitoring > Performance section within the CDN configuration. Then select the CDN Distribution you just created (namespace-cdn).

     .. image:: _static/lab6-015.PNG
    
#. Click around to review to the dashboard statistics. 

     .. image:: _static/lab6-016.PNG
     
#. On the main dashboard, you will see various statitics including total requests, hits, misses

#. Lab Completed!

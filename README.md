
# OCI-Resource-Manager
Hands On Labs (HOL) using Resource Manager (Terraform) to create resources in Oracle Cloud Infrastructure (OCI).  

**Agenda**<ul>
    <li>Lab 1: Create a Virtual Cloud Network (VCN)</li>
    </li>Lab 2: Create a Compute VM instance</li>
    <li>Lab 3: Create a Oracle Database Cloud Service (DBCS) instance</li></ul>
<b>Prerequisites</b><ul>
<li> An Oracle Cloud Account. 
     You can obtain an Oracle Free Tier account by <a href="https://myservices.us.oraclecloud.com/mycloud/signup">clicking here</a>.</li>
<li> SSH Keys. You can create the keys by following instructions <a href="https://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/compute-iaas/generating_ssh_key/generate_ssh_key.html">here</a></li>
</ul>

<ul>
<b>Fun Fact:</b><blockquote>
Terraform is a tool for "infrastructure-as-code". 
OCI Resource Manager is service that allows you to leverage on Terraform to automate the process of provisioning your OCI resources. For more info on Resource Manager, read <a href="https://docs.cloud.oracle.com/en-us/iaas/Content/ResourceManager/Concepts/resourcemanager.htm">here</a>.
</blockquote>
</ul>

Let's begin.
<hr>

## Lab 1 - Create Virtual Cloud Network
Steps:
<ol>
<li>After login to your OCI account, click on the hamburger menu on the top left hand corner. Scroll down to <b>Identity</b> and navigate the mouse to the submenu <b>Compartments</b> as shown in image below:
</li>
<img height="400px" src="/images/GotoCompartmentsMenu.png"/>
<hr>
<li>Click on <b>Compartments</b>. On next page, click on <img width="160px" align="middle" src="/images/CreateCompartmentButton.png"/></li>
<hr>
<li>Fill in the details as shown below. Do note the (root) compartment will be yours instead of what is shown above. Once you are done, click on <img width="160px" align="middle" src="/images/CreateCompartmentButton.png"/>. After a few seconds, You should see your newly created compartment in the table view.</li>
<img height="400px" src="/images/CreateCompartmentHOL.png"/>

<ul>
<b>Fun Fact:</b><blockquote>
A compartment is a logical container, to organize and control access to the Oracle Cloud Infrastructure (OCI) Resources. You should create sub-compartments, (not your root compartment) to better manage your resources. This is why we have created HOL to do our labs. For more info on compartments, read <a href="https://docs.cloud.oracle.com/en-us/iaas/Content/Identity/Tasks/managingcompartments.htm">here</a>. 
</blockquote>
</ul>

<hr>
<li>Click on the hamburger menu on the top left hand corner. Scroll up until you see  <b>Resource Manager</b> and navigate the mouse to the submenu <b>Stacks</b> as shown in image below:
</li>
<img height="300px" src="/images/GotoStacksMenu.png"/>
<hr>
<li>Click on submenu <b>Stacks</b>. Stacks page will appear. Make sure the compartment is <b>HOL</b>. Otherwise, select the compartment from the dropdownlist on the left (shown below). Once you are done, click on <img width="100px" align="middle" src="/images/CreateStackButton.png"/>.

<img width="500px" src="/images/StacksInHOL.png"/>
</li>
<hr>
<li>On the create stack page, ensure <b>MY CONFIGURATION</b> is selected. Download the zip file <a href="files/VCN_Creation.zip" download>here</a> and drop it into the upload area.
Fill in the rest of details as shown below. Once done, click on the <b>Next</b> button.
<img width="650px" src="/images/CreateStackPage.png"/>
</li>
<hr>
<li>Fill in the details as shown in screenshot below. Once done, click on the <b>Next</b> button.
<img width="650px" src="/images/ConfigStackVariables.png"/>
</li>
<hr>
<li>Review input information is correct (screenshot below), click on the <b>Create</b> button.
<img width="650px" src="/images/ConfirmStack.png"/>
</li>
<hr>
<li>Now, we click on <b>Plan</b> as shown in the screenshot below. </li>
<img width="550px" src="/images/ClickPlan.png"/>
<hr>
<li>On the displayed popup screen, click on <img width="50px" align="middle" src="/images/PlanButton.png"/> as shown below.
</li>
<img width="500px" src="/images/PopupPlanScreen.png"/>
<hr>
<li>On the Job Details display, the RMJ icon will turn Orange. After a while, the job will complete and RMJ icon will turn Green (shown below). 
</li>
<img width="500px" src="/images/RMJSucceeded.png"/>
<hr>
<li>Navigate back to the Stack Details page (shown below)</li>
<img width="500px" src="/images/BacktoStackDetails.png"/>
<hr>
<li>Now, Apply the Plan (shown below)</li>
<img width="500px" src="/images/ApplyPlan.png"/>
<hr>
<li>The Apply Popup page will appear. Click on the <b>Apply</b> button.</li>
<hr>
<li> Once completed, the Orange RMJ icon will turn Green.
 Congrats! Your Virtual Cloud Network (VCN) is now provisioned. 
 You can verfy this by clicking on the top left hamburger menu and scroll up till you see <b>Networking</b>. Navigate and click on the submenu <b>Virtual Cloud Networks</b> (shown below)
</li>
<img width="500px" src="/images/GotoVCNMenu.png"/>
<img width="650px" src="/images/VCNCreated.png"/>
<hr>
</ol>
End of Lab 1
<hr>

## Lab 2 - Create Compute VM Instance

Steps:
<ol>
<li>Login to your OCI account, click on the hamburger menu on the top left hand corner. Scroll to <b>Resource Manager</b> and navigate the mouse to the submenu <b>Stacks</b> as shown in image below:
</li>
<img height="300px" src="/images/GotoStacksMenu.png"/>
<hr>
<li>Click on submenu <b>Stacks</b>. Stacks page will appear. Make sure the compartment is <b>HOL</b>. Otherwise, select the compartment from the dropdownlist on the left (shown below). Once you are done, click on <img width="100px" align="middle" src="/images/CreateStackButton.png"/>.

<img width="500px" src="/images/StacksInHOL.png"/>
</li><li>On the create stack page, ensure <b>MY CONFIGURATION</b> is selected. Download the zip file <a href="files/ComputeVM_Creation.zip" download>here</a> and drop it into the upload area.
Fill in the rest of details as shown below. Once done, click on the <b>Next</b> button.

<img width="650px" src="/images/CreateComputeVM.png"/>
</li>
<hr>
<li>Fill in the details as shown in screenshot below. Once done, click on the <b>Next</b> button.

<img width="650px" src="/images/ConfigComputeVMVariables.png"/>
</li>
<hr>
<li>Review input information is correct, click on the <b>Create</b> button.
</li>
<img width="550px" src="/images/ConfirmComputeVM.png"/>
<hr>
<li>Click on <b>Plan</b> as shown in the screenshot below. 
</li>
<img width="550px" src="/images/ClickPlanVM.png"/>
<li>On the displayed popup screen, click on <img width="50px" align="middle" src="/images/PlanButton.png"/>.
</li>
<hr>
<li>On the Job Details display, the RMJ icon will turn Orange. After a while, the job will complete and RMJ icon will turn Green. Navigate back to the Stack Details page (shown below)
</li>
<img width="500px" src="/images/BacktoStackDetailsVM.png"/>
<li>Apply the Plan (shown below)</li>
<img width="500px" src="/images/ApplyPlanVM.png"/>
<hr>
<li>The Apply Popup page will appear. Click on the <b>Apply</b> button.
</li>
<li> Once completed, the Orange RMJ icon will turn Green (will take a few minutes).
Congrats! Your Compute VM is now provisioned. 
You can verify this by clicking on the top left hamburger menu and scroll up till you see <b>Compute</b>. Navigate and click on the submenu <b>Instances</b> (shown below)
<hr>
</li>
<img width="500px" src="/images/GotoInstancesMenu.png"/>
<img width="650px" src="/images/VMCreated.png"/>
</ol>
End of Lab 2
<hr>

## Lab 3 - Create a Oracle Database Cloud Service (DBCS) instance
<ol>
<li>Login to your OCI account, click on the hamburger menu on the top left hand corner. Scroll to <b>Resource Manager</b> and navigate the mouse to the submenu <b>Stacks</b> as shown in image below:
</li>
<img height="300px" src="/images/GotoStacksMenu.png"/>
<hr>
<li>Click on submenu <b>Stacks</b>. Stacks page will appear. Make sure the compartment is <b>HOL</b>. Otherwise, select the compartment from the dropdownlist on the left (shown below). Once you are done, click on <img width="100px" align="middle" src="/images/CreateStackButton.png"/>.

<img width="500px" src="/images/StacksInHOL.png"/>
</li><li>On the create stack page, ensure <b>MY CONFIGURATION</b> is selected. Download the zip file <a href="files/DBCS_Creation.zip" download>here</a> and drop it into the upload area.
Fill in the rest of details as shown below. Once done, click on the <b>Next</b> button.

<img width="650px" src="/images/CreateDBCSInstance.png"/>
</li>
<hr>
<li>Fill in the details as shown in screenshot below. Once done, click on the <b>Next</b> button.

<img width="650px" src="/images/ConfigDBCSVariables.png"/>
</li>
<hr>
<li>Review input information is correct. (Be mindful of the stringent criteria for DB_ADMIN_PASSWORD). When done, click on the <b>Create</b> button.
</li>
<img width="550px" src="/images/ConfirmDBCS.png"/>
<hr>
<li>Click on <b>Plan</b> as shown in the screenshot below. 
</li>
<img width="550px" src="/images/ClickPlanDBCS.png"/>
<li>On the displayed popup screen, click on <img width="50px" align="middle" src="/images/PlanButton.png"/>.
</li>
<hr>
<li>On the Job Details display, the RMJ icon will turn Orange. After a while, the job will complete and RMJ icon will turn Green. Navigate back to the Stack Details page (shown below)
</li>
<img width="500px" src="/images/BacktoStackDetailsDBCS.png"/>
<li>Apply the Plan (shown below)</li>
<img width="500px" src="/images/ApplyPlanDBCS.png"/>
<hr>
<li>The Apply Popup page will appear. Click on the <b>Apply</b> button.
</li>
<li> The Orange RMJ icon indicates work-in-progress. Last I tested, it took sabout 15 minutes to complete.
When your RMJ icon turns Green, you are done!
Congrats! Your Database is now provisioned. 
You can verify this by clicking on the top left hamburger menu and scroll up till you see <b>Compute</b>. Navigate and click on the submenu <b>Instances</b> (shown below)
<hr>
</li>
<img width="500px" src="/images/GotoDBCSMenu.png"/>
<img width="650px" src="/images/DBCSCreated.png"/>
</ol>
End of Lab 3
<hr>


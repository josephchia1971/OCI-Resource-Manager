# OCI-Resource-Manager
Hands On Labs (HOL) using Resource Manager (Terraform) to create resources in Oracle Cloud Infrastructure (OCI).

**Agenda**<ul>
    <li>Lab 1: A Virtual Cloud Network (VCN)</li>
    </li>Lab 2: A Compute VM instance</li>
    <li>Lab 3: A Oracle Database</li></ul>
<b>Prerequisites</b><ul>
<li> An Oracle Cloud Account. 
     You can obtain an Oracle Free Tier account by <a href="https://myservices.us.oraclecloud.com/mycloud/signup">clicking here</a>.</li>
<li> SSH Keys. You can create the keys by following instructions <a href="https://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/compute-iaas/generating_ssh_key/generate_ssh_key.html">here</a></li>
</ul>

<ul>
<b>Fun Fact:</b><blockquote>
Terraform is a tool for "infrastructure-as-code". 
OCI Resource Manager is service that allows you to leverage on Terraform to automate the process of provisioning your OCI resources. For more info on Resource Manager, read <a href="hhttps://docs.cloud.oracle.com/en-us/iaas/Content/ResourceManager/Concepts/resourcemanager.htm">here</a>.* 
</blockquote>
</ul>

Let's begin.
<hr>

<b>Lab 1:</b>
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
A compartment is a logical container, to organize and control access to the Oracle Cloud Infrastructure (OCI) Resources. You should create sub-compartments, (not your root compartment) to better manage your resources. For more info on compartments, read <a href="https://docs.cloud.oracle.com/en-us/iaas/Content/Identity/Tasks/managingcompartments.htm">here</a>. 
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
<img width="600px" src="/images/ConfirmStack.png"/>
</li>

</ol>

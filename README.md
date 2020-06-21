
<style type="text/css">
hr {
height: 20px;
}

# OCI-Resource-Manager
Hands On Labs (HOL) using Resource Manager (Terraform) to create resources in Oracle Cloud Infrastructure (OCI).

<b>Agenda</b><ul>
    <li>Lab 1: A Virtual Cloud Network (VCN)</li>
    </li>Lab 2: A Compute VM instance</li>
    <li>Lab 3: A Oracle Database</li></ul>
<b>Prerequisites</b><ul>
<li> To run these labs you will need access to an Oracle Cloud Account. 
     You can obtain an Oracle Free Tier account by <a href="https://myservices.us.oraclecloud.com/mycloud/signup">clicking here</a>.</li>
<li> SSH Keys. Follow instructions <a href="#">here</a></li>
</ul>

<ul>
<b>Fact:</b><blockquote>
Terraform is a tool for "infrastructure-as-code". 
OCI Resource Manager is service that allows you to leverage on Terraform to automate the process of provisioning your OCI resources. 
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
<img height="400px" src="/images/CreateCompartmentHOL.png"/>
<li>Fill in the details as shown above. Do note the (root) compartment will be yours instead of what is shown above. Once you are done, click on <img width="160px" align="middle" src="/images/CreateCompartmentButton.png"/>. After a few seconds, You should see your newly created compartment in the table view.</li>
<hr>
<li>Next, click on the hamburger menu on the top left hand corner. Scroll up until you see  <b>Resource Manager</b> and navigate the mouse to the submenu <b>Stacks</b> as shown in image below:
</li>
<img height="400px" src="/images/GotoStacksMenu.png"/>
</ol>

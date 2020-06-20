# OCI-Resource-Manager
Hands On Labs (HOL) using Resource Manager (Terraform) to create VCN, Compute and DBCS

Objective:
This lab will show you how to use Oracle Cloud Infrastructure (OCI) Resource Manager to setup
<ul><li>
    Lab 1: A Virtual Cloud Network (VCN) </li><li>
    Lab 2: A Compute VM instance</li><li>
    Lab 3: A Oracle Database</li>
</ul>
Prerequisites
<ul>
<li> To run these labs you will need access to an Oracle Cloud Account. 
     You can obtain an Oracle Free Tier account by <a href="https://myservices.us.oraclecloud.com/mycloud/signup">clicking here</a>.
</li>
<li>
     SSH Keys. Follow instructions <a href="#">here</a>

<h>About Terraform and Oracle Cloud Resource Manager</h>
Terraform is a tool for building, changing, and versioning infrastructure safely and efficiently. 
OCI Resource Manager is service that allows you to automate the process of provisioning your OCI resources. Using Terraform, Resource Manager helps you install, configure, and manage resources through the "infrastructure-as-code" model. 

Let's begin.

<h>Lab 1:</h>
Steps:
<ol>
<li>On landing page after login to your OCI account, click up the hamburger menu on the left hand corner. Scroll down to <b>Identity</b> and click on the submenu <b>Compartments</b> as shown in image below:
<img src="/images/GotoCompartmentsMenu.png"/>
</ol>
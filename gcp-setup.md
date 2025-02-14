Certainly! Here's a comprehensive guide for setting up a Google Cloud Platform (GCP) account, creating a Google Compute Engine (GCE) virtual machine, and deploying a sample Python script.

GCP Setup Guide
Steps to Create a GCP Account
Visit the GCP Website

Go to Google Cloud Platform.
Start Free

Click on the Get started for free or Try Free button.
Sign In

Sign in with your existing Google account or create a new one.
Accept Terms

Read and accept the Google Cloud Platform Terms of Service.
Provide Account Information

Fill in your personal and billing information (note: your credit card won't be charged for free tier services).
Complete Sign-Up

Follow the prompts to complete your GCP account setup.
Steps to Set Up a Google Compute Engine (GCE) Virtual Machine (VM)
Log in to GCP Console

Sign in at Google Cloud Console.
Create a New Project

From the top-left corner, select the project dropdown, and click on New Project.
Enter a project name, select your billing account, and click Create.
Navigate to Compute Engine

In the left-hand sidebar, click on Compute Engine then VM instances.
Enable Compute Engine API

If prompted, enable the Compute Engine API.
Create a VM Instance

Click on Create to start setting up a new VM instance.
Virtual Machine Configuration
Name and Region

Enter a name for your VM instance.
Select a region and zone closest to your location.
Machine Type

Choose an appropriate machine type, e.g., e2-micro which is in the free tier.
Boot Disk

Under Boot disk, click Change and select Debian (or another preferred OS).
Click Select.
Firewall

Ensure "Allow HTTP traffic" and "Allow HTTPS traffic" are selected.
Create

Click Create to launch the VM.
Steps to Deploy a Sample Python Script
Connect to VM via SSH
SSH Command
In the GCP Console, navigate to your VM instance and click SSH to open a browser-based terminal.
Prepare the VM
Update Packages



sudo apt update && sudo apt upgrade -y
Install Python



sudo apt install python3 -y
Create and Run the Python Script
Create Script File

Create a new Python script file named add_numbers.py.


nano add_numbers.py
Add Script Content

Add the following content to the file:
def add_numbers(a, b):
    return a + b

if __name__ == "__main__":
    num1 = 10
    num2 = 20
    print(f"The sum of {num1} and {num2} is {add_numbers(num1, num2)}")
Save and Close

Press Ctrl + X, then press Y, and Enter to save and exit the editor.
Run the Script

Run the Python script with the following command:


python3 add_numbers.py
Verify Output

You should see the following output:
The sum of 10 and 20 is 30
This content provides a comprehensive guide to setting up a GCP account, creating a Google Compute Engine VM, and deploying a simple Python script. Each step is clearly defined to assist beginners in navigating through the GCP console and deploying their first application on a VM.
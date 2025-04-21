practical 1 
Aim: Define a simple services like Converting Rs into Dollar and Call it from different platform like
JAVA and .NET

steps:
create java new project name practical 
click on practical  then new webservices
name the new web application as CurrencyConverter
click insert code then click add web service operation
add operation name intro dollar
then code 
package server;

import javax.jws.WebService;
import javax.jws.WebMethod;
import javax.jws.WebParam;

/**
 *
 * @author Lenovo
 */
@WebService(serviceName = "CurrencyConverter")
public class CurrencyConverter {

    /**
     * Web service operation
     */
    @WebMethod(operationName = "InrtoDollar")
    public String InrtoDollar(@WebParam(name = "a") double a) {
        //TODO write your implementation code here:
        return "The Indian rupees " + a + " in Dollars is : " + (a / 83.17);
    }
}


then click on currencyconverter then test webservices

then click on practical create new jsp file
name new jsp file as input and ek aur jsp file output naam ka
then write this code in input

<%@page contentType="text/html" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
        <title>JSP Page</title>
    </head>
    <body>
        <form action="output.jsp">
            <pre>
    Enter Indian Rupees to Convert : <input type="text" name="t1">
    <input type="submit"> <input type="reset">
            </pre>
        </form>
    </body>
</html>

then new webservice client
click currencyconverter
check if http/localhost jaisa kuch ki nhi 
then ok 
open input


practical 1b

create project as java web /web application
name as practical
after create a project click on practical and 
click on practical  then new webservices
name the new web application as CurrencyConverter
click insert code then click add web service operation
add operation name intro dollar
then code 
package server;

import javax.jws.WebService;
import javax.jws.WebMethod;
import javax.jws.WebParam;

/**
 *
 * @author Lenovo
 */
@WebService(serviceName = "CurrencyConverter")
public class CurrencyConverter {

    /**
     * Web service operation
     */
    @WebMethod(operationName = "InrtoDollar")
    public String InrtoDollar(@WebParam(name = "a") double a) {
        //TODO write your implementation code here:
        return "The Indian rupees " + a + " in Dollars is : " + (a / 83.17);
    }
}


then click on currencyconverter then test webservices


Now Open Microsoft Visual Studio 2022
Create new Project
then search console App (.NET Framework) c#
configure ur project currency

then click add /references 
add references system.service_model,system.xml,system.xml.linq
then add srvices referces

uske baad wapas netbeans pe aur click on new web services client 

click on browse and then click currency converter
then copy localhost800 aisa link hoga usko visual pe jake 
add reference pe paste karo
phir solution exploure mai serviceReference1 pe click karkr 
write code  
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using currency.ServiceReference1;

namespace currency
{
    internal class Program
    {
        static void Main(string[] args)
        {
            CurrencyConverterClient client = new CurrencyConverterClient();
            Console.WriteLine("Enter the currency in Indian Rupees: ");
            double d = double.Parse(Console.ReadLine());
            Console.WriteLine(client.InrtoDollar(d));
            Console.ReadLine();
        }
    }
}


practical 2A
Aim(A) : Create a Simple REST Service
create a java web application
name as restfullwebservice
create new restfullwebserviceclient from pattern
nme project : RestfullService
location: source package
resource package : StringOperationPackage
path: generic
class name : StringOperation
MiME: text/html
representation class : java.lang.string

then insert code 
@PUT
@Consumes("text/html")
public void putHtml(String content) {
}

@PUT
@Consumes("text/html")
@Path("/Uppercase")
public String toUpperCaseMethod(String str) {
    return str.toUpperCase();
}

@PUT
@Consumes("text/html")
@Path("/Lowercase")
public String toLowerCaseMethod(String str) {
    return str.toLowerCase();
}

then clean verify deploy and test restfulwebservices








practical 2b
(B) Consuming Restful Service
create new project RestfullClientafter 
creating project click on new then 
click on other then restfull java client
new restfull java client give class name as StingOperationClient
package: StringPackage
then browse and select Stringoperation[generic]

package restfullclient;

import StringPackage.StringOperationClient;

/**
 *
 * @author Lenovo
 */
public class RestfullClient {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        StringPackage.StringOperationClient client = new StringOperationClient();

        System.out.println(client.toUpperCaseMethod("cloud computing and web services - tycs"));
        System.out.println(client.toLowerCaseMethod("CLOUD COMPUTING AND WEB SERVICES - TYCS"));
    }

}

then run file


prac3
Aim: Create a Simple SOAP service.
create new project on visual studio 
search web application and click ASP.NET Web Application (.NET Framework)
select ,net feamework 4.7.2\
then create empty web application
then click add new item
search webservice
[WebMethod]
public double D2R(double dollar)
{
double ans = dollar * 82;
return ans;
}
[WebMethod]
public double R2D(double rupees)
{
double ans = rupees / 82;
return ans;
}

run
and click webservice1.asmx then view in browser


 
 prac3
Aim: Create a Simple SOAP service.
create new project on visual studio 
search web application and click ASP.NET Web Application (.NET Framework)
select ,net feamework 4.7.2\
then create empty web application
then click add new item
search webservice
[WebMethod]
public double D2R(double dollar)
{
double ans = dollar * 82;
return ans;
}
[WebMethod]
public double R2D(double rupees)
{
double ans = rupees / 82;
return ans;
}

run
and click webservice1.asmx then view in browser


 
 prac3
Aim: Create a Simple SOAP service.
create new project on visual studio 
search web application and click ASP.NET Web Application (.NET Framework)
select ,net feamework 4.7.2\
then create empty web application
then click add new item
search webservice
[WebMethod]
public double D2R(double dollar)
{
double ans = dollar * 82;
return ans;
}
[WebMethod]
public double R2D(double rupees)
{
double ans = rupees / 82;
return ans;
}

run
and click webservice1.asmx then view in browser


 
 prac3
Aim: Create a Simple SOAP service.
create new project on visual studio 
search web application and click ASP.NET Web Application (.NET Framework)
select ,net feamework 4.7.2\
then create empty web application
then click add new item
search webservice
[WebMethod]
public double D2R(double dollar)
{
double ans = dollar * 82;
return ans;
}
[WebMethod]
public double R2D(double rupees)
{
double ans = rupees / 82;
return ans;
}

run
and click webservice1.asmx then view in browser


practical 4 google 

1. First of all we need to create an Java Web Application with any name, 
let it be Practical4 here using
Netbeans IDE.
new jsp 
give file name input
and write this code 
<%-- 
    Document   : input
    Created on : 10 Mar, 2024, 11:22:03 PM
    Author     : Lenovo
--%>

<%@page contentType="text/html" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <title>JSP Page</title>
</head>
<body>
    <form action="index.jsp">
        <pre>
        Enter latitude:<input type="text" name="t1"/>
        Enter longitude<input type="text" name="t2"/>
        <input type="submit" value="Show"/>
        </pre>
    </form>
</body>
</html>


3. Before running the application we need the Google API key.
The steps are shown here: - Visit Google
APIs Console (https://console.developers.google.com, you have to login with your Google account).

https://console.developers.google.com

4. Create a new API Project.
5. Enter the name to your project.

6. Create another file index.jsp
index.jsp

code 
<%@page contentType="text/html" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
    <style>
        #map{
            height:400px;
            width:100%;
        }
    </style>
</head>
<body>
    <%
        double lati=Double.parseDouble(request.getParameter("t1"));
        double longi=Double.parseDouble(request.getParameter("t2"));
    %>

    <h3> Google Maps </h3>
    <div id="map"></div>

    <script lang="javascript">
        function initMap() {
            var info={lat: <%=lati%>, lng: <%=longi%>};
            var map = new google.maps.Map(document.getElementById('map'),
            {
                zoom:4, center:info
            });

            var marker = new google.maps.Marker({
                position:info, map:map
            });
        }
    </script>
    <script async defer
    src="https://maps.googleapis.com/maps/api/js?key= &callback=initMap">
    </script>
</body>
</html>

7. Right click & Deploy the project.
8. Run file -> input.jsp.



practical 5
AIM : Develop application to download image/video from server or upload image/video
 to server using MTOM techniques

Select ASP.NET Web Application(.NET Framework)
name project DownloadImagefromws
code // To allow this Web Service to be called from script, using ASP.NET AJAX,
// uncomment the following line.
// [System.Web.Script.Services.ScriptService]

public class DownloadImageWS : System.Web.Services.WebService
{
    [WebMethod]
    public string HelloWorld()
    {
        return "Hello World";
    }

    [WebMethod, Description("Get Image Content")]
    public byte[] GetImageFile(string fileName)
    {
        if (System.IO.File.Exists(Server.MapPath("~/Images/") + fileName))
        {
            return System.IO.File.ReadAllBytes(Server.MapPath("~/Images/") + fileName);
        }
        else
        {
            return new byte[] { 0 };
        }
    }
}

then add new item 
generic handler
namespace DownloadImageFromWS
{
    /// <summary>
    /// Custom HTTP Handler for Serving Images
    /// </summary>
    public class MyHandler : IHttpHandler
    {
        public void ProcessRequest(HttpContext context)
        {
            DownloadImageWS ws = new DownloadImageWS();
            byte[] binImage = ws.GetImageFile(context.Request["fileName"]);

            if (binImage.Length > 1) // Ensuring valid image data is returned
            {
                context.Response.ContentType = "image/jpeg";
                context.Response.BinaryWrite(binImage);
                context.Response.End(); // Stop further execution
            }
            else
            {
                context.Response.StatusCode = 404;
                context.Response.Write("Image not found.");
            }
        }

        public bool IsReusable
        {
            get { return false; } // Indicates that the handler is not reusable
        }
    }
}

add new item web form

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
</head>
<body>
    <form id="form1" runat="server">
        <div>
            <center></center>
        </div>
    </form>
</body>
</html>

then click view and on toobox

Drag Label & TextBox from Toolbox (downloadaspx ke design ke ander)

uske baad boder style pe click krna h 
phir downloadaspx.cs mai yeh code 
protected void Button1_Click(object sender, EventArgs e)
{
    Image1.ImageUrl = "~/MyHandler.ashx?fileName=" + TextBox1.Text;
    Response.Write("Downloading of Image is done");
}

add new folder images
and paste save image 
and then view in browser

Practical No. 6

Aim: Installation and Configuration of virtualization using KVM.
Open Terminal & Update and Upgrade Ubuntu System:
sudo su
sudo apt-get update

Check if Virtualization is enabled:
sudo grep -c “svm\|vmx” /proc/cpuinfo
cat /proc/cpuinfo

Verify if KVM virtualization is enabled:kvm-ok
sudo apt install -y cpu-checker
kvm-ok

Install KVM:
sudo apt install -y quem-kvm virt-manager libvirt-daemon-system virtinst libvirt-client bridge-utils

Enable the virtualization daemon:
sudo systemctl enable --now libvirtd
sudo systemctl ststus libvirtd

sudo usermod -aG kvm $USER
sudo usermod -aG libvirt $USER

and search Run KVM Virtual Machines Manager:

create new virtual machine
install fedora work station and browse it
memory should be in 4 digit and cpu 2
then after creating new virtual machine show to miss

Practical No. 7

AIM : Implement FOSS-Cloud Functionality VSI (Virtual Server Infrastructure)
Infrastructure as a Service (IaaS), Storage

open ubuntu and create new vitual machince by foss server

Practical No. 8
AIM : Implement FOSS-Cloud Functionality - VSI Platform as a Service (PaaS)
then window r and type regedit
then click command folder and then new key = 1 
then edit string remote-viewer%1

the click on default


Practical No.10

Aim: Implementation of Openstack with user and private network creation

https://www.javatpoint.com/openstack

https://docs.openstack.org/devstack/pike/

In order to install the DevStack in a system, first, you have to create a Linux VM on your computer
(such as using VirtualBox or VMware) or remotely in the cloud (such as using AWS).

The VM must have at least 4GB of memory, and the proper internet connection is also important.
Here, we are going to use one version of the ubuntu, i.e., 18.04.

Follow the following steps to install the OpenStack in your ubuntu virtual machine:

Step 1: Update Ubuntu System

Open the terminal and run the following command to ensure that the system is up to date:
$ sudo apt update
$ sudo apt -y upgrade
$ sudo apt -y dist-upgrade

Reboot the system after running the above command. To reboot the system, run the following
command:
$ sudo reboot
or
$ init 6

Step 2: Create Stack User

$ sudo useradd -s /bin/bash -d /opt/stack -m stack
$ echo "stack ALL=(ALL) NOPASSWD: ALL" | sudo tee /etc/sudoers.d/stack
$ sudo su - stack

Step 3: Install the Git
$ sudo apt install git -y

Step 4: Download OpenStack 
Once you install the git, use the git command to download the DevStack from Github. 
$ git clone https://git.openstack.org/openstack-dev/devstack  

Step 5: Create a DevStack Configuration File 
First of all, go to the devstack directory by running the following command : 
$ cd devstack

nano local.conf
following line of content in the file : 
[[local|localrc]]  
  
# Password for KeyStone, Database, RabbitMQ and Service  
ADMIN_PASSWORD=StrongAdminSecret  
DATABASE_PASSWORD=$ADMIN_PASSWORD  
RABBIT_PASSWORD=$ADMIN_PASSWORD  
SERVICE_PASSWORD=$ADMIN_PASSWORD 
  
# Host IP - To get your Server or VM IP, run the 'ip addr' or 'ifconfig' command  HOST_IP=192.168.56.103  
Here, ADMIN_PASSWORD is the password that we will use to log into the OpenStack login page. The  default username for an OpenStack is 'admin'. 
And HOST_IP is the IP address of your system. To get your Server or VM IP, run the 'ifconfig' or 'ip  addr' command. 
Step 6 : Install OpenStack with DevStack 
To install and run the openstack, execute the following command : 
$ ./stack.sh  
DevStack will install the following components: 
Compute Service (Nova) 
Image Service- Glance 
Identity Service-Keystone, 
Block Storage Service - Cinder 
OpenStack Dashboard - Horizon 
Network Service - Neutron 
Placement API - Placement
Object Storage - Swift 
The installation will take about 10-20 minutes, mostly depends on your internet speed. 
At the very end of the installation, you will get the host's IP address, URL for managing it and the  username and password to handle the administrative task. 

Step 7: Accessing OpenStack on a browser 
Copy the horizon URL given in the installation output and paste it into your browser : 
http://<IP Address>/dashboard 
 
To login to OpenStack with the default username - admin or demo and configured password - secret. 
Once you login into the OpenStack, you will be redirected to the Dashboard of OpenStack. This  dashboard screen is called the Openstack management web console.

Step 8: Create an Instance 
On the main dashboard screen, you will see the instance's overview. 
You can also create your own instance in the OpenStack. Instances are nothing but a virtual machine.  To create a new virtual machine, click on the instances from the left side of the page. 
And then click on Launch Instances. Fill in all the required fields. Once you fill all the required fields,  an instance will create.
./stack.sh

 







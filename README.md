# AWS-SSO-SSM-GUI-Connector-App

This tool aimed to visualize and simplify the whole process of connecting to an EC2 instance through AWS SSM Session manager.\
The Connector App include the authentication process through AWS Identity Center.

The application knows how to receive a configuration file in JSON format for setting constant variables and also knows how to work without the file or without part of the variables in the file.\
The application supports connection to Linux operating systems with SSH and Windows via RDP.

The tool was built with full automation, which is provided in accordance with the limitations with AWS - the identification process with AWS Identity Center currently does not support the injection of flags in advance, so I had to build with interactive window in front of the user and then the connection process with SSM is completely automatic.

This tool is aimed to make the user exprience as closer as can to regular Client VPN exprience.

#########\
Inputs\
#########\
<u>Instance ID:</u> The EC2 Instance ID as appeared in the AWS Console\
Region: The region where the EC2 Instance\
Profile: The profile name you get after you make the authentication process (You will see it in the CMD window after you finish the authentication process) - In most times it's the Permission set name with the account ID number\
Instance OS: The EC2 Instance operating system - can accept Windows or Linux


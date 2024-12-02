# AWS-SSO-SSM-GUI-Connector-App

This tool aimed to visualize and simplify the whole process of connecting to an EC2 instance through AWS SSM Session manager.\
The Connector App include the authentication process through AWS Identity Center.

The application knows how to receive a configuration file in JSON format for setting constant variables and also knows how to work without the file or without part of the variables in the file.\
The application supports connection to Linux operating systems with SSH and Windows via RDP.

The tool was built with full automation, which is provided in accordance with the limitations with AWS - the identification process with AWS Identity Center currently does not support the injection of flags in advance, so I had to build with interactive window in front of the user and then the connection process with SSM is completely automatic.

This tool is aimed to make the user exprience as closer as can to regular Client VPN exprience.

I attached a full step by step guide how to use the tool - probably the first time can be little bit long to understand then the other times are fast and smooth.

#########\
Inputs\
#########\
Instance ID: The EC2 Instance ID as appeared in the AWS Console\
Region: The region where the EC2 Instance\
Profile: The profile name you get after you make the authentication process (You will see it in the CMD window after you finish the authentication process) - In most times it's the Permission set name with the account ID number\
Instance OS: The EC2 Instance operating system - can accept Windows or Linux
\
\
Requirments before run: 
1. AWS CLI Installed - https://awscli.amazonaws.com/AWSCLIV2.msi
2. AWS SSM Session Manager plugin Installed - https://s3.amazonaws.com/session-manager-downloads/plugin/latest/windows/SessionManagerPluginSetup.exe

\
![Screenshot](https://github.com/user-attachments/assets/6a5a8f97-a953-47ea-9e19-b1148e1b4b49)

#########\
Troubleshooting\
#########\
If the RDP window getting an error - try close it (the error windows only) and click on the Start SSM Session button again

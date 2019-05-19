.ebextensions script for automatically installing letsencrypt SSL with Webroot mode on an Elastic Beanstalk running on Nginx without Elastic Load Balancing 

(!) Based on : https://gist.github.com/tony-gutierrez/198988c34e020af0192bab543d35a62a

# STEP 0 :
Opened up port 443 in your EC2 instance Security Group.

# STEP 1 : 
set two enviroment variables "CERTDOMAIN" and "EMAIL" on your Elastic Beanstalk app.

# STEP 2 : 
Create a folder .ebextensions and stick the file "AWS_Single_LetsEncrypt.config" in it (don't forget to change the extension)

# STEP 3 :
Deploy your app and enjoy the green lock ;)

##refs
* https://ishanbhagawati.in/install-a-lets-encrypt-certificate-to-aws-elastic-beanstalk-single-node-application-in-6-easy-step/

# with load balancer ELB
* https://blog.alejandrocelaya.com/2016/08/16/setup-a-lets-encrypt-certificate-in-a-aws-elastic-load-balancer/

# with cloudFront
* https://medium.com/@jbesw/how-to-add-ssl-certificates-to-elastic-beanstalk-and-cloudfront-452f68591ca5

# aws certificate manager
* https://aws.amazon.com/certificate-manager/

# https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/configuring-https.html

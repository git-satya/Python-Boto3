## Python Boto3 setup on Windows10
### Install Python and boto3   
$ python -version    
$ pip install boto3  


### Create IAM user for Windows10  
AWS -> IAM -> Create user.  
Attache Admin full access policy to user.  
Download security credentials. Access key ID and Secret access key.  

### Credentials setup.   
create *credentials* and *config* files in '.aws' folder of home directory.   

credentials file:     
```
[default]  
aws_access_key_id = AK....   
aws_secret_access_key = YzKI..................   
```

config file:   
```
[default]  
region = us-east-1  
output = json  
```

### Test boto3 setup from cmd prompt
```   
$ python   
import boto3   
b1 = s3.buckets.all()  
for buck in b1:
  print (buck.name)
```













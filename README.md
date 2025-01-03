# AWS documentation for awscli with localstack


- istall awscli on ubuntu
```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```



```
aws configure 
```

- secret = dummy
- key = dummy
- region = us-east-1





### Create new Bucket in Amazon S3 (Simple Storage Service) 
```bash
aws --endpoint-url=http://localhost:4566 s3 mb s3://test-bucket
```
- to verify 

```bash
aws --endpoint-url=http://localhost:4566 s3 ls
```

- upload a file
```bash
echo "Hello, LocalStack!" > test-file.txt
aws --endpoint-url=http://localhost:4566  s3 cp test-file.txt s3://test-bucket
```

- download
```bash
aws --endpoint-url=http://localhost:4566 s3 cp s3://test-bucket/test-file.txt downloaded-file.txt
```

- delete file and bucket

```
aws --endpoint-url=http://localhost:4566 s3 rm s3://test-bucket/test-file.txt
aws --endpoint-url=http://localhost:4566 s3 rb s3://test-bucket
```






 

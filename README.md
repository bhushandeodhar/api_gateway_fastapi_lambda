# api_gateway_fastapi_lambda
Application That uses AWS API Gateway + FASTAPI + Lambda 

Step 1:
login to AWS CLI

Step 2:
create docker image with command
docker build --network=host -t fastapi . 

Step 3:
tag the image
docker tag fastapi:latest 806929883711.dkr.ecr.us-east-2.amazonaws.com/fastapi:latest

Step 4:
push the image on aws ecr 
docker push 806929883711.dkr.ecr.us-east-2.amazonaws.com/fastapi:latest

Step 5: 
create lambda function from container image

Step 6:
In Test, select 'ap-gateway-aws-proxy'
modify payload attributes:
  "path": "/",
  "httpMethod": "GET",


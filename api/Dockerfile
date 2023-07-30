FROM public.ecr.aws/lambda/python:3.9
COPY . ${LAMBDA_TASK_ROOT}
COPY requirements.txt  ${LAMBDA_TASK_ROOT}
RUN pip3 install -r requirements.txt
CMD ["main.handler"]
FROM python:3.9

#set working dir in container
WORKDIR /usr/src/app

#cpy dependencies file to working dir
COPY requirements.txt ./

#install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

#cpy content of the local src dir to working dir
COPY . .

#run app
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "88"]
First I registered to AWS and created an EC2 instance. I started the server and ran:

sudo yum install git

sudo yum install docker 

To install both git and docker into the cloud server.

I started the docker daemon by running:

sudo systemctl start docker

Then I cloned the following repository: 
https://github.com/academicpages/academicpages.github.io.git⁠

And went into the copied directory:
cd academicpage.github.io/

I built the image as follows: 
sudo docker build -t academic-site .

Then I made sure that port 4000 was open on the firewall configurations of the server.

And then ran the container as follows: 
sudo docker run -p 4000:4000 --rm -v $(pwd):/usr/src/app academic-site

I could then access the site at the following url (note http and not https):

http://3.145.191.84:4000/
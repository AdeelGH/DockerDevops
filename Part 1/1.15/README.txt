Start by cloning the following repository: 
https://github.com/academicpages/academicpages.github.io.git⁠

Go into the directory
cd academicpage.github.io/

Build the container as follows: 
docker build -t academic-site .

Run the container as follows: 
docker run -p 4000:4000 --rm -v $(pwd):/usr/src/app academic-site
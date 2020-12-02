# build docker image
docker build . -t jamamel/jama_rstudio:3.6.3

# run docker image
docker run -d -p 8787:8787 -v /home/jamamel/Projects:/home/jamamel/finwe -e ROOT=FALSE -e USER=jamamel -e PASSWORD=spitfire --name jama_rstudio jamamel/jama_rstudio:3.6.3
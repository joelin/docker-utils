docker build -t jeklly .
docker run -v /source:/opt/site-src -v /site:/opt/site -t  jeklly

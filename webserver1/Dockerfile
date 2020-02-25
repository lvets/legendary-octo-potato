FROM alpine:3.9

RUN apk add --no-cache python
RUN echo '<h2>Hello world from Webserver1!</h2>' > /index.html

EXPOSE 8081

CMD ["python", "-m", "SimpleHTTPServer", "8081"]

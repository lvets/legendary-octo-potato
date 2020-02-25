FROM alpine:3.9

RUN apk add --no-cache python
RUN echo '<h2>Hello world from Webserver3!</h2>' > /index.html

EXPOSE 8083

CMD ["python", "-m", "SimpleHTTPServer", "8083"]

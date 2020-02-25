FROM alpine:3.9

RUN apk add --no-cache python
RUN echo '<h2>Hello world from Webserver2!</h2>' > /index.html

EXPOSE 8082

CMD ["python", "-m", "SimpleHTTPServer", "8082"]

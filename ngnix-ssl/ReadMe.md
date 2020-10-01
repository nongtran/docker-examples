# generating a single Self-Signed Certificate
`openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx.key -out nginx.crt`

`docker build -t nginx:latest .`

`docker run -p 80:80 -p 443:443 --name nginx-ssl -tid nginx-ssl`
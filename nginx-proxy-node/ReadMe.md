` docker build -t docknode . `
` docker run -d -p 3333:3333 --name node-server  docknode `


` docker build -t docknginx . `
` docker run -d -p 8080:80 --link node-server:server --name nginx-proxy  docknginx `
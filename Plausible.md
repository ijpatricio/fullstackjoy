## Plausible Analytics

Reference: [Self Hosted Plausible Analytics](https://plausible.io/docs/self-hosting)

Repository: [Plausible on GitHub](https://github.com/plausible/hosting)


#### Reference for Nginx reverse proxy
```
# Reference: https://github.com/plausible/hosting/blob/master/reverse-proxy/nginx/plausible

server {
	# replace example.com with your domain name
	server_name example.com;
	
	listen 80;
	listen [::]:80;

	location / {
		proxy_pass http://127.0.0.1:8000;
		proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
	}
}
```

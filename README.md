
## ARSITEKTUR
Client  
&nbsp; &nbsp; &nbsp;|  
&nbsp; &nbsp; &nbsp;| :80  
&nbsp; &nbsp; &nbsp;v  
Nginx  
&nbsp; &nbsp; &nbsp;├── /auth        → api-auth (php-fpm)  
&nbsp; &nbsp; &nbsp;├── /generic     → api-generic (php-fpm)  
&nbsp; &nbsp; &nbsp;└── /transaction → api-transaction (php-fpm)  
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |  
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; v  
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; MySQL  



## STRUKTUR REPO  
infra/  
├── docker-compose.yml  
└── nginx/  
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ├── nginx.conf  
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; └── conf.d/  
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; └── app.conf  

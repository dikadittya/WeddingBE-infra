ARSITEKTUR

Client
  |
  | :80
  v
Nginx
  ├── /auth        → api-auth (php-fpm)
  ├── /generic     → api-generic (php-fpm)
  └── /transaction → api-transaction (php-fpm)
                        |
                        v
                     MySQL




STRUKTUR REPO

infra/
├── docker-compose.yml
└── nginx/
    ├── nginx.conf
    └── conf.d/
        └── app.conf

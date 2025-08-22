# Laravel

## Session (config/session.php)
### Session prefix
Set cookie prefix
```
'cookie' => '__Secure-' . env(
        'SESSION_COOKIE',
        Str::slug(env('APP_NAME', 'laravel'), '_') . '_session'
    ),
```
### Session variables (.env)
```
# Session
SESSION_SECURE_COOKIE=true
SESSION_HTTP_ONLY=true
SESSION_SAME_SITE=lax
```
# php
## Cacher la version de php
```
    location ~ \.php$ {
        ...

        # SOLUTION : Cacher le header "X-Powered-By" envoyé par PHP
        fastcgi_hide_header X-Powered-By;
    }
```
# php-fpm

# nginx

# Donnés(exemple: storage, public, .env)


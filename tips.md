# composer 
composer create-project symfony/skeleton:"^5.4.*" api
composer require lexik/jwt-authentication-bundle
composer require symfony/maker-bundle --dev

# serveur
php -S localhost:8000 -t public/
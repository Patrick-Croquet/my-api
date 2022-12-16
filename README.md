# my-api

# création d'un repository my-api

symfony new my_activities_api --version="6.0.*"

cd my_activities_api 

symfony composer require api

# installer Doctrine
composer require symfony/orm-pack
composer require --dev symfony/maker-bundle

# .env
DATABASE_URL="mysql://root:root@127.0.0.1:3306/myapp?serverVersion=8&charset=utf8mb4"

symfony console doctrine:database:create
symfony console doctrine:schema:create

php bin/console make:entity

Next: When you're ready, create a migration with 
php bin/console make:migration

Then: Run the migration with 
php bin/console doctrine:migrations:migrate

symfony server:start



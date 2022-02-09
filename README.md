Kabarak Timetabling
Requirements
Composer
MySQL
Laravel Websockets (Custom version)
Redis
Installation
1. Clone the repository
git clone https://github.com/Phil-Reck/unes-junior-dev.git
2. Install the dependencies
Ensure you have composer installed on your computer before proceeding. Navigate to the root of the project. i.e If you are on linux terminal: $cd timetabling

The run:

composer install
3. Setup environment variables
Create a database for the project in MySQL then configure the parameters DB_DATABASE, DB_USERNAME and DB_PASSWORD in the .env file at the project root directory.

4. Run database migration
Make sure configuration is not cached:

php artisan config:clear
Then run migration. This will run database scripts to create database tables:

php artisan migrate
5. Seed the database
If the migration is successfull, seed the database with roles and permissions and add default users. This will create two users; admin@mail.com and timetabler@mail.com, with TtableAdmin##@@ and timetabler as their passwords respectively.

php artisan db:seed

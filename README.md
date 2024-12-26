Symfony Demo Application
========================

The "Symfony Demo Application" is a reference application created on https://github.com/symfony/demo/ using docker.

Requirements
------------

  * Docker in your local system;
  * Have cloned main symfony app via https://github.com/symfony/demo/;
  * IDE like phpstorm

Installation
------------

Inside the main project root direct run 

```bash
docker-compose -up
```
Make sure to enable docker in phpstorm, and once done, you will see something like

![image](https://github.com/user-attachments/assets/fa4e00a7-0e5d-401e-84fb-ef91df40cc21)

To setup database and tables, run migrations command

```bash
php bin/console make:migration
php bin/console doctrine:migrations:migrate
```
Then run fixtures to load dummy data into the database

```bash
php bin/console doctrine:fixtures:load
```

Head back to fpm-php container, run

```bash
symfony serve
```

Then access the application in your browser at the given URL (<https://localhost:8000> by default), replace 8000 with 8080 port


[1]: https://symfony.com/doc/current/best_practices.html
[2]: https://symfony.com/doc/current/setup.html#technical-requirements
[3]: https://symfony.com/doc/current/setup/web_server_configuration.html
[4]: https://symfony.com/download
[5]: https://symfony.com/book
[6]: https://getcomposer.org/

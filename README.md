# Itamae Recipes for Nice Rails Environment

## Target

Amazon Linux OS

## Environment

* Ruby (rbenv)
  * 2.5.1 : it can be added and modified by `nodes/node.json`.
* MySQL
  * There's no my.cnf default template now (todo!)
* Nginx
  * User is changed for EC2.
  * Conf file would be overwrriten by `remote_files/nginx.conf`.
  * nginx is configured for using **Unicorn**.
* Redis

## How to

1. Clone this repo.

```
$ git clone https://github.com/totzyuta/rails-itamae-recipes.git
```

2. Run Itamae.

__e.g.__

```
$ itamae ssh -h my_host -u ec2-user -j nodes/node.json recipes/base.rb
```

# Note

* Nginx look at `/var/www/app/*` for Rails App on AWS.
* Each daemon starts automatically when run Itamae recipes.
* Add the file name in `recipes/base.rb` when you add a new recipe. (I thought its like ActiveRecord-like architecture and cool ya?)

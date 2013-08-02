#load 'deploy'
# Uncomment if you are using Rails' asset pipeline
    # load 'deploy/assets'
#load 'config/deploy' # remove this line to skip loading any of the default tasks

set :rvm_ruby_string, '1.9.2'


use_recipes :git, :rails, :bundle, :unicorn

server 'mydepot.amazon.athex.ru', :web, :app, :db, :primary => true
set :user, 'ubuntu'
set :deploy_to, '/home/www/web-app'
set :repository, 'git@github.com:dyavolick/MyDepot.git>'

after 'deploy:update', 'bundle:install'
ssh_options[:keys] = ["#{ENV['HOME']}/MyServ.pem"] 
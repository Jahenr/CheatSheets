Rails:

# Create a new application
1. If needed, install the Rails gem:
    gem install rails
2. Start a new app with PostgreSQL
    rails new my_app --database=postgresql
3. Initialize database
    rake db:create
4. Start server
    rails s
5. Stop server
    Ctrl + C

# Model Commands
1. Generate model
    rails g model model_name
2. Generate model with table columns for migration
    rails g model model_name column_name:data_type column_name:data_type column_name:data_type

# Controller Commands
1. Generate controller
    rails g controller controller_name
2. Generate controller with routes
    rails g controller controller_name route route

# Migrations
1. Migrate all
    rails g migrate
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
1. Generate migration to add column
    rails g migration Add(column_name)To(table_name) column_name:data_type
2. Generate migration to remove column
    rails g migration Remove(column_name)From(table_name) column_name:data_type
3. Migrate all
    rails g migrate

# Data Types:
1. :boolean
2. :date
3. :datetime
4. :decimal
5. :float
6. :integer
7. :primary_key
8. :references
9. :string
10. :text
11. :time
12. :timestamp

# Routes
1. Create custom route by mapping end-point to controller action
    # config/routes.rb
    get 'hello' => 'pages#hello'
2. Create all routes for a model
    # config/routes.rb
    resources :hello
3. Create route for one end-point for a model
    # config/routes.rb
    resources :hello, :only => [:index]

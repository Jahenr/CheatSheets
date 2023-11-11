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
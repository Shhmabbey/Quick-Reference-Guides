rails new URLShortener -G --database=postgresql
creates a new rails project
berr db:create
creates a database
bundle exec rails g model <table name>
makes model and migration
berr db:migrate
adds migration
bundle exec rails d model <table name>
bundle exec db:drop
deletes model
berr db:create then berr db:migrate
bundle exec rails db:setup
create, migrate and seed

bundle exec rails generate migration Create<Table>

berr db:create
berrgm AddColToTable || DeleteColFromTable || CeateTableName
berr db:migrate
berr db:migrate:status
berr g migrations CeateTableName

models are name in singular snak_case.rb
Model class should be single camel in file snake_single.rb
table lower_snake_plural

To run annotate gem:
bundle exec annotate --models

in pry run reload! true!

common migration terminal commands
berrgm Create{TableName}
berrgm Add{TableName}
berrgm Remove{TableName}
berrgm AddIndexTo{TableName}

rails aliases
alias berr='bundle exec rails'
alias berrg='bundle exec rails g'
alias berrgm='bundle exec rails g migration'
alias berrc='bundle exec rails console'
alias bea='bundle exec annotate --models'
alias rdbm='bundle exec rails db:migrate'
alias rdbms='bundle exec rails db:migrate:status'
alias rdbr='bundle exec rails db:rollback'

generate a new migration for the db
function rgm() {
      if [ -n "$1" ]; then bundle exec rails g migration "$1"; 
      else bundle exec rails g migration; 
      fi 
}

postgresql alias
alias pgstart="sudo service postgresql start"

open bash file
code ~/.bashrc

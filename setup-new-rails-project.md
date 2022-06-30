
Create a new rails project:
  * without git
```
rails new URLShortener -G --database=postgresql
```

  * with git
```
rails new URLShortener --database=postgresql
```

Create database
```
bundle exec rails db:create
```

To create a new table
```
bundle exec rails generate migration Create<Table>
```

To make model AND table
```
bundle exec rails g model <table name>
```

To run migration, then check status
```
bundle exec rails db:migrate
```
```
bundle exec rails db:migrate:status
```

Create, migrate and seed
```
bundle exec rails db:setup
```


[Dropping Migration Table, Models, Controller](https://gist.github.com/chand/3c646d7ef8f32599ea17ae37c6ebde86)

Naming conventions
  * Model classes should be in singular camel case
    * ClassName
  * Model files should be in singular snake case
    * class_name.rb
  * Tables should be named in lower snake plural
    * some_tables
  * Migration naming suggestions
    * AddColToTable
    * DeleteColFromTable 
    * CeateTableName
[More Naming Conventions](https://gist.github.com/iangreenleaf/b206d09c587e8fc6399e)

To run annotate gem:
```
bundle exec annotate --models
```


suggested rails alias
```
alias berr="bundle exec rails"
```

postgresql alias for windows users
```
alias pgstart="sudo service postgresql start"
```

To open bash file
```
code ~/.bashrc
```

# Git
### Prework
Create a new repository in github.

### CLI setup work
Start one directory level up from the project workspace.  When cloning git will create a new subfolder named after the repository to be cloned.

```
git clone origin git@github.com:<username>/<repository name>.git
```

If you haven't done so, create the README.md file:
```
touch README.md
```

and push it to github
```
git push origin main
```


# Rubocop
### Prework
We need an empty Gemfile so create it:
```
touch GemFile
```

### CLI setup work
setup Rubocop at a project level using bundle
```
bundle add rubocop --group development --require false
rubocop --init
```

### Edit Gemfile
ODIN project recommended setup:
```
source 'https://rubygems.org'
gem 'rubocop', require: false
gem 'rubocop-performance', require: false
```

## Edit .rubocop.yml
ODIN project recommended setup:
```
plugins:
  - rubocop-performance

AllCops:
  NewCops: enable
```

### From the CLI
Note: to manually run rubocop
```
bundle exec rubocop
bundle exec rubocop -a # fixes some violations
bundle exec rubocop -A # fixes more violations
```

### Rubocop notes:
Sample .rubocop.yml
```AllCops:
  NewCops: enable
  Exclude:
    - 'db/schema.rb'
    - 'bin/**/*'
    - 'node_modules/**/*'

Layout/LineLength:
  Max: 120

Metrics/MethodLength:
  Max: 20

Metrics/BlockLength:
  Exclude:
    - 'spec/**/*'
```

# RSpec

### Prework
Add a spec directory to the project root directory:
```
touch spec
```

### CLI
Run the following:

```
bundle add rspec --group development,test
bundle exec rspec --init
```

### Edit .rspec
Add the line:
```
--format documentation
```

### Test it:
At the CLI run:
```
bundle exec rspec
```
You should see output similar to:
```
Finished in 0.00033 seconds (files took 0.0879 seconds to load)
0 examples, 0 failures
```

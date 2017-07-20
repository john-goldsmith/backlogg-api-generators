# Backlogg API Generator

## Thor
Generators are built using a Ruby gem called [Thor](https://github.com/erikhuda/thor). Additional generators (such as [Slush](http://slushjs.github.io) or [Yeoman](http://yeoman.io/)) can be added as needed.

## New generator guidelines

### Folder structure
```
<language>/
  └ <framework>/
    ├ <templates>/
    │ └ file.ext.tt
    ├ bin
    └ README.md
```

### CLI arguments
`./path/to/bin <resource> <version>`

### Binary starter template

```ruby
#!/usr/bin/env ruby
require 'thor'
require 'active_support/inflector'

class BackloggApiGenerator < Thor::Group

  include Thor::Actions

  desc "Scaffolds a Backlogg microservice"
  argument :resource, type: :string, required: true, desc: 'The singularized service resource (i.e., user)'
  argument :version, type: :string, required: true, desc: 'The API version (i.e., v1)'
  class_option 'resource-plural', aliases: '-p', type: :string, required: false, desc: 'The pluralized service resource (i.e., users). Useful for overriding ActiveSupport::Inflector.'
  class_option 'docker-port', aliases: '-d', type: :string, default: '3000', required: false, desc: 'The port that Docker should expose'

  def self.source_root
    File.dirname __FILE__
  end

  def parse_templates
    directory 'templates', '.'
  end

  def git_init
    run 'git init'
  end

end

BackloggApiGenerator.start
```

### Top-level files
The following is a list of top-level files and commands that new generators should take into consideration.

* README.md
* Dockerfile
* .dockerignore
* .gitignore
* .env
* .env.example
* docker-entry.sh
* Run `git init`

## To do
* A generator for generators?
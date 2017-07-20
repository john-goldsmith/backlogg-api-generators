# Backlogg API Generator - Ruby on Rails

- [X] `rails new . --api`

- [X] README.md
- [X] Gemfile
- [X] Dockerfile
- [X] .dockerignore
- [X] .gitignore
- [X] .ruby-version
- [X] docker-entry.sh

- [X] app/controllers/application_controller.rb
- [X] app/controllers/{version}/api_controller.rb
- [X] app/controllers/{version}/{resource}_controller.rb
- [X] app/controllers/{version}/docs_controller.rb
- [X] app/controllers/{version}/concerns/exception_handler.rb
- [X] app/controllers/{version}/concerns/respond_with.rb
- [X] app/controllers/{version}/concerns/docs/api_controller.rb
- [X] app/controllers/{version}/concerns/docs/application_controller.rb
- [X] app/controllers/{version}/concerns/docs/docs_controller.rb
- [X] app/controllers/{version}/concerns/docs/{resource}_controller.rb

- [X] app/models/{resource}.rb
- [X] app/models/concerns/docs/application_record.rb
- [X] app/models/concerns/docs/{resource}_record.rb

- [X] app/serializers/application_serializer.rb
- [X] app/serializers/{version}/api_serializer.rb
- [X] app/serializers/{version}/{resource}_serializer.rb

- [X] config/initializers/active_model_serializers.rb
- [X] config/database.yml
- [X] config/routes.rb

- [X] db/migrate/{timestamp}_create_{resource}.rb

- [X] test/test_helper.rb
- [X] test/controllers/{resource}_controller_test.rb
- [X] test/fixtures/{resource}.yml
- [X] test/models/{resource}_test.rb
- [X] test/routes/{resource}_routes_test.rb

- [X] `git init`
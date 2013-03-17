# Copyright 2012, Dell
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#  http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
source "https://rubygems.org"
#source 'http://rubygems.org'

gem 'rails', '~> 3.2.11'

# Bundle edge Rails instead:
# gem 'rails', :git => 'git://github.com/rails/rails.git'

gem 'sqlite3'
gem 'haml'
gem 'sass-rails',   '~> 3.2.3'
gem 'simple-navigation'
gem 'syslogger'
gem 'kwalify'
gem 'puma'
gem 'amqp'
gem 'xml-simple'
gem 'delayed_job_active_record'
gem 'daemons'
gem 'active_scaffold'
gem 'devise'

gem 'jquery-rails'

group :development do
  gem "rails-erd"
end

# rcov supports only Ruby 1.8, while simplecov supports only Ruby 1.9. So
# pick the right one based on the Ruby version. Simplify once 1.8 support is
# dropped.
gem 'rcov',      :platforms => :ruby_18, :group => [:development, :test]
gem 'simplecov', :platforms => :ruby_19, :group => :test, :require => false
gem 'coveralls', :platforms => :ruby_19, :group => :test, :require => false

#gem "chefspec", :group => [:development, :test]
gem 'rspec-rails', :group => [:development, :test]

# These to require Ruby 1.9.3
gem "factory_girl", "<3.0" , :group => [:development, :test]
gem "factory_girl_rails", "< 3.0" , :group => [:development, :test]

#gem "foodcritic", :group => [:development, :test]
gem "email_spec", ">= 1.2.1", :group => [:development, :test]
gem "database_cleaner", ">= 0.7.2", :group => [:development, :test]
gem "launchy", ">= 2.1.0", :group => [:development, :test]

# To use ActiveModel has_secure_password
# gem 'bcrypt-ruby', '~> 3.0.0'

# To use Jbuilder templates for JSON
# gem 'jbuilder'

# Use unicorn as the app server
# gem 'unicorn'

# Deploy with Capistrano
# gem 'capistrano'

# To use debugger
# gem 'debugger'

# to use digest auth in cli unit tests
gem 'net-http-digest_auth'

# Install gems from each barclamp.  The crowbar_path variable is
# needed by Gemfile.d/*.gemfile so that they can determine the correct
# path at run-time rather than having to hard-code a path at
# install-time which may be different and therefore incorrect.
crowbar_path = File.dirname(__FILE__)
Dir.glob(File.join(crowbar_path, 'Gemfile.d', '*.gemfile')) do |gemfile|
    eval(IO.read(gemfile), binding)
end

source 'http://rubygems.org'

gem 'rhoconnect', '3.2.0'

# Helps with some of the limitations of green threads, not needed in ruby 1.9.x
gem 'SystemTimer', '~> 1.2.3', :platforms => :ruby_18
gem 'win32-process', :platforms => [:mswin, :mingw]

# use thin and eventmachine everywhere except JRuby
platforms :ruby, :ruby_19, :mingw, :mingw_19 do
	gem "eventmachine", "~> 1.0.0.beta"
	# using thin by default
	gem 'thin'
end

# for async framework
# for Async, Eventful execution
platforms :ruby_19, :mingw_19 do
  gem 'rack-fiber_pool'
  gem 'async-rack'
end

platforms :jruby do
  gem 'jdbc-sqlite3', ">= 3.7.2"
  gem 'dbi', ">= 0.4.5"
  gem 'dbd-jdbc', ">= 0.1.4"
  gem 'jruby-openssl', ">= 0.7.4"
  gem 'trinidad'
  gem 'warbler'
end

gem 'sqlite3', ">= 1.3.3", :platforms => [:ruby, :mswin, :mingw]

group :development do
  gem 'rhomobile-debug', ">= 1.0.2"
end

group :test do
  gem 'rack-test', '>= 0.5.3', :require => "rack/test"
  gem 'rspec', '~> 2.6.0'
  gem 'rhomobile-debug', ">= 1.0.2"
end

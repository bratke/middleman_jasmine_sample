# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://guides.rubygems.org/specification-reference/ for more options
  gem.name = "middleman_jasmine_sample"
  gem.homepage = "http://github.com/bratke/middleman_jasmine_sample"
  gem.license = "MIT"
  gem.summary = %Q{middleman_jasmine_sample}
  gem.description = %Q{middleman_jasmine_sample}
  gem.email = "bratke@stroeermobilemedia.de"
  gem.authors = ["Ludwig Bratke"]
  # dependencies defined in Gemfile
end

begin
  require 'jasmine'
  load 'jasmine/tasks/jasmine.rake'
rescue LoadError
  task :jasmine do
    abort "Jasmine is not available. In order to run jasmine, you must: (sudo) gem install jasmine"
  end
end

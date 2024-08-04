# frozen_string_literal: true

begin
  require 'bundler'
rescue LoadError => e
  warn e.message
  warn "Run `gem install bundler` to install Bundler"
  exit(-1)
end

begin
  Bundler.setup(:development)
rescue Bundler::BundlerError => e
  warn e.message
  warn "Run `bundle install` to install missing gems"
  exit e.status_code
end

require 'rake'

require 'yard'
YARD::Rake::YardocTask.new

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new

namespace :lint do
  desc "Lint exploits"
  RSpec::Core::RakeTask.new(:exploits) do |t|
    t.pattern    = 'lint/exploits_spec.rb'
    t.rspec_opts = ['--format', 'progress']
  end
end
task :lint => 'lint:exploits'

task :test => [:lint, :spec]
task :default => :test

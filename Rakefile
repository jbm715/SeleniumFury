#!/usr/bin/env rake
#require 'rubygems'
#require 'bundler/setup'

require 'rspec'
require 'rspec/core/rake_task'
require 'cucumber'
require 'cucumber/rake/task'

require "bundler/gem_tasks"

RSpec::Core::RakeTask.new(:spec)
Cucumber::Rake::Task.new(:feature)

task :default => :spec



#desc 'Push gem to gem server'
#  task 'release' => ['gem:build', 'gem:git:release'] do
#    jeweler = Rake.application.jeweler
#    gemspec = jeweler.gemspec
#    command = "gem push pkg/#{gemspec.name}-#{jeweler.version}.gem"
#    puts "Executing #{command.inspect}:"
#    system command
#  end
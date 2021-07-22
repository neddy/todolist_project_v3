require "rake/testtask"
require 'find'
require "bundler/gem_tasks"

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'List files'
task :list do
  Find.find(".") do |path|
    Find.prune if path.match(/\/\./)
    puts path if File.file?(path)
  end
end

Gem::Specification.new do |s|
  s.name        = 'todolist_project'
  s.version     = '1.0.0'
  s.summary     = 'Todo List Manager!'
  s.description = 'This is a simple todo list manager!'
  s.authors     = ['Pete Williams']
  s.email       = 'pw@example.com'
  s.homepage    = 'http://example.com/todolist_project'
  s.files       = ['lib/todolist_project.rb', 'test/todolist_project_test.rb']
end

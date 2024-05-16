require "rake/testtask"
require "bundler/gem_tasks"
# require 'find'

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

desc 'List unhidden files'
task :list_files do
  # Find.find(__dir__) do |path|
  #   if File.basename(path).start_with?('.')
  #     Find.prune if File.directory?(path)
  #   else
  #     puts path if File.file?(path)
  #   end
  # end

  Dir.glob(File.join('**', '*'),
           base: File.dirname(__FILE__)) do |filename|
    puts filename if File.file?(filename)
  end
end

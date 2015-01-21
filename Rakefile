require 'bundler'
require 'rake/testtask'

Bundler::GemHelper.install_tasks

task :default => "test"

Rake::TestTask.new do |t|
  t.test_files = Dir['test/**/*'].select { |f| f.match(/\.rb$/) }
  t.warning    = true
end

desc "Add or update rdoc"
task :doc do
  `rdoc lib/`
end

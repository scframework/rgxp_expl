# frozen_string_literal: true

require "bundler/gem_tasks"
require "minitest/test_task"

Minitest::TestTask.create

require "rubocop/rake_task"

RuboCop::RakeTask.new

task default: %i[test rubocop]

namespace :build do
  desc "Compile and prepare the artifact"
  task :build do
    sh "gem build  sc_ree.gemspec"
  end
end
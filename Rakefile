# require "bundler/gem_tasks"

# namespace :cucumber_rake_runner do

#   desc "STDOUT test"
#   task :stdout_test do
#     puts "String expected to be sent to STDOUT"
#   end

#   desc "Time test"
#   task :time_test, :delay do |t, args|
#     delay = args[:delay] || 1
#     sleep(delay.to_f)
#   end

# end

#Sample rake file
=begin
require 'cucumber/rake/task'

require 'rdoc/task'

#desc ‘generate API documentation to doc/rdocs/index.html’

RDoc::Task.new do |rd|

    rd.rdoc_dir = 'doc/rdocs'

    rd.options << '–all'

    rd.options << '–inline-source'

    rd.options << '–line-numbers'

    rd.options << '–all'

    rd.options << '–fileboxes'

    rd.options << '–diagram'

end

Cucumber::Rake::Task.new :features do |t|

    t.cucumber_opts = [

                      '*/*.feature',

#                       ‘–tags’, ‘~@smoke’, # Exclude tests with @smoke tag

                      'tags', '@smoke',

                      #'–format progress -o log/features.log',

                      #'–format junit -o log/',

                      '–format html -o log/features.html',

                      #'–format pretty'
                      ]

    t.fork=true

end
=end

require 'cucumber'
require 'cucumber/rake/task'
 
#desc 'Run Cucumber features and generate an HTML summary, JUnit XML and a plain text log'
 
Cucumber::Rake::Task.new(:features) do |t|
 
  t.cucumber_opts = [
                     "--no-color",
                     "--tags @smoke",
                     "--format progress -o log/features.log",
                     "--format junit    -o log/",
                     "--format html     -o log/features.html",
                     "--format pretty"]
end
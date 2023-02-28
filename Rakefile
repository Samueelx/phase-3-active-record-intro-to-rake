namespace :greeting do
  desc 'Outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'Outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end

namespace :db do
  desc 'migrate changes to our database'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed our table with dummy data'
  task seed: :environment do
    require_relative './db/seeds.rb'
  end

  task :environment do
    require_relative './config/environment'
  end
end
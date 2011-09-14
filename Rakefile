require 'rubygems'
require 'sinatra'
require 'dm-core'
require 'dm-migrations'

namespace :db do
  require './config/database'

  desc "Migrate the database"
  task :migrate do
    DataMapper.auto_migrate!
  end
  
  desc "Add some test users"
  task :user do
    u = User.new
    u.login = "admin"
    u.email = "e@mail.com"
    u.password = "change-me"
    u.save
  end    
end
    

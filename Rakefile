# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require File.expand_path('../config/application', __FILE__)

# Below is the temp fix for the NoMethodError: undefined method 'last_comment'.
# It should be removed when it is fixed in later version of Rake.
module TempFixForRakeLastComment
  def last_comment
    last_description
  end 
end
Rake::Application.send :include, TempFixForRakeLastComment
# End ot the temp fix

Rails.application.load_tasks

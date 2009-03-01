require 'jewelry_portfolio'

namespace :portfolio do
  PORTFOLIO = JewelryPortfolio.new('alloy', :work_directory => File.expand_path('..', __FILE__))
  
  desc "Generate the HTML"
  task :generate do
    PORTFOLIO.render!
  end
  
  desc "Release the HTML"
  task :release do
    PORTFOLIO.release!
  end
end
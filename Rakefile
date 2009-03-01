require 'jewelry_portfolio'

namespace :portfolio do
  desc "Generate the HTML"
  task :render do
    portfolio.render!
  end
  
  desc "Generates the HTML and commits and pushes the new release"
  task :release do
    portfolio.release!
  end
  
  private
  
  def portfolio
    if spec_file = Dir.glob('*.gemspec').first
      spec = eval(File.read(spec_file))
    end
    JewelryPortfolio.new('alloy', spec)
  end
end
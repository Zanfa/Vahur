require 'rake'

require 'sass'
require 'haml'

task :build do 
  styles = [File.read('reset.css')]

  sass_engine = Sass::Engine.new(File.read('style.scss'), syntax: :scss)
  styles.push sass_engine.render

  haml_engine = Haml::Engine.new(File.read('index.haml'))
  html = haml_engine.render(Object.new, style: styles.join("\n"))
  
  File.write('index.html', html)

  puts 'Generated index.html'
end

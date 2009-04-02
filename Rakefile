require 'fileutils'

desc "Install snipmate.vim the lazy way"
task :install do
  #TODO: No idea where .vim/ is on Windows
  vim_dir      = File.expand_path("~/.vim")
  snipmate_dir = File.dirname(__FILE__)

  Dir['**/'].each do |d|
    FileUtils.mkdir_p "#{vim_dir}/#{d}"
  end

  Dir["**/*.{txt,snippet,snippets,vim}"].each do |f|
    cp "#{snipmate_dir}/#{f}", "#{vim_dir}/#{f}"
  end
end

def cp(src, dst)
  puts "Copying #{src}\t=> #{dst}"
  FileUtils.cp src, dst
end

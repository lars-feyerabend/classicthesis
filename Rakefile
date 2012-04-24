desc "Clean auxiliary files"
task :clean do
  puts "Cleaning LaTeX auxiliary files..."
  system "./latexmk.pl -c"
end

desc "build"
task :build do
  system "./latexmk.pl  -pv ClassicThesis.tex" # -silent
end

desc "build continously"
task :watch do
  system "./latexmk.pl -silent -pvc ClassicThesis.tex"
end

desc "refresh previewer"
task :refresh do
  system "osascript -e 'tell application \"Skim\" to revert document \"ClassicThesis.pdf\"'"
end

task :default => [:build, :refresh]

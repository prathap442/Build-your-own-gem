# Build-your-own-gem
Building your own gem on a toplayer
*  For this we first create folder MAKE_MY_GEM
   mkdir MAKE_MY_GEM
   cd MAKE_MY_GEM
* Now we create lib folder and we write the necessary classes that are required for us
* under the lib/bossindro.rb   this basically consits of small code what you wanted to write and the written class should be made available in the gemspec file

_$ touch bossindro.gemspec_
      ``
      *Gem::Specification.new do |s|
          s.name = %q{bossindro}
          s.version = "0.0.1"
          s.date = %q{2019-06-15}
          s.summary = %q{boss is the best}
          s.files = [
            "lib/bossindro.rb"
          ]
          s.require_paths = ["lib"]
          s.author = "prathap"
          s.homepage    =
            'https://rubygems.org/gems/hola'
          s.license       = 'MIT'
        end
       `` 
- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+)  `Red Color` 

 #### $ gem build bossindro.gemspec
 
    Now this command will create gemspec file which is of binary format 
    Successfully built RubyGem
    Name: bossindro
    Version: 0.0.1
    File: bossindro-0.0.1.gem

# Build-your-own-gem
Building your own gem on a toplayer
*  For this we first create folder MAKE_MY_GEM
   `mkdir MAKE_MY_GEM`
   `cd MAKE_MY_GEM`
* Now we create lib folder and we write the necessary classes that are required for us
* under the lib/bossindro.rb   this basically consits of small code what you wanted to write and the written class should be made available in the gemspec file

`$ touch bossindro.gemspec`
      
       Gem::Specification.new do |s|
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
        
- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+)  `Red Color` 

 #### $ `gem build bossindro.gemspec`
 
    Now this command will create gemspec file which is of binary format 
    Successfully built RubyGem
    Name: bossindro
    Version: 0.0.1
    File: bossindro-0.0.1.gem
    
 #### $ `gem install ./bossindro-0.0.1.gem`   
 
    Successfully installed bossindro-0.0.1
    Parsing documentation for bossindro-0.0.1
    Done installing documentation for bossindro after 0 seconds
    1 gem installed

 * once these above commands are done successfully then we need to check in irb whether the things are working in the way i explain .
 
    If you’re using an earlier Ruby than 1.9.2, you need to start the session with irb -rubygems or require the rubygems library after you launch irb.
 >  
      
       % irb
       >> require 'bossindro'
       => true
       >> Bossindro.broken
       ["yes", "i", "do", "that", "because", "i'm", "boss"]
 
 > 
 
  
   Now we need to have login with the rubygems.org because we need a account with them and they give the credentials like apikey that can be used for authenticating who is the host to rubygems
   
    curl -u username https://rubygems.org/api/v1/api_key.yaml > ~/.gem/credentials; chmod 0600 ~/.gem/credentials
    Now this asks for the password and enter the password
    Enter host password for user 'username':
    
    Give password
    
  
  `$ gem push bossindro-0.0.1.gem`
     Pushing gem to RubyGems.org...
     Successfully registered gem: bossindro (0.0.1)
  
     In just a short time (usually less than a minute), your gem will be available for installation by anyone. You can see it on the RubyGems.org site or grab it from any computer with RubyGems installed:
     
     gem list -r bossindro
     
     *** REMOTE GEMS ***

     bossindro (0.0.1)

     % gem install bossindro
     Successfully installed bossindro-0.0.1
     1 gem installed
     
     
  
  `gem install bossindro` 
   does the successfull installation of the gem bossindro
     
  
  
  
   
 

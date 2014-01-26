How To Build
=====

Check out the repository:
    
    git clone https://github.com/Zanfa/zanfa.github.io && cd zanfa.github.io
    
Generate a new build.html from Haml and SASS sources:

    bundle && bundle exec rake build
    
Run a local server to serve up the html (FontAwesome won't work locally)
    
    python -m SimpleHTTPServer

and visit

    http://localhost:8000/build.html

### Developing

Run Guard to automatically regenerate build.html when index.haml or style.scss is updated

    bundle exec guard


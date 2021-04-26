pushing a site to heroku, oftern I ran into the same gemlock file problem: *Failed to install gems via Bundler*
here's a solution that worked. for me:
- bundle lock --add-platform x86_64-linux   
- gco -b fix-heroku-bundle-bug  
- git add .
- git commit -m "fix heroku bundle lock"  
- git push origin fix-heroku-bundle-bug 

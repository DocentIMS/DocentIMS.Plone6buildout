# docent.buildout
cd /home/testsite/webapps/plone51

./bin/buildout -c buildout_master.cfg

./bin/instance restart

=============
THIS IS WHAT PRODUCT DOES - THIS NEEDS TO BE UPDATED FOR PLONE 6 AND THE PROPER PRODUCTS

* install all products, including my products on Github 
* install backup:  give location as:  "Backups/<site name>" at root of my site.  Will it create <folder> if not there?  make sure it Isn't backed up on the local of the plone instance.
* crontab?  How?  define cron job.  How?() - a) weekly for backup done, b) coming soon (daily - twice/day) 
* new Roles per the site definition document.  TBD
* timezone.  (done)
* restart if not running   TBD


UPDATE FROM ESPEN:

# How to install a site

So, plone installs now with these commands

1) make a folder ‘instance_8090_port_something’
2) go (inside) that folder
3) run:

python3.9 -m venv .

bin/pip  install pip==23.0.1 setuptools==67.6.1 wheel==0.40.0  zc.buildout==3.0.1

(maybe use pip== 23.1.2)

4) copy buildout_master.cfg to the folder. 
   Edit the line that says 'port' if you have several sites
5) run:

bin/buildout -c buildout_master.cfg


6) Start Plone with 

bin/instance start

7) In control panel: Install the action-items add-on

8) Optionally: go to the 'action items' folder and restrict content types that can be added to that folder



rstudio-init
============

Quickly install R, rstudio-server, and DVCS tools on a fresh AWS Ubuntu server.

Usage
-----

    $ wget https://raw.github.com/mjr5749/rstudio-init/master/rstudio-init.sh
    $ chmod u+x rstudio-init.sh
    $ sudo ./rstudio-init.sh

As part of the installation, you will be prompted to set the password for the rstudio user.  You will use this password 
later to log into the rstudio-server web UI.

Accessing RStudio Server
------------------------

RStudio server will run on port 8787 by default.  Connect to your server via ssh with a port tunneling argument:

    ssh -i aws-key.pem ubuntu@hostname.amazonaws.com -L 8787:localhost:8787
    
You should now be able to log in to RStudio Server at http://localhost:8787.

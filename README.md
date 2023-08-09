# Autorun youtrack
Run automatically youtrack zip installation at server startup

You can download the file and put it in this directory: `/etc/systemd/system/`
Or create a file with your favorite name (will be the name of service, eg. my-service.service)

Using `sudo nano my-service.service` you can edit/add property
Make sure you set the right permission with: `sudo chmod 664 /etc/systemd/system/my-service.service`
After that you NEED reload the deamon with: `systemctl daemon-reload`

To manually enable our service we need run:

    systemctl enable my-service.service

To manually force it to start the first time, just send this command:

    systemctl start my-service.service

To stop our autorun service (it will not run during startup):

    systemctl disable my-service.service

To stop temporarly (maybe just before some edit or fix):

    systemctl stop my-service.service

Everytime we modify our service, we NEED reload the deamon.


If you want to extend this basic service you can look https://www.shellhacks.com/systemd-service-file-example/ for more information.

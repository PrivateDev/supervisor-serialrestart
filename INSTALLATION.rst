============
Installation
============

At the command line::

    $ easy_install supervisor-serialrestart

Or::

    $ pip install supervisor-serialrestart


And then add into your supervisor.conf::

    [ctlplugin:serialrestart]
    supervisor.ctl_factory = supervisorserialrestart.controllerplugin:make_serialrestart_controllerplugin
    wait_for_listen = 0 # if 1 then wait for process start listen some port
    wait_for_listen_retries = 10 # seconds to wait


# [robot_upstart](https://github.com/clearpathrobotics/robot_upstart/tree/jade-devel)

## Usage

The basic or one-off usage is with the `install` script, which can be as simple as:

```bash
rosrun robot_upstart install myrobot_bringup/launch/base.launch
```

This will create a job called `myrobot` on your machine, which launches base.launch. It will start automatically when you next start your machine, or you can bring it up and down manually:

```bash 
sudo service myrobot start
sudo service myrobot stop
```
If the job is crashing on startup, or you otherwise want to see what is being output to the terminal on startup, check the upstart log:
```bash
sudo tail /var/log/upstart/myrobot.log -n 30
```

Details:
* [install](http://docs.ros.org/jade/api/robot_upstart/html/install.html) script
* [uninstall](http://docs.ros.org/jade/api/robot_upstart/html/uninstall.html) script
# this is example from
[here](https://github.com/espressif/esp-mesh-lite/tree/master/examples/mesh_local_control)

# origin readme
[here](https://github.com/espressif/esp-mesh-lite)

# how to listen
1. in `sdkconfig` file configure `CONFIG_SERVER_IP="192.168.0.1"`
There should be IP of your PC where server will be started at port 8070.
2. compile
3. flash
4. run in your PC
`socat - TCP-LISTEN:8070,fork,reuseaddr`
5. enjoy
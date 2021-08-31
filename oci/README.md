# Overview
This module automatically creates all the virtual machines available in the free tier of Oracle OCI, along with the basic necessary networking configs. Since I didn't want to deal with installing Oracle's OCI Ansible collection natively on my machines, I also containerized everything to make provisioning more convenient. Do note that some of these configs, such as the configs in `launch_compute_instance/vars`, are specific to my infrastructure and may not work for everyone.

# Usage
1. Create a `config` file to store your Oracle OCI credentials. To create and grab your Oracle OCI credentials you will need to navigate to Oracle OCI profile -> API Keys.
2. Make a `keys` directory. Put your ssh keys you want to add to your VM's in `keys/ssh_authorized_keys` and your OCI private API key as `keys/oci.pem`.
3. Edit the variables in `launch_compute_instance/vars` to match your tenancy, image, instance hostname, compartment, etc.
4. Spin up the ansible container to provision your machines.
```
docker-compose up
```
4. Profit!

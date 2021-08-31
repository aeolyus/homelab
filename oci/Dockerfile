FROM ubuntu

ENV VIRTUAL_ENV=/opt/env
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

# Install prerequisites
RUN apt-get update && apt-get install -y \
      --no-install-recommends \
      ansible \
      python3-venv
RUN python3 -m venv $VIRTUAL_ENV
RUN pip3 install wheel
RUN pip3 install ansible
RUN pip3 install oci
RUN ansible-galaxy collection install -f oracle.oci

# CMD ["/bin/bash"]
CMD ["ansible-playbook", "/launch_compute_instance/main.yaml"]

# Overview

Popular linux distributive images repackages to have minimal requirements
for installing Ansible. This is to help automating Ansible Galaxy roles testing
when it needs to install different Ansible version.

Images don't have ansible inside but dependencies.


To build images

    ./build <dist name> <dist version>

    # example
    ./build debian jessie

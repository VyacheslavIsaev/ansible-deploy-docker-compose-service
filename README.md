Deploy Docker Compose Service
=========

A brief description of the role goes here.

Requirements
------------

Host is enable for docker-compose services.

Role Variables
--------------

service_name:   - name of the service how it will appear on the host
service_host:   - ip address to check open ports
service_ports:  - dictionary of service ports to expose
service_image:  - container image to use inside docker-compose
service_environment: - dictionary of container environment variables
service_volumes:     - dictionary of service volumes to configure

Dependencies
------------

No dependencies 

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: ViacheslavIsaev.deploy_docker_compose_service
            vars:
              service_name: "ServiceName"
              service_host: "{{ansible_default_ipv4.address}}"
              service_ports:
                8181:8181
                9080:9080
              service_image: "{{service_name}}:latest"
              container_environment:
                SERVICE_NAME : "{{service_name}}"


License
-------

BSD

Author Information
------------------

Viacheslav Isaev has two decades of experience of distributed high payload systems development. He has been in charge of developing control systems for safety-critical facilities like railroads and particle accelerators, high-payload event processing systems for cybersecurity and mobile access points, introducing in house CI/CD practices. His hands-on experience incldues all stages of IT solutions development and operation. Vyacheslav’s interests lays in automation spectr either it is pure software or hardware-software solutions. Vyacheslav defines the key to success in 3 pillars  Domain Driven Design, Behavioral Driven and Test-Driven Development, which are standing on the foundation of  Object Oriented Design and Clean Code practices.

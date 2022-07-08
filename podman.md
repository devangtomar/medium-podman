EXPLORING NEW TECH

**Podman (An alternative to Docker !?!) 🦭**

What is Podman? 🤔

Podman is a daemonless, open source, Linux native tool for finding, running, building, sharing, and deploying applications that use Open Containers Initiative (OCI) Containers and Container Images.

It operates very similar to Docker and is simple to set up.

Containers can run as root or in a rootless manner.

Documentation : <https://podman.io/>

**How different from Docker? 🐳**

The primary distinctions between Docker and Podman (Pod Manager Tool) are as follows:

- **Daemonless** — *This characteristic distinguishes itself from Docker, which executes operations via a docker daemon. Podman is lightweight and does not require an instance to be active at all times in order to execute containers.*
- **Rootless** — *Podman can be operated as root or as a non-root user. We can run Podman containers as non-root users while being compatible with container running.*
- **Pods** — *The word Pods was coined by Kubernetes. Pods are groups of containers that run as close together as feasible. Podman includes this capability by default for running many containers concurrently.*

**Architecture 🏛️:**

**Many individuals still refer to a “container” as a “Docker container.”**

This does not accurately represent the existing container ecosystem. Docker generates OCI container images that may be used with different runtimes. *Kubernetes is one such example, as is Podman.*

As a result, the essential functionality of Podman and Docker overlaps. Both generate images that may be used to run containers by the other. On top of the basic containerization functionality, the two runtimes provide their own specializations.

**Setup ⚙️**

And as it’s OCI-compliant, Podman can be used as a drop-in replacement for the better-known Docker runtime. Most Docker commands can be directly translated to Podman commands.

Simply **put alias as, ‘docker=podman’** on your machine and you’re set

Installation of Podman is pretty straightforward over a Mac. If you’re on other OS, follow this [documentation](https://podman.io/getting-started/installation). WSL over Windows works.

Request admin access from Self-service app and then open terminal. The Mac client is available through [Homebrew](https://brew.sh/).

brew install podman

To start the Podman-managed VM:

podman machine init

And then

podman machine start

Once the installation is complete, you can then verify the installation information using:

podman info

**TLDR 📌**

As stated before, Podman is just an alias for docker. Whatever commands you can execute with docker, you can execute with Podman.

**Building an Image**

podman build -t “containername” .

**Docker file :**

**Image building via the command :**

podman build

**Push Image**

podman push “registryname/imagename:tag”

**List images**

podman images

Command screenshot :

**Run container**

podman run “imagename”

Command screenshot :

**Remove image**

podman rmi imagename

Command screenshot :

**Show Podman process status**

podman ps -a

Rest of the support commands is shown as below :

If you use docker-compose , there is an alternative for this [podman-compose](https://github.com/containers/podman-compose).

**Note :** Natively docker-compose is yet not supported by Podman yet at the time of my testing of Podman Release v4.0.0 version. And the one available is very unreliable.

The setup is straightforward. Install Python if you don’t already have it, and then podman-compose.

brew install python@3.10pip3 install podman-compose

Podman in conjunction with podman-compose works well.

I’ve had trouble getting podman-compose over Mac because there isn’t an official document for installation other than the one mentioned above.

**Conclusion 💁🏻‍♂️**

Podman wraps around Docker’s capabilities to provide a lightweight container runtime that can be used in Daemonless and Rootless modes.


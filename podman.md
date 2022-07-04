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


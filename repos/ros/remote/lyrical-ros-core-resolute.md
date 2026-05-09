## `ros:lyrical-ros-core-resolute`

```console
$ docker pull ros@sha256:c56ac343fa97862e38b58a098c606573bea79b7922add04090676d1a08f85edf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-core-resolute` - linux; amd64

```console
$ docker pull ros@sha256:82aa0cda98eab0df52ef080f8387daa8e406eb0e0a9546a15a69f6377733d029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188466326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac5db437362b6daab8a68ebe5a455bdab6fccfb73ba453b7332fb3977934e4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Fri, 08 May 2026 22:59:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:39 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 23:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:28 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 23:00:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 23:00:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58fc8dd5a66dc7fa8b8c570fa7912cd1c0d64d137d2aa56def7154e90cf727b`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 740.5 KB (740458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feca8694738697c1567a29afc471a4b7ea676c3eddc5759f9263533970f2f16`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 9.8 MB (9823544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922240d09f956ad29b9fa276615b85985d409423150635bb69c069cd5b23557`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 89.6 KB (89556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0b6b69c6e422a26e80d97a17324c51f973ec6ef420d6aba5e4f7d584849c2`  
		Last Modified: Fri, 08 May 2026 23:01:10 GMT  
		Size: 136.3 MB (136257322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b86f409736327ea3469de3310b97135181291004f0273e763aea3cb96f6b794`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:eb46362455c4113d7895b0d1e6f0456499f1371be26e115ce317b93337eccf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22640304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6230aa06d1c826e706389a1870ed6c999bda4f9928e779de7143eddfcacafb0`

```dockerfile
```

-	Layers:
	-	`sha256:25fac0a70e1f25b7ce71e4c5cee97e5aca2b8212309e34ee96fc331b2d384a22`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 22.6 MB (22624638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e3389d5c21f95719680f1f7aee20a78bc1f0b1894867d1187d62ad83f9e702`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 15.7 KB (15666 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-core-resolute` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b7ada19442522356c41068b118d09779c23b6378fa0c62a1eda69e1778432a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180883012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43557dd5db2663de83be96d768e175ca14caf53c167390b08106a510738ba0ac`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Fri, 08 May 2026 22:48:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:00 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 22:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 22:49:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e85634d1fbebf47d4daecf57083015fec4d5e485c1672a194d0ea711fa89a2`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 741.1 KB (741149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354d4deb457ddf1c54c92b584b50e1d8c4f6fc494cbf5fad0095d18627edc58`  
		Last Modified: Fri, 08 May 2026 22:50:28 GMT  
		Size: 9.6 MB (9647454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e37e3b34a50099f4c08800cbd5d3901ef914cbcf05d8d305b5404f0f833461`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 90.3 KB (90294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8803f3bbdab9cc7b7ea61c314b1d91a491f614fceb1bdb9620b41d8f27fcf`  
		Last Modified: Fri, 08 May 2026 22:50:31 GMT  
		Size: 129.7 MB (129674576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd39f44e283c4ea1d22ea3fdf9f08689d73bf11fd40ca5a59259aa3648f8063`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:b6100031a7e8e5dd64fc8906212a49b5eb3faa34f85d0a886449f01d8649ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22613122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273948cc2e96b5ce4e6eb43e0311b063a8142b0b5edd61c6f6f2093cdb1ee085`

```dockerfile
```

-	Layers:
	-	`sha256:346f29057dc412460266bcc5190b7124bacade959410d25bd2e7e4a07998c1bc`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 22.6 MB (22597330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a7cc396851c248c045d334cb5a5bb84f21c0f07c6c2a1b8808232ab344328a`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

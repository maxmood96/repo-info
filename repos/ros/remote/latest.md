## `ros:latest`

```console
$ docker pull ros@sha256:b1f52aa94aee73f004225d88622ed2885e2ca4793f4dc8992710438cfe9b0269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:ebffd7c6adcde3c6303f0632eb2a3bbefa5277c687189d4b43fbb2eaf7c47b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339655385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8685d999868b860c00cc60c45c93198a60605418fed94cb0a6d88d33993ac189`
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
# Sat, 30 May 2026 00:27:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:28:19 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0a66e0e4ba2827013cfdb6d7d0277845dd90d29cf5be6f6b1a2edb35b35b8f8f`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 740.5 KB (740466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d768bea23ca17d73373bced93b07f016d49dc73083020b677ca88820b6e206`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 9.8 MB (9817877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d56e888694023b5e25084b3279db49e8acf8dd01b333bc892018778ac0b6217`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 89.6 KB (89573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568aec1aaa0eab51b8b82e80be56f21f3b816a67df5322fffb3616f28e0eaa6d`  
		Last Modified: Sat, 30 May 2026 00:29:04 GMT  
		Size: 136.5 MB (136498683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27deaf91b06f9331b9e482842dd053ce65d106daab5a1476638159a380ccdeab`  
		Last Modified: Sat, 30 May 2026 00:29:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf73fcb880fdad57bb9149fe62bb72bc7699322651dd7861846cc93bf6d4cd8`  
		Last Modified: Sat, 30 May 2026 01:14:39 GMT  
		Size: 124.7 MB (124738161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb98ddcadc581f4284f2401341e74d96eeb4a8b0c0cffa70f0027f78d6717859`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 374.9 KB (374916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dca66423f9da379a39cc77d5c07fe0ba0b022d4a9d0f0f1bdf2f74d6b68275`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 130.8 KB (130835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf504e38ad1b753e11ce22c64c2a1292309176deb0360051f00e3b8d011be59`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 25.7 MB (25709430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:ac13d7c667b3e5b5923e550e6c2924f5d3c66db47111f71de5619557196f55c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29150209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489aac56c60fb12f8ff1e1fccc2da64c1983bcc15fb126fb83dbe38d8476897b`

```dockerfile
```

-	Layers:
	-	`sha256:87b27261aee59a095152f7795ec83a54620eca7d4a9a58a9d4769d929d59fb4f`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 29.1 MB (29132760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d510f4666455834694e12ab4639c3f662718b503a8cfa4459249fdd8723a95b`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 17.4 KB (17449 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5a1c58d9707d8638e25295ecffdad6b0569163f89e741eeeb1ca46b7cdda0b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324407583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf262eb9952e8435db3c947512095d094f11144f0190a1cd6e28d9ce606136f`
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
# Sat, 30 May 2026 00:26:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:46 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:27:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:27:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:27:47 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:adc2ad364c506093b49a14399caae9c415d779931557582d1064c20883556f3a`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 741.2 KB (741165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f72c9d5baed137ff572cc6144d1b1c3ee48d9da3e8ec830a0a2b85445a8bf`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 9.6 MB (9641306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37666b6096b138cbf3a42a8c82ab2e084f00595ad4f69a0d0541a2255a450ce1`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 90.3 KB (90277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44192943d5ae755decbe581424aa597252ca509537720b2177b1dabb1ec588a9`  
		Last Modified: Sat, 30 May 2026 00:28:29 GMT  
		Size: 129.9 MB (129891737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f43a2870356aaff3f0fdef23de031b83b26a6a66afe29f02ed3cdaf6285b0ea`  
		Last Modified: Sat, 30 May 2026 00:28:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febeea5348f53a21fe0cc3e79465fbb577084e2a5245c53b4f19de2fbc6dd77`  
		Last Modified: Sat, 30 May 2026 01:14:36 GMT  
		Size: 118.2 MB (118153757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69509140db50f8e6085dd132443c50152cb3b18cbb37424e9e337f0cc9039c9`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 374.9 KB (374930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f65f07e25403ce1a636329c36ec386befaf8605da702e491c52ccb2fd1552`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 130.8 KB (130836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051992ea02b83d9b9d3abce9d9a9297bc29e5518b3d5bf9264b784bbad059354`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 24.7 MB (24654035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:aceda4a3c59c3da902d23035f92a710b56e9420ce4e7843e7ea1f20edaa7356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29214989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48992051392bf1b5555fa9ccd291800d9f7a47248d24fd60048e1e69a374f43c`

```dockerfile
```

-	Layers:
	-	`sha256:f468707c5422a2ffa2917b8a68997e6f8b3aef41168edabfee6f356c792a4545`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 29.2 MB (29197390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e0f3ffb85f88f59189d315ffd3b001b4f237eb6214a12175d74eca17c4d2460`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 17.6 KB (17599 bytes)  
		MIME: application/vnd.in-toto+json

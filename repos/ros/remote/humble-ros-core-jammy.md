## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:6692e2470f6f2ff0b35190b695ca6129345f6981bb53da62d91fafb3e982ceac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:a115d56b8bbbfd9f7f95e3b8c40da8a677403521a514386ceb7bdc48e18a76aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141916625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe11fb97e089bf8e581566803823aa40d2d1b629dbb84d89579009b61aba8d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 20:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8e3ada8f618169b57768a6e62adc5b4af07d0209a93f1fdbf6ef8ce8479f1`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 1.2 MB (1215547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358c4c08448ffd11c0958b21ecd32e6379061f941d586cf4c76a28ee837809`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 6.0 MB (5994365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf96e61ad269ae729e2d85ef0baba1d0e8a2a8b8793c365d1e4fbeb6c5509b9`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 97.2 KB (97163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4858fc5748850341f9a6eb1c5fca3016eda83db7833c5b56a64c261d1e619f`  
		Last Modified: Wed, 15 Apr 2026 20:55:13 GMT  
		Size: 104.9 MB (104872855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd7919b7abedda1fa31f5bf8a06f4007ba2ab1d6c9fe37fd4433cddc2f5e0d2`  
		Last Modified: Wed, 15 Apr 2026 20:55:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:6629137527899e2d686ca245175881accb128d96bea80b6e4819ffee14ed6767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17817501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e55a0caf0d52b742cace530a80d8332ba22b3066adb296aec162298bbed4f4`

```dockerfile
```

-	Layers:
	-	`sha256:79794308a686f8f07a4cf67445e845e0688932249c15cd56d1dae88115b25ee5`  
		Last Modified: Wed, 15 Apr 2026 20:55:12 GMT  
		Size: 17.8 MB (17802889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f87e84b20dd3533c31e8c940cdcfe1155a139d26860bdb4d1dee7c1ccfe11e`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 14.6 KB (14612 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:55d9908102dd6ff2d2184aa9b0c4e8a51e91117b42304f781a0f44ef0236e1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137493180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe4e59fd18c89523d45efb0bfac536f00b854d6abb82ddb802113c34bd79878`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 21:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2a0a46477190f0fa6eb8e1e24937a7a892a2da4dbfde5fedbff1165bc202f`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 1.2 MB (1215780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3d402648b828b47f89d64b7e7e7aa20ed8278ae37c701230808b7ff6266b`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 5.9 MB (5948659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1a9f3d6434e09d0c3553ce1602fdaa06bf41a5cb1e81eaba5d388ef3f9e73`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 97.3 KB (97282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2a633b06933c84562c54062201c1d1e0115d0309e004101ca6f8bad53e75e`  
		Last Modified: Wed, 15 Apr 2026 21:02:41 GMT  
		Size: 102.6 MB (102624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd5ee001a0f676fb3515f3e51de0d6d59ce44b9ed65795991b7dc06bc652dcb`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:311ea494555619bde2709c2f93d4965b663c4176fabc2849697d12b365222d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17803973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58206d88fcbae8b27c8a7dbbedf203c85d091d7a2d48717eb15bfcc130a47feb`

```dockerfile
```

-	Layers:
	-	`sha256:afb861e8bd8684f76b4fa477b37bc36fd2c4766e39a917d8bfa8e9b3dc916718`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 17.8 MB (17789234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647ff0c8d1a703bc44c581bbf630b1ea86e9bd916a7adb386b722a0210413120`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

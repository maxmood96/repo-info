## `ros:kilted`

```console
$ docker pull ros@sha256:09fc4eafc58d55baba80fa2179761af87a1a24586c88049e5a2f2a76215b2071
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:711c35fa022e029585c6bd0445cd4e90a64d147945e93f0d17e8658dada9edf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296822799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f3e53ea06654ca18393a63c24bf43ef1f2273575e6b31000eac328d06b568`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 20:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:54 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1e8c88b55de7bb95fc86629c092b8ee1185957ce194ca3e8c032521218d23`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe78e730b0bc01704683bee8ea5c7144c34bc29d7f64e8f86e0fd3581c744d`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 6.8 MB (6751659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05bcb8e9e38af2e16e36258cd57336a7d9f443d029737a994e0cbcde39dc7d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 94.1 KB (94108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8e25e7760a7f86e056446fe983fc96739a4cbc9010d4e8c16779f7f1ebb51`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 120.9 MB (120908551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66fff459f77a979cc988155538d6cd842c44afec85e542f5659cee33be6ed7a`  
		Last Modified: Wed, 15 Apr 2026 20:55:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b585e3d82ffce0664bce0c8a5cd547fab5ca89e846fcded5bfdea2945c92b0e3`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 110.2 MB (110194522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d9e768ed960260076e36fb5349f0f2bf428da3dd7ca881955f651442db85d`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 379.8 KB (379842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f42645bfe1400d71c15649094acea6a941875adfdfbfdcdf5da5a0cf7329e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b740609d32d16cf76c7d87805eff7096e854a1b987b669162d4caf38ef205d04`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 28.1 MB (28074461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:d5936346f135b582a261511d5983f9753ba160d0e43bb40ab9f5197266174b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd670b4353b1ad937dc8af910e89de70ce1a49678f9e5b3e4dce0f1951471a64`

```dockerfile
```

-	Layers:
	-	`sha256:420c0d5f20dafba09120bcbd505d4a20dd050524f990d868e4ef6c8fae194468`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 24.8 MB (24750608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d4c3744b9b9428d48825b5d40907bd738a9f30e5032264b201a51cf55221a6`  
		Last Modified: Wed, 15 Apr 2026 21:46:51 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cf195d400ea1b9522336650a09081c2b9bbd58c4567abaf065ae033d6c461831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285201575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e0b5a1092889590aeb2db6c88a896e4c0ec19dea93f92f768959ffdc096016`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:03 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 21:02:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:53 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f0a2684d9babfb3177690b0c4a2b1ff0db4cf333b9a4f77b7eb9e6f53a0b5b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff337ea7733134af43106880ebb5e900603a2b5e4bd370721d73a7a25a8a3b86`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 6.8 MB (6765008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c6d8e1bd0a4b9a42f8763d22cd8574e5086ed2804ba50f19de93f76d72e0b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca663cb32814a19e937ea07bd86b12869cbb41a47cc848ddf0559c75b785cfa3`  
		Last Modified: Wed, 15 Apr 2026 21:03:25 GMT  
		Size: 115.6 MB (115633032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb611bb0edd49e965a3a9b4f6c4c6dc8471d483595597dd92e232531e2c6d27`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005d2616fb0134c4e667bf18779a12515e093b7032480fa955cae8082b1ed00`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 105.6 MB (105606696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c761530a5f45bde84b650345ffc0508fcb42841ff5090e705b63da0fe1389fdc`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 379.8 KB (379849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf27eb0b81b347de06b64c5b5e76195336cec112119695b36d7718b2e4e07b3c`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 2.5 KB (2545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c00b01c95a9e75af81929c29b402746eb47e5ae30c7836299919af679dc2fe7`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 27.2 MB (27159941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:a574bc9e18529c423a7eed4fc7c73966ca33d7573d7547e9c5fcd2d59ffdc36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37c1c3d7e653759b7faf430a8ef65f87120f742604c33691af856b141fe6b90`

```dockerfile
```

-	Layers:
	-	`sha256:a70c674dcb660d44b806bb08907a34c2fb46f5a40eab10a7b9b0b205bb907724`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 24.8 MB (24772870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655d938644d51b7909a0fc104ddd54b1fd9b8353f9a4d630fcfb58e3840172eb`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

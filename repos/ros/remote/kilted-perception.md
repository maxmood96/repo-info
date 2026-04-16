## `ros:kilted-perception`

```console
$ docker pull ros@sha256:2055c0120e6fd8d6662c450fd8c9746c349a0d9c6e1cce3030f852d06618bf27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:dd682ae4e08bb96dcfc6dff6e2bca25ea3915154586f7ab6aab30058e6315fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081432609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7348d9cf4178bc7c9ce2dcaa5d5fb7a497c176f829241f6462de5f9a8bb79cb2`
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
# Wed, 15 Apr 2026 22:29:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:79e1a4f7ac439011b9742367eb967d6d84afb4296b45e3baf0177fe657416ca4`  
		Last Modified: Wed, 15 Apr 2026 22:32:59 GMT  
		Size: 784.6 MB (784609810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9bb1691b6c8bda914acbde13ac6e67853cf23b1094802c42378bcb5e1e0c463e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60936687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d1b39c7bc48d12c18024b0a74e66445fcda50e21c5a68c36fa019a866f21f9`

```dockerfile
```

-	Layers:
	-	`sha256:1e278c0f0f182591f8ab3e55bc03fd20721793f3459a8420f332cb17ff93fbbf`  
		Last Modified: Wed, 15 Apr 2026 22:32:42 GMT  
		Size: 60.9 MB (60927336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed143f06f6ccc96627a9fdae7240f16c6ceae5e0e1b251818da1e86386b44b88`  
		Last Modified: Wed, 15 Apr 2026 22:32:39 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:37c7a50cb69db09a48cdef703cf232250801a6a3f84754f6d5ae51ff0e9c8460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.0 MB (983992526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1fb1c2968fdba99837795ed9505a8e58e91e78fa4fbac541f06a69032bab14`
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
# Wed, 15 Apr 2026 22:37:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b6bb2d57d9b6531470bcaa5ec13f20c40e645ddb5ed8bf5f6ed3d0d0fc1e9e16`  
		Last Modified: Wed, 15 Apr 2026 22:40:48 GMT  
		Size: 698.8 MB (698790951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:164b7cebbfd5cbb0aebbe7662898de3b590171fa7a6c8ddaeb6abf9d0a7fe993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60867289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0613531574d30ce6d022b0641b1d53dc85eae0100a098dcac0962b8386960`

```dockerfile
```

-	Layers:
	-	`sha256:e0346651bfe269c2ae312325647afa7b3680071fb67669c8c98a3aa8961a8603`  
		Last Modified: Wed, 15 Apr 2026 22:40:29 GMT  
		Size: 60.9 MB (60857857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ca0d0c0395f7fddc186c9cf92000b993cb743201673e179aca9ebc46f2b612`  
		Last Modified: Wed, 15 Apr 2026 22:40:27 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

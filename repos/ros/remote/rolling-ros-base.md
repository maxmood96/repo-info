## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:03b21c7e02310c36ee67989187b761b650208ea92eca94845d26c1bb75d8ab5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e739313b7d2fb1ababd2d333fcdaa84448209b4a3ad36787ac2e6ffab04f7d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312088168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4aab199b4141ca03f141b6644020bab6c2223e12fdbda6c8ccda5736d27363`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:54 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:15:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f800b8b948e2673ed8a226bf87790ce00fed571ccb6c4b173a0cabcca72ffb`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 684.1 KB (684097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1a9e9cde4587bd6cf0f5b0fabcf7d3189d45eccf2f222d367ab918b3546d4`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 6.8 MB (6752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56d831ad55abb49cb53e65cfd1ad9fd5d4fba9814b9ac9e993e50f908fb4da`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 94.3 KB (94255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade12bd0c8da06f9f8cffd3821b01ad33941d8191f1c43b9e32d410c172f35fd`  
		Last Modified: Tue, 02 Jun 2026 08:22:26 GMT  
		Size: 136.3 MB (136275173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36b877151687a62b70993e03d67da073122fab5b4b321e63db93e2c5edbb8`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd736e314821ca6bc39a29747a5901b7a4af9de87fb942b611e0eeb21b5855d`  
		Last Modified: Tue, 02 Jun 2026 09:15:57 GMT  
		Size: 110.2 MB (110198452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3b1b218c3c81f3b6bc9604076e4bd565ec55459d589870fb537c3af1bdaf51`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 375.5 KB (375530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fac4062e9505018fab524f3cb6f79a11f076f20fe34b6b7d2ee7573afc44551`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0a696c577f262fe36d1b033fc3f465aad16d27f2e23aa7448c628ee5d60043`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 28.0 MB (27972755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:6896fdacf0d2ed99c41465e01a2b9663fc1dbe8b67478bb20996eee99c71b021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25802586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61545d37d677be67efd0aa52a4a770e60dbcbf3c0b2c0eccbf5287805c6f2c7c`

```dockerfile
```

-	Layers:
	-	`sha256:c18f77d29bb3b6f7ef6442d42c08ab1aea1c0fc3796da25a61a1219225453ab2`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 25.8 MB (25786221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0309052d34ad4f0de264afd8c42f98e496616d63fe0f4294f92430ebbf301f`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6db8780587ca47c71f3f865077964e095c8cd49199fc02bb153484457d3a0c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 MB (299989403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf4c9099568efccdcdf9ce529975fb469621983c0f9878105e51db2bb9ba730`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:29 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c406762b81207255596e095cf975ba8240b31d52ee968dcc75f4c880d0502f`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 684.2 KB (684226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9fba424e9faebc1fe6f68dd31bd1d59510a0e267a489cc349d57160dc34e1`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 6.8 MB (6765708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8afafd31ec8c2a476944df80ebf75303ef613b85a1c437fcaefdca4a63062`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 94.3 KB (94344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbcd5fc4c1de0dd8f6a5aa0049688a282ae87bc3d8662fc8c7c043e9a20701a`  
		Last Modified: Tue, 02 Jun 2026 08:23:03 GMT  
		Size: 130.5 MB (130503862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca7c1cb0e994f3341efba4e27156f34adb46f0efbda2c5ce962c0235a4f7a3`  
		Last Modified: Tue, 02 Jun 2026 08:23:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3839ccbd60cd31fb7491524fb550bd15c57e5c7487e9e85fe75dca92838d1362`  
		Last Modified: Tue, 02 Jun 2026 09:24:31 GMT  
		Size: 105.6 MB (105612317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408525ea7965dba176c91032bc80beea1aae6417206f14d57e6bf0420ed93d88`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 375.5 KB (375527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f00ad1e48967daefe8d637096d70964af44fa44de59419ac56ab3e54eb48bf7`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997608089522005e479a4c0a53a53e6d8e975347849eadd7f98e57f76c100066`  
		Last Modified: Tue, 02 Jun 2026 09:24:29 GMT  
		Size: 27.1 MB (27074294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:bea2e9bc3c8dd4630f03bc02e7231bdf379122020b132bd7c631c65d903a1bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25825186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f70f9e2b593a0a58973922a8bfd23e60a442988a0e8bbad08d6a949f0894cd`

```dockerfile
```

-	Layers:
	-	`sha256:58debcdc1f44dea30a1bfff9a3d47cb8e226d66a8dd5bf6db5f6025f594f1592`  
		Last Modified: Tue, 02 Jun 2026 09:24:30 GMT  
		Size: 25.8 MB (25808685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff13e2379f5b668bcc731262f9ee6f02e993eb3505523741b9d0a608a8e328c`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 16.5 KB (16501 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:bc2b66a6b3694342fdb3d2190bd177e64246d1230451bdea0f755b9f8e3b4aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:f1b0743fb61ffd9855b5754ad20f9a8c383968540bb9530aeb89e3099da85a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1097074076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e272916a7f18110877463cb7d689674cece7253a95639e319d8c70b539c6710`
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
# Tue, 02 Jun 2026 10:18:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:10f52f1fc65b742ea6467b319f1e26ef6baa33b5d627f2e71ca5e0fc3df40399`  
		Last Modified: Tue, 02 Jun 2026 10:21:29 GMT  
		Size: 785.0 MB (784985908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4d866617f63dba25ab2e59589373c8c95a63a8ef93daa176c812a847146a0965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62001217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf3f39c292ad065810fdd916c893d4650a8aeafc66c9b29e5f6120aa9dc58c5`

```dockerfile
```

-	Layers:
	-	`sha256:2a413eacac16155396f5c8625ec4200d78c227cee0a45ed37b41c4244a36cbcf`  
		Last Modified: Tue, 02 Jun 2026 10:21:15 GMT  
		Size: 62.0 MB (61991856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddde8e6390032bba8f86ffb5fe4e146d8dbf5366113ca674146934bbc12f7197`  
		Last Modified: Tue, 02 Jun 2026 10:21:13 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bad9e79fb2cbcaf7f53918b8b1bbc137331a7b0eecaa4dfa0474aeab5bc20466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **999.0 MB (999046831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91b104156784613163df70793d325052fcb8c3a29da8b9986d2e520ae3e553d`
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
# Tue, 02 Jun 2026 10:14:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:85be6d70f44bad3511541dabf046edcf2f204b5b4faaac2b2c31573b2168705c`  
		Last Modified: Tue, 02 Jun 2026 10:17:45 GMT  
		Size: 699.1 MB (699057428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fe6a69401efbc91ab497bcc79b9bf3b02b275ce13587d2b3eeb5f50240c57ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61932025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e03f6a64d52e42d51414d0a82d65ba94b91ff3a9d9e9966035c043f029733e`

```dockerfile
```

-	Layers:
	-	`sha256:0d5874db2ea2182eb2d18f0e3f894586dfd29b072b374f4d0589e5ef799814e6`  
		Last Modified: Tue, 02 Jun 2026 10:17:31 GMT  
		Size: 61.9 MB (61922584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e5817acfdef624d182bacfbf40158bb2f4d275f63541ef8634620c390f237b`  
		Last Modified: Tue, 02 Jun 2026 10:17:28 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

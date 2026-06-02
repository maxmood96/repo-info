## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:aa3ab3073d7177076615213f10b652627c6d00fbdb0d2da9bcc27ac7c90fa98a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c6b5b6f1c66aebbacbc5c353e81015bc57dadbd5d475fb104d776ee4116c7b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173538927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4875753e5835c960a46aef181ea2128b03e417965dcba92dad6f77272cf77553`
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

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d4f68316c56c147462afa7bf298b00ca522168bb13eec158acb81bb8fead26f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19552455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be959f2f4be6a2822447a1135ed4c269cd412660c8fd7a054688aa3196483c`

```dockerfile
```

-	Layers:
	-	`sha256:f15e97baa0d7e5608b7f0d05529776e537cf01a674edb3c07271e48009d8685f`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 19.5 MB (19537834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dddafaab1c7897d4058001a906c1601b50b7819f87b8a3a1a75961adc0d3ec3b`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:de1b758c206e05882d575665a5f0dffcef987389fa1f6c3a6c2f2b3880955590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166924741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd92305ff7d2f376f1cf94fe2e09513ff68c3e29a29cc96b41642df2f5972d2`
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

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:db3fb153c03aeca727af415fa3ff6fbb4811a249ce800fe942fa6b9a51ce7fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19526797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d42897f458d7fa6bc0ef2ddcacbd4919d5729988df8aa7c3b88fa0f9061bc4d`

```dockerfile
```

-	Layers:
	-	`sha256:dadfbd9b89532e46b66a4dc7677f0e98ae95435671bc86c9075c0d27146cfde6`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 19.5 MB (19512050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9176903f26887f1209af2993320caf7a750a657e7cc5b48ad683d1277cd2050`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json

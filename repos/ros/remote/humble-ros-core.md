## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:6148c7f47a9675737a01831de25a1fc2a07cbcb55c6cd6e8dd13c830b05c9b33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:11c70a102287b0592d9e9b5fabeedc11615fb3b301ce4692f793298f546a3163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141545723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80abeb3297c13c98c0f836eb2184377b0f524882f80b8ef34dcc60bbb11d3e1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb36daf1fd72d28fa8ec7db41232743c3310a7741ffbc8152bffda0ad41ef11`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 1.2 MB (1214126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd385ae5eca81d51f71602ffd0c89d6ae513071108777acc462ae236d556c3`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 6.0 MB (5993180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ffd6227ede7b59ad35a384a3c785d3c2db04c4c8a0bcec8b0cfd1097e1cd9`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 97.2 KB (97205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa16a8334ff652d9dd37f3c92c179213d69b28d690ee89a1248fa684e142ef`  
		Last Modified: Tue, 17 Feb 2026 20:31:20 GMT  
		Size: 104.7 MB (104703650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a7e01561e2d489e6b3ed49c38ee395e8def51debf09490e489bb6cae204c8`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:652e2a056f579fe63480e1d81d849a3e5c44e59779794e86c78d4ac3bfe9cc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17696040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f500caf885fbc06ad2fe874993a6b5e35415fa94f65cb9a332debaaf9ee98bf`

```dockerfile
```

-	Layers:
	-	`sha256:af17cf1784658186af363176782bca7625f37ff722b955ac0ce6c8c85fa823c9`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 17.7 MB (17681426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311ad3ad152e9842bc5a81a96f0e2010214cbe7dc15fb9908ba3f97a5ce29266`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3d7af74d41a146cfb65826f2dfcd9060cf5db8fce5e51ce3d8c19cac2a6113ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137108487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae88015583e04ddfa4f0ee76e958c48b3cbbc252ae89d2702ee5533e2e4a3ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18645ec48b5cd0e87d0e4506c045b481e37fe9b3b2eb25377907d2ae7ed29051`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 1.2 MB (1214337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b648a1d2602bc1c46cfe4b71c4ab2dfc0fb3fdb33c518b7c63dc71856f941`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 5.9 MB (5947042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e31d31174c558cb94211479bd475553c14e828fa2a2cd3859d32335c4b151`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 97.4 KB (97391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da891479386a1689d6abd774292e94671dd860097637b72325ef426d9ac33033`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 102.5 MB (102464576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b865c43a1147148db9b69f0ce6c6bff04b54689a86aca56ffa1262b4648096b9`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:4b4cb824863d060930fff9f12e1f7dbb8377bbe2ad5e263f7bb70ac82675821d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17682510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56afe4995a0f209c9ead007d27e754c18e4671e607d3d894cda8a026db455b82`

```dockerfile
```

-	Layers:
	-	`sha256:959690f92f969525c8001243651525912a56c6b4390d3964235e3e1daf326c48`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 17.7 MB (17667771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204012cbc471431ffa57a2f389bccb1cb1f923ea5d63a63079a72676b289f238`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

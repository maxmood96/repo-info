## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:67ea1ec506b2b134928ddf3a7bc27f286c33192d30f36ac956768fe5d38acf83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:592aa96c4bed38273f9db0806f8d68680cdd69d516b6baa7630b2258015d9a38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155382797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bc46b6422cd2f63f97602b1eebc864c6fa256f599b9ba1ef116a92ffc9d928`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:09:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:09:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:22:49 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 07 Jan 2022 04:22:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 07 Jan 2022 04:22:58 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jan 2022 04:22:58 GMT
ENV LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 04:22:58 GMT
ENV ROS_DISTRO=foxy
# Fri, 07 Jan 2022 04:23:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:24:00 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 07 Jan 2022 04:24:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 07 Jan 2022 04:24:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07d6b806a5eae974734f3df21a5799c46db4c8dc12ffc6bab4a8ca2f802d1b5`  
		Last Modified: Fri, 07 Jan 2022 04:34:49 GMT  
		Size: 1.2 MB (1182238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f179e9829abe90277c32bc8a0ae588e6e8cc1695c6fc68725929e756102e57`  
		Last Modified: Fri, 07 Jan 2022 04:34:47 GMT  
		Size: 5.5 MB (5546941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9703d7991cf24346be83227ed5301b773e0d61d93effd34a9263fd4c67504f`  
		Last Modified: Fri, 07 Jan 2022 04:37:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ee04ca82bf5b24a9b55f2bdbfb80b5ea009b8419a3e8611d2d0a551404face`  
		Last Modified: Fri, 07 Jan 2022 04:37:46 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e5fcbc56cc018564403b3e0d7a2ba1c551dbbfef70614bab532a6cec5e4b17`  
		Last Modified: Fri, 07 Jan 2022 04:38:06 GMT  
		Size: 120.1 MB (120084781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca376e51cfddbb5565d4cb5bcd27b84bd29b7814c3a10f1f27d006fd2fdb5f57`  
		Last Modified: Fri, 07 Jan 2022 04:37:46 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7f880c87a1212402733ced060c175cd0f25f941b385342f95b2e18cdd80d9721
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137958981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f49ee6b978d8824f20fab73ce324f315c5754ffbd0c2cf5d844cb46c111b48a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:15:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:15:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:21:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 07 Jan 2022 03:21:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 07 Jan 2022 03:21:31 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jan 2022 03:21:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 03:21:33 GMT
ENV ROS_DISTRO=foxy
# Fri, 07 Jan 2022 03:22:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:22:27 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 07 Jan 2022 03:22:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 07 Jan 2022 03:22:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1b5c31769a3e9a4ae40d97f3d7edbb0e388c814d495803544ea752c6e9d6ce`  
		Last Modified: Fri, 07 Jan 2022 03:35:30 GMT  
		Size: 1.2 MB (1184196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94701350f1a3f3c228c3daa7b1471a93f50e71219e0bf9152dedc5131dbdc27`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 5.3 MB (5322571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ad9922ff69bb25ec018c299f28319acded05b5533ed0199dcde7dfdaf6f38d`  
		Last Modified: Fri, 07 Jan 2022 03:38:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f333e9ff5288dcdc1fe0dd0332bc451df49b84edb59aba98cfd562e29f254d`  
		Last Modified: Fri, 07 Jan 2022 03:38:13 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66a92a9fd6a8886d123d670db5303b8dd67ddd77a81725baeb2a0b505ced2a`  
		Last Modified: Fri, 07 Jan 2022 03:38:30 GMT  
		Size: 104.3 MB (104278769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28861e6a517aa6142fc99de642cca95e1dd5a89fd9ed6a6b91f4fb027858c9`  
		Last Modified: Fri, 07 Jan 2022 03:38:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

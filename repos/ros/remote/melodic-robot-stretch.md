## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:7910c58128fe2a2c50853fe4ed34d4a4998f844a201ed32b4197cd9e09cce2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:5309d6bc6a1e371c38a7ea720f3e4c7eab363b4283b3d0e86e347ce590d41a5d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518801512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef452033f1a3eb7a9163240087cae6a15063200e1f9bc0e3250c1f892528ef7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:41 GMT
ADD file:8a9218592e5d736a05a1821a6dd38b205cdd8197c26a5aa33f6fc22fbfaa1c4d in / 
# Sat, 01 Feb 2020 17:23:41 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:49:37 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:49:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 01 Feb 2020 18:49:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 01 Feb 2020 18:50:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:50:37 GMT
ENV LANG=C.UTF-8
# Sat, 01 Feb 2020 18:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Feb 2020 00:04:51 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Feb 2020 00:05:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Feb 2020 00:06:13 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Feb 2020 00:06:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 06 Feb 2020 00:06:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Feb 2020 00:06:14 GMT
CMD ["bash"]
# Thu, 06 Feb 2020 00:06:58 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Feb 2020 00:07:27 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3192219afd04f93d90f0af7f89cb527d1af2a16975ea391ea8517c602ad6ddb6`  
		Last Modified: Sat, 01 Feb 2020 17:28:49 GMT  
		Size: 45.4 MB (45380658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a905ca7a93e1f1f1e5a3c9d5dacdf39395a357b216f42962d54cb9f2f2779419`  
		Last Modified: Sat, 01 Feb 2020 18:59:03 GMT  
		Size: 10.5 MB (10476666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39d9067426f73e53072c040a66d4e587fa9badca3da3aed990b6ef8afe8385b`  
		Last Modified: Sat, 01 Feb 2020 18:59:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47253481cad39c6f079e90a602a37b6638204f66869e48320e2d414b8ec82be5`  
		Last Modified: Sat, 01 Feb 2020 18:59:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822fec1fbb983df499d36a4c4325090bc1538e03ea008262104c269ccf6d6dc4`  
		Last Modified: Sat, 01 Feb 2020 18:59:18 GMT  
		Size: 64.8 MB (64771303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16863f4abfb019c6e8a8fea1c6e62b6143066c7f5e93a79efe3e9b651ebc248`  
		Last Modified: Thu, 06 Feb 2020 00:22:18 GMT  
		Size: 416.3 KB (416299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c16c2d9ace030f8cf7130554cca720123d8d98ac042030446e8e63d2fed7575`  
		Last Modified: Thu, 06 Feb 2020 00:24:16 GMT  
		Size: 270.4 MB (270396052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169dc5fb275b853031a6119ad6970232236aa67ec1091eb754ef605ddcdb0ec0`  
		Last Modified: Thu, 06 Feb 2020 00:22:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3989e70d294fe3d20b5496caf95ff8bbbd3a87f2767957b524094176593b4b0`  
		Last Modified: Thu, 06 Feb 2020 00:25:02 GMT  
		Size: 108.5 MB (108474848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48acfe3e6448d771edf6c928458b2e5cbe5dae5edc4e219005163fa45b161a6c`  
		Last Modified: Thu, 06 Feb 2020 00:25:23 GMT  
		Size: 18.9 MB (18883868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:da6820004bf5b06088f5bd90ea08d2f224b22d3045caad28018c3b9eb4de31f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.2 MB (461208680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fb7a7dd21f823b6b8715e65ea2fc99a14070b893afded93929a42552d46a50`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:44:36 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:44:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sun, 02 Feb 2020 07:44:43 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sun, 02 Feb 2020 07:45:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:45:51 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2020 07:45:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Feb 2020 00:44:35 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Feb 2020 00:44:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Feb 2020 00:47:36 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Feb 2020 00:47:42 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 06 Feb 2020 00:47:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Feb 2020 00:47:43 GMT
CMD ["bash"]
# Thu, 06 Feb 2020 00:49:13 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Feb 2020 00:50:15 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c33db3715bc6e9bf1a2a078edf3e50c65fa4c60d49ae91fb5933f1ca2b6ba0`  
		Last Modified: Sun, 02 Feb 2020 07:59:22 GMT  
		Size: 9.8 MB (9774849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef236eba576ebb9a25d74c7aabaca4cecfb50c11e85c6f3f3a8ba87e92fdb8c1`  
		Last Modified: Sun, 02 Feb 2020 07:59:20 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78592c06f0a0dcaa5ea7f016f166ea880f0093889e2b6ef20091a6247aa2e8b8`  
		Last Modified: Sun, 02 Feb 2020 07:59:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635f3fb9af5701ab0e946f90c9fcd0e121a3732cd2cde396b5250944ae47a01c`  
		Last Modified: Sun, 02 Feb 2020 07:59:38 GMT  
		Size: 62.1 MB (62086326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9633a2f72aeb46b53c191d8a95623614565619e6fca3f92ee343bb9b0ebf0655`  
		Last Modified: Thu, 06 Feb 2020 01:19:23 GMT  
		Size: 417.4 KB (417351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43fc38624bcf261ba8fee2107c3ccaaf64aabe0fef1b9673b147922c376218f`  
		Last Modified: Thu, 06 Feb 2020 01:20:35 GMT  
		Size: 224.6 MB (224571978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58d6b229b7975ce24aa7088b3427617bcb6d1cf24afd20f524c6133172798de`  
		Last Modified: Thu, 06 Feb 2020 01:19:23 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea81a13f34793283e5dc90ad98b69cf229c8fdef3eccf7c97393f6ac5735974`  
		Last Modified: Thu, 06 Feb 2020 01:21:13 GMT  
		Size: 103.0 MB (102962235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848ea506611201cf5102d89af2de8cf92708f292924f883d943ed2e367b6d50d`  
		Last Modified: Thu, 06 Feb 2020 01:21:31 GMT  
		Size: 18.2 MB (18227373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

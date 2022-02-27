## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:febddba9f7554b96548c6609664c5c359a9ccdd3ab8a62e60442728d2578f225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:84822036f2bf5e1bc59ec22042b7e455b44e7ec73967b9882a5204dd101b2e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160202876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681a973fa09ea97cbf71579d5e8c6ea723ee33e0c7cb06c4704665f9ae2e0be8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:15:16 GMT
ADD file:3f673e2aa3a51c7980f0f25985b44578e091d31b3e0a8f481069c20b363a216c in / 
# Wed, 02 Feb 2022 02:15:16 GMT
CMD ["bash"]
# Sat, 26 Feb 2022 02:24:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 02:24:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 02:24:42 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 26 Feb 2022 02:25:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Feb 2022 02:25:22 GMT
ENV LANG=C.UTF-8
# Sat, 26 Feb 2022 02:25:22 GMT
ENV LC_ALL=C.UTF-8
# Sat, 26 Feb 2022 02:25:23 GMT
ENV ROS_DISTRO=rolling
# Sat, 26 Feb 2022 02:28:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 02:28:08 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 26 Feb 2022 02:28:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 26 Feb 2022 02:28:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c610536171e3c233fc979d34130a90e9c9bc030425e5af141fd0c3aa8bcf5fb2`  
		Last Modified: Wed, 02 Feb 2022 02:17:11 GMT  
		Size: 30.5 MB (30532381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69865bdeb36f9908dc95f897cfa52157f167b05547180cd39a6b299ec5066824`  
		Last Modified: Sat, 26 Feb 2022 02:29:52 GMT  
		Size: 1.2 MB (1191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9177dcd66ad47879d77e6a83c2c8c0ed121ac7569db4fa355a902abcba68fe9f`  
		Last Modified: Sat, 26 Feb 2022 02:29:50 GMT  
		Size: 3.8 MB (3828294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51aecbdc07d493e58edb2120715fa312a3a4778f6353c8b89a6dde38c41a3f9`  
		Last Modified: Sat, 26 Feb 2022 02:29:49 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09813fd921e82b5beee394a1640678fb2aae5b027828684f1b9d44378d7cfebd`  
		Last Modified: Sat, 26 Feb 2022 02:29:49 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7938cab3e71d4742241763bd05ede6ea9f334f91b7e7c012d24c36e84982ea`  
		Last Modified: Sat, 26 Feb 2022 02:30:12 GMT  
		Size: 124.6 MB (124647963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279917d4e15f9b0770a34b92772a0887b229ae8b81ba2d4812e08ce19bd41591`  
		Last Modified: Sat, 26 Feb 2022 02:29:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7cb23184ce64af595bd46a022a59e49209848a4bc024bd2971e9bd667cf9a95c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156946942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ef104d5a0d94a7616be0b38d2095cbb696584149a6571ddf5162a869783b0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:55 GMT
ADD file:14faf487f471b0c41efdbd2280f1d905387bf534ef8810abd3a37774ba55ca12 in / 
# Wed, 02 Feb 2022 03:19:56 GMT
CMD ["bash"]
# Sat, 26 Feb 2022 00:44:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:44:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:44:29 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 26 Feb 2022 00:45:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Feb 2022 00:45:07 GMT
ENV LANG=C.UTF-8
# Sat, 26 Feb 2022 00:45:08 GMT
ENV LC_ALL=C.UTF-8
# Sat, 26 Feb 2022 00:45:09 GMT
ENV ROS_DISTRO=rolling
# Sat, 26 Feb 2022 00:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 26 Feb 2022 00:46:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 26 Feb 2022 00:46:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a99755935c0ed83076913ebdfc8b5a435fda0bdb7463e3f44b9c68ccfbabfc15`  
		Last Modified: Wed, 02 Feb 2022 03:22:20 GMT  
		Size: 29.0 MB (28957023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58066ccb94244f7b05c1e3f0da559277e10da1c9c0ba92fa419a08eae94a70e0`  
		Last Modified: Sat, 26 Feb 2022 00:49:20 GMT  
		Size: 1.2 MB (1193898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319c7eb9c853b6e46cdbca80f7eef1ecd99450449be76c3335cc15b720c9870d`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 3.6 MB (3596216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40894fefa8f50a868c983395fcabf33b97aa0717112a45273475437fa80fbace`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f288530d3ee34e27854ee0c701df63d10fb414ed7a7bb00ae7cbfa0371f494`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58266d751be66d0d2f814c0010414fe3821c7a1daaa0b2d848cbd773734e67f5`  
		Last Modified: Sat, 26 Feb 2022 00:49:39 GMT  
		Size: 123.2 MB (123197430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6502c9f94ca6d8962989e8134a1c6b91908eb368eede3f2e9a328364a566bb`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

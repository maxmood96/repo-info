## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:194e21946e9f68344080cf3fe30ebc68d304ddbe517fcf380ea75ab5fa871e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:f087b83240089280044b9e91586e79d41be9c5686e6ae15971fff06334e32060
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.0 MB (463002374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0874d97344aa45bb23cbc0e581058c81bc2238ec07823e6a891c3db7a0b9311c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:36 GMT
ADD file:53e587afdbeaee60cc14bd95907f14c8303c04b98c72f98e2c54d4343f15dd38 in / 
# Tue, 12 Jan 2021 00:32:37 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:08:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:08:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 12 Jan 2021 01:08:47 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 12 Jan 2021 01:08:48 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 01:08:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 12 Jan 2021 01:08:48 GMT
ENV ROS_DISTRO=noetic
# Tue, 12 Jan 2021 01:10:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:10:26 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 12 Jan 2021 01:10:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 12 Jan 2021 01:10:27 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:11:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:11:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 12 Jan 2021 01:11:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9a857cbf04d2c0d2f0f6b73e894b20a977a6d3b6edd9e27d080e03142954950`  
		Last Modified: Tue, 12 Jan 2021 00:38:49 GMT  
		Size: 50.4 MB (50399171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d472a295ebd41d3968f8d863e1015d367c18e985c1c0f56d543463857ec9647e`  
		Last Modified: Tue, 12 Jan 2021 01:24:06 GMT  
		Size: 10.9 MB (10890313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d374fcbac4a1edeece11e802c028e58bcfd68f594a873fe3daa75cb39560a5a`  
		Last Modified: Tue, 12 Jan 2021 01:24:02 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82e0241a79b24e9ee7ee6f9df3d32a58e6a527c754d734ffdeab34eb9f7d189`  
		Last Modified: Tue, 12 Jan 2021 01:24:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f94ca05cb3b6e59c6c7edda6c987adc2e22ba0327be09a7d9209b23653182`  
		Last Modified: Tue, 12 Jan 2021 01:25:15 GMT  
		Size: 238.9 MB (238919824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a4f8987d94cbf12fbebd2ede2b2e65b75267777ba507219d725e88a9a5cb21`  
		Last Modified: Tue, 12 Jan 2021 01:24:03 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b600712acb247824ee23a4eb56fa59e128ee396bf36b595f1e74c7421fe03eb`  
		Last Modified: Tue, 12 Jan 2021 01:25:53 GMT  
		Size: 86.6 MB (86563501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e7c2dfc7eb08cc8406fb38c8de6b7a3415b24b609e877ee9a2a590b64df5ce`  
		Last Modified: Tue, 12 Jan 2021 01:25:23 GMT  
		Size: 261.2 KB (261205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf02b5e910f2c0aabe6b7afcfee54c2b7c8d48e2d345983eab101a31b3b6a7d`  
		Last Modified: Tue, 12 Jan 2021 01:25:48 GMT  
		Size: 76.0 MB (75966525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:79e2463407b661181dfa791131a21c8f02854d36d46bf391b051f0d3581add00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402911890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa96b45a6dff24099642a17753203ca190af7dd813b25b851ece86cdbca444a6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:40:39 GMT
ADD file:849d424ecc8572facb3ca68eff836dce211bc677cb32d3c3eaa129d364d33878 in / 
# Tue, 12 Jan 2021 00:40:43 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 17:04:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 17:04:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 12 Jan 2021 17:04:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 12 Jan 2021 17:04:57 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 17:04:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 12 Jan 2021 17:04:59 GMT
ENV ROS_DISTRO=noetic
# Tue, 12 Jan 2021 17:07:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 17:07:22 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 12 Jan 2021 17:07:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 12 Jan 2021 17:07:24 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 17:08:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 17:08:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 12 Jan 2021 17:09:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6e5587ff5efa4e647ae927194fac9b961a68d46b23b68a3119c90016e58f17aa`  
		Last Modified: Tue, 12 Jan 2021 00:51:18 GMT  
		Size: 49.2 MB (49183736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133c142d67041b46437f81b1fad2248d916b31913015d0e9591ddd43e55a565`  
		Last Modified: Tue, 12 Jan 2021 17:23:32 GMT  
		Size: 10.9 MB (10882904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60827e914e9a578cc39153a996201569f0ac261afe2e8dd41b065ad0d72c9983`  
		Last Modified: Tue, 12 Jan 2021 17:23:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a4e1d21af11d75e8ff018a40f258e7cf9512d5bdf7a0b141113b7f039f1cb6`  
		Last Modified: Tue, 12 Jan 2021 17:23:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3812d77ac9cfc80389a8b87c3125fc82218e04f068455d0b4378af6503f7023c`  
		Last Modified: Tue, 12 Jan 2021 17:24:26 GMT  
		Size: 184.1 MB (184140147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f0e2a67e831045ba59fe86e0deda4aa5281459060f3c1b51a35b44db073eba`  
		Last Modified: Tue, 12 Jan 2021 17:23:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adfab3ab3df14a532c6a647e4bdd966155f097cb3bf1ddbaf99b3b510db8ab5`  
		Last Modified: Tue, 12 Jan 2021 17:24:50 GMT  
		Size: 84.4 MB (84353671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c980982f3d5f27708016f53ea3298c3838e5d5b387a2a044f0fd6e71bd5a23a2`  
		Last Modified: Tue, 12 Jan 2021 17:24:33 GMT  
		Size: 261.3 KB (261268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2ea4eb5a9646660b14f96839384a2710939c0e33e1243f0ac2bda38b02108`  
		Last Modified: Tue, 12 Jan 2021 17:24:49 GMT  
		Size: 74.1 MB (74088325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

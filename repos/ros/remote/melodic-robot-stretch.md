## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:ba63c43c5a7b4218a5c8d1117da38d8bc527ec741914d4644b58dc6c33515e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:c327cae2d2b3c94252ee32560138221124dccf8c7b86c6c807a75a275d811bbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.8 MB (462753894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837b85abb4915fe6032613048557dff658e5fcf5824fd4c34be7a5f56512bdb9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 19:17:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:17:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 13 Oct 2020 19:17:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 13 Oct 2020 19:17:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 19:17:46 GMT
ENV LC_ALL=C.UTF-8
# Tue, 13 Oct 2020 19:17:46 GMT
ENV ROS_DISTRO=melodic
# Tue, 13 Oct 2020 19:19:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:19:18 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 13 Oct 2020 19:19:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 13 Oct 2020 19:19:19 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 19:20:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:20:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 13 Oct 2020 19:20:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:21:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e64d6a7fc5320867400c03832cf54957cbbf98b99714a200a9090f67fa0af6`  
		Last Modified: Tue, 13 Oct 2020 19:32:22 GMT  
		Size: 6.9 MB (6866999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ec983be87cbebfea0a9dea300e1ae958cdc96a8fd550ed6ba63ceeed46116`  
		Last Modified: Tue, 13 Oct 2020 19:32:19 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7303450037ec364ecd0bff523fa0140a41fbc939b44bcb48abe60b9fe2d1fdc4`  
		Last Modified: Tue, 13 Oct 2020 19:32:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04058250f482c63226262abef7876d3f158f937c4535066c3bacf84b047b5f9c`  
		Last Modified: Tue, 13 Oct 2020 19:33:29 GMT  
		Size: 269.9 MB (269927678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876e825fea60d421a44ae42f1fb98d96cf6acdcf20af70678fd093ce7bc7211a`  
		Last Modified: Tue, 13 Oct 2020 19:32:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b3345f7bb5574ca7d580696fd7f3e8c218a503004f3eff3679e6b29efee8f4`  
		Last Modified: Tue, 13 Oct 2020 19:33:51 GMT  
		Size: 70.2 MB (70152916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59a685afc6f0c271459de511b5c166bbced15374a2f8482920687c0181f415`  
		Last Modified: Tue, 13 Oct 2020 19:33:35 GMT  
		Size: 264.6 KB (264554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d8e96833fe2accef120b31842c4fd2a18a1f5f4685b04fe0b84ae6cbffde54`  
		Last Modified: Tue, 13 Oct 2020 19:33:49 GMT  
		Size: 55.1 MB (55053833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1954a7f36bc0a1045135c4b43f2b359dd2bf8e8c5546a91cf75ada212750aa3d`  
		Last Modified: Tue, 13 Oct 2020 19:34:04 GMT  
		Size: 15.1 MB (15119321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6cecefd0ae811d6fdb3ec5c71003b27a5226ac20157639b6d0057039cbc407c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.6 MB (407627110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90641b0b0674144309732156105934d741b903ae984d22d094282c8526ad35a6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 17:49:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 17:50:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 10 Sep 2020 17:50:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 10 Sep 2020 17:50:21 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 17:50:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 10 Sep 2020 17:50:29 GMT
ENV ROS_DISTRO=melodic
# Thu, 10 Sep 2020 17:54:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 17:55:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 10 Sep 2020 17:55:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 10 Sep 2020 17:55:15 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 17:55:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 17:56:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 10 Sep 2020 17:57:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 17:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dfa29a8456bb2ebaef0eca491538c026723b1f78edb1a107569756d2a3ce15`  
		Last Modified: Thu, 10 Sep 2020 18:26:17 GMT  
		Size: 6.4 MB (6440792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed82b5af61f8168bdb9f6ab1b7c9f527bf108fa930fe26b10e944e45d24a0ca5`  
		Last Modified: Thu, 10 Sep 2020 18:26:14 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8570d91b0afd4af1ff2447141b92ed7ed471251fd9dbea0da2488b14076d7ceb`  
		Last Modified: Thu, 10 Sep 2020 18:26:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ea2bf9d7559afeca0cb6b14223851a53a5095de6b0276a34e4c771a53eba2c`  
		Last Modified: Thu, 10 Sep 2020 18:29:47 GMT  
		Size: 225.0 MB (225019969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a962f8b50b62e542f16e34961b364c107269e8cce651cf1d923e3ac9ad28d`  
		Last Modified: Thu, 10 Sep 2020 18:26:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b783b685508fd965750768c3cb97a40d09ff7593ceb437fc6f5534d7a70e6ce3`  
		Last Modified: Thu, 10 Sep 2020 18:30:35 GMT  
		Size: 64.8 MB (64840223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2e98aaad76b576724aafc57e9428a6156147c26b8d92098d7822eb7b6cbd12`  
		Last Modified: Thu, 10 Sep 2020 18:29:54 GMT  
		Size: 260.0 KB (260013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0286415c21856d5c24fc4082c2388f19d463b0661f6e08d52060ee579d46ffbf`  
		Last Modified: Thu, 10 Sep 2020 18:30:31 GMT  
		Size: 53.2 MB (53242372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22564a0d622e0d32c0f40d35e265fc42138b65650584bbf23da0e3520d3d2a3`  
		Last Modified: Thu, 10 Sep 2020 18:30:50 GMT  
		Size: 14.7 MB (14650221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:4aacd54df9485207fb5576a12055dd67599d924f68d3e56e6f57d52738123b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:33469620b61bf346857ea107808f9b6490c4c053877906144f4bc06c492626fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.0 MB (484032615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7f349468ed21495000bf29975c6dce97a35822d3b8c761641311a3b0f2f985`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:33 GMT
ADD file:4b03b5f551e3fbdf47ec609712007327828f7530cc3455c43bbcdcaf449a75a9 in / 
# Tue, 04 Aug 2020 15:42:34 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:52:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 06:52:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Aug 2020 06:52:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Aug 2020 06:52:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 06:52:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Aug 2020 06:52:22 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Aug 2020 06:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 06:53:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 05 Aug 2020 06:53:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Aug 2020 06:53:25 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:53:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 06:53:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Aug 2020 06:54:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 06:54:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6ff36c9ec4822c9ff8953560f7ba41653b348a9c1136755e653575f58fbded7`  
		Last Modified: Tue, 04 Aug 2020 15:48:55 GMT  
		Size: 50.4 MB (50396000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91563a4363bc60194f754cd55795c0bdfd23e4f12bea50c0b292fe358d804b57`  
		Last Modified: Wed, 05 Aug 2020 07:05:18 GMT  
		Size: 10.9 MB (10889327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5545a9d65404a1ec0f4ff1975cb1e36517cb1d3802322aad3431ab80904851f5`  
		Last Modified: Wed, 05 Aug 2020 07:05:17 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a6b1162c9ea2f144147436037369d117fa022b280ca47916332d60261d2aa6`  
		Last Modified: Wed, 05 Aug 2020 07:05:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385b447fa489face0db0cc3e93da19b0ce94793a5ffee49fa58430ab4db43c0e`  
		Last Modified: Wed, 05 Aug 2020 07:06:08 GMT  
		Size: 238.8 MB (238837794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92df0de08e6899d24b543e9bbc6149bb2edb3dace806003b21a59de091c8b766`  
		Last Modified: Wed, 05 Aug 2020 07:05:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3a303e5f36b6f9e3a9a51c68b6340eac0f78baf627eeacbbbcee6ccf9677d3`  
		Last Modified: Wed, 05 Aug 2020 07:06:29 GMT  
		Size: 86.6 MB (86563387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a308844e1aa8521ee17afaa75cf33ac4532600f2653696f7dff40983a785917f`  
		Last Modified: Wed, 05 Aug 2020 07:06:12 GMT  
		Size: 211.6 KB (211617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de64a72d41978d089c929cb781e0c291b3e7e838f6106d192079e6cfad3d7847`  
		Last Modified: Wed, 05 Aug 2020 07:06:26 GMT  
		Size: 76.0 MB (75965133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fc9d94c236cc79f53494d3d735484e913f46a1cfd3577cba3adedc201781fc`  
		Last Modified: Wed, 05 Aug 2020 07:06:36 GMT  
		Size: 21.2 MB (21167521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:16868e4633e835c700a7d76284764ddda8cec899ab20a1fc1f30374ac8e4890f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.6 MB (423618747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7acc643b1e28e955a454077a7cc6a978913108dc190dba1cf266f28cf9b081`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:21 GMT
ADD file:c8c11e622b1b8a1e31f32e2457ff4d1314d5cd4a7ad22b3991ab9d0542db23fd in / 
# Wed, 09 Sep 2020 23:50:22 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 18:07:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 18:07:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 10 Sep 2020 18:07:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 10 Sep 2020 18:07:09 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 18:07:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 10 Sep 2020 18:07:12 GMT
ENV ROS_DISTRO=noetic
# Thu, 10 Sep 2020 18:11:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 18:12:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 10 Sep 2020 18:12:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 10 Sep 2020 18:12:17 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 18:13:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 18:14:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 10 Sep 2020 18:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 18:16:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d3a32671b6316bd11f4bf18cb034394ac94d2bb3bc6d09de388b19b06fb94b91`  
		Last Modified: Wed, 09 Sep 2020 23:58:45 GMT  
		Size: 49.2 MB (49175549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fada41445f002b0de9ef1f01bf1b05aed044cbb407b487db5a5e1352bbda16d`  
		Last Modified: Thu, 10 Sep 2020 18:33:20 GMT  
		Size: 10.9 MB (10881945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eda9628763a567c13b6ffd0c5b79fc235c51103fa9724f14598a3a0e06ef180`  
		Last Modified: Thu, 10 Sep 2020 18:33:16 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd2b7a76d7308a1d2560bca63b7771f0798ece16b3cd1df9c596fca20686592`  
		Last Modified: Thu, 10 Sep 2020 18:33:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15dd71827aa7b3a011f910eecfe88aacbe135cae512a657976fdf9dbaf1dea8`  
		Last Modified: Thu, 10 Sep 2020 18:34:19 GMT  
		Size: 184.1 MB (184073881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ddc38cd48b4e686de79d8ff245c8b7ffd578bcfd845d6e4f33b043f826bb36`  
		Last Modified: Thu, 10 Sep 2020 18:33:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc61790a22052687e1a3883fde6f9ee45a7bc98021a2998b93e2befce29beb`  
		Last Modified: Thu, 10 Sep 2020 18:34:46 GMT  
		Size: 84.4 MB (84355549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211a09c9e39609d1ec9adc086f9f8d2cdd69fd7e46f0d6f98181a19730ce8dc0`  
		Last Modified: Thu, 10 Sep 2020 18:34:28 GMT  
		Size: 224.5 KB (224473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb1ef5f83a4daae14ff5664ae2b9b86c52eb5e79b04c64240c1e477ce359825`  
		Last Modified: Thu, 10 Sep 2020 18:34:46 GMT  
		Size: 74.1 MB (74089936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5212463de83084b75fd6e07c0358461d3f1e60a4bb14cfcb92d35c3a48029`  
		Last Modified: Thu, 10 Sep 2020 18:34:58 GMT  
		Size: 20.8 MB (20815577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

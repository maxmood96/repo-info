## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:0e185ff94ac73619b41fcbdddaa8508da917335aae03e3aae245010f76a869c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:26ff0b66e8070fb5883bc6d3e79e429be979ce4fbc5e78f5735ece8ff91cb000
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348611143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbea4c2c80151dacde3a8b0ffc4e53500e6be19da3c08f93ef911fa2bc15dad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 13:29:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:29:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:29:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:29:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:30:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:30:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:30:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:31:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:31:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:31:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:31:26 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 13:31:26 GMT
ENV ROS2_DISTRO=foxy
# Tue, 02 Aug 2022 13:32:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:32:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:32:49 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52ae16f14310233a6e7249f0fa763fae9f5995610d370d531d882fff1f338d`  
		Last Modified: Tue, 02 Aug 2022 14:01:37 GMT  
		Size: 120.1 MB (120094593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe4231b7280f383df6653740ce8b62eb7b3b26eb9b73063194fb33adaad0c5`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860d019f8d83ce737fa22bbc20d50e8ad9ee06c8b790aecd7ad5f4f5b7b4217`  
		Last Modified: Tue, 02 Aug 2022 14:01:58 GMT  
		Size: 73.3 MB (73321236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4deaeff6a713d4b6767976eb346827c701fe347d528f6851b6092cdc151c65`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 260.9 KB (260923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6111214e0f2e935ae823a1da2de08f1d686923dc249d6d4372d640bdbb42e92`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eacb7c7081c45f56ff2d971ab52dbff21183ebd2588413f8c7e8a957b2fd35c`  
		Last Modified: Tue, 02 Aug 2022 14:01:50 GMT  
		Size: 21.7 MB (21663296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286d636529f999eca09444b318ce3241d317e552f0a4f640b0c1031c9324e7e0`  
		Last Modified: Tue, 02 Aug 2022 14:02:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7c3f4a148e52800a0deda3bb24c15be7027cffdfb1f971d66d6671897590ae`  
		Last Modified: Tue, 02 Aug 2022 14:02:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637c665fa6f5986478cebe9e16d9818f4577a2b1579d903cd92409ef63ae5a7b`  
		Last Modified: Tue, 02 Aug 2022 14:02:26 GMT  
		Size: 76.4 MB (76429024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5363e563fb5b79bdebe0877b556c871de06f2c9c6837bf93b788c1191cf8a1`  
		Last Modified: Tue, 02 Aug 2022 14:02:16 GMT  
		Size: 21.5 MB (21535985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a857bad74b67654b2f1ab2d8ffbac122b18319ed2133b987de53f69657798f`  
		Last Modified: Tue, 02 Aug 2022 14:02:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e908c2d0016f5d0b80de3417ac4423550a10f52342b98bb9573ce1755a66d93e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316275648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07eb9def03493c71fa102c9e773ce7c768b6ce2584769d25759492121f77825e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:23:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:23:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:23:17 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 15:23:18 GMT
ENV ROS2_DISTRO=foxy
# Tue, 02 Aug 2022 15:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:06 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbde1dfcc79d4a7217b8a62168774cb73c2d182e5e154b8bf035c2212d263fc`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e84b0413c2629b20c17fe09106bfb54cbd61d076c1bfd09aba3cb192db7f7b6`  
		Last Modified: Tue, 02 Aug 2022 15:47:39 GMT  
		Size: 76.3 MB (76269498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e39c8f9bee1fefc9e6920baef31896530bf3cf37e7d7f1d16af3ace537f8a35`  
		Last Modified: Tue, 02 Aug 2022 15:47:27 GMT  
		Size: 14.0 MB (13957252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa581353eb222963439f599d8089571c19a9b3791d685d31ca76bababdbf27f`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

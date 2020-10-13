## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:d99eed17c24a35decf1449b6cbd70576730ffe5164738cc4d15da80eb2801428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:8c789faf60bf684ba716b389c2c54547a831543f3eb2a1ad3db2e63eb1f385c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.1 MB (484118955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6821c8dde635154bf776765f921f340e9ff95ba45bbbf2b4a102e01732645b39`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:38:30 GMT
ADD file:6627ad39ea0cb9fcb212342326d14efaff51aece1fd0dc16d5bbcaa25d858622 in / 
# Tue, 13 Oct 2020 01:38:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 19:24:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:24:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 13 Oct 2020 19:24:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 13 Oct 2020 19:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 19:24:04 GMT
ENV LC_ALL=C.UTF-8
# Tue, 13 Oct 2020 19:24:04 GMT
ENV ROS_DISTRO=noetic
# Tue, 13 Oct 2020 19:25:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:25:11 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 13 Oct 2020 19:25:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 13 Oct 2020 19:25:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 19:25:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:25:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 13 Oct 2020 19:26:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:26:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4c3d3e4f7b024979a1c12daa4073f6353b2ba92d96418bc90451994927c9bff`  
		Last Modified: Tue, 13 Oct 2020 01:48:02 GMT  
		Size: 50.4 MB (50395978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a3a13f4da8a989cd47e5141fdd6f9cd9de6e86ccc396db6a668ad032a3160`  
		Last Modified: Tue, 13 Oct 2020 19:36:04 GMT  
		Size: 10.9 MB (10889343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64390ddd28a581349979be4bea66a21751b2ec96485b72280d0c7af425fbb8c`  
		Last Modified: Tue, 13 Oct 2020 19:36:02 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caaf435d5f32518773b64abc379057bbd924c553cfeb58874f5b1315bfc735d`  
		Last Modified: Tue, 13 Oct 2020 19:36:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cfcaa897657f532536be04cfe0020d87bf81257a618757661653ce5441d295`  
		Last Modified: Tue, 13 Oct 2020 19:37:01 GMT  
		Size: 238.9 MB (238865739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14a3cb8bc6bc5df16b3677390c9b4780ea98a150b28e461422e141dbd5323b3`  
		Last Modified: Tue, 13 Oct 2020 19:36:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10751931502218188347b32494cacb109998b797c31081a9c99eac57d9c52da3`  
		Last Modified: Tue, 13 Oct 2020 19:38:34 GMT  
		Size: 86.6 MB (86562665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30482bd4183c03270a07fd2049f64776fce3ddebf54010a29379ff573d417dc`  
		Last Modified: Tue, 13 Oct 2020 19:37:10 GMT  
		Size: 232.5 KB (232476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edca43a1ddc44fc6a1f726452f297fa8c8c8b9029467fd689383dcc58ae4d0a`  
		Last Modified: Tue, 13 Oct 2020 19:37:26 GMT  
		Size: 76.0 MB (75966171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6af23ee1c7b439ccdbd465e3a347ddab2c9bd1f13b51decd66fb30ea8e834b4`  
		Last Modified: Tue, 13 Oct 2020 19:38:48 GMT  
		Size: 21.2 MB (21204748 bytes)  
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

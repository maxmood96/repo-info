## `ros:melodic-perception-stretch`

```console
$ docker pull ros@sha256:66cc7b9d8a6aba93f78af7983d258ea9eef75ec17ecd38b1e09ce149dc9aa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-perception-stretch` - linux; amd64

```console
$ docker pull ros@sha256:b7f8d6758da9e5cc41c967b406dc90d79b902a365eafb107abf01a023e3de66b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **813.7 MB (813736824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80be3cf255bdb07009cd84884e4097c0c2eab4f7b09dc6e852078c0006772029`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Wed, 27 May 2020 00:40:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:40:24 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 00:40:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 00:40:25 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 00:40:25 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 00:40:25 GMT
ENV ROS_DISTRO=melodic
# Wed, 27 May 2020 00:41:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:41:55 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 00:41:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 00:41:56 GMT
CMD ["bash"]
# Wed, 27 May 2020 00:42:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:42:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 00:43:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:45:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b28b20c8c413ed647ed74f3f10133be8da4590c9925bf94a9d2319ffb2f7a8f`  
		Last Modified: Wed, 27 May 2020 00:56:31 GMT  
		Size: 6.9 MB (6865154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2a66cab0412b434c4a2500c5cec7decca877232cc612f58d7e4b73609be25b`  
		Last Modified: Wed, 27 May 2020 00:56:29 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeebda54a351b9b0cfeed08f111e7c8499bd2df81854da04d1e381ac5a3d7802`  
		Last Modified: Wed, 27 May 2020 00:56:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef33ca1dc9083382ef51b03efe176f7b62118f29b79b53ec1bcd8826e1539b82`  
		Last Modified: Wed, 27 May 2020 00:57:23 GMT  
		Size: 269.9 MB (269864464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfe8e8aa3afa6faf61324475cebe6fdc50502c69491f443342ba48f33127c1e`  
		Last Modified: Wed, 27 May 2020 00:56:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7f72e40487afc172f24e1502e68b3997a0705af028d54062439ae655373c8e`  
		Last Modified: Wed, 27 May 2020 00:57:41 GMT  
		Size: 70.2 MB (70150269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aff17de8219cffc22ee1df7ccc29b1ac3d2f19bdd7a404452d58dde21db6490`  
		Last Modified: Wed, 27 May 2020 00:57:27 GMT  
		Size: 248.1 KB (248106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f117343e149e4c9132c0d85084fc0ca2ee5d8e4ccf367bb179b8891ba0c2a97e`  
		Last Modified: Wed, 27 May 2020 00:57:40 GMT  
		Size: 55.4 MB (55407140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35cb8ebb8b9438ecc16a0242575f6360a071d51abd69f3e2cacc81091dee82d`  
		Last Modified: Wed, 27 May 2020 00:59:04 GMT  
		Size: 365.8 MB (365824672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:90f18da076e0c97b2d75d71d2503ac3cf6c397554290d23363dd65dd7486195f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **735.8 MB (735759378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3312bd02f2139da3fbbb9eaafc6ff66395f929b1bf7a74148e8e971a314bc0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 12:48:07 GMT
ADD file:251053dbd1ce0b3744de3eecf53a3ef8ccf92ea509678e59800952c3dbd1b32c in / 
# Fri, 15 May 2020 12:48:09 GMT
CMD ["bash"]
# Wed, 27 May 2020 01:02:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:02:20 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 01:02:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 01:02:27 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 01:02:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 01:02:32 GMT
ENV ROS_DISTRO=melodic
# Wed, 27 May 2020 01:06:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:06:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 01:06:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 01:06:30 GMT
CMD ["bash"]
# Wed, 27 May 2020 01:07:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:07:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 01:08:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:15:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e144e997aec62ed9c3bb1ff83ae2a62cbea252858abfb48ac60bb2078817a6c`  
		Last Modified: Fri, 15 May 2020 12:55:43 GMT  
		Size: 43.2 MB (43163052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bb7dde3e3561e87557cebe7de969685384f466c682af973da45c12bcc43085`  
		Last Modified: Wed, 27 May 2020 01:32:48 GMT  
		Size: 6.4 MB (6438332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a537d9c8c0d1e133bdb333ad502d6718dae1d1df0c59f7da5bbf1fd1e8319a20`  
		Last Modified: Wed, 27 May 2020 01:32:47 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6649d21277ddc660bf76c0ceac943bc20c9faf42252a24f0482b6109d07095`  
		Last Modified: Wed, 27 May 2020 01:32:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843cc150f483c331a133b68de675a0ca25fcb4ea66003d9f3d3b6c3f1af6eae7`  
		Last Modified: Wed, 27 May 2020 01:33:52 GMT  
		Size: 225.0 MB (224958569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ed78ce063c2428401737cdeeeb1d7fffe600c33253c04d2073b8d4ac6d18b3`  
		Last Modified: Wed, 27 May 2020 01:32:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7224e7f35cc441fb67b880973547e53aaed68a1972de310dd247f703589e6`  
		Last Modified: Wed, 27 May 2020 01:34:19 GMT  
		Size: 64.8 MB (64836575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2deb0c13c518e4b6906ad82b7071baa1f66715fa92e5bd37f8a13d4e1c7ab2b4`  
		Last Modified: Wed, 27 May 2020 01:34:01 GMT  
		Size: 248.2 KB (248165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385b53a0850fc170c5dea60518008b44193e96e3869680062a3382dffdd9ce27`  
		Last Modified: Wed, 27 May 2020 01:34:16 GMT  
		Size: 53.6 MB (53579219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bacd597676e310d5d80baee7c3a85b9c4cadb71730e01fa3f66bb4ca854a97`  
		Last Modified: Wed, 27 May 2020 01:36:11 GMT  
		Size: 342.5 MB (342533644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

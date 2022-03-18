## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:755e2d6ab3def14d216dbaf878f877993dc651edbcc23dc49f5038b5531bf349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:38d0eda59074a76c2fedabc17e427a77f20a382ad5134a0598d41f3aa6f32af8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281486234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9b430563473d41dfe87af5f554ec8a99c1fe055ea18e2d8f40a036f90c5e95`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:48 GMT
ADD file:9819681ee3999b437c13bff560a32c11eff16275eebf27adae84e96bcd687c87 in / 
# Thu, 03 Mar 2022 20:19:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:13:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:18 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:14:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 23:16:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:16:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:16:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:16:49 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:18:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:18:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:18:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:19:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9e826c39a5168edf554e8eafc809c69b421ddb67d281f317701f2e68286572e`  
		Last Modified: Thu, 03 Mar 2022 20:21:20 GMT  
		Size: 30.5 MB (30494980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4dc87efafd76095187b9b08077be01b83bde15c579cfe05bbab1b3f63d7a15`  
		Last Modified: Thu, 03 Mar 2022 23:28:43 GMT  
		Size: 1.2 MB (1192034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d3b3f063c560dae631f46501c2c2ed1bf5c561f9798967a66da02c749e05ec`  
		Last Modified: Thu, 03 Mar 2022 23:28:41 GMT  
		Size: 3.8 MB (3827015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c343a4279e03a0022358b546056ce7f7e9b4b77cef16db7afc0015666a941f27`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af60ffccd86a7ef972999007193d41e24dddc29c85ab84f305447dbb54d65d6`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83f7fbe0ba4f2f696faf33efcff82102506241eb673f48aa1952c167e345326`  
		Last Modified: Thu, 03 Mar 2022 23:29:07 GMT  
		Size: 121.5 MB (121532323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4ac8443dc7c2edded48c4c8264b4a51695b9faa55a0238605be85b5241623d`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead5a34546f8900cda4e9de96e9cd4a7a650d5be1f5949942016571a4244032`  
		Last Modified: Thu, 03 Mar 2022 23:29:33 GMT  
		Size: 101.4 MB (101445856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca5b6585cca9cbb05be933a805b52aae270c65c73d7ef24f9ee011077f40b11`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 265.2 KB (265159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e91f5eb941c683c8d2b964e8d20709acdb6ea51277119e994ee237e60a961`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5835613a889cfce3aa74a609f078371294f96cc09e3d67b30d8ba77d03333f`  
		Last Modified: Thu, 03 Mar 2022 23:29:22 GMT  
		Size: 22.7 MB (22724265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fcd2be142f079e58f2e96193cb417b4b27d3dc3d4dfa8c43c73ea7a6e428de1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267793838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a34026bc9d979398ca8a8f7a494b3e3cf61d68286e37065a5dd24790a4c71bf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:41:10 GMT
ADD file:c81be95ae491788086dc606dd86ac47b679f2ce48c96016d4ba321e995541bca in / 
# Fri, 18 Mar 2022 00:41:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 01:14:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:14:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:14:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 18 Mar 2022 01:15:24 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Mar 2022 01:15:25 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 01:15:26 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Mar 2022 01:15:27 GMT
ENV ROS_DISTRO=rolling
# Fri, 18 Mar 2022 01:16:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:16:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 18 Mar 2022 01:16:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Mar 2022 01:16:22 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 01:16:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:16:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Mar 2022 01:17:02 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 18 Mar 2022 01:17:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8037d5c930bd3f2cc0b5ef6849e32124c3c5efaf4389d0974934bba554464390`  
		Last Modified: Fri, 18 Mar 2022 00:43:17 GMT  
		Size: 28.4 MB (28425528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52a2d6d51d5672d6a89bcd061ceb0abb70543ab14cf758b52dae0ea10a9ed89`  
		Last Modified: Fri, 18 Mar 2022 01:29:49 GMT  
		Size: 1.2 MB (1193964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a484c953b5a8ac5a49bdfa6ef2654513ce04b2c545724ed23887ed4e26ecf1e0`  
		Last Modified: Fri, 18 Mar 2022 01:29:46 GMT  
		Size: 3.6 MB (3594382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c71cdbe64ce9e2a57214b4db9fcdfb68ece3c8c4d618cd6e7ca840103a663f3`  
		Last Modified: Fri, 18 Mar 2022 01:29:46 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff9291a332798080bfb5b2e8ffa0d988a72c8939ca254eb21592d43f1716372`  
		Last Modified: Fri, 18 Mar 2022 01:29:46 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b90c99c3d8313d7660084c587776cc644ff55ca2453c2b9abd86d7d6236df1`  
		Last Modified: Fri, 18 Mar 2022 01:30:05 GMT  
		Size: 116.0 MB (116006679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124e2c942e9e5613f749e090c5d6e24e6309980924397b270887cdec8ef21a9a`  
		Last Modified: Fri, 18 Mar 2022 01:29:46 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1ad18863e690660ff2da1cf5734414de53b7815bf58fcd1c7dbac36a107152`  
		Last Modified: Fri, 18 Mar 2022 01:30:31 GMT  
		Size: 96.2 MB (96155191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3c6b05283aa818a9d773afa7b1d3f5f76f2e8842f5ef23f90cc496c3d4dfca`  
		Last Modified: Fri, 18 Mar 2022 01:30:17 GMT  
		Size: 265.3 KB (265325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80fd2612b798c76dea877085bf4e5f263d60d4f6332625917549ce24ac497c1`  
		Last Modified: Fri, 18 Mar 2022 01:30:16 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd394d49e57956f6844b2e0b95fb1dd971c02f60f1c5e3456cda64c0f5dd2f6`  
		Last Modified: Fri, 18 Mar 2022 01:30:20 GMT  
		Size: 22.1 MB (22148265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

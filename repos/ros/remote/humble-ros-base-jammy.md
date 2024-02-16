## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:d254bb722b9b490d3b71723dc2a55591170daad2851ad45e367114c211889120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b5873864423bb6f669f32e4df4996e8647aeec3418ddec1ca4b440202ba2bb58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263557808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a28846ad48b383d0c7619dc85bdf0d956629acc770989a79c865fea416650bb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 02:32:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:32:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:32:21 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:33:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:33:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:33:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:34:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd46df5b586152474291f517cc5304c420d8f7f52e5604ceecb4f9f5ca2f73b5`  
		Last Modified: Fri, 16 Feb 2024 02:50:11 GMT  
		Size: 106.5 MB (106493044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06479915931fcc3b2eac705bbb368afe26bf9b7079ee628b10d388eb13cebd14`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b578444c314f4183a82a2470575f2f6b399491d63e2059853bf6e7062c0f7`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 98.1 MB (98137779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f945a0b34607bf2bb40053ff1689acf2902add4b2a1f3710126f236f08f4f`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 328.8 KB (328773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac53ad1c8b6a3ed726b1c4ce440cb2e6ec03ea9c7567d839b434eb2189c3fdb`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94d8a09e4a010d92764ffd2d8ded04c3227ea1847236e217399bffb9329c26`  
		Last Modified: Fri, 16 Feb 2024 02:50:23 GMT  
		Size: 23.1 MB (23097854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5b530b78b01b3429d086b49a776dc4f5e6240677122d723b8211e6b46d73c471
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256170722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73b7994e5284da433bbaf5270f0a53664605479b33a7301cf7d3f9689d778a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 05:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:21:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:21:00 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:21:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:21:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:22:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4911c0776f2ae7fe89cd66c93d0756d78612a13c99e608d2d93c7e831c7e9e`  
		Last Modified: Fri, 16 Feb 2024 05:40:14 GMT  
		Size: 104.2 MB (104217966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b39b7ccfac9f954cfc61d6e781869a803f4824048f7d6672687e545e673a49`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e4f660e2ab4b30e946b77496f8b67fb109bbc6aa0dd1c153e3858e775535da`  
		Last Modified: Fri, 16 Feb 2024 05:40:35 GMT  
		Size: 95.7 MB (95684460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33ff5103ddc8d8e2639b35aa6fdd477b18c2b6b7d47ec633524ebaefe79ed4`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 328.8 KB (328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779051c6b69728da04857f95ad57e73f3daacf073e2d9fa103e10ec2837f0465`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0a04bef770df3e0e27ace254b6e3b47b7204042f28fe2a7bb975c5acf66bec`  
		Last Modified: Fri, 16 Feb 2024 05:40:27 GMT  
		Size: 22.5 MB (22517283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

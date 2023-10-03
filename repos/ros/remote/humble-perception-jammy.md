## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:936a70cf45a24022312d6fae82ec367ae7784eef98bddbf2d23b3e3756577add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:5e5ea6fd504d3d0a45bd8c464e0d9da7c113d318d6ee9a346c8a1cd4fba7b8c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.6 MB (953584554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc9075856b7daa752a9aff6d139115ff9db78fe2cf98222c71740a1003e2697`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 01:33:10 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:33:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:33:16 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Sep 2023 01:33:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Sep 2023 01:33:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Sep 2023 01:33:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Sep 2023 01:33:18 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Sep 2023 01:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:34:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Sep 2023 01:34:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Sep 2023 01:34:32 GMT
CMD ["bash"]
# Sat, 02 Sep 2023 01:35:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:35:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Sep 2023 01:35:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Sep 2023 01:35:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:43:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f47086b0f36cc3913cae9fd9a64b76b6129a2606dd36083ea54931e271e7446`  
		Last Modified: Sat, 02 Sep 2023 01:50:36 GMT  
		Size: 1.2 MB (1212988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ce8b5b88e015c84c9a67a934f7df859d067527ea2af03630538139167a0512`  
		Last Modified: Sat, 02 Sep 2023 01:50:34 GMT  
		Size: 3.8 MB (3828806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e4c2aec0b05dc7aa86106527a8efdc0f0315ee0879765aaf12f0b2b116b10a`  
		Last Modified: Sat, 02 Sep 2023 01:50:33 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37a5c0d84afcb36509046b20e6bd1f755a5b271715dfd3d1ee82a8cf78eee1e`  
		Last Modified: Sat, 02 Sep 2023 01:50:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537e66f33d318c436f08fd59b9535f8c20afbc41d9d7fe918d01784046bbde6c`  
		Last Modified: Sat, 02 Sep 2023 01:50:49 GMT  
		Size: 106.4 MB (106393782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941567335e5935ceef4278336eb962350c2dd265f6daec9c649f2229e64f67ca`  
		Last Modified: Sat, 02 Sep 2023 01:50:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74c4906d79a11eff8f78dcccd3c6d7ae490a0f02a581f3f3e96a6811b9afe08`  
		Last Modified: Sat, 02 Sep 2023 01:51:11 GMT  
		Size: 98.1 MB (98119987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bcf88c07168233fc1f6f6898e4db9da4b4059228dfd1e3e46d397186946e38`  
		Last Modified: Sat, 02 Sep 2023 01:50:58 GMT  
		Size: 314.3 KB (314302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32be25f77b8e406c44975f550fa8153ab4077501118853bb2332a5c1f532e8e5`  
		Last Modified: Sat, 02 Sep 2023 01:50:58 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e776a75381e899f2343f05d298944ff4ae87f06edf6090b6b69ecc5bc342863e`  
		Last Modified: Sat, 02 Sep 2023 01:51:02 GMT  
		Size: 23.1 MB (23089197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb7bd313849f09cf70f1a2108141db6f7610dc479829316180863437ffc52a1`  
		Last Modified: Sat, 02 Sep 2023 01:52:52 GMT  
		Size: 690.2 MB (690181677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:879dbdcced6ef3675895242b71774249367eda69120cdbe02bd40eecde14c555
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914123792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d5494322d15adffb1aa8aaf0098bd916e9558c8e8fe2a82047aa914d12263`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:10:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:10:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:10:12 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 05:10:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 05:10:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 05:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 05:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 05:11:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:11:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 05:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 05:11:49 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 05:12:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:12:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 05:12:28 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 05:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:22:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567357a40a55ff2268dfac488427459902e263f939839a24f9d1b901cf5c8dd`  
		Last Modified: Tue, 03 Oct 2023 05:30:35 GMT  
		Size: 1.2 MB (1214608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da413fa715aac7a7a4100b22a2e18a7f2b4cd29938ce8a0a6b263f0a51c121a6`  
		Last Modified: Tue, 03 Oct 2023 05:30:32 GMT  
		Size: 3.8 MB (3802011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67273dca36f3012d77922fcbea760da02232a9931fd815f04929c27c4dd1f8e5`  
		Last Modified: Tue, 03 Oct 2023 05:30:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20f8c322b2dd583d11ffaf30c31598da144c4d0b1a69e626f5b921bab4e507b`  
		Last Modified: Tue, 03 Oct 2023 05:30:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79486d8e6c10325fed5cc7962eaff0c7de0bc9dcf76fef575f1b9d5461ae1f37`  
		Last Modified: Tue, 03 Oct 2023 05:30:53 GMT  
		Size: 104.1 MB (104140752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94d8b8b484a034819dabde04b8ce6fb24472a723cc074f7f44be992b6a93241`  
		Last Modified: Tue, 03 Oct 2023 05:30:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0af4ff5245eed0a4354c14146b10ba61409280f1cc9bc55d46174ad996f84c`  
		Last Modified: Tue, 03 Oct 2023 05:31:13 GMT  
		Size: 95.7 MB (95683903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf566e180a96e78b048ccc6e2f69eabee7394a552b350a84d7f77286cf1c8314`  
		Last Modified: Tue, 03 Oct 2023 05:31:01 GMT  
		Size: 318.3 KB (318271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab82a37730ae257b23989207d150aae5637941fe1f979a72a9890ccb968611`  
		Last Modified: Tue, 03 Oct 2023 05:31:01 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0f7aa2d8166af245decc2f6e029470a0b859b62915607fc35988bb30a117b`  
		Last Modified: Tue, 03 Oct 2023 05:31:05 GMT  
		Size: 22.5 MB (22516532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b62f1668152dab6094cc2826139e8bfea5d6870cbc9f66540466c1f9496ebc5`  
		Last Modified: Tue, 03 Oct 2023 05:32:49 GMT  
		Size: 658.1 MB (658050747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

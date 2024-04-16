## `ros:iron`

```console
$ docker pull ros@sha256:a0ad16c1f6c05c306d54701f58c074fad269e3ab4729e5aa9204a3dcd2f78904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:1ae402199a2ebd0051846c168556dbaa7fcfa55d10dde07d76fd5ddb955a5ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268950751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fa1b6c4bfab7ddd0fee2d0a48836d96091c80d0847f743b73dc332898b0421`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:07:26 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 06:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:08:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:08:15 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:08:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:08:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:09:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727b503e9d63f1b3aeb6612958d9a4232c958077d92ca9573074954db20ce689`  
		Last Modified: Tue, 16 Apr 2024 06:29:10 GMT  
		Size: 124.3 MB (124253346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5622b9e20b4fc93b6cd8461b90c909b335a8850a708ef14b35ca233c62080273`  
		Last Modified: Tue, 16 Apr 2024 06:28:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a87942f9d01dfde36dea2865ef2eaf530bfbee41622f8219995d49b3887132`  
		Last Modified: Tue, 16 Apr 2024 06:29:29 GMT  
		Size: 85.2 MB (85171843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd24d9cec1c5a6d7f6341dabe522c7320bd9e43fca6fff9476c135303463376`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 303.1 KB (303063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe0fc7dc345e163298196053abe2e4b66f4d5a64025a62fa91c99fda6ecbe99`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa65e7c084726567829c16beec4011e5319e724d8dd2d7926764cd0c42906d5`  
		Last Modified: Tue, 16 Apr 2024 06:29:22 GMT  
		Size: 23.7 MB (23733464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:843e23952d90e4a3276f7d70f39ebf750a57199558c9b8929678873235532082
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261437296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781cdf661615ad74e6487da82ec5b15bc71399de6cebd9252c61062bb0dae5f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:22:35 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 04:23:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:22 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:23:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:23:22 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:23:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:23:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:24:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5d5ecc9595a1354b977a8c6539b21f9f10617e634ffec2c2b4cd3829cbda5`  
		Last Modified: Tue, 16 Apr 2024 04:32:05 GMT  
		Size: 121.7 MB (121742019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1940bcead61acceacf0b309cca3527216d8a4e3760dd527f596e3dfe7e52ce`  
		Last Modified: Tue, 16 Apr 2024 04:31:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441faad2245eb58df35d4666f35a9c96bcb1efce87245957d7c2544c15b7921`  
		Last Modified: Tue, 16 Apr 2024 04:32:26 GMT  
		Size: 82.8 MB (82848126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefaf205056cc4a47796d83cc8aa33b0a133aabdeacb31e5849a229bd913cb8`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 303.1 KB (303069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e2526138d639016cab5460e48f1e9781b7615736945037d5e823d35aa8a61b`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d64acab4807aebf316411a4d1fee5638d1ed3b786841c344a056528ec7f61`  
		Last Modified: Tue, 16 Apr 2024 04:32:22 GMT  
		Size: 23.1 MB (23121700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

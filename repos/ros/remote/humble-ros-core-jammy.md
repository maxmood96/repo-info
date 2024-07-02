## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:b3ab5c4c532d2e6775051f541c51e4e6a563954bb172ffa8e6389cb50cfd600f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:d10a1f66a393bb6caa8f32ac54941540d614b399ba4d1d1c12035ad0b54ab755
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142021452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763d28f7c3ea4435a11e893e96df003288839d8489c53b2d07707c59ebdcb7c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 06:13:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:13:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:13:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:13:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6ad111ea9e627c5ddd919cccc3f44a8ffe7ba3b24068fae2b35143321f834`  
		Last Modified: Tue, 02 Jul 2024 06:27:23 GMT  
		Size: 106.5 MB (106534706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1089c45a27fa6775af871e4c2a4fe847d10f55db1aeddfc745406207518119`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:83aa819731f39b0abb83eb438ae4464df909892bc8ee99355d1acc2f9fdb01c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137679738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2732ba8618deb2ce3ae0837f2ad92b9f0b2ab1d60e4cd0c7c0dcf61d7b0c6752`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 04:40:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:40:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:40:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31d95c6effa23866939e90b650996f401ea05eaf75999b406ee415479b71bb`  
		Last Modified: Tue, 02 Jul 2024 04:55:21 GMT  
		Size: 104.3 MB (104259492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cfca808ce5a3e85fef69e383034dbf3d4c4420da1763be2c07f0fb1cc5cd8`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

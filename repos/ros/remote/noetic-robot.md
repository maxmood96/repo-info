## `ros:noetic-robot`

```console
$ docker pull ros@sha256:99ad37a4b45de140c26d04dee130099124353535038d9a8dc53c46e19b50fb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:74b585c00c52a11bc9ec0958cc34a2a5cc8e7095c64212e77683c08a3a5281d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359072544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e4b1ab66575af3b1bb37ec6aa0a39b517f644917f4a44bfb92ef5c30c0b5c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:41:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:41:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:43:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c2048f289191c959ae1bde0b76c4c37af804966f66c4599e4745a47810cad`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 50.9 MB (50939858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad18f9d687633622e84262935b3873354dcf6c1ce6c32d67568aa7f9c351f`  
		Last Modified: Tue, 04 Jul 2023 20:07:28 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b129af37cdd180a7f4bb7fc69172d71d5bbc7c2e1eb95896ae3fa7a973fe`  
		Last Modified: Tue, 04 Jul 2023 20:07:39 GMT  
		Size: 79.6 MB (79604734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c101713292cc95f42a217f6ed45522650943e3e1a114dec8b652fc43e710b2e`  
		Last Modified: Tue, 04 Jul 2023 20:07:52 GMT  
		Size: 15.9 MB (15862359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9cd1b1ca2f064657e51e039dd1e8d3732503bd9e53154ec28d56e12e567bf580
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303379129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca73e319f53dd262315677632c97c32581d5179f0b30d78bd374e983b43c9e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:55:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:58:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec7ad778d705ac798c8c4e72ac5e0a3d97e71bf31fb07dc28dc1c7dbfde0b`  
		Last Modified: Tue, 04 Jul 2023 20:07:17 GMT  
		Size: 40.5 MB (40503772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4463c21fd1b24a56ceff0c21678439984b89244a4de1cebf2ca5d1e4fe6f6c`  
		Last Modified: Tue, 04 Jul 2023 20:07:12 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825a9d60f2d0bb1d7c24f20b6232803e0cae89bbd590ec88ddcddd9186193f1a`  
		Last Modified: Tue, 04 Jul 2023 20:07:21 GMT  
		Size: 60.5 MB (60493692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e70a84a8ae6597832e2577f2ea351fd41792040b5899b69b5057d9c0f51f2e`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 14.1 MB (14067418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1e22313404c5ca312b67aa4f87c8eb00e8e9ac59e2a25732055b3b7dddc76db9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338380354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f1af6ab834f1257ede11a3c92856f1389605c55fedefbd2504a62e28c74361`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 14:25:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:25:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:25:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 14:25:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 14:25:42 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 14:25:42 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 14:25:42 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 14:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:28:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 14:28:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 14:28:29 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:29:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 14:30:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:31:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28cdd39b6ea2b9a0ce173cf2e1f26322497d5a9c7710030e37439ad5d4b2523`  
		Last Modified: Tue, 04 Jul 2023 14:59:38 GMT  
		Size: 1.2 MB (1199222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb204de59b70d94654e7760fc586c55bcd195218315dbf7589d66289510f275`  
		Last Modified: Tue, 04 Jul 2023 14:59:36 GMT  
		Size: 5.5 MB (5532648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b74969841e6f58cb9e0f0a3c29463b5877ac9e57c3ce30bfcf3c1a6f5d74b6e`  
		Last Modified: Tue, 04 Jul 2023 14:59:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed7a86bfb6803f03f9f877eab39ae2496795feb327436a44d9450ce2781b071`  
		Last Modified: Tue, 04 Jul 2023 14:59:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d91c98424c5722a91cb12e54ca5c7af9f12c034b801df540e013a52df8e938`  
		Last Modified: Tue, 04 Jul 2023 15:00:09 GMT  
		Size: 171.5 MB (171511899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493841186da8cc28dcd3542f3c5e48f6853b465d5389b8a2e595292fe4acfa57`  
		Last Modified: Tue, 04 Jul 2023 14:59:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656ccdb00e6c88095176998c459e8fbff2585a38ed2a7781a7812e457b3abe9a`  
		Last Modified: Tue, 04 Jul 2023 15:00:26 GMT  
		Size: 45.2 MB (45204441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cbde3a0d7e6e385474cc8f84e37c7ddb2ac72700849e7e7a586690a0a29efb`  
		Last Modified: Tue, 04 Jul 2023 15:00:21 GMT  
		Size: 302.7 KB (302677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a52ffd06935d7fffa1923572f179f9d9aa8e0661022b715746f72ad0673679`  
		Last Modified: Tue, 04 Jul 2023 15:00:30 GMT  
		Size: 72.0 MB (71970399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a7976716fa1fb13821d8de1ed68e5a9f2ccf40cb3d3f3a7ced0a62d94bc635`  
		Last Modified: Tue, 04 Jul 2023 15:00:43 GMT  
		Size: 15.5 MB (15458325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

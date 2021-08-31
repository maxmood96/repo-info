## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:61ec2e6ca3c265c4c386236cd53d996e64bb78b5d98b99edbd3333155f93f06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:75a3bb07c9b6265827bf559fcc633d660776bb8f408b6dc4c3901f8d48a7fc3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291869847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947363507d39ea6611167fc1c338d12ef5b49ba0a2a5cc6274d9860949f1d3a8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:bbd128c88179834dd78f67e2f697f122e407e77a4a2f0e86dc2873ff0deca7f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266167808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71b21d55415e370ea0f2efce7f099343d10317d448c608d9927230700632df0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8558b06cba0b0fe5b01aa01eb86def7df91430b506aa3dfdb92f009424071a34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281386858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d265980b900e789c6ab4768716d4add45868e8d5ddde032b8882870373f5041`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

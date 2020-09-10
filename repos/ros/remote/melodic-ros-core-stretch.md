## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:55ec58009e2add3647529ae8f74c0a5380a36ca07903c120030c703c76119fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:0e4d2a0ad1bddb9ca580eccaebef9258c2cf891f02f9f5b44606940b52989933
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322119466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9354e8ea42029350d176adb5113c1d8b4f1ac32d01c35ac2572a261c53beed16`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:46:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 06:46:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Aug 2020 06:47:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Aug 2020 06:47:00 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 06:47:00 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Aug 2020 06:47:01 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Aug 2020 06:48:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 06:48:26 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 05 Aug 2020 06:48:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Aug 2020 06:48:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae70a4ac92afa745eca40bc9c10b2b1a4178e76b079107c67dfc365e8b9cc37`  
		Last Modified: Wed, 05 Aug 2020 07:02:16 GMT  
		Size: 6.9 MB (6866461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd09b8777edb3312770ea102d89becdbaa8ce1405c8ca848c91be9864b21698c`  
		Last Modified: Wed, 05 Aug 2020 07:02:14 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f33914001586acf8a14dbdf92edba1c9ff4ff86098a74b288072d18c613283`  
		Last Modified: Wed, 05 Aug 2020 07:02:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21922ef3a7cbaf6d454d3ca6fba32f59401db9c03952f4dd656287dc998acf`  
		Last Modified: Wed, 05 Aug 2020 07:03:09 GMT  
		Size: 269.9 MB (269884481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16bcb18292043bc82bd5f157326157ad4a247d9363205ce280e385bcd78211e`  
		Last Modified: Wed, 05 Aug 2020 07:02:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1ffc873a24d2de8d07363d13fed784e92797c1ffb81fadf62ea30a4794d976f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274634281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1093ead4aa456d7aef7528f2e101a756194850480f0403bcb69ed43b2c7eae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 17:49:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 17:50:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 10 Sep 2020 17:50:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 10 Sep 2020 17:50:21 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 17:50:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 10 Sep 2020 17:50:29 GMT
ENV ROS_DISTRO=melodic
# Thu, 10 Sep 2020 17:54:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 17:55:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 10 Sep 2020 17:55:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 10 Sep 2020 17:55:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dfa29a8456bb2ebaef0eca491538c026723b1f78edb1a107569756d2a3ce15`  
		Last Modified: Thu, 10 Sep 2020 18:26:17 GMT  
		Size: 6.4 MB (6440792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed82b5af61f8168bdb9f6ab1b7c9f527bf108fa930fe26b10e944e45d24a0ca5`  
		Last Modified: Thu, 10 Sep 2020 18:26:14 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8570d91b0afd4af1ff2447141b92ed7ed471251fd9dbea0da2488b14076d7ceb`  
		Last Modified: Thu, 10 Sep 2020 18:26:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ea2bf9d7559afeca0cb6b14223851a53a5095de6b0276a34e4c771a53eba2c`  
		Last Modified: Thu, 10 Sep 2020 18:29:47 GMT  
		Size: 225.0 MB (225019969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a962f8b50b62e542f16e34961b364c107269e8cce651cf1d923e3ac9ad28d`  
		Last Modified: Thu, 10 Sep 2020 18:26:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

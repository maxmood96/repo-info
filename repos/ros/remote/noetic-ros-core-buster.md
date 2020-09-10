## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:4fe2aa6749e35d2340bd85ffabba8292b8df69a5babda1a4a1cd390d6759ff6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:1cc83fb322c9cfa617d80fb92d8da1f901c426e9779f2ff779d338db0053d265
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300124957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81d7ab491699b5dfe35727407c40f4b3361c0a33aae47f4783bbb2f38037adb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:33 GMT
ADD file:4b03b5f551e3fbdf47ec609712007327828f7530cc3455c43bbcdcaf449a75a9 in / 
# Tue, 04 Aug 2020 15:42:34 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:52:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 06:52:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Aug 2020 06:52:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Aug 2020 06:52:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 06:52:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Aug 2020 06:52:22 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Aug 2020 06:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 06:53:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 05 Aug 2020 06:53:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Aug 2020 06:53:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d6ff36c9ec4822c9ff8953560f7ba41653b348a9c1136755e653575f58fbded7`  
		Last Modified: Tue, 04 Aug 2020 15:48:55 GMT  
		Size: 50.4 MB (50396000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91563a4363bc60194f754cd55795c0bdfd23e4f12bea50c0b292fe358d804b57`  
		Last Modified: Wed, 05 Aug 2020 07:05:18 GMT  
		Size: 10.9 MB (10889327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5545a9d65404a1ec0f4ff1975cb1e36517cb1d3802322aad3431ab80904851f5`  
		Last Modified: Wed, 05 Aug 2020 07:05:17 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a6b1162c9ea2f144147436037369d117fa022b280ca47916332d60261d2aa6`  
		Last Modified: Wed, 05 Aug 2020 07:05:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385b447fa489face0db0cc3e93da19b0ce94793a5ffee49fa58430ab4db43c0e`  
		Last Modified: Wed, 05 Aug 2020 07:06:08 GMT  
		Size: 238.8 MB (238837794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92df0de08e6899d24b543e9bbc6149bb2edb3dace806003b21a59de091c8b766`  
		Last Modified: Wed, 05 Aug 2020 07:05:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0a722a91b875036279223b323080c52d856ae2d0925315c242827efd204b049a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244133212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53728ac7d126c5f4419a52bfeba3b04b7b57259bda0892beecfc33cea89682c2`
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

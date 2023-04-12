## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:e0356ad1fb87e4f6175064f0a30ac2f883aa1ca071a1fd147a76bf7f1b7b86af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:d99612e72bdf98dda92fbca4c9c05f8b1ba7bfbe468bc61cc41d5b6a6be1971e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484658612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0868037cc1b95666a5b616c9aaca63a8bf0cc3f0358afa2fb0cfe95045f848`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:38 GMT
ADD file:f5e6e6cbfbb36f50f49f06fbac953a130383acb67a1c5e9979441f1915b1077d in / 
# Thu, 23 Mar 2023 01:30:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 14:55:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 14:55:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 23 Mar 2023 14:55:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 23 Mar 2023 14:55:57 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 14:55:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 Mar 2023 14:55:57 GMT
ENV ROS_DISTRO=noetic
# Thu, 23 Mar 2023 14:57:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 14:57:27 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 23 Mar 2023 14:57:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 Mar 2023 14:57:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 14:58:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 14:58:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 23 Mar 2023 14:58:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 14:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e2befb7f5d18aa27b3619ddf1b93607e62ca82d0c627557537c149893346d86`  
		Last Modified: Thu, 23 Mar 2023 01:34:40 GMT  
		Size: 50.4 MB (50448639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c6e6f6091b92ed07213d644f33e47d06757c8ca846e3d9a92c276d9c5fc330`  
		Last Modified: Thu, 23 Mar 2023 15:03:40 GMT  
		Size: 10.9 MB (10897008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbe51e5bdfc4bbbd1863dc733210842df4d4773451ad3e3b97158a12c75d3f`  
		Last Modified: Thu, 23 Mar 2023 15:03:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33da2fadde18416a222a60396cc301bfff00c8711e0e97d1310a94069eccb2b3`  
		Last Modified: Thu, 23 Mar 2023 15:03:38 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7dd060cdb612260d95ac8b282e306e49400054b218aa4fb72f4aaa4f9f73a15`  
		Last Modified: Thu, 23 Mar 2023 15:04:09 GMT  
		Size: 239.2 MB (239238838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03121257a2ad34392087234c38a5c370cf1e3bf6b3d297da74d7d92db294fe5b`  
		Last Modified: Thu, 23 Mar 2023 15:03:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47f986fd943fc96c63708211cd0029fd4f4a1ce0dae877067bcfd2542a709e3`  
		Last Modified: Thu, 23 Mar 2023 15:04:27 GMT  
		Size: 86.6 MB (86624647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567e0013c342030410d9c35f66aaa240bf6a9f0fd8e2861bba61f268f832408c`  
		Last Modified: Thu, 23 Mar 2023 15:04:16 GMT  
		Size: 311.9 KB (311926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f32a3234d59d9cfb3f15c364a962ee5ed705cc1f608a38154c5fbdb5186b5e`  
		Last Modified: Thu, 23 Mar 2023 15:04:25 GMT  
		Size: 76.0 MB (75978138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e58fb3f3c7f611d108b35cf26f48531df1ea3d3bc8bfc3dedde98c23b774b3f`  
		Last Modified: Thu, 23 Mar 2023 15:04:36 GMT  
		Size: 21.2 MB (21157003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e02060cddc00b5e7425b09f32d96167b94622b3f1eee50fc5098e674fc3c60bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424191041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582ac484d974eb0b874fa8dbce396a268b8582220cdc2c68768393ace9d01a40`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 03:17:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 03:17:48 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 12 Apr 2023 03:17:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 12 Apr 2023 03:17:50 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 03:17:50 GMT
ENV LC_ALL=C.UTF-8
# Wed, 12 Apr 2023 03:17:50 GMT
ENV ROS_DISTRO=noetic
# Wed, 12 Apr 2023 03:19:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 03:19:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 12 Apr 2023 03:19:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 12 Apr 2023 03:19:15 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 03:19:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 03:19:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 12 Apr 2023 03:20:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 03:21:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926daaa3f39d210833d9a3a75b2e33aafd38f4adcda623bb40686f5480d8eda7`  
		Last Modified: Wed, 12 Apr 2023 03:25:46 GMT  
		Size: 10.9 MB (10902667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef889428a3c0c2686a4bb8d4e5af08778a1b25251d4873a4635b0b2af721d8`  
		Last Modified: Wed, 12 Apr 2023 03:25:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b211d556fba373cffc4c30d24942793ca6d51c78179037897e5f465fc65e4408`  
		Last Modified: Wed, 12 Apr 2023 03:25:45 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161bac3145a70b13a85c49796d22151dc27a76ea04b256183b318cc9efc8686d`  
		Last Modified: Wed, 12 Apr 2023 03:26:06 GMT  
		Size: 184.4 MB (184427087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc91b09fc5f446950a1e8e392c05737de9820b95e50745e93232b6ff4dba0617`  
		Last Modified: Wed, 12 Apr 2023 03:25:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d31bfc2a7fad06ba1563ddcf7f96daf937621936041ba76fb2e42b45d9f327`  
		Last Modified: Wed, 12 Apr 2023 03:26:21 GMT  
		Size: 84.4 MB (84395801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ec420fccc4bc3cf3805910ff22f8789cd48387fcefed5829785ab9279e8e9f`  
		Last Modified: Wed, 12 Apr 2023 03:26:13 GMT  
		Size: 313.0 KB (312977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e8033e5e52d2e2310af7d82b5846e3f1900897dee49ceb23bf0721dac3353e`  
		Last Modified: Wed, 12 Apr 2023 03:26:20 GMT  
		Size: 74.1 MB (74090563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9d228ccf7178e163cfc639dea467a73470e631550cd2c405a24752317598e`  
		Last Modified: Wed, 12 Apr 2023 03:26:29 GMT  
		Size: 20.8 MB (20820902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:392e4c723de2c18a9eb9fb7de5b07530da215390799ca6c3e6e2ba667ac00772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:757813b4e28c2434adab9df264ea30b524608fa87f72acf68beb26ea9b541b02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.3 MB (951346769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a390071e96f433888f357032ab666982178c4fd66c01826b84356a17e0f08b18`
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
# Thu, 23 Mar 2023 15:02:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b7ca0a8d59c74383fd3d3a52a7fda61bc16f896edfa9e4ab93d2d0d83a560c6b`  
		Last Modified: Thu, 23 Mar 2023 15:05:51 GMT  
		Size: 487.8 MB (487845160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:980152242b671d03db9a26efee4daf2633661b4247037bbd3acc946f3ac4444b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.1 MB (868115447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e8b5202e5fb2faaf4a1dee3bd47c886e64dc7f1589ca5a6b67bb2579e11c30`
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
# Wed, 12 Apr 2023 03:24:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1c366ae282bf50e572d970fd7d54011aaa06faca583dc1548110f0865cdc3809`  
		Last Modified: Wed, 12 Apr 2023 03:27:22 GMT  
		Size: 464.7 MB (464745308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:5a6f99d5c13075e4ab2e6ac053eeff5a5558197670fef11934174ea790890038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:67e35104757429ba80c5b9b36a4f17fb50dd1fd5ad120ca9b1f1705a023ccefe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300173059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b70e47d760f1a47de6c55150bb707f2021db474a527e9794c866f0f507efbba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:32:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:32:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 18 Nov 2020 12:32:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 18 Nov 2020 12:32:22 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 12:32:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 18 Nov 2020 12:32:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 18 Nov 2020 12:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:33:30 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 18 Nov 2020 12:33:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 18 Nov 2020 12:33:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aca0ca778cc2177e241c5afe31769387d68d3dcb7f78b879d5dfa030fb3fe19`  
		Last Modified: Wed, 18 Nov 2020 12:48:51 GMT  
		Size: 10.9 MB (10889760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314469df0ae376029d20cbae47623ebe9fe730656cb17c83bf623f04609ace79`  
		Last Modified: Wed, 18 Nov 2020 12:48:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6434606e30c8d9eeb6c144d67d638cfdc9e9e9693b2c352db307015d64eeb92a`  
		Last Modified: Wed, 18 Nov 2020 12:48:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd89e8059370d211bef01f9a812f67441ba294edf0140d44ae0258ab4eb82d5`  
		Last Modified: Wed, 18 Nov 2020 12:49:45 GMT  
		Size: 238.9 MB (238883738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8710be83226bac5cb358bab625b9ca6e142833bb7b936cf68e0f3d23afed3fe0`  
		Last Modified: Wed, 18 Nov 2020 12:48:49 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3af5ae05cba4b6700725717eeb2e937c33685761d1306f3987917c0cecf2188c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244180665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074dbd295db64160e8c1b72bf0e5c62c8a4e1b87c74709c32f9cc50f753e030d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:04 GMT
ADD file:28343d2066831f0ffb2002914f158698f92b4af6dc16ac22e3d8e9c388c688bb in / 
# Tue, 17 Nov 2020 20:23:05 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 09:27:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:27:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 18 Nov 2020 09:27:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 18 Nov 2020 09:27:15 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 09:27:16 GMT
ENV LC_ALL=C.UTF-8
# Wed, 18 Nov 2020 09:27:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 18 Nov 2020 09:29:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:29:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 18 Nov 2020 09:29:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 18 Nov 2020 09:29:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22518ad4a7da48a5acd01946dad2fbee99e4fca910d23b78cd7e4a16c3bd1e5b`  
		Last Modified: Tue, 17 Nov 2020 20:31:35 GMT  
		Size: 49.2 MB (49179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0016ba602c48f6ebaa4fc89ef88b2543e0081b204301c8d09c790655e635d418`  
		Last Modified: Wed, 18 Nov 2020 09:51:38 GMT  
		Size: 10.9 MB (10882463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44661561f3ffbc31e4ae03215f7cb7c0cb64819066af65f8aee0c5f103fdf7c8`  
		Last Modified: Wed, 18 Nov 2020 09:51:36 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee70efb1eaf577d44f01bec2a8ca443c1d3a74c230395810bc92fe2b35da0bb`  
		Last Modified: Wed, 18 Nov 2020 09:51:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34c5b73ad0576d535dcf95aea891345972ad34120925e401d1eae2e9a7d8e52`  
		Last Modified: Wed, 18 Nov 2020 09:52:29 GMT  
		Size: 184.1 MB (184117149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82c57dce96eaa14614e982c3617dbd9a4f73085d417b220eb5f7faeb79777a9`  
		Last Modified: Wed, 18 Nov 2020 09:51:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

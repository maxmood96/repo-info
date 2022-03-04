## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:63e9e99c3b05bfecd088d098c62b89e35bde93e2e3a132ce9881595ab1513427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:18a5e1a66a17f012c48465ec3d6af2defd495e33b8cf5516a3b508f29e6dea70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157048767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54cc4f069f109a484a13840fb28d8ce7bb8410e41da083e163285dbb68832af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:48 GMT
ADD file:9819681ee3999b437c13bff560a32c11eff16275eebf27adae84e96bcd687c87 in / 
# Thu, 03 Mar 2022 20:19:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:13:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:18 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:14:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 23:16:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:16:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:16:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:16:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b9e826c39a5168edf554e8eafc809c69b421ddb67d281f317701f2e68286572e`  
		Last Modified: Thu, 03 Mar 2022 20:21:20 GMT  
		Size: 30.5 MB (30494980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4dc87efafd76095187b9b08077be01b83bde15c579cfe05bbab1b3f63d7a15`  
		Last Modified: Thu, 03 Mar 2022 23:28:43 GMT  
		Size: 1.2 MB (1192034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d3b3f063c560dae631f46501c2c2ed1bf5c561f9798967a66da02c749e05ec`  
		Last Modified: Thu, 03 Mar 2022 23:28:41 GMT  
		Size: 3.8 MB (3827015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c343a4279e03a0022358b546056ce7f7e9b4b77cef16db7afc0015666a941f27`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af60ffccd86a7ef972999007193d41e24dddc29c85ab84f305447dbb54d65d6`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83f7fbe0ba4f2f696faf33efcff82102506241eb673f48aa1952c167e345326`  
		Last Modified: Thu, 03 Mar 2022 23:29:07 GMT  
		Size: 121.5 MB (121532323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4ac8443dc7c2edded48c4c8264b4a51695b9faa55a0238605be85b5241623d`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bc7955d291b0751463181a4b33562cd75f6c951543abb23ce21866e5603b0068
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153485893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efc2a70e5ba2f0e64350096fd50366ef42dce1aaa266f72cbd5caab6d2e5767`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:34:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:35:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:35:09 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:35:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:35:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 21:36:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:36:11 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:36:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:36:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913010b6995b5164a1549824b8740252b134f42bdbfd66c186edd8996fe831cc`  
		Last Modified: Thu, 03 Mar 2022 21:46:54 GMT  
		Size: 1.2 MB (1194373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89fb22e35ba47ea1110fdb11cb4cb95a691245ed9e2a91a3a7b58fa5b8dc01c`  
		Last Modified: Thu, 03 Mar 2022 21:46:52 GMT  
		Size: 3.6 MB (3594847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d16bcb793950fd11553a33ebaeecb9e7bfb47ece6a96be98044a4f1ce9e0834`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfb4c8069516cf1840c780cf0b359af1585479edbc36ca828f5fea5be4e8c2d`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adbc630fc1669a96b7ac2781a007e4aac2b3c4bc418bee6825d38ad9d5fe64c`  
		Last Modified: Thu, 03 Mar 2022 21:47:10 GMT  
		Size: 120.3 MB (120269595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871d52e65e8c1899c5818fd43e766b4c3660974b4ab50336f98156616d4f3142`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

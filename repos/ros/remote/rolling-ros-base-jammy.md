## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:f8484b4f1ae03c8f5e0bd1e4b5c8cba6c905c5854770e5c79d4c615722680ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:38d0eda59074a76c2fedabc17e427a77f20a382ad5134a0598d41f3aa6f32af8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281486234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9b430563473d41dfe87af5f554ec8a99c1fe055ea18e2d8f40a036f90c5e95`
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
# Thu, 03 Mar 2022 23:18:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:18:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:18:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:19:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2ead5a34546f8900cda4e9de96e9cd4a7a650d5be1f5949942016571a4244032`  
		Last Modified: Thu, 03 Mar 2022 23:29:33 GMT  
		Size: 101.4 MB (101445856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca5b6585cca9cbb05be933a805b52aae270c65c73d7ef24f9ee011077f40b11`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 265.2 KB (265159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e91f5eb941c683c8d2b964e8d20709acdb6ea51277119e994ee237e60a961`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5835613a889cfce3aa74a609f078371294f96cc09e3d67b30d8ba77d03333f`  
		Last Modified: Thu, 03 Mar 2022 23:29:22 GMT  
		Size: 22.7 MB (22724265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89f4fcdebd12236d4a9d6b9bd92aee24307c8bb21390fc29512f6e533416537b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274639882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12ecb26d0b4a8988881ba584fed194d12808f67b77c86b80937ec3a3514c942`
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
# Thu, 03 Mar 2022 21:36:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:37:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:37:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:90fa110d993e661579fc2549e60076ef96c7596fd264edeccb0e9bb4bee943a5`  
		Last Modified: Thu, 03 Mar 2022 21:47:36 GMT  
		Size: 98.8 MB (98753517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4259e629fc55157753363b5dc198f34af61fc52b31cc34e309d23c49701431e6`  
		Last Modified: Thu, 03 Mar 2022 21:47:22 GMT  
		Size: 265.1 KB (265110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e145d15a9076a5707c76250e341ffa4ad41ec8e5d686c0f851caab37e3a8aa4a`  
		Last Modified: Thu, 03 Mar 2022 21:47:21 GMT  
		Size: 2.2 KB (2155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c843328f781595a670b1eb748b22e0a2b1190545a3c7f305724f1ec54ef9daf`  
		Last Modified: Thu, 03 Mar 2022 21:47:25 GMT  
		Size: 22.1 MB (22133207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:a8742825a37880d6b7ed7528eb5b55fc736f30a4966a3dd76771513c6650908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:b3011a1fdc77b575ccc88ff92ca5304f833354396c7ca7e47f9d1972f1ae2509
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322237176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf67b5f3044167242e1188225fa3423a75a1ea7efaefae66ff4966c0e98b025`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:25:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:25:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 18 Nov 2020 12:25:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 18 Nov 2020 12:25:35 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 12:25:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 18 Nov 2020 12:25:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 18 Nov 2020 12:27:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:27:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 18 Nov 2020 12:27:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 18 Nov 2020 12:27:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7919f5b7d60254cafc73c0d097b8ccffb72e0b6472957ece4dd5b378c5ca7cc1`  
		Last Modified: Tue, 17 Nov 2020 20:30:26 GMT  
		Size: 45.4 MB (45377037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53909938ab5beefdbc8f467139ac5be21a1ceaa8a03f462afe676e8948d31245`  
		Last Modified: Wed, 18 Nov 2020 12:45:38 GMT  
		Size: 6.9 MB (6867031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462bfd9d286b988f9d3fa75e6cc220a0eb9a72df86168b0399a7e087c63c2762`  
		Last Modified: Wed, 18 Nov 2020 12:45:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79872cd9faff5df4b6235db27bbc01a36078312f6eb70183ca439c563bdf73d5`  
		Last Modified: Wed, 18 Nov 2020 12:45:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c2a048915dc93ab5c68f0217bb1d6eabd1bb343064bfdd1e60d50c74e33ffd`  
		Last Modified: Wed, 18 Nov 2020 12:46:37 GMT  
		Size: 270.0 MB (269991292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489598e19ca98bbc7a13b91ffd7e195a4dcebed25e3c5f57c3ad7454fecb1e6a`  
		Last Modified: Wed, 18 Nov 2020 12:45:37 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3759b2b91a0359c8682964119b1d0b88a28d3cb7d835afa000f5f71102f2f334
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274705020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43d88c9920f62f6d3bb842b7ab456aed5876e255ffa410fa0d6254bd97ed763`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 09:12:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:13:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 18 Nov 2020 09:13:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 18 Nov 2020 09:13:07 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 09:13:08 GMT
ENV LC_ALL=C.UTF-8
# Wed, 18 Nov 2020 09:13:09 GMT
ENV ROS_DISTRO=melodic
# Wed, 18 Nov 2020 09:17:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:18:01 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 18 Nov 2020 09:18:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 18 Nov 2020 09:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92602d4f5b35fbaf1e8fb6e411e04e5971ce33abe3c7fd5964643892b701db93`  
		Last Modified: Wed, 18 Nov 2020 09:48:11 GMT  
		Size: 6.4 MB (6440978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf801218bf713e927fb087f64d89fe28628b81fd8acd57df9e4ba24ba6c30ef3`  
		Last Modified: Wed, 18 Nov 2020 09:48:10 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48643aeb8ff25cf211053dc193b030b253350d3971e2e58d453851c9d6e2e7`  
		Last Modified: Wed, 18 Nov 2020 09:48:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264bb6a4cb2e6ef5b80b5c02c9dd2dc4f790e1ad5c5e9db55d0014d33248f173`  
		Last Modified: Wed, 18 Nov 2020 09:49:09 GMT  
		Size: 225.1 MB (225086213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6c7356b45f618401b91d614bfe17badbbe1fedbd8b057ac7d88df4f9045be4`  
		Last Modified: Wed, 18 Nov 2020 09:48:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

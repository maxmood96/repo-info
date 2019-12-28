## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:7f6d57bf3e025d7f7311adeee42aa8042c51c5f2decb742908aad12d1444c56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:43aaaa6cfb47d8de9eb5b33e656a4e9747a57a7c09c3933cac178d0052794aea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 MB (391485934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bac88139a4ae488377be19ec7123f1ce8e6e1e001bef55d16813f80f4aa1e54`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:26:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:26:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 08:26:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 08:27:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:27:02 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:27:03 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 08:27:21 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 08:27:21 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 08:29:05 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:29:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 08:29:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 08:29:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cf93dae3672c4b23e304be8bfbd86a1a70e192920d9bb7d980774a433b7123`  
		Last Modified: Sat, 28 Dec 2019 08:34:45 GMT  
		Size: 10.5 MB (10476716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4d94fcfba96b58c2a901f6286ca7d1ce99dacfe09968fc037d5553f2025e8a`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa7ebb2626a2bc1ed27e07d7ca29f5a02c7cfb09f84608d38f9c99b1b798ced`  
		Last Modified: Sat, 28 Dec 2019 08:34:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc08219e7fdb9a27aa4c99a6f1d467eab7640d963871a1400ebfdaae3af68c57`  
		Last Modified: Sat, 28 Dec 2019 08:35:00 GMT  
		Size: 64.8 MB (64771041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4191195f75e3d8a24ce1e680579fd09913504e418871b9b7ec1e38aaa061fdd1`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 451.5 KB (451468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9fd3f2a56a2d531756ee769940fada1e88517a593b70c3e21e959874a7bc78`  
		Last Modified: Sat, 28 Dec 2019 08:35:41 GMT  
		Size: 270.4 MB (270404151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0106c5e798490c33945ce9ebe7647215eb890cf55e081b770471e498436353`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f5ec08ded445c9338b439668c8e668290ed0528a5cc3278334fe8e7b6a44f748
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340053502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed90e0838aeb67fd3fa8237f21c25198eacd48a0305185d1e41973423fc8b5e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:34:23 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:34:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 18:34:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 18:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:35:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 18:35:41 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 18:36:03 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 18:36:04 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 18:38:50 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:39:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 18:39:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 18:39:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facfbd1fae886a379926b7add3095adbf575d32e87e67282e12488332f12f747`  
		Last Modified: Sat, 28 Dec 2019 18:48:28 GMT  
		Size: 9.8 MB (9774604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a6b709bed6b18e5ba839847d0f3e3a5a4e53a163b69ea7858c561fdc7f1e3a`  
		Last Modified: Sat, 28 Dec 2019 18:48:25 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af9a8179e95515f1f6e62a300ca75906566906d949c7403c9f61b8511afc033`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23b6ea616f3e8e138683f48ca757b84bc23de865b250839eba047a141cc6721`  
		Last Modified: Sat, 28 Dec 2019 18:48:46 GMT  
		Size: 62.1 MB (62085764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101b4656b4d26f6236d97a86a31ae20834b113b525d2830521853323cfb6369`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 451.5 KB (451514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e52b33734a366437f8b9e807980e3273684eeef72d2fd1822dc4ea7ae5638`  
		Last Modified: Sat, 28 Dec 2019 18:49:32 GMT  
		Size: 224.6 MB (224573326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de7b9c0321a0098bd333b1ceb564c2a4389249dc4f9e3f45da7c389198a1ba`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

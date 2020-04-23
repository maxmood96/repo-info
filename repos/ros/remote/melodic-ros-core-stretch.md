## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:a920bfb78dd6968a06fd20e7b06af72a4e1c240a35628d3f69b19b11d55f89f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:4e99e0674aaf8fa6f3233e962b2bb6ada5924952fbb12db10c976d477a4c8729
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397102190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac079112a237c0a542c2553a5a172b851aa7171437f97aa7fcd01c5b8367b0cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:22:48 GMT
ADD file:21bf6969c2166c361350c07b1089a1a4b34b7cd3e802a602385d83c49f44a7f6 in / 
# Thu, 23 Apr 2020 00:22:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 18:52:25 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 18:52:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 23 Apr 2020 18:52:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 23 Apr 2020 18:53:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 18:53:08 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 18:53:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 Apr 2020 18:53:09 GMT
ENV ROS_DISTRO=melodic
# Thu, 23 Apr 2020 18:53:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 23 Apr 2020 18:54:35 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 18:54:36 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 23 Apr 2020 18:54:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 Apr 2020 18:54:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99760bc62448fbba69f6f0981d09bb4b7532e17362ecfb709141a7195d9b01d3`  
		Last Modified: Thu, 23 Apr 2020 00:27:35 GMT  
		Size: 45.4 MB (45375951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58b7f48e83e20128df0a5d01b7597348ab8defb574e053595a286e2f6dd83ea`  
		Last Modified: Thu, 23 Apr 2020 18:59:22 GMT  
		Size: 10.5 MB (10476675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5e67ddc538ab1e6267748cb2d36fc52164160d58d5a4927d63df43108003cd`  
		Last Modified: Thu, 23 Apr 2020 18:59:20 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a21115f1856212c2e904666812621614e3fb4642584d56aa9dc0b2a832530`  
		Last Modified: Thu, 23 Apr 2020 18:59:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b59b4c42bf8fce527bd9a5b078245c1b782c8c7f6717c2c2b744ca3703c3de`  
		Last Modified: Thu, 23 Apr 2020 18:59:36 GMT  
		Size: 64.8 MB (64795852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2ddeb58199d3bf69f7b34c082eb78cd896e630d8812193d84f172678b2b096`  
		Last Modified: Thu, 23 Apr 2020 18:59:19 GMT  
		Size: 243.1 KB (243050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc03040fa343c16f66391480ae273c73bc6acd90b522c88035c2a1c21997b64`  
		Last Modified: Thu, 23 Apr 2020 19:00:20 GMT  
		Size: 276.2 MB (276208845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128231c42e0e52246bd0dffc8f39c2f25530f7afe8fc9fcc6fbe4be635b0d3ba`  
		Last Modified: Thu, 23 Apr 2020 18:59:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c0bc5b0df570463816044360cfc1f671e112c42d3969feeae8540df525d36a8b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345677739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c1664b138614872e61e929b18da0af16adc268966a4b28d35df6270da09680`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:58:27 GMT
ADD file:4921b222c4914e830c4c018324aed1904bf1526e01493120ddc9c905373b2673 in / 
# Thu, 23 Apr 2020 00:58:29 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 10:19:27 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 10:19:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 23 Apr 2020 10:19:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 23 Apr 2020 10:20:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 10:21:02 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 10:21:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 Apr 2020 10:21:04 GMT
ENV ROS_DISTRO=melodic
# Thu, 23 Apr 2020 10:21:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 23 Apr 2020 10:24:02 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 10:24:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 23 Apr 2020 10:24:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 Apr 2020 10:24:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:decabe2933bfe1939dff94ad523be4904c90e7bea69033943dd32f459d115bab`  
		Last Modified: Thu, 23 Apr 2020 01:05:29 GMT  
		Size: 43.2 MB (43159022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b84e9b12c5036e24d270012ffc332ba283c66c65bb1a11c9c36b62ac52c316`  
		Last Modified: Thu, 23 Apr 2020 10:33:34 GMT  
		Size: 9.8 MB (9774901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863092d8428511c061a2c0340a7ec4d93abf5f123245890332e777c71423f808`  
		Last Modified: Thu, 23 Apr 2020 10:33:30 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b36b14c03269a863c72850458f82fa87b8d312d31a723483b3f5702fdc05a2`  
		Last Modified: Thu, 23 Apr 2020 10:33:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2835519f2d237d39236d2dce0f921f1a6dfd9c0631be6c87023f67600d84dcb`  
		Last Modified: Thu, 23 Apr 2020 10:33:48 GMT  
		Size: 62.1 MB (62097551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966f60228a5fb4c85cc691071f60a0fc0154ee013df14567edd599f828c3b6ad`  
		Last Modified: Thu, 23 Apr 2020 10:33:28 GMT  
		Size: 243.1 KB (243119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee00549af9a42e3dd1e9bc8593968eee697343c02e19600216d07d73c9874cc`  
		Last Modified: Thu, 23 Apr 2020 10:34:38 GMT  
		Size: 230.4 MB (230401327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619c48071b4dbff1dd36122924749c4e683b84b45a23f252dd209bc3f04d4ada`  
		Last Modified: Thu, 23 Apr 2020 10:33:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

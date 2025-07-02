## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:e53caa061da22545ce77ea8b1a7ff81a793e713bd04346653706b1137261babe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:5cdc37bfe31bf795e7d81a6f00dfc4e0364f8c521d2972788d73b77288939e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308220446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72f9c81b3ab31a485c1703e525dad2aa09296ce0caabc1132684552739b6cde`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d91b30c7ff9e55f538edeb417f53d4dfb70cc741627149d8b2bc11bb4c6d855`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 683.8 KB (683757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440c05e0c6d584917470bf0bc6bf509bcd76b9d9764f2423cb91dfa3e85246d`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 6.7 MB (6745407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55c4ebd36770b2e03164d34f70b12811197e63c53da6d33184e1f4971a1d76`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (93995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2e7ff368031161d10e8464ade9bd7caecbbe51f61c0c96f634858e2cbbe1c`  
		Last Modified: Wed, 02 Jul 2025 04:13:22 GMT  
		Size: 132.4 MB (132410874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a3327298c7d6a49febab8e70915f0fc56946fe8468d9b8499c90f344e9f08`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcffa4abafb7ede5ec75389b55e4e36fc64d99306eb3a34d5efcea8775bec12`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110185283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd41262773d2505a4003851c5c45d572effbce42010711603e88ea0c8ad0a36e`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 346.7 KB (346688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c95e84a6b5f769319af314a910888e4978710b6ca98d90a42d1b5d5e01cd6f`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75ec61d69c1def2f1e185c02f880666563593f62844279b713ff44c35f2f07`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 28.0 MB (28033451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:e27cea9583e52fc0d60ea377b967a69542e2692aaff89c7470af6d836d34b1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24533433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07f975a56cd54a04589a5ad52f0e0e4420551792cac47eb8c5a89bbeec3b86b`

```dockerfile
```

-	Layers:
	-	`sha256:4e43f49e9e74006b7cff18e98d021456eadb85c52db3afa68c6842e4a1b650c1`  
		Last Modified: Wed, 02 Jul 2025 07:18:23 GMT  
		Size: 24.5 MB (24517025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653827fa9ddf396343f546cc01698d8eea594cbb2ba9c2203691561fe7c7072d`  
		Last Modified: Wed, 02 Jul 2025 07:18:24 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bf4caadd7eea9a8926c5546902344c59e883dc47859c103fd2bec0d2f060f0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296453696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7d4ff7af311d586876215b87c1f87589cd73021e4b114170b2058d66081fb7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46fee428ca8064da8e42ab2a83edde8864b2387c92ad4288a4f0a8f4dea7b0d`  
		Last Modified: Tue, 10 Jun 2025 18:23:31 GMT  
		Size: 127.0 MB (126997135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c56dbcf3bcee78c66e7611653fffffc90f5c02e8a46764509d6a4168c73778`  
		Last Modified: Tue, 10 Jun 2025 18:23:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fae5e91ffe6d48fa6890f1367c170da0c10e901ec4337a30791a899b68a883`  
		Last Modified: Tue, 10 Jun 2025 18:45:36 GMT  
		Size: 105.6 MB (105596040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f565bdcba0c35ecd1cd3d834fbcb8a96e7f87e42d22d85cc01708bea55ed5dc6`  
		Last Modified: Tue, 10 Jun 2025 18:45:28 GMT  
		Size: 345.2 KB (345208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8718eda1d80b4639b71439e318296b002a6b947659a62c101ef0700615df21c`  
		Last Modified: Tue, 10 Jun 2025 18:45:28 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633c9dcdacf75d6cc0ef05e66749bc40bc374e58679978adc043c1b7e1a8e57e`  
		Last Modified: Tue, 10 Jun 2025 18:45:31 GMT  
		Size: 27.1 MB (27123509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:7d1a37a49879ceae1d1fa6c0c09e2bdb7ad5a62099767bcb874a84d49c0506db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24562330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74bf7dca688d1859e574c9cfb05dc88a29389bf0b4c90647a495c1fc1d73bdd`

```dockerfile
```

-	Layers:
	-	`sha256:b5482aad171d09c918c0aefa3a6197182010577ec51990f8778bf441735a2180`  
		Last Modified: Tue, 10 Jun 2025 19:17:56 GMT  
		Size: 24.5 MB (24545785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9615559a7af261ba562363b965361e9d06a309632d9225a6d7a06710b28eb62d`  
		Last Modified: Tue, 10 Jun 2025 19:17:58 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

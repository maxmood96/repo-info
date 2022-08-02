## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:33870f62e883c4205382ec9ff2c2f144f010d3e9101691be15a38ae456eb8ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:17a8176d6e886bb868eb2fe93712548382781b762f62424ee98a64e194050ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437513102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2864ef7a388d5748aa5fd301591d1925922027f2e8d9189cf76018e5420737c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:02:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:02:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b7f91cbaa1e44e2ecae278c9b9bcec5d83eb8397cfd098ce9f394ca3642d2`  
		Last Modified: Tue, 02 Aug 2022 13:53:39 GMT  
		Size: 70.3 MB (70259542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e26ed31df7e549f55f79f7b17b78d0ba6d56d1cf0cd9a4f352729bc4be37f67`  
		Last Modified: Tue, 02 Aug 2022 13:53:27 GMT  
		Size: 283.1 KB (283134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99508511f69fc265efef3003c1bd53483ecc3d71f1bf6cdb319a64a2946042b0`  
		Last Modified: Tue, 02 Aug 2022 13:53:43 GMT  
		Size: 75.0 MB (74994419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:8e3ceed077fce82a58f61e42dcf7ffcdf1ac40b9cdd7aec02ab53741f70290b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386058530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69498dc4a9cdd7010aeadee61ff767774c6d805477a3a6d8e29f3f5118e3b251`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 22:59:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:59:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03108c0184ca678f48226bd3277b4d8468a25b0016664e2d80eb4c968264856f`  
		Last Modified: Mon, 11 Jul 2022 23:15:47 GMT  
		Size: 54.8 MB (54848442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67520f2af1ef3aca6f8a6fa40d040de75a19438828ea7962a63fb9846b807b4`  
		Last Modified: Mon, 11 Jul 2022 23:15:18 GMT  
		Size: 282.4 KB (282374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4114dbccc760d1e5c5ac46a04ddf9364e3769d0e596ad434cee93f0188f5ce`  
		Last Modified: Mon, 11 Jul 2022 23:16:02 GMT  
		Size: 64.7 MB (64746381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e19db181648b571c1a017e730f52145de920147e64052fa8662b7f611ac707db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411718282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56b623ecaac63fef2cd569acd1b109d44ce4a7318e7d3bda7b0c6d1e2ab1334`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

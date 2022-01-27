## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:d02ac84330454cfa90b9f5e63b23d436d8a74bca8520fb4cc41945ca4e087e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:196317766d67ba91bb5d054d0af10a397aeb1a10db4df779d28c0e88044c2359
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484704864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbeffbf8330452a6ecd305580ea2461aa7633a1adf03d9a0a369518fe5ca6f5d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:47 GMT
ADD file:a290acee3581e1e9c42c0a37b53086a8f070cb0730179be81a6ba24a620b6ee4 in / 
# Wed, 26 Jan 2022 01:40:47 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 23:06:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 23:06:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 26 Jan 2022 23:06:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 26 Jan 2022 23:06:51 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 23:06:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 26 Jan 2022 23:06:52 GMT
ENV ROS_DISTRO=noetic
# Wed, 26 Jan 2022 23:08:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 23:08:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 26 Jan 2022 23:08:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 26 Jan 2022 23:08:06 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 23:08:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 23:09:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 26 Jan 2022 23:10:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 23:10:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a024302f8a017855dd20a107ace079dd543c4bdfa8e7c11472771babbe298d2b`  
		Last Modified: Wed, 26 Jan 2022 01:47:01 GMT  
		Size: 50.4 MB (50437057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3823eedbc6821d5269b80c411515be9b79976290c5103ffea81e7312ae7e1a`  
		Last Modified: Wed, 26 Jan 2022 23:14:45 GMT  
		Size: 10.9 MB (10892052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d099017bec30424d4915d68fb48dcbb228e34aba240d5e2b00461f9b6f1230aa`  
		Last Modified: Wed, 26 Jan 2022 23:14:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef28492cab33e9c258e7458fbfe930870076e193244c77e71fc0701802d2d0`  
		Last Modified: Wed, 26 Jan 2022 23:14:42 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ee9154a1f0201850267a2d2be33d729bd2149b7236e914346385b47a4241a9`  
		Last Modified: Wed, 26 Jan 2022 23:15:33 GMT  
		Size: 239.1 MB (239083081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1686eb9ab8f2536ba7e71ff4cfde415b5d79ca59a463b9bbd872432eb6be60d9`  
		Last Modified: Wed, 26 Jan 2022 23:14:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86896ba4f61eda31b778ec342f233728fe775ef6e8fbde1c7472ebcacc517230`  
		Last Modified: Wed, 26 Jan 2022 23:16:05 GMT  
		Size: 86.6 MB (86566985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a50759417747196a92c6019a731f921df640ff86c38404efef33c4a915446`  
		Last Modified: Wed, 26 Jan 2022 23:15:47 GMT  
		Size: 301.3 KB (301283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd602dda916cfc36c8b1817430e2bc5ab1e04d67a062b0ede10a76bbd1638b81`  
		Last Modified: Wed, 26 Jan 2022 23:16:05 GMT  
		Size: 76.0 MB (75977236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d03f798aef3d66bf69f6ef723d817e9d70e80b0abcb46bcaac6703fa6bd4560`  
		Last Modified: Wed, 26 Jan 2022 23:16:24 GMT  
		Size: 21.4 MB (21444753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:576fa82187bd220314afd85c2dec1edd5a3dbff7ab9760bb708d809a53b36fa1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.8 MB (423837943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9c26c1d05bf8b845e9a78785db8b6c44eecb7d35712cae34868c7bace68ac4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:41 GMT
ADD file:98a75269e438ff15cee16ad2763fe2698fb436bc4770c0ca27c059f66b65e56a in / 
# Wed, 26 Jan 2022 01:42:42 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 07:43:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 07:43:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 26 Jan 2022 07:43:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 26 Jan 2022 07:43:57 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 07:43:58 GMT
ENV LC_ALL=C.UTF-8
# Wed, 26 Jan 2022 07:43:59 GMT
ENV ROS_DISTRO=noetic
# Wed, 26 Jan 2022 07:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 07:45:12 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 26 Jan 2022 07:45:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 26 Jan 2022 07:45:15 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 07:45:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 07:45:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 26 Jan 2022 07:46:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 07:47:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ccd458f933f7966e412773ee1551aaf2433a5bf9adaae519e2ac7c9c3f8b5f89`  
		Last Modified: Wed, 26 Jan 2022 01:49:28 GMT  
		Size: 49.2 MB (49223041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646734dd4c9771207c4468eadc7ddcededd306975b1af9c589d4cdcda9b7c07b`  
		Last Modified: Wed, 26 Jan 2022 07:52:46 GMT  
		Size: 10.7 MB (10688073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3aad39826b43f6faf1264f98a0a52a206ef90890c6834072d8d9f87d882868d`  
		Last Modified: Wed, 26 Jan 2022 07:52:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed8a7e03b40bfdb16508119c9ee410dd3684b3a5cf4bc31f5f6dd1597a12fee`  
		Last Modified: Wed, 26 Jan 2022 07:52:44 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32e34cb56b02431259e0ed70e5f2a62c5cbae86038cc51c240276d1c687014f`  
		Last Modified: Wed, 26 Jan 2022 07:53:15 GMT  
		Size: 184.3 MB (184306695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86270cb85ef2ff4c03d623ecfac134b2c9cc1bbd6a17a0d9a16eb961841ab45`  
		Last Modified: Wed, 26 Jan 2022 07:52:44 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead2d175559e1deb0533f1a26d062151a70ee020c83b271d672febcae2962201`  
		Last Modified: Wed, 26 Jan 2022 07:53:34 GMT  
		Size: 84.4 MB (84350117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ee083a5f0a1bb7f96a6fa942a09843a7a85dd23f6c421fc1030cc2233c1fb0`  
		Last Modified: Wed, 26 Jan 2022 07:53:24 GMT  
		Size: 301.2 KB (301224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f310f444237727027c0400435c277b87c69c67df7b68e96da508934404d5a1`  
		Last Modified: Wed, 26 Jan 2022 07:53:34 GMT  
		Size: 73.9 MB (73864375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d183952954eb4bb2037eb954eb068a02e117f48638cb6a216bd8ae16200ca0`  
		Last Modified: Wed, 26 Jan 2022 07:53:46 GMT  
		Size: 21.1 MB (21102047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

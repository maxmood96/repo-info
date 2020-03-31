## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:4d5031bee02644af09d695a79ce9fa50e1a067a02ca85ebf33672764720e9aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:5f498483e45cf0e3d1acfa06d7752c3661ac698250364ab23511d0eba9862533
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518836021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82445c20abb5269640b348a104577de4d59cf65f2d52fa70402d21a110bf95f5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 18:17:30 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:17:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 26 Feb 2020 18:17:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 26 Feb 2020 18:18:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:18:26 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 18:18:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 26 Feb 2020 18:18:26 GMT
ENV ROS_DISTRO=melodic
# Wed, 26 Feb 2020 18:18:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 26 Feb 2020 18:20:45 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:20:47 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 26 Feb 2020 18:20:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 26 Feb 2020 18:20:48 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 18:22:07 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:22:51 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7851b385b3454126f02da75d871c31cab343adb6252f96c606208321ebe5f424`  
		Last Modified: Wed, 26 Feb 2020 18:26:49 GMT  
		Size: 10.5 MB (10476682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0f3c809d5bd964fa9c99f4d533d31508fe61ced1652651935ec77d4fa693fe`  
		Last Modified: Wed, 26 Feb 2020 18:26:46 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d860519553be9002ec6cc168b986adc95e13723c9d114964b18cbea0e19c90`  
		Last Modified: Wed, 26 Feb 2020 18:26:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16b9d760787b93bb8c3f0c7872b401fb00d96f3fd2a870a6f83e531d20d85e`  
		Last Modified: Wed, 26 Feb 2020 18:27:07 GMT  
		Size: 64.8 MB (64770161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9baabdeab314d3737e662c388e0b2b03c57de9e21f1e9e6aad43c4f78764c81`  
		Last Modified: Wed, 26 Feb 2020 18:26:45 GMT  
		Size: 426.8 KB (426764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b928396e18c50dff7d8bbe31d6340783a3d4472fa5f16f33a49fab28739f228`  
		Last Modified: Wed, 26 Feb 2020 18:27:50 GMT  
		Size: 270.4 MB (270426039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647876d988155403f463b985cdcbf476c331e01ce9b2bfd71b391abd87b27540`  
		Last Modified: Wed, 26 Feb 2020 18:26:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ed7a7ca1ab232e4fbf2652a60bbcc29ea6fe09a6c4dabb1b2db4de08ae08e9`  
		Last Modified: Wed, 26 Feb 2020 18:28:21 GMT  
		Size: 108.5 MB (108474685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160c41d0824bffb133bb650bb7af94fa3176c89975d9f594530b8065c5679f99`  
		Last Modified: Wed, 26 Feb 2020 18:28:30 GMT  
		Size: 18.9 MB (18883941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e606a1ff5eaf81a5a8261b20a333ffaa3ccf45a6e432922a5162a0aaa3c77f91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 MB (467061616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a6d5268b78978d2c1623f036d0b33f0a48d052077e96873337c5bd565ca7df`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 08:50:19 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:50:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Mar 2020 08:50:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Mar 2020 08:51:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:51:56 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 08:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Mar 2020 08:52:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Mar 2020 08:52:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Mar 2020 08:55:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:55:32 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Mar 2020 08:55:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Mar 2020 08:55:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 08:56:58 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:57:53 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffb04892983b197ec2012ff1e5f489d298a3d1e097fd400e600d9f5ba5b696`  
		Last Modified: Tue, 31 Mar 2020 09:05:05 GMT  
		Size: 9.8 MB (9774723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6b8b721a085eab12f64779dec536ba34ac8f16dd1717c52ef7b9c274c7dcec`  
		Last Modified: Tue, 31 Mar 2020 09:05:02 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a13c4ba112de5fca316200409698b68af67bb359c22880fedb9f0c978529dae`  
		Last Modified: Tue, 31 Mar 2020 09:05:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550ce74e2e465788ad2b3705897a2121bdf9917d0c435e7fdda3fbf0ff46e225`  
		Last Modified: Tue, 31 Mar 2020 09:05:18 GMT  
		Size: 62.1 MB (62092992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1d9278a758d83e399e2983b086d9bb98a57834e9baab02613f2bf95d5eca06`  
		Last Modified: Tue, 31 Mar 2020 09:05:01 GMT  
		Size: 440.0 KB (439964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c288a14eff30367048e215968facd583b69208c88f246db36f95de84f9f95f2`  
		Last Modified: Tue, 31 Mar 2020 09:06:04 GMT  
		Size: 230.4 MB (230401952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869ba1a44b39237de723e6eda8cbc9d92fa5702dd1accdffa458c18710105b60`  
		Last Modified: Tue, 31 Mar 2020 09:05:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e006598e8f8b8d7108107e4dfe8806ed90da205417bf5afa1a33fc09b12f664a`  
		Last Modified: Tue, 31 Mar 2020 09:06:37 GMT  
		Size: 103.0 MB (102959855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d08a535c9140d80207b2374b2474327c57d353afcff792fd6a2f233599434d`  
		Last Modified: Tue, 31 Mar 2020 09:06:48 GMT  
		Size: 18.2 MB (18232195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

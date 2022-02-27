## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:53f2cc58acc113e7f02e52887aa64672ba285a563478f0310903b02090c0e8a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a9f06a2cd3783fdd97d9963962b46c15a75b64e87cab2a7912757ef2e1e2158b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276681459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc563451289e59c32428decce473402ad442b81721f9011c23dba27fb3cad4d9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:55 GMT
ADD file:14faf487f471b0c41efdbd2280f1d905387bf534ef8810abd3a37774ba55ca12 in / 
# Wed, 02 Feb 2022 03:19:56 GMT
CMD ["bash"]
# Sat, 26 Feb 2022 00:44:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:44:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:44:29 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 26 Feb 2022 00:45:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Feb 2022 00:45:07 GMT
ENV LANG=C.UTF-8
# Sat, 26 Feb 2022 00:45:08 GMT
ENV LC_ALL=C.UTF-8
# Sat, 26 Feb 2022 00:45:09 GMT
ENV ROS_DISTRO=rolling
# Sat, 26 Feb 2022 00:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 26 Feb 2022 00:46:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 26 Feb 2022 00:46:11 GMT
CMD ["bash"]
# Sat, 26 Feb 2022 00:46:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:46:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 26 Feb 2022 00:47:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 26 Feb 2022 00:47:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a99755935c0ed83076913ebdfc8b5a435fda0bdb7463e3f44b9c68ccfbabfc15`  
		Last Modified: Wed, 02 Feb 2022 03:22:20 GMT  
		Size: 29.0 MB (28957023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58066ccb94244f7b05c1e3f0da559277e10da1c9c0ba92fa419a08eae94a70e0`  
		Last Modified: Sat, 26 Feb 2022 00:49:20 GMT  
		Size: 1.2 MB (1193898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319c7eb9c853b6e46cdbca80f7eef1ecd99450449be76c3335cc15b720c9870d`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 3.6 MB (3596216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40894fefa8f50a868c983395fcabf33b97aa0717112a45273475437fa80fbace`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f288530d3ee34e27854ee0c701df63d10fb414ed7a7bb00ae7cbfa0371f494`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58266d751be66d0d2f814c0010414fe3821c7a1daaa0b2d848cbd773734e67f5`  
		Last Modified: Sat, 26 Feb 2022 00:49:39 GMT  
		Size: 123.2 MB (123197430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6502c9f94ca6d8962989e8134a1c6b91908eb368eede3f2e9a328364a566bb`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe21fb9f030b837dd1aba2be729d795ac8f13ac5ae07aaabe204b50d84b1b0d`  
		Last Modified: Sat, 26 Feb 2022 00:50:05 GMT  
		Size: 97.2 MB (97191425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd56872b6acb157d053d0a7b471ee7e96bff8302b49c71b111542e9504f43311`  
		Last Modified: Sat, 26 Feb 2022 00:49:51 GMT  
		Size: 264.6 KB (264550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ac08fde67a71b5457791a4fa367ad73577ea97fcfcc06494cc178db47b6921`  
		Last Modified: Sat, 26 Feb 2022 00:49:50 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50a89cadb283b5a6d249f660c12216298fc56d461e1f120905c14cae4d41bba`  
		Last Modified: Sat, 26 Feb 2022 00:49:54 GMT  
		Size: 22.3 MB (22276404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

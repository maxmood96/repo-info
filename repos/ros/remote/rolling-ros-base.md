## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:687e5b668a62a58ed0b829430fdea44e41b30434762f31367bf698b19fca101a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:8e4a0a03e314891d8e91dfac9ae459fdc8c5f024eeb28a41fa966302cd017c7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234174050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2884534333126ef55c819fb2a2e54f1a6fb37114fc526ec904ea28510c3fbf1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:38:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:02:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Feb 2022 05:03:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 05:03:32 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 05:03:32 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 05:11:07 GMT
ENV ROS_DISTRO=rolling
# Wed, 02 Feb 2022 05:11:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:11:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 02 Feb 2022 05:11:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 05:11:56 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:12:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:12:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 05:12:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 02 Feb 2022 05:12:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762bb72141f73c9f8d23d9bc2396670126e4d86b9784e31484c651effc425f91`  
		Last Modified: Wed, 02 Feb 2022 03:38:42 GMT  
		Size: 1.2 MB (1182237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52b7e3f584549fa72b610dfd0819030eb6eb0a3a76a5d820599a986bb362dfb`  
		Last Modified: Wed, 02 Feb 2022 05:17:49 GMT  
		Size: 5.5 MB (5546994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ae25a4694ef2001927cb29325cd8fc4076b59d0d944cec831ce55095c4cb64`  
		Last Modified: Wed, 02 Feb 2022 05:20:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b7b6d92a2fd7f05c2ab982e2eaf8a7bb43a271459e4c3d5b978ff3f3de151f`  
		Last Modified: Wed, 02 Feb 2022 05:20:30 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a604e8b32e44634ee8bc44c5db72cf946ed924a3bd6b8a88c00005d30f659`  
		Last Modified: Wed, 02 Feb 2022 07:03:36 GMT  
		Size: 105.2 MB (105176656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cf2a28f9189a2e1160ff4ad2036e2fe72707cba2e34219d80788386b694234`  
		Last Modified: Wed, 02 Feb 2022 07:03:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2feec7b9c814f54176381aff001dad9f176dcc0d305eded40d4bb8e41709ae61`  
		Last Modified: Wed, 02 Feb 2022 07:03:57 GMT  
		Size: 70.8 MB (70808484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7987a75570b7bd28f024428bb3a29092902bd8f41ee4f9fd24d8509c21d6c288`  
		Last Modified: Wed, 02 Feb 2022 07:03:46 GMT  
		Size: 252.4 KB (252440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8546ff2ddead8c40774bad773231a693f4125f9a3dde7f454e8dc7cfeb30f49a`  
		Last Modified: Wed, 02 Feb 2022 07:03:46 GMT  
		Size: 2.2 KB (2202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cc68e59034c3716b3df6f8f0cc69b5a22ae592cb7c6429dd0241f017ebcde5`  
		Last Modified: Wed, 02 Feb 2022 07:03:50 GMT  
		Size: 22.6 MB (22638523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

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

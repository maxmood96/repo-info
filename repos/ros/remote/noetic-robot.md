## `ros:noetic-robot`

```console
$ docker pull ros@sha256:5cc5578f038e0536340a965355dc7871db0095460e947c71c0c00201f7bb7214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:f7140a67da24853af70f42b8d78d682bcf9cc45907ad74f9886cedb3c4939f83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354946140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b211266230d77466432d034f5d374384bdf95b61211922e43c03a0c77af7cb4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:53:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:26:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:26:02 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 03:26:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 03:26:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 03:26:10 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 Oct 2021 03:26:10 GMT
ENV ROS_DISTRO=noetic
# Sat, 16 Oct 2021 03:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:28:05 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 16 Oct 2021 03:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 03:28:05 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:28:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:28:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 03:30:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:30:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3c993d4c25d2ec8adbe5b497acc2226d8b6b602f68679037b8993f53617e2b`  
		Last Modified: Sat, 16 Oct 2021 03:02:27 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e9dfa7092d8b77085dc1f7f400d3a0618187cefd4af7037e9dec2f88eadec7`  
		Last Modified: Sat, 16 Oct 2021 03:46:47 GMT  
		Size: 5.5 MB (5547495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ef1669a6b741da8d10348ca5478bc92ed459dd5ae9dc872bc2901aa4a4885a`  
		Last Modified: Sat, 16 Oct 2021 03:46:46 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7bc8cdeda44965808907e244e5edd3ed9d6efd6c0105fc84123b986946a806`  
		Last Modified: Sat, 16 Oct 2021 03:46:46 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b82bc5a2b4db46195d4cb9bb39816b83ede6c31f565651abb9b15e6d4335ee8`  
		Last Modified: Sat, 16 Oct 2021 03:47:14 GMT  
		Size: 176.7 MB (176707219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6389d5741667b5453a3f2fd8e79c5521bf1f17e95d6042d56595b80623e04aba`  
		Last Modified: Sat, 16 Oct 2021 03:46:46 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d0df0db2441b7744370d28a551a1152f79b7249050aa09e18996bbd0428ebf`  
		Last Modified: Sat, 16 Oct 2021 03:47:32 GMT  
		Size: 47.3 MB (47259872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80707a4f3d4ddd0562cb757ab166458ffe0a134b59935f1619d10653486a8049`  
		Last Modified: Sat, 16 Oct 2021 03:47:24 GMT  
		Size: 322.9 KB (322897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626c61368773f58359917c9e5cd1e8c6555b27f66d55fda64ca5306f6748046b`  
		Last Modified: Sat, 16 Oct 2021 03:47:37 GMT  
		Size: 79.6 MB (79604503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943befb25f2aa4af6ba036d4dab1cede9f6b46fa36708c220fc86920c38bbfcf`  
		Last Modified: Sat, 16 Oct 2021 03:47:52 GMT  
		Size: 15.7 MB (15748462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9a7de897dae99a7589a7d920c3fc323a2b1b2ab317f8d997a0958605ec26188b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298573997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4021fb42a3360ba288aadda7e5e6d7d9f5b59bfcf5ecb74b9ca689f5d238c6f7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:12:00 GMT
ADD file:625e3906181f4bd86e59a0e9748f67fcb1391a2e65e36c729e71353381a49757 in / 
# Sat, 16 Oct 2021 01:12:00 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:17:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:17:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:17:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 02:17:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 02:17:54 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 02:17:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 Oct 2021 02:17:55 GMT
ENV ROS_DISTRO=noetic
# Sat, 16 Oct 2021 02:20:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:20:16 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 16 Oct 2021 02:20:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 02:20:17 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:21:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:21:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 02:22:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:22:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8795d4da4abd6abcafe7285749aa85d3a164999e84720a3845f764e56e306771`  
		Last Modified: Sat, 16 Oct 2021 01:15:01 GMT  
		Size: 24.1 MB (24064451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764ddf81fcf398a2a4cf14036409b82f4f4a06bd8f23171e840ff36accba4d4f`  
		Last Modified: Sat, 16 Oct 2021 02:29:43 GMT  
		Size: 1.2 MB (1186846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02b4dedc9080b63cee4513e2787d54376223246780de27866414412fce505a7`  
		Last Modified: Sat, 16 Oct 2021 02:29:43 GMT  
		Size: 4.7 MB (4676770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb049eda64c876c1ee585dd51f3f8b9a9807c82541e8243ea725bcf5ee59fb2c`  
		Last Modified: Sat, 16 Oct 2021 02:29:40 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7037e3e565c8acccf66678f470f9ceae8503c90974e2dd927764191193ffdbb`  
		Last Modified: Sat, 16 Oct 2021 02:29:40 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69724b9a0973ce0c31fba9293b5ca2cc8e252ee13673b3053258594c1fa8b815`  
		Last Modified: Sat, 16 Oct 2021 02:31:48 GMT  
		Size: 157.2 MB (157179504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df68017d0a78706560ec19c60581120f31997ecd5e9223e1eec432c47ae86e8`  
		Last Modified: Sat, 16 Oct 2021 02:29:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb98f2a916633a1fb1a69dd5aebc5416fb396d43233943523788ff874a76fde`  
		Last Modified: Sat, 16 Oct 2021 02:32:19 GMT  
		Size: 36.7 MB (36691673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7242c94fc3e260adf5325a33e1e99237f52197a87e7ea5b471bdd8bd9eb4b0b0`  
		Last Modified: Sat, 16 Oct 2021 02:32:00 GMT  
		Size: 322.9 KB (322903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5bbb4e057a5f879119a31a98e9617ab535d39046bf80b55735ded907115af3`  
		Last Modified: Sat, 16 Oct 2021 02:32:38 GMT  
		Size: 60.5 MB (60484275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a73ef1a5ea79bedbff1bb66d2f1ca1debb4e3e7765cdeeb3e358f8ce0414b5`  
		Last Modified: Sat, 16 Oct 2021 02:33:03 GMT  
		Size: 14.0 MB (13965158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2f3aeaf51a9ac77b48225d1409b34c215f795f9a712512976654c5aca682694b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333540491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43134256327b8117993acef98a723b33f18ce79eeb96bc4afdc4664950dcbe35`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:19:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:19:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:19:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 02:19:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 02:19:41 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 02:19:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 Oct 2021 02:19:43 GMT
ENV ROS_DISTRO=noetic
# Sat, 16 Oct 2021 02:20:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:20:37 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 16 Oct 2021 02:20:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 02:20:39 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:21:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:21:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 02:21:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44426e3a0ed188569ceb995612f61d01b012f19e6849dacdcdef24f70e9e820b`  
		Last Modified: Sat, 16 Oct 2021 02:44:04 GMT  
		Size: 1.2 MB (1186725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74557b92a76c488a6e2f31c091f03671baadbd5b593c4af9dbde2baea1616333`  
		Last Modified: Sat, 16 Oct 2021 02:44:02 GMT  
		Size: 5.3 MB (5322455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c260b335cf07f336d1a4e8a82a9d7c692b2bd9787a59304939f8efa4f0101336`  
		Last Modified: Sat, 16 Oct 2021 02:44:01 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c22181ff3d3903d9cd1bf4e764959b25637ae8513f97bce318dd8a7bd39e5ac`  
		Last Modified: Sat, 16 Oct 2021 02:44:01 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4102e4fa66f5f968fd33f8eba29fb388cbe15692b65aa6ee4b73ee49911cc03c`  
		Last Modified: Sat, 16 Oct 2021 02:44:31 GMT  
		Size: 171.1 MB (171127704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd3223aef57941776d9e8c82021b54601bc6c98c9c4e37c09088868f34689ad`  
		Last Modified: Sat, 16 Oct 2021 02:44:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67dce296a497287c39667aecbda14a56772cabb7fce0bf6814c5b0fc71fe902`  
		Last Modified: Sat, 16 Oct 2021 02:44:48 GMT  
		Size: 41.3 MB (41305313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b380c08d48bfaa5743c1d9aa123728e4bfe4d4de65c3042c42b18d2316d777`  
		Last Modified: Sat, 16 Oct 2021 02:44:42 GMT  
		Size: 322.8 KB (322832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c1c8b80456c31f0be34412d39189749a6937d731e58136ac9d81186b6dbc6b`  
		Last Modified: Sat, 16 Oct 2021 02:44:52 GMT  
		Size: 71.8 MB (71754103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9588c58320e3d7dc3f7913b1c3e314b42ff8f4161ab305728a1932470117d2b`  
		Last Modified: Sat, 16 Oct 2021 02:45:09 GMT  
		Size: 15.3 MB (15348088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

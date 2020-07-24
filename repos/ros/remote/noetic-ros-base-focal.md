## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:c2eb7a5509c473b693f7f06077e7415bd76d965c9d21d92e561c176c9dd7ef15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:e75100c19ae74ffa8ecf7079565674b0baa5aef4b2dac457a572d6899424693b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334539158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc7024b45dc184528697afc6d5dbb07867c9695cf9bd8701ac32e8acd05bf1f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:51:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:49:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jul 2020 00:49:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jul 2020 00:49:01 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jul 2020 00:49:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jul 2020 00:49:02 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jul 2020 00:51:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:51:10 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 07 Jul 2020 00:51:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jul 2020 00:51:10 GMT
CMD ["bash"]
# Tue, 07 Jul 2020 00:51:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:51:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jul 2020 00:52:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbd34696aad22f9a861bdae9aed1bc14aed3426d245147e55a759747acc2357`  
		Last Modified: Tue, 07 Jul 2020 00:03:20 GMT  
		Size: 1.2 MB (1175806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8d44cae379b4797d812ed05b65c080aba6074d55e8d8b0b0c612b3923d9f5a`  
		Last Modified: Tue, 07 Jul 2020 01:21:06 GMT  
		Size: 5.5 MB (5549483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220c1b9e59cfca503e7910992752f72112d96b996c272d25c279bcbe31fb9210`  
		Last Modified: Tue, 07 Jul 2020 01:21:05 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a4ba7e4fc497b4f1a0be7a446e50235b46dad5ccad278a3a8ee1cc40e891f2`  
		Last Modified: Tue, 07 Jul 2020 01:21:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3553832b88c00e08e2838c2b9831cdd3d12abea4969df2f9170580e76d7b7a`  
		Last Modified: Tue, 07 Jul 2020 01:21:49 GMT  
		Size: 173.0 MB (173047564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af350ef5cb0c86ea4497ddb587024085e35048a6edae8416c61954111ed90ce`  
		Last Modified: Tue, 07 Jul 2020 01:21:05 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb8012838b451399d9b57fa8eb40bbfc912ace7dc1daf6671bfa781a6bc50eb`  
		Last Modified: Tue, 07 Jul 2020 01:22:06 GMT  
		Size: 46.4 MB (46376782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33c9f959bd295d8b1b1f5d11901bcb3abb802c2c534df01d6e0404b40d9836`  
		Last Modified: Tue, 07 Jul 2020 01:21:56 GMT  
		Size: 208.3 KB (208299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5a4dffdb19655973f9340673658972b78a8c4584ad6df4035e99e40d54170f`  
		Last Modified: Tue, 07 Jul 2020 01:22:12 GMT  
		Size: 79.6 MB (79589297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:8ed028798a4d96a61ef52241ac83bef0f96f8ac18b98eb394eb62924cd7ea2b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283364277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961de88153281aa16c10812d1172cabfec46d7c5bba098aeb2a5d9159ae08ebc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:06:12 GMT
ADD file:bcba01fb27d025c2931e46af0b091f98e743ab46eaa1d2d2dd38e6aeb9706267 in / 
# Fri, 24 Jul 2020 16:06:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:06:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:06:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:06:55 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:56:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:57:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:57:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 16:57:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 16:57:40 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 16:57:40 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 16:57:42 GMT
ENV ROS_DISTRO=noetic
# Fri, 24 Jul 2020 17:00:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:00:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Jul 2020 17:00:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 17:00:27 GMT
CMD ["bash"]
# Fri, 24 Jul 2020 17:01:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:01:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 17:02:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86924fd76ad7a77a1ec54ad07fdb4d2d51c12b6070f2dfe92dbf92e3f99702d7`  
		Last Modified: Mon, 20 Jul 2020 15:50:15 GMT  
		Size: 24.0 MB (24034159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e967235e6adc918de90ffb2d143fb1ad2659c63f6c0c8a9c70c8e08bff13917`  
		Last Modified: Fri, 24 Jul 2020 16:14:35 GMT  
		Size: 32.3 KB (32349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabf100c8ea14f6342f16b9b10cb81a1355aa9a9d6b8f607c04119c9790f1a51`  
		Last Modified: Fri, 24 Jul 2020 16:14:35 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344cec738d225bc4e9abb563b22a040685352088e9d588d910c09039fa47ac35`  
		Last Modified: Fri, 24 Jul 2020 16:14:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db3aa3613375ef4b3a20f761ea9ee7b4a2d7a5a8ba02beaf139afca5ba98016`  
		Last Modified: Fri, 24 Jul 2020 17:39:24 GMT  
		Size: 1.2 MB (1176123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca1f53a3e050e644e9835020656893ba92f99f89ea00f2fa201ca3ca70eede6`  
		Last Modified: Fri, 24 Jul 2020 17:39:22 GMT  
		Size: 4.7 MB (4674467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbb05f89ba7c924c242b65fb6989694fd3ad576d16ef0b3a36b0eb84fc17d06`  
		Last Modified: Fri, 24 Jul 2020 17:39:20 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30bb8e6d3ab246ab3341492777db22a2ec2aa222a9512b6a56ce65a616f6c6b`  
		Last Modified: Fri, 24 Jul 2020 17:39:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a829353a0e8b7a79b7e6c40a51ed16c28cb36bdb08b54c2d069b25735cdfc7`  
		Last Modified: Fri, 24 Jul 2020 17:40:36 GMT  
		Size: 156.9 MB (156930285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1115b30ceb9d322e7704f0537f41adf925596263b80ff9f92d9e2e2f0b4a4277`  
		Last Modified: Fri, 24 Jul 2020 17:39:20 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a4d4e295300a02c20154993910715d3dec4b0ffc57be2f5e7fe154d0108df8`  
		Last Modified: Fri, 24 Jul 2020 17:40:58 GMT  
		Size: 35.8 MB (35825432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cd4c4ee78aa6572e183ca112e24abcb0595743376636ec590e11007260790b`  
		Last Modified: Fri, 24 Jul 2020 17:40:46 GMT  
		Size: 214.1 KB (214071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f36828c5b50134fdd8a55e19a85c39643ea1d4d41a3301cbe3acb77aa0643`  
		Last Modified: Fri, 24 Jul 2020 17:41:08 GMT  
		Size: 60.5 MB (60474513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c434e5ba2b0316a78f599914e7d533b2c93b9ac252f402a7f8782ed8a88667e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314219572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3822d6c40e2094df0af9f0f5b22a780aac0f4715807258bfc9dd366d8a754f7b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:24:06 GMT
ADD file:26bd57f1dbcfd1a91715cc84cf0f221783655f16bbb7a912aaf20507cc252535 in / 
# Fri, 24 Jul 2020 16:24:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:24:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:24:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:24:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:57:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:57:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:57:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 16:57:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 16:57:55 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 16:57:57 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 16:57:58 GMT
ENV ROS_DISTRO=noetic
# Fri, 24 Jul 2020 17:00:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:00:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Jul 2020 17:00:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 17:00:27 GMT
CMD ["bash"]
# Fri, 24 Jul 2020 17:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:01:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 17:01:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3583fd5e2faf2976fb6333a3a15414f2708dc284c018a672e37112326bc7b7a1`  
		Last Modified: Mon, 20 Jul 2020 15:50:10 GMT  
		Size: 27.2 MB (27159444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2d9e0aed378588f59f8f4276e70ea379b773d7d6507046cd7a044601499785`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 32.3 KB (32333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4a6dca9e536449681a937b8f49022cb56b230e352da8aed9b616fadb14dc30`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d9e98650a6106452fc9e640abe8929399fa4f7a0d3ef58a593e8d68cdf3a6`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877914f23fdc8a3fd15f9b3daa4a5a017f378e476b524967a0ab3874b518fe5`  
		Last Modified: Fri, 24 Jul 2020 17:48:49 GMT  
		Size: 1.2 MB (1175990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd422d18fc87ff73ecb113f2cf765e9b4e16079bb0f4c697b78fc61dfbbbb2f`  
		Last Modified: Fri, 24 Jul 2020 17:48:49 GMT  
		Size: 5.5 MB (5511790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dec9f244ed77fbf977c9357ced59b8843bba14d99bbbaf00a19cb797f655a`  
		Last Modified: Fri, 24 Jul 2020 17:48:43 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff367bc918482f32060ec178a70e4778da4ab726a2cac0b3486544c7a149b8`  
		Last Modified: Fri, 24 Jul 2020 17:48:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d578882beeae62473352d92f147d6f53c4066c644758437cfff4acf1ea540a9`  
		Last Modified: Fri, 24 Jul 2020 17:50:52 GMT  
		Size: 167.5 MB (167527427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19eb24859fd470fbf7eb93317002cb77e6df727d668fba9c9096191d061e2c3f`  
		Last Modified: Fri, 24 Jul 2020 17:48:43 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd422968fddb9e9d3185e814e8e00601cc83b257dd245e8ee9676d8bd92d9a28`  
		Last Modified: Fri, 24 Jul 2020 17:51:21 GMT  
		Size: 40.6 MB (40626996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d561ef02b56885e46087f88211bf84cbbf834df962f3d635733c22763b73b9`  
		Last Modified: Fri, 24 Jul 2020 17:51:04 GMT  
		Size: 214.1 KB (214079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f2d68529c416ffa427fcb5086a686db08f43c9c70c2547e89209103606e1b9`  
		Last Modified: Fri, 24 Jul 2020 17:51:36 GMT  
		Size: 72.0 MB (71968640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

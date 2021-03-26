## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:c0da95632b6c1ffc0437a8cdacdaef6d96b601cf6591b13eae930e0894bc2e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:8712d2e283cfb7a60aef1d4b008a0e1b6a4a0b77280b807356d789450d8df016
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.0 MB (833988756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdac3356c2653b4158023bc8f860c9e2d6f56b2e65caac42b6fc286aabe4f8e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:08 GMT
ADD file:a8d2f02fbaddf8cec8e4da320cd03c06435f395e9d454f69954efe422eb6e1ba in / 
# Thu, 25 Mar 2021 22:33:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 11:25:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:52:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:52:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 12:52:52 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 12:52:53 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 12:52:53 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 12:52:53 GMT
ENV ROS_DISTRO=noetic
# Fri, 26 Mar 2021 12:55:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:55:52 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 26 Mar 2021 12:55:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 12:55:52 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 12:56:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:56:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 12:58:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:07:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04a5f4cda3eea2313a61a2f72208342a57ea36a9326dff54f4f26ed47d145c7c`  
		Last Modified: Thu, 25 Mar 2021 22:34:46 GMT  
		Size: 28.6 MB (28569428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff496a88c8ed9b745dab2f00bfbd9013c6d1db198442a6a8683998a29a85458a`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce83f459fe7e0bf459d0c222ef3b2ca4d9911f6b0f9aae02c2120561b54ca18`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4c238a927e44fc68e49f93b318a224102c5d7eed49fc3af359975559e12857`  
		Last Modified: Fri, 26 Mar 2021 11:46:19 GMT  
		Size: 1.2 MB (1182444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31284e097e1d0ebfe603632f456f1b3448f6f14c43b12ead735c6914fe702e0`  
		Last Modified: Fri, 26 Mar 2021 13:37:24 GMT  
		Size: 5.5 MB (5547694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d7646f67a7f499fee4f81d175005244721e2da4e7c26ca4043e71e31ecf316`  
		Last Modified: Fri, 26 Mar 2021 13:37:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70198e83abfa521fda587ae8a3d2baf770df4e5dc959d762067057a2c2308f84`  
		Last Modified: Fri, 26 Mar 2021 13:37:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9ee2aa76928d771b6dfe2695bee64940c368adb80d8134d25fcfaaa5ea3493`  
		Last Modified: Fri, 26 Mar 2021 13:38:03 GMT  
		Size: 173.3 MB (173295586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5a7dd3465b6e52f39ff3887c53e2751c36bdf468a087017b8221ae04c56b02`  
		Last Modified: Fri, 26 Mar 2021 13:37:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8e6a722d5b755c0832d4bdce3e8c61d5ea3eb36525b75e797068ae2c96b227`  
		Last Modified: Fri, 26 Mar 2021 13:38:24 GMT  
		Size: 46.4 MB (46384402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6262dec7be56d79f14a3cd0f0ed661a385d04374295e7ba919856bec13f562c9`  
		Last Modified: Fri, 26 Mar 2021 13:38:14 GMT  
		Size: 279.5 KB (279525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b2947ee31f1717373ef43334dbb57d3598fef05528eb281d6ee5944ca4c266`  
		Last Modified: Fri, 26 Mar 2021 13:38:29 GMT  
		Size: 79.6 MB (79600502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4940f812f2d76cbd5c24eb1806a0c9bb604694f808b57b860443e83bdbb9fc`  
		Last Modified: Fri, 26 Mar 2021 13:40:33 GMT  
		Size: 499.1 MB (499126303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:0d9af03b6f648f1ad00b91a636252fc612410c36ce24df48f1a252a3f009f68f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.0 MB (726991934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e92f28dacab6d2dcb5719f6c0d7dcda08a0072628b593bbd58cc8ae0b8810c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 09:13:57 GMT
ADD file:25837d016ed8e3cc502b297c3a904ffacc471c2f9d4ee2cd1131bd652ea28faf in / 
# Fri, 26 Mar 2021 09:14:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 26 Mar 2021 09:14:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 26 Mar 2021 09:14:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 26 Mar 2021 09:14:24 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:17:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:18:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:18:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 14:18:21 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 14:18:24 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 14:18:25 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 14:18:26 GMT
ENV ROS_DISTRO=noetic
# Fri, 26 Mar 2021 14:21:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:21:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 26 Mar 2021 14:21:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 14:21:09 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 14:21:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:22:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 14:23:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:29:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c694f656c1b09a697b76142fc22d737f2aa522515c6c1361bf3ccca7ce42f17f`  
		Last Modified: Fri, 26 Mar 2021 09:16:41 GMT  
		Size: 24.0 MB (24047936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb044b09d0cc8ed58817ae0ce7784aafe41640dd7e214d6700b162b10629353`  
		Last Modified: Fri, 26 Mar 2021 09:16:34 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58af11d697841141a01eee137c7fe4870f077615c2691bf041ba9b331e3de7fc`  
		Last Modified: Fri, 26 Mar 2021 09:16:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba64b3ebc8e28942d0d4a89413be25f6e14f8594d7d344f3e3bee71d72491907`  
		Last Modified: Fri, 26 Mar 2021 14:55:57 GMT  
		Size: 1.2 MB (1182827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342f00c9ba64a9974d07460a9b84f6dabbe0522e445b0dbf0b7320c592364a7`  
		Last Modified: Fri, 26 Mar 2021 14:55:51 GMT  
		Size: 4.7 MB (4676514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5653571daf085d44fe5a76b6f40d0a17af15fa6eb186d9510ccf7b03921585`  
		Last Modified: Fri, 26 Mar 2021 14:55:47 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52284787efb0dfe4b561df66911fe5780055b038912f55bd4160ca6c293b66e9`  
		Last Modified: Fri, 26 Mar 2021 14:55:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c6853b71a6bbf1d5a75106a2d2aa823586dd609d78539f7cd5b502bffe71b3`  
		Last Modified: Fri, 26 Mar 2021 14:57:46 GMT  
		Size: 157.2 MB (157156861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87b28140a1a006d06e1ebb4bfdf2d259ca237b337692abe273f79868ae98ee9`  
		Last Modified: Fri, 26 Mar 2021 14:55:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fa4e87d722288c2794904fffb34c8b9372454f2961ac04d536874d91943a23`  
		Last Modified: Fri, 26 Mar 2021 14:58:05 GMT  
		Size: 35.8 MB (35832254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43809d4d22ca3854cbdcddcf454a3d56d497171ec0011cdd26f665c268859ca`  
		Last Modified: Fri, 26 Mar 2021 14:57:55 GMT  
		Size: 279.5 KB (279540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151a88786b497c2e3220d719c3861329c83b9db60af475033762291a5ffaa391`  
		Last Modified: Fri, 26 Mar 2021 14:58:15 GMT  
		Size: 60.5 MB (60478502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcfe3f3c6006433abada01c7e454b17f72ebf3d65ea0922f3fb29f4635de4b5`  
		Last Modified: Fri, 26 Mar 2021 15:01:18 GMT  
		Size: 443.3 MB (443334625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:805a824a06cb5c46dd9bb34afc3d69c557d10c1a60e906ad4fadf59d26665cdd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **782.9 MB (782882454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea6808e4013a6398c80c6654b4c1f7e12e7b8fb29c742c6cdb5f36584864354`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 23:22:32 GMT
ADD file:ee49f9e75d7f5923826cf089f2ac0100a27ef7051f10c31b310b573f9c26d91f in / 
# Thu, 25 Mar 2021 23:22:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:22:59 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:23:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:23:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:43:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:44:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:44:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 14:44:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 14:44:21 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 14:44:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 14:44:24 GMT
ENV ROS_DISTRO=noetic
# Fri, 26 Mar 2021 14:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:46:46 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 26 Mar 2021 14:46:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 14:46:48 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 14:47:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:48:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 14:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:54:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c5b23ab54a1c0bb81bfc8f1ef83601638d672cc89e3bd3d49290ecfe0834ea2f`  
		Last Modified: Thu, 25 Mar 2021 23:28:04 GMT  
		Size: 27.2 MB (27176798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de628c73ef9a73e299e0e05bce39612341c12b0907fb5a1f8e9a569631ad20c`  
		Last Modified: Thu, 25 Mar 2021 23:27:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61ee5c846071ed2213196ef64402731d6ed75cca1bb954645d89b53db8d2266`  
		Last Modified: Thu, 25 Mar 2021 23:27:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da2f3772e7d14f6c8dd92787d62ebcc31d2930ead31dc0a5b82c4462c3444ae`  
		Last Modified: Fri, 26 Mar 2021 15:27:30 GMT  
		Size: 1.2 MB (1183079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3209da98cad32d45c3b49245366b4b28933f6fc899ead421d14c9c30784bc235`  
		Last Modified: Fri, 26 Mar 2021 15:27:28 GMT  
		Size: 5.5 MB (5513254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf7f90a086ceae99b2f71d9ecb6b27ca9bf4412f7198bce0252b1f2d1903ad0`  
		Last Modified: Fri, 26 Mar 2021 15:27:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b590c714cf121e43e675e096dda827c2e2c8c45c8b40f2e615f6dac621e4cee3`  
		Last Modified: Fri, 26 Mar 2021 15:27:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc938fe0edd9cc9bab39959d109f826be70eb3e77a8c5839be9d8141c4204887`  
		Last Modified: Fri, 26 Mar 2021 15:28:49 GMT  
		Size: 167.7 MB (167729430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd39cc8f82bd7c746fba7159b7986e9ff8d4b1bddfb1534380448ff7c41bdec3`  
		Last Modified: Fri, 26 Mar 2021 15:27:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4575e8c3b17f5c2700b2818e8852c2c26225a00392750b54fe2b9e6c56c393e5`  
		Last Modified: Fri, 26 Mar 2021 15:29:11 GMT  
		Size: 40.7 MB (40650814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6463a201455de19c40e4e409c8570168021e60b51ce967e1839e52872d6e7539`  
		Last Modified: Fri, 26 Mar 2021 15:28:59 GMT  
		Size: 279.5 KB (279534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ca3fe694746c0590d7b0c828ddb6f342c6c99eb7bda07b7af68a07d8ac1efd`  
		Last Modified: Fri, 26 Mar 2021 15:29:17 GMT  
		Size: 72.0 MB (71972731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022f7da8ab29022b9252d5550e80dcf59e5295ba9ba0cb6f45f40018e158a73`  
		Last Modified: Fri, 26 Mar 2021 15:31:43 GMT  
		Size: 468.4 MB (468373939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

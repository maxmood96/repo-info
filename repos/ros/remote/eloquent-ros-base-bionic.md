## `ros:eloquent-ros-base-bionic`

```console
$ docker pull ros@sha256:880957eb44e6a0f18d965203ab8f31109927877c4bf23791b20dcb46aa6ffd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:77eccd0b6ce36bd3018094f4e0c8b9418d35ac4ecfc55dc48d408278a3c3a0a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283520543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91508ca0535cfb7da1c0f88d1894c119cbef780e38d9bd94038c445b7fb0b406`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:33:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:45:21 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:45:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 22 Feb 2020 00:45:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 22 Feb 2020 00:45:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:45:57 GMT
ENV LANG=C.UTF-8
# Sat, 22 Feb 2020 00:45:57 GMT
ENV LC_ALL=C.UTF-8
# Sat, 22 Feb 2020 00:47:18 GMT
ENV ROS_DISTRO=eloquent
# Sat, 22 Feb 2020 00:47:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 22 Feb 2020 00:47:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 22 Feb 2020 00:47:33 GMT
RUN pip3 install -U     argcomplete
# Sat, 22 Feb 2020 00:48:11 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:48:11 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 22 Feb 2020 00:48:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 22 Feb 2020 00:48:12 GMT
CMD ["bash"]
# Sat, 22 Feb 2020 00:48:29 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fe4c16cf9b0d96d5ca63260c28e39ec2082af1f69bdc406d460e68fd3378f0`  
		Last Modified: Fri, 21 Feb 2020 23:47:45 GMT  
		Size: 838.2 KB (838151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da966be4a5099d61ead50dae69ffda05b90d272819d01c77cf0097c0e5606dd`  
		Last Modified: Sat, 22 Feb 2020 00:54:38 GMT  
		Size: 152.0 MB (152015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3928787e8e1be86d8fe671227cf4f3820d04eacaac3455ff12ba5e7a6cd0727`  
		Last Modified: Sat, 22 Feb 2020 00:54:11 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c2c32b925d8251fdfb81071414186ff0cfe58b7a7c4a40c6819887f73ea508`  
		Last Modified: Sat, 22 Feb 2020 00:54:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b70c1a6759a69c6bdacdc8d0e9e2adc2a19e3f1efe646b2c04a6d19a7679b31`  
		Last Modified: Sat, 22 Feb 2020 00:54:18 GMT  
		Size: 28.4 MB (28395722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239b83760638ae6f2143db8648a7c92a844b47bb873594399bc20b6375c44c7b`  
		Last Modified: Sat, 22 Feb 2020 00:54:51 GMT  
		Size: 431.2 KB (431210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d124f37844464555d0c94391dc7110178ab70200eb2f08ea894c050d8d1c0ae7`  
		Last Modified: Sat, 22 Feb 2020 00:54:51 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bfde953dd2e815d0a5cdf9b41354ee1d042aadf3ac078fb91114abea10e195`  
		Last Modified: Sat, 22 Feb 2020 00:54:51 GMT  
		Size: 207.9 KB (207880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b30ce52367ec58066394e8e27c0b9d7d7fd7e5fa5af56f2a592a257403aa34`  
		Last Modified: Sat, 22 Feb 2020 00:55:12 GMT  
		Size: 70.3 MB (70296629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897b94a85b2460065ed2dab8fb076195022dc065c492f07191d2335d5b8ed4c7`  
		Last Modified: Sat, 22 Feb 2020 00:54:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465a3f7006123954038fea264761122de129d9f97bcae6c9178059c77c1e6ea8`  
		Last Modified: Sat, 22 Feb 2020 00:55:18 GMT  
		Size: 4.6 MB (4603147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:3ffc1de27ce3aabc3819f37627275aa91f0ca7c7dda9639e9296f63c7667b22d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237272358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751c0875af9f0f4e4e87df70bb51225e562a5c16b868fec4d9872cdd44e65c7c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:04:48 GMT
ADD file:548fc3249b705bf3e94efcc50c1c9141e03d1ce51edfc194a84bd631d1a7b6d4 in / 
# Fri, 21 Feb 2020 22:04:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:04:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:05:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:05:02 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:34:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:47:57 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 21 Feb 2020 22:48:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 21 Feb 2020 22:49:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:49:08 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2020 22:49:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 21 Feb 2020 22:52:05 GMT
ENV ROS_DISTRO=eloquent
# Fri, 21 Feb 2020 22:52:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 21 Feb 2020 22:52:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 21 Feb 2020 22:52:30 GMT
RUN pip3 install -U     argcomplete
# Fri, 21 Feb 2020 22:53:51 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:53:53 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 21 Feb 2020 22:53:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 21 Feb 2020 22:53:55 GMT
CMD ["bash"]
# Fri, 21 Feb 2020 22:54:23 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9b5ae93466ea2cca8f47e7e02dc1907faaaae6ed617360e47259eb4cac4d0a7`  
		Last Modified: Fri, 21 Feb 2020 22:06:53 GMT  
		Size: 22.3 MB (22275658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8983199234a3f5beecbe2be6e21b4a49e67dd5726e7080e999c6f2cea91bc2`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 35.5 KB (35470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e76f87f706a4e3e6b5f3d9fabd021b46b875dc9058e26d31877057069115333`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b196ba84f492bbca6bb4979ae6e8d2d3a952559cdf3dfd11e99c3a4c11aa0891`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c94681626ece376a18f3e47c882222f1de6ea03203910197f3121573b1854cf`  
		Last Modified: Fri, 21 Feb 2020 22:58:20 GMT  
		Size: 838.0 KB (838036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5d8ad0470cc0da41ae5f0f48462ab292e750c6357adc668ac3e0b72e0b0e75`  
		Last Modified: Fri, 21 Feb 2020 23:03:30 GMT  
		Size: 133.6 MB (133567881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c51b40381f7c57eb48f4c7680ceed8fd1cb86e6e1c827ae7ee0cdd194362704`  
		Last Modified: Fri, 21 Feb 2020 23:02:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f2ef24fd75d1e785fc5b15916673b7f3bb246e8c910607bc1fb6671032f58d`  
		Last Modified: Fri, 21 Feb 2020 23:02:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6705414e608e99036e1a63bb9111cbf2a4fec5cdfd21141f9dd2726561c36802`  
		Last Modified: Fri, 21 Feb 2020 23:03:04 GMT  
		Size: 25.4 MB (25367051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345e62cdefc5bf78c9602a57479c10ce469d05b802e3025b71b4846bbcd62602`  
		Last Modified: Fri, 21 Feb 2020 23:03:48 GMT  
		Size: 429.8 KB (429803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c9450f3685b6f4031b6400ae4869abd268966d337b2ad7663773dc4615496a`  
		Last Modified: Fri, 21 Feb 2020 23:03:48 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880e07bedb17d9459542bbaa99de7fc9721b641813fee5932a174006e2f20b04`  
		Last Modified: Fri, 21 Feb 2020 23:03:49 GMT  
		Size: 208.1 KB (208111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1699fcfc035b984ac79831ab2a6d20ec7b0fa65564008b212e553a25bf115c0c`  
		Last Modified: Fri, 21 Feb 2020 23:04:09 GMT  
		Size: 51.0 MB (51028905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694db7cc23ff163fd039767ffe17aa114ab77d1149dd5e5ade9e33c841b37c87`  
		Last Modified: Fri, 21 Feb 2020 23:03:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23f38d15750f052846e0a60602265614caf188b56f1b97ab46bd907f5b5eb13`  
		Last Modified: Fri, 21 Feb 2020 23:04:19 GMT  
		Size: 3.5 MB (3516666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3e68d469ee2cac92b4f412c224de222bd05b2bf37fcf39c815cada016dfcb78b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257058861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055b56b794cd9fee6633759e311637e7cf52ed3d4fb4052a085a362294c01856`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:19:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:33:16 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:33:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 21 Feb 2020 23:33:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 21 Feb 2020 23:34:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:34:32 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2020 23:34:33 GMT
ENV LC_ALL=C.UTF-8
# Fri, 21 Feb 2020 23:37:39 GMT
ENV ROS_DISTRO=eloquent
# Fri, 21 Feb 2020 23:38:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 21 Feb 2020 23:38:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 21 Feb 2020 23:38:17 GMT
RUN pip3 install -U     argcomplete
# Fri, 21 Feb 2020 23:39:50 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:39:53 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 21 Feb 2020 23:39:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 21 Feb 2020 23:39:56 GMT
CMD ["bash"]
# Fri, 21 Feb 2020 23:40:28 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9245e73b2caf8b938074b23c3c20fbcce64fd1928003222258b8814ca4d7659`  
		Last Modified: Fri, 21 Feb 2020 23:44:29 GMT  
		Size: 838.1 KB (838054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d73493808ce6f6f7d45ca5fb1333b3ce950d0cdc1640ccca46fc16f60570abd`  
		Last Modified: Fri, 21 Feb 2020 23:48:48 GMT  
		Size: 143.2 MB (143187904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282fd2aa8436bc43624281f20dcf830dccd5351b5be9efd46c8159cbf8ae0bef`  
		Last Modified: Fri, 21 Feb 2020 23:48:11 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f7023ae98237ea9145a2625fa0cf720c553c89bdcd208a4646a65c5ca8efd`  
		Last Modified: Fri, 21 Feb 2020 23:48:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966bff3fa4bbcab602445ad3a933a89124fd887b628dfab15441b44295988c55`  
		Last Modified: Fri, 21 Feb 2020 23:48:19 GMT  
		Size: 27.1 MB (27080861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145391f2f629875b1fca7741ec8701d86f9caab78614468dec6ad11bb27a192a`  
		Last Modified: Fri, 21 Feb 2020 23:49:06 GMT  
		Size: 429.8 KB (429807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34744fe6cdefc249c10c14b6f56762b4f4ed35010c992270823fcdc6d2f1e179`  
		Last Modified: Fri, 21 Feb 2020 23:49:06 GMT  
		Size: 1.9 KB (1916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a0203544be95dcd8bfee7c584c574e44556aeb6f9a8a42851ff810a552d32c`  
		Last Modified: Fri, 21 Feb 2020 23:49:06 GMT  
		Size: 208.2 KB (208162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656760554510f95cce9b5260e2787d84fe4a4f80758214822bc76a564c893f73`  
		Last Modified: Fri, 21 Feb 2020 23:49:30 GMT  
		Size: 57.6 MB (57597501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ac7e83b90fd3748ccfd7072c4be8743c764ef914c3be98075659ad673075eb`  
		Last Modified: Fri, 21 Feb 2020 23:49:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc5a6b81bb1b6013a11049ee388e06f80f98fee37e9b14fa3806960437e4436`  
		Last Modified: Fri, 21 Feb 2020 23:49:39 GMT  
		Size: 4.0 MB (3955436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

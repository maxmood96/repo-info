## `ros:dashing-ros-core`

```console
$ docker pull ros@sha256:281973e5f260e460aa7d70220d178a2ef7ce109c193f93bd7d67f4d2564c1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:5cb1a827dadeb3680689ad012c85b7dfd30c3bcb90783072ae0bf04056013abf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276709219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5bf8f53d79642893a8d4bc21d0e94515279baf28111fdbd67ee77525dacfb6`
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
# Sat, 22 Feb 2020 00:45:57 GMT
ENV ROS_DISTRO=dashing
# Sat, 22 Feb 2020 00:46:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 22 Feb 2020 00:46:08 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 22 Feb 2020 00:46:11 GMT
RUN pip3 install -U     argcomplete
# Sat, 22 Feb 2020 00:46:53 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:46:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 22 Feb 2020 00:46:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 22 Feb 2020 00:46:54 GMT
CMD ["bash"]
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
	-	`sha256:2a948b279d83acfa13fc8ba206da3da7e40ed19b8915f1aaaba599979d17519f`  
		Last Modified: Sat, 22 Feb 2020 00:54:09 GMT  
		Size: 431.2 KB (431215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a68418cfe6a1da2b80130ce9f6eba94beac90ecd22c560138b35fcf1a0d5a90`  
		Last Modified: Sat, 22 Feb 2020 00:54:09 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9448a84bb86ed570f856fc1cef1c23716fc8b0ba031aa63710f06e8aff498b10`  
		Last Modified: Sat, 22 Feb 2020 00:54:09 GMT  
		Size: 207.9 KB (207889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1049f6fef203479acfba1c05e8b6190faa348b5eb82de5e124372d8fabc1cc57`  
		Last Modified: Sat, 22 Feb 2020 00:54:32 GMT  
		Size: 68.1 MB (68088474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da4046905a2b449e59ee9d90a7eb8b9d0005b3de43ec964b3ae05fc2308434`  
		Last Modified: Sat, 22 Feb 2020 00:54:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:57026a7940bab8c308cd137364cd064c63065cb18ae4f3f335e82481fa2684e5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231988307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abed97c2198a8c9467b62fc53fb5d8c86ffffac3729867f4e6683ae27ef89bd1`
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
# Fri, 21 Feb 2020 22:49:09 GMT
ENV ROS_DISTRO=dashing
# Fri, 21 Feb 2020 22:49:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 21 Feb 2020 22:49:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 21 Feb 2020 22:49:35 GMT
RUN pip3 install -U     argcomplete
# Fri, 21 Feb 2020 22:51:15 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:51:18 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 21 Feb 2020 22:51:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 21 Feb 2020 22:51:21 GMT
CMD ["bash"]
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
	-	`sha256:dc228f61b9a73e78088e575985fad147d213afa62e6cfad76a07e579ea0eb13b`  
		Last Modified: Fri, 21 Feb 2020 23:02:53 GMT  
		Size: 429.8 KB (429808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e586f5d1e985eb5e07d390e9b213e277ca150f22222e32c3c357f4a7f42fe22`  
		Last Modified: Fri, 21 Feb 2020 23:02:53 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13523ecae6c9b3ce4e218c043da5defad9be19749cdc06cffdd6ba23f66ff5c7`  
		Last Modified: Fri, 21 Feb 2020 23:02:53 GMT  
		Size: 208.1 KB (208089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213c19412f11f19cfd43d01ac4999ddecdae0e426d864db542aaf7f66a356b2f`  
		Last Modified: Fri, 21 Feb 2020 23:03:13 GMT  
		Size: 49.3 MB (49261529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf8db0ea13d86e0242057ab143cf0b39443c852ba671f6f2f6f354ab7899a96`  
		Last Modified: Fri, 21 Feb 2020 23:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:10f15e1da6a1bd7ea0bad5777e80e8a7aa87f1a434b4529bb1a939c12fde3d26
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251066413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e731a59bd276dbd127ade924ebc42ced600927ccd0c9280a37e8c3aad2bc8416`
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
# Fri, 21 Feb 2020 23:34:34 GMT
ENV ROS_DISTRO=dashing
# Fri, 21 Feb 2020 23:34:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 21 Feb 2020 23:35:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 21 Feb 2020 23:35:06 GMT
RUN pip3 install -U     argcomplete
# Fri, 21 Feb 2020 23:36:32 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:36:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 21 Feb 2020 23:36:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 21 Feb 2020 23:36:47 GMT
CMD ["bash"]
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
	-	`sha256:a82df4c5f22c0fb4a2d7f6a4051dad1f9be0815a9b485614eaab5f64e367c425`  
		Last Modified: Fri, 21 Feb 2020 23:48:08 GMT  
		Size: 429.8 KB (429799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759c7996a80ba90618164151c7207be827adfb9555b606c66347222004bbf9a7`  
		Last Modified: Fri, 21 Feb 2020 23:48:09 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738fdfb2846bf2beee368b2c4596dfc6a2f7e49aedfb76d763a7a0f60ff6a54b`  
		Last Modified: Fri, 21 Feb 2020 23:48:08 GMT  
		Size: 208.2 KB (208172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005e20c3397ce01be2c8ebc3d8b9ec521a8060dc633960093fd618208980f757`  
		Last Modified: Fri, 21 Feb 2020 23:48:30 GMT  
		Size: 55.6 MB (55560485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf2d06299030ad963e8cc03908a1728af04232b1574617be5a1c205662ce28f`  
		Last Modified: Fri, 21 Feb 2020 23:48:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

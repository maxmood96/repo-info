## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:020b6bdccc72aeb5d70d6f57a88edce520b7c5e5acb115992f17ed824e0940a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:bf7dfead3ee05d0b41886d27fe0c6a4673699d2fce0f22d0b50d85e2965940b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350422337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b7ab770c1ac126818025745658f563e6d5bb9caf90fe5c5cc5d08d893e56a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:23 GMT
ADD file:1b4ec50586b9f0621095f51ee6baecc00a7f6d95b4a04e3bedc5393b28bc8a54 in / 
# Wed, 16 Sep 2020 22:20:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:25 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:37:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:34:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:34:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 01:34:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Sep 2020 01:34:54 GMT
ENV LANG=C.UTF-8
# Thu, 17 Sep 2020 01:34:55 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Sep 2020 01:34:55 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Sep 2020 01:36:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:37:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 17 Sep 2020 01:37:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Sep 2020 01:37:01 GMT
CMD ["bash"]
# Thu, 17 Sep 2020 01:37:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:37:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Sep 2020 01:38:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6ca3592b14484be6a9719617680e0c810e0107d89c437162c75d2401637c72c`  
		Last Modified: Wed, 16 Sep 2020 15:19:59 GMT  
		Size: 28.6 MB (28557166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a5505201da9ddb334b5b2fcb3cec45fcafccd8e91b93ad4852e1a1bb318c1`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990916bd23bbbf9c30d202dad557e813562d028f3076bf57904830c69d4cde83`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43f844b454143fefb276b0d47a08c31858e330ffeceef21130f4f907c2691e`  
		Last Modified: Thu, 17 Sep 2020 00:52:12 GMT  
		Size: 1.2 MB (1176444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25929632fd5b65202802f96157aaae95b55bcb587a77c708a4d63e5d2100db09`  
		Last Modified: Thu, 17 Sep 2020 02:08:15 GMT  
		Size: 5.5 MB (5547001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa5e6421658a99911cb295c7f31b4f12e6a3f61860c7814b87cddc1a985e215`  
		Last Modified: Thu, 17 Sep 2020 02:08:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a08b3a0fa22f573c1974b55b35f35bee430803f9352893dda6c90b5051ff7ce`  
		Last Modified: Thu, 17 Sep 2020 02:08:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a3150b7ebf5f39ac69437ee618ef8d8735baa61c28519cbb838b489d558de1`  
		Last Modified: Thu, 17 Sep 2020 02:09:00 GMT  
		Size: 173.1 MB (173092194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6818a58433a4e5bd8791193ade13c8e960d66bc46c614f7a8c254d0410d544d`  
		Last Modified: Thu, 17 Sep 2020 02:08:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3982fde693cee7629d5550179ee449f5fef5aec52c4cae7dede5c7398fe2bd77`  
		Last Modified: Thu, 17 Sep 2020 02:09:16 GMT  
		Size: 46.4 MB (46377174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800d48bd2bc741156f49ce8da99aef91ff96e9bbf13e7609cd1ccf9e382e93b8`  
		Last Modified: Thu, 17 Sep 2020 02:09:06 GMT  
		Size: 230.3 KB (230335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f447b188084466193deeee8a915e99196a4d9c8bb961bff5244262abd70da392`  
		Last Modified: Thu, 17 Sep 2020 02:09:23 GMT  
		Size: 79.6 MB (79589374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad23caeb4b07476fce5a0f38598ad8cf4e7d3963a885938680580e4b4fd343`  
		Last Modified: Thu, 17 Sep 2020 02:09:31 GMT  
		Size: 15.8 MB (15849812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:68c6fab1c5f6959f97e807a5249b8a85012d2bb4126d5f641da8dcba197ed801
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297502100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e67a6625af6dae3f90d0a65bf767d8efd1428509c5845d88d3b07bd6e08602`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 25 Sep 2020 23:05:07 GMT
ADD file:545bf1be9048265e6c534b9b28f9f47c4a67fe2fe7331c7652187f3b43999005 in / 
# Fri, 25 Sep 2020 23:05:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:05:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:05:13 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:05:14 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:03:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:03:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:04:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Sep 2020 00:04:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 26 Sep 2020 00:04:15 GMT
ENV LANG=C.UTF-8
# Sat, 26 Sep 2020 00:04:16 GMT
ENV LC_ALL=C.UTF-8
# Sat, 26 Sep 2020 00:04:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 26 Sep 2020 00:06:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:06:52 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 26 Sep 2020 00:06:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 26 Sep 2020 00:06:55 GMT
CMD ["bash"]
# Sat, 26 Sep 2020 00:07:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:07:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 26 Sep 2020 00:08:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:09:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:39f6a73f1e6a145d93dd5878cc833f3930759e9c59f35905b5ebbcfba8669f0d`  
		Last Modified: Fri, 25 Sep 2020 23:06:54 GMT  
		Size: 24.0 MB (24038486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde417f16107c5260abc78817e22ed7d1fa0eab20e58929e4265b9b782fbc020`  
		Last Modified: Fri, 25 Sep 2020 23:06:47 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b336701abcacc2258baaa4f6e1714b011d5ca0ddbc5231e18f2b7b050b9bfb3`  
		Last Modified: Fri, 25 Sep 2020 23:06:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1365c477ebb042985a05bdae57de2b67b864fe7131f13f5318d0c57cb19327`  
		Last Modified: Sat, 26 Sep 2020 00:47:24 GMT  
		Size: 1.2 MB (1177969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc4d3c40b4137bf9ba4ddae9ace53bac9f385ca5df38b8d5f9d82ae11403a05`  
		Last Modified: Sat, 26 Sep 2020 00:47:22 GMT  
		Size: 4.7 MB (4676373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e225de48c4fdf5e54861f963be8a02ef0268b5a129c77554a6db6c17a6ae9735`  
		Last Modified: Sat, 26 Sep 2020 00:47:21 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cad782b0d7b1df7e6473d2bdb593c99de90dffcb1100a59b55d2e36bd0ff2c`  
		Last Modified: Sat, 26 Sep 2020 00:47:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2347f7891e6e7300eb8f46b9c8343cb6249b75b27afa77f71bea88c2c6cb1f2`  
		Last Modified: Sat, 26 Sep 2020 00:49:16 GMT  
		Size: 157.0 MB (156979809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28701a4beb918795eba0f50ecea8573aa7b7ca59120e2e84f6f1d84a58bab8d`  
		Last Modified: Sat, 26 Sep 2020 00:47:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241300aa269922053e62935f01f2786cb91b09628e898ace847fa35cfc477acf`  
		Last Modified: Sat, 26 Sep 2020 00:49:36 GMT  
		Size: 35.8 MB (35827377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7fe0ebc3c16b6d3be0872e2d096c4ef400e528beffc9589d7197cec7cb37e`  
		Last Modified: Sat, 26 Sep 2020 00:49:26 GMT  
		Size: 232.8 KB (232807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad39776f83d9b04f408774314a8192f809f79d9c07efabe82b7d736e4d36c180`  
		Last Modified: Sat, 26 Sep 2020 00:49:46 GMT  
		Size: 60.5 MB (60480670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340c328b958a950897fe1d642c2ce4a577b60347161a5648c78a3fe1bdbc5e9`  
		Last Modified: Sat, 26 Sep 2020 00:50:00 GMT  
		Size: 14.1 MB (14085729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d7aa9c5988612e743214c513f37c9c633f74fa0dd9346321145ba67ae80963fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329681179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddf077469d3b9a82a2f6f9cfce382386aeef383940710805d9ef56bf8d29bf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Sep 2020 23:16:56 GMT
ADD file:063d9d9577619d2eeb19bbc784fecf567039a314d8f741500841f6b4f3c847b3 in / 
# Wed, 16 Sep 2020 23:17:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:17:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:17:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:17:04 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 01:44:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:44:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:45:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 01:46:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Sep 2020 01:46:16 GMT
ENV LANG=C.UTF-8
# Thu, 17 Sep 2020 01:46:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Sep 2020 01:46:30 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Sep 2020 01:48:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:48:47 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 17 Sep 2020 01:48:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Sep 2020 01:48:50 GMT
CMD ["bash"]
# Thu, 17 Sep 2020 01:49:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:49:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Sep 2020 01:50:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:52:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33c9bf8777b52e6bc989f3a77a8a680861b9a7f7385e2d5ee02fdede89acf606`  
		Last Modified: Wed, 16 Sep 2020 08:25:33 GMT  
		Size: 27.2 MB (27158462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1900e162114f589f3e78ba5b26957f2b6ec38c8aaa6efdd8afbfaf5d9e8841`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53c8a81c25472b52dd428e136c84a1f407ce933911cab5910676d1a7b7a4df3`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ddde6856911f795c55f1e3e7d0658aa1d457594dbf63fd18f6cbc10fd0658`  
		Last Modified: Thu, 17 Sep 2020 02:36:11 GMT  
		Size: 1.2 MB (1177642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3c413801c3e32051187650ead158523b1424776c96e4f3d3410b393309dc4`  
		Last Modified: Thu, 17 Sep 2020 02:36:03 GMT  
		Size: 5.5 MB (5513389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe76cc3db355f14c9557f875c35c68fbbd7d00a458bbc2ab91a3dd10ae61464b`  
		Last Modified: Thu, 17 Sep 2020 02:36:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372076c09ee9fa7ab9680d608066a4328b581d4d6a0cdd0e563635e37d01f022`  
		Last Modified: Thu, 17 Sep 2020 02:36:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abe5c95f9b521fb933eb6c0a56f039b74cdff1cf43524a636cf01c29783632d`  
		Last Modified: Thu, 17 Sep 2020 02:38:05 GMT  
		Size: 167.6 MB (167564640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9377c2f6201eb2f92c12ebc3b10de7df54fb37ec390e847d1036e4646aaa4455`  
		Last Modified: Thu, 17 Sep 2020 02:36:03 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867590d4acfe4c8222b83e3768213effff85c78a6b5d62838f16730b8320fb67`  
		Last Modified: Thu, 17 Sep 2020 02:38:29 GMT  
		Size: 40.6 MB (40629278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d9fd2672deecea8ea0324945e5bc52a9b65a5b715af8277a7ecc58b19c93a`  
		Last Modified: Thu, 17 Sep 2020 02:38:14 GMT  
		Size: 230.4 KB (230390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d763062de7864be519c4e3dd0ee57def442546edeea53dfd0ee4a390081fac4f`  
		Last Modified: Thu, 17 Sep 2020 02:38:59 GMT  
		Size: 72.0 MB (71972483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb54bb904e763c6e4b767a675595fce2902e38b8d1a358b39a2465df5d261ab`  
		Last Modified: Thu, 17 Sep 2020 02:39:18 GMT  
		Size: 15.4 MB (15432020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:3412d3a53b0bf970e98ab5854523966e34bab68770d17c3b40369a6cd4166929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:1cedb90bab3c2a76ba924d7e2f1a9744c3be7318739aff4b71a6811199acf1c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208571547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcf4d1faa999fb21f739d9cd15f94a02285fb020c018abdefb21b5c6dd05c26`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:38:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:13:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:13:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 11:13:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 11:13:13 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 11:13:13 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 11:13:14 GMT
ENV ROS_DISTRO=noetic
# Thu, 21 Jan 2021 11:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:15:21 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 11:15:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 11:15:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b329de66e00a76df07e660eb83a5097f2bbaca25d0f8030ae04b2a9045d726e`  
		Last Modified: Thu, 21 Jan 2021 08:55:02 GMT  
		Size: 1.2 MB (1181953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ca6f3074dc19264c495086cc66977079fd2553a4803bff7061524587caeff8`  
		Last Modified: Thu, 21 Jan 2021 11:47:40 GMT  
		Size: 5.5 MB (5547368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b12fc1d4ab992cb14f16c7af9bd19f75b5fd82db79e4e925e38bcb4969667`  
		Last Modified: Thu, 21 Jan 2021 11:47:39 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c0fd3ff8f479851264ac4d439ba4d741f90088138ded2ab31716869cbdf028`  
		Last Modified: Thu, 21 Jan 2021 11:47:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36414a1a90ea19a1a3f07f601ab8faf8bfa85011ec60d72d903bc064931a45e7`  
		Last Modified: Thu, 21 Jan 2021 11:48:25 GMT  
		Size: 173.3 MB (173273493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7cb5f97c49b2c57dc87e98cc8143f8843d498772ccb3754962ed722193af24`  
		Last Modified: Thu, 21 Jan 2021 11:47:40 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:8403a1281da214298c5375fb6298ac0a5a8fad80fccd85ae7546542327200634
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187079865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781f07d452232928d912a8f09faed7e2d4fda4c55214a0a223807bc3c0633a3e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:15:51 GMT
ADD file:874b5c952a766aaeff6c0d01f72a2644501ac0c8ab3ea3eef70339f045f09897 in / 
# Thu, 21 Jan 2021 03:15:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:15:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:15:57 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:15:59 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:41:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:42:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 04:42:21 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 04:42:22 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 04:42:25 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 04:42:27 GMT
ENV ROS_DISTRO=noetic
# Thu, 21 Jan 2021 04:44:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:44:58 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 04:44:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 04:45:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f5b689817f397e49f6802d29f6e262a92b16ef6fd29e0dbe7c957ecf60421c1f`  
		Last Modified: Thu, 21 Jan 2021 03:18:26 GMT  
		Size: 24.0 MB (24043427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b105a146cef196c701ff39cc8b99248972b0b02b544bb5fc1346bf37b870383`  
		Last Modified: Thu, 21 Jan 2021 03:18:19 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22943c6e232d1034beb778a2094ae7d8bb94122e5e562c65769abc93a3ab1731`  
		Last Modified: Thu, 21 Jan 2021 03:18:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da94c2e1ffe7a207cb16387dad3b7bdb14e1ae74ff5ebabe6670f20a2590bbd3`  
		Last Modified: Thu, 21 Jan 2021 05:16:04 GMT  
		Size: 1.2 MB (1183165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc0bd3c7c8507acfba5a1709d766b0fb7073f21a2abdc0fb08dc3513be90682`  
		Last Modified: Thu, 21 Jan 2021 05:16:03 GMT  
		Size: 4.7 MB (4676841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b65d68849907d97ed8c56594ed5c564b5b697d5c30b1d279fa96d856d8caaa`  
		Last Modified: Thu, 21 Jan 2021 05:16:00 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a72237a1f08d55965016589ac175e3d7390c84c942f8c1c65f1dafb899370c`  
		Last Modified: Thu, 21 Jan 2021 05:16:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec039649d5d1f6a5f97883f049f2cc038bebe026fbc0b5f5af534d4287d69eef`  
		Last Modified: Thu, 21 Jan 2021 05:16:59 GMT  
		Size: 157.2 MB (157173558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424cf09681c7cbde74a8bf71b7b5a7d6e0ed90babb5c8d1fb3637e66f75c4b97`  
		Last Modified: Thu, 21 Jan 2021 05:16:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5e2a44883f3fc8e03d9c5df0d90fdac182b9146e917960bfb9b41bdceab95641
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201620636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307adab9e47ce7a3af5e2a61d3530fe0b3b707d3786b593299ff8b333270ee72`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 03:22:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:22:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:22:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 03:22:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 04 Mar 2021 03:22:39 GMT
ENV LANG=C.UTF-8
# Thu, 04 Mar 2021 03:22:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 04 Mar 2021 03:22:41 GMT
ENV ROS_DISTRO=noetic
# Thu, 04 Mar 2021 03:25:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:25:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 04 Mar 2021 03:25:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 04 Mar 2021 03:25:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1317e878738b2e361ab2bc6c5e9dad3effcdd7f83f6a2e3687fc82bc9c1ada3`  
		Last Modified: Thu, 04 Mar 2021 04:04:00 GMT  
		Size: 1.2 MB (1182875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba5f746c529c10d1d08e23f12a45a07e2921c194edd5618c4b72f862233e909`  
		Last Modified: Thu, 04 Mar 2021 04:03:59 GMT  
		Size: 5.5 MB (5512834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea8b4c459768d7eb6fc2a16d12531aface693a3d22b366e35336593ee89d6ad`  
		Last Modified: Thu, 04 Mar 2021 04:03:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eecb3e613c32cdcaf95e9ff1c2bca8076ca8109c82abc46aaac30fdda393f88`  
		Last Modified: Thu, 04 Mar 2021 04:03:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2abe5add42bec709ddb08a5174fb61aa16a17e0172cd3cb8efb6e1f0542d55a`  
		Last Modified: Thu, 04 Mar 2021 04:04:49 GMT  
		Size: 167.7 MB (167746250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aec9fcc6dbe4e86533f2c0fec339f14a7acaf1dff8dd8b877e0b5f9edb2d6ba`  
		Last Modified: Thu, 04 Mar 2021 04:03:58 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

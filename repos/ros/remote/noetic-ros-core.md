## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:a22c0b4fcdb3c6e124339d9c9d46ff3b1236bc97591d292eede2624ea75f872e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

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

### `ros:noetic-ros-core` - linux; arm variant v7

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

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f51aaf574cd43dac71beaf1b1d20c6b7f2e51d3ef56d5d906eb5e2c7a1364a08
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201603786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5741cd34fbe806ad47863a35d9c245e76dc9469581df4c825b288134dbc0ba0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 06:45:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:45:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:45:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 06:45:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 06:45:41 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 06:45:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 06:45:42 GMT
ENV ROS_DISTRO=noetic
# Thu, 21 Jan 2021 06:47:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:47:32 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 06:47:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 06:47:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf194558d7d697893645e2928d8c12f602b77dd0aaf2f5344233277d7b160d1`  
		Last Modified: Thu, 21 Jan 2021 07:29:34 GMT  
		Size: 1.2 MB (1183038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f15cd3db3fa7d5351aa9b332d57ca02a4276fef9f7b3363ef98b2c4f9611d8`  
		Last Modified: Thu, 21 Jan 2021 07:29:31 GMT  
		Size: 5.5 MB (5514280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de67e6495e9d3639f76b9c4f19a8a602bcf7fe068fb7b7f08ee8cba855c1f301`  
		Last Modified: Thu, 21 Jan 2021 07:29:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5636e62e6134016f8370d4853fea403034c3fcd18c3651677cecfb47de873`  
		Last Modified: Thu, 21 Jan 2021 07:29:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ca3e0796ba1efb532cbfa066cbeccfb034b32b48c7cb654d151e2a65870aa2`  
		Last Modified: Thu, 21 Jan 2021 07:30:19 GMT  
		Size: 167.7 MB (167730659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2f02cabedc2ba334cde9f352b285fd92fddfac028ed13666ac864d1187a7b9`  
		Last Modified: Thu, 21 Jan 2021 07:29:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

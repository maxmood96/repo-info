## `ros:rolling-ros-core-focal`

```console
$ docker pull ros@sha256:c1c6b01ba4b56774b0f18ef7c855402d1889a50da87367966bd09faf11bf9291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:1aa8737f77e103778d209c71767869b139ec485f6cbb396e944984ccc18caae7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155192779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff97b8ffc5a83d77bcf7d4d42978861725786b228afc1672bff42257b387d09`
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
# Thu, 21 Jan 2021 11:34:22 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 11:34:23 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 11:34:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 11:38:04 GMT
ENV ROS_DISTRO=rolling
# Thu, 21 Jan 2021 11:38:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:38:59 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 11:38:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 11:39:00 GMT
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
	-	`sha256:d7b4b846f1510e05ec2e9f03bfbb1e0865f69dcb23742f4f04590bed5d988feb`  
		Last Modified: Thu, 21 Jan 2021 11:54:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473d7c7711794b1c585dd584be338c44f3b523d8987710c5cb9e6a9cedf08494`  
		Last Modified: Thu, 21 Jan 2021 11:56:17 GMT  
		Size: 119.9 MB (119894720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adf58a25a3026bb6417f5d53984a109397e3d1a3db800b7fc7060be3bcef9af`  
		Last Modified: Thu, 21 Jan 2021 11:55:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:333ead5745ce662ee11f100d1524e27daa71f131827630dfcbd5bf2f64abbe0f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137832682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae0987f19fa13c26f935436e87ee5e3294aad966bf52ef367cc3782bd826ef7`
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
# Thu, 21 Jan 2021 07:09:09 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 07:09:09 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 07:09:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 07:14:48 GMT
ENV ROS_DISTRO=rolling
# Thu, 21 Jan 2021 07:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:16:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 07:16:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 07:16:42 GMT
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
	-	`sha256:0dba3fea46fa21f2e435af76ebf72934a3b25fc18e9d03b07f583304b0335d7e`  
		Last Modified: Thu, 21 Jan 2021 07:36:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fe15401fa20919feee7ef656cc89d14e3fd4588d3acf9afa81ba5d694e418`  
		Last Modified: Thu, 21 Jan 2021 07:38:55 GMT  
		Size: 104.0 MB (103959553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65506f9e42a413dd004c5ca05f35b5c93d44d17eaaaed4ecb4a0ba086f6d5788`  
		Last Modified: Thu, 21 Jan 2021 07:38:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

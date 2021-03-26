## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:67cee0a6fe5413f3229488966ea9d582a7d89c3799e5dd53c8c88855dfbc228d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f49a2182fae227c1e6c8d1ba9ddd7670968666b83b8f2d542bb47f2925c3e045
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155206852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e53d764322957ce1569582ade34a13496a7273f4cf6d0fe82aa58dd06b5a31`
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
# Fri, 26 Mar 2021 13:20:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Mar 2021 13:20:17 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 13:20:18 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 13:20:18 GMT
ENV ROS_DISTRO=foxy
# Fri, 26 Mar 2021 13:22:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:22:28 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 13:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 13:22:29 GMT
CMD ["bash"]
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
	-	`sha256:60bdc4b51bc40412fcaa260772905420e5f00507790e2e926d26be5e759fa190`  
		Last Modified: Fri, 26 Mar 2021 13:44:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f7f266847e24ead25f7ca2d87c21dd29a8f6143e5d9dfe25ea0b3388460aed`  
		Last Modified: Fri, 26 Mar 2021 13:45:13 GMT  
		Size: 119.9 MB (119904410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77037c0775c3d5d1819042c8624f8501491576b92d21d53fc5f1c883c63ac6c`  
		Last Modified: Fri, 26 Mar 2021 13:44:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9d9fe43849b753606354cb1abae203e91d02a90cec86e5426bc07739ea3837d9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137964984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d29a2804c73352acbf2e8ccb2944dc16e8e1fb0f7e9768fad8b90f340cf7a1`
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
# Fri, 26 Mar 2021 15:09:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Mar 2021 15:09:57 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 15:09:58 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 15:09:59 GMT
ENV ROS_DISTRO=foxy
# Fri, 26 Mar 2021 15:12:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:12:10 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 15:12:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 15:12:13 GMT
CMD ["bash"]
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
	-	`sha256:8238ce340fac0e12b439ee9e06f2f3dd9943e7b2eed79c2b74f442b23842c8d9`  
		Last Modified: Fri, 26 Mar 2021 15:36:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78a426e426e221718cc3228b118b077a444dc32e6ed643405b2ccf34f3d306a`  
		Last Modified: Fri, 26 Mar 2021 15:36:34 GMT  
		Size: 104.1 MB (104088975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dd9262c9ff647c08e920ac6102bb6e26339d60272dc99748e82a685003d4db`  
		Last Modified: Fri, 26 Mar 2021 15:36:05 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:92e3ab2a73d3cde89d8fe2f61ea12ff41a25f3417ab94822dd08e5ef8bda6ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:d6b2ca95d059529d60848175a39e0d98c8a664203b15a176931459c4b0ee2551
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208567404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69764c468949d70e11b4c16bcfb56455a01934d695d57e34f7a5b405d91fae85`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:05:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 24 Apr 2021 01:28:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 24 Apr 2021 01:28:08 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 01:28:08 GMT
ENV LC_ALL=C.UTF-8
# Sat, 24 Apr 2021 01:28:08 GMT
ENV ROS_DISTRO=noetic
# Sat, 24 Apr 2021 01:31:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:31:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 24 Apr 2021 01:31:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 24 Apr 2021 01:31:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f60c1e15de5890db12b66dcdc9fead43b285bea7d10d147a7baddfe0093488`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 1.2 MB (1183512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fbc9697fb73e1f55467886a56de4ed73ea1fa95a907d4eaa7cc7795c3f4438`  
		Last Modified: Sat, 24 Apr 2021 02:08:15 GMT  
		Size: 5.5 MB (5548747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a95aef5c90fc3ad3fbdf62df2fe49070101223c648c5648548adffb4b1602`  
		Last Modified: Sat, 24 Apr 2021 02:08:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8139f2b8ee0684f5ad51361558e831b44fd2d1d504f8f63fefe426b8e4bf8c26`  
		Last Modified: Sat, 24 Apr 2021 02:08:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44bd776b6ad6f36d9902027f0f225b6df006bf2222485b077d9a41e2f36eb61`  
		Last Modified: Sat, 24 Apr 2021 02:08:52 GMT  
		Size: 173.3 MB (173292647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec14a11c7657829be226e65a17b7772f4120244b3c9e6a75cee45a96ed20ece`  
		Last Modified: Sat, 24 Apr 2021 02:08:14 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:3b66849ddd8284b1e6cde1e7495709b005a8ff86f70e318504015a9e3ea4d04c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187121488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cba911256c4260a361e77d2d3b5c30fcd40a50cc0e91e817be0af730faa470`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 May 2021 17:00:36 GMT
ADD file:928fc93f670d53bf065ee8446f4af7f103050e96939dfae34f986b5332254115 in / 
# Wed, 26 May 2021 17:00:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 17:00:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 17:00:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 17:00:38 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 00:05:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:05:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:05:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 27 May 2021 00:05:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 27 May 2021 00:05:59 GMT
ENV LANG=C.UTF-8
# Thu, 27 May 2021 00:05:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 27 May 2021 00:06:00 GMT
ENV ROS_DISTRO=noetic
# Thu, 27 May 2021 00:07:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:07:29 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 27 May 2021 00:07:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 27 May 2021 00:07:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cd0d4853c44dd92753bc49779ae8c6f5bd76ba358989832b5afa42e3a341b4eb`  
		Last Modified: Fri, 23 Apr 2021 22:40:15 GMT  
		Size: 24.0 MB (24038553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d9a278ae85c6e20b2a660aec6ce81a669bf95f4bcc1f342352c4bcd340f086`  
		Last Modified: Wed, 26 May 2021 17:03:21 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5bd319502444cd19bef903c9880fd79e6a3e4992ce96feea91b56600320b0a`  
		Last Modified: Wed, 26 May 2021 17:03:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944fd4ab8f3cfc07b27885e5b3c0da643c62e1a8b62f017ac6866dfce12d87d6`  
		Last Modified: Thu, 27 May 2021 00:28:53 GMT  
		Size: 1.2 MB (1183201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00163d0e6cbc90b94fbbc0f937861d21102d23e965135395e7f3a45e8e65eed`  
		Last Modified: Thu, 27 May 2021 00:28:51 GMT  
		Size: 4.7 MB (4676239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f23a2228891d41ee4ca6256dcabc9884d32b1b536889e7e1e4d4639d892805`  
		Last Modified: Thu, 27 May 2021 00:28:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d76e341ced70af7837ecaf03f3f98d78ef34f0e929acee3f3ef4c7438ce06a`  
		Last Modified: Thu, 27 May 2021 00:28:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e040db962e033be72684ea0701c524665ce3dc13b2c1816ef3ed3f623ad11d7`  
		Last Modified: Thu, 27 May 2021 00:29:39 GMT  
		Size: 157.2 MB (157220628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f544ac35e7ee80b00ab7e43990ab7076e553096443791872e02d0dca221877b7`  
		Last Modified: Thu, 27 May 2021 00:28:49 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1965c94669af70a2635bad6bf306b2fc1e9d3cac513bc45d29cbedd9bdd3cfdb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201567718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450d56a12be71fc90fd57e879b1d466c25d25705f4dedac3050ba42be271d4d3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:47:51 GMT
ADD file:57e6f432b1329c286e596ded8065bebdfc70a87fae91dd79bd805363ef008e5d in / 
# Fri, 23 Apr 2021 22:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:47:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:47:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:47:59 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:35:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:35:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:35:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 24 Apr 2021 00:35:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 24 Apr 2021 00:35:58 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 00:35:59 GMT
ENV LC_ALL=C.UTF-8
# Sat, 24 Apr 2021 00:36:00 GMT
ENV ROS_DISTRO=noetic
# Sat, 24 Apr 2021 00:38:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:38:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 24 Apr 2021 00:38:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 24 Apr 2021 00:38:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:80bc30679ac1fd798f3241208c14accd6a364cb8a6224d1127dfb1577d10554f`  
		Last Modified: Fri, 16 Apr 2021 08:25:26 GMT  
		Size: 27.1 MB (27144417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf18fab4cfbf479fa9f8409ad47e2702c63241304c2cdd4c33f2a1633c5f85e`  
		Last Modified: Fri, 23 Apr 2021 22:50:04 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5979309c983a2adeff352538937475cf961d49c34194fa2aab142effe19ed9c1`  
		Last Modified: Fri, 23 Apr 2021 22:50:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5640cda7d848ef5b04d758634ab76476adb99c6e4f36fd0876acb8b0d5070b`  
		Last Modified: Sat, 24 Apr 2021 01:28:52 GMT  
		Size: 1.2 MB (1183393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8fa2e488481008e367def774dfbd264e85adfbce864696adfd6a4c7be8b317`  
		Last Modified: Sat, 24 Apr 2021 01:28:49 GMT  
		Size: 5.5 MB (5513419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206e4140f5b6ce4017663c411cff9bd57b65d1654307bec54dbd320713febb3c`  
		Last Modified: Sat, 24 Apr 2021 01:28:48 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca40aeec3dc251c3bfd22ae94facd7daae9365a555779c16e669988e9dfe131`  
		Last Modified: Sat, 24 Apr 2021 01:28:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c9b20fb9eb73b0d98142a02f5419c6df361b77d0652267f766c75a750b59ac`  
		Last Modified: Sat, 24 Apr 2021 01:29:59 GMT  
		Size: 167.7 MB (167723611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c587857b1382c5713d0fbc5bd542e31b23dd07854182b4f305a93eec5ca62f`  
		Last Modified: Sat, 24 Apr 2021 01:28:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

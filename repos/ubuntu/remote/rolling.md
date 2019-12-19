## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:6075f79170a360e652d7bd59e21aa5270cc9d4fe64cea8f16e87167c807818f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:c519a5ed1b9a44f53fb6d971cb0e6b4f943e0b7d7f4e92ac9ed3293ed6f467c1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28303581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351ab52170e57e284ef537d34c45e81f1050df7b09c64a1a21e6cb5a86b8f23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:01 GMT
ADD file:68f49478e86266afd7187da72d07c968a0fb8fe02ee58e12f8346fc9057d86ef in / 
# Wed, 27 Nov 2019 00:22:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 27 Nov 2019 00:22:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4fc5deeb8d45be92d96fd4e57bcdaf779545687c0e476cdc9a78c779d05599c4`  
		Last Modified: Sun, 03 Nov 2019 10:05:17 GMT  
		Size: 28.3 MB (28271982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70e07bddb7c721d1e4d14b9ff939e0b4ccb10aefae70b33f29a284be92a3508`  
		Last Modified: Wed, 27 Nov 2019 00:23:09 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bf564c51f3d467a0cb54851e92db65f1731f313234bb26aa427c292400c77d`  
		Last Modified: Wed, 27 Nov 2019 00:23:09 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111c7f4c8fb3613f909e5c351e9b83d5aeceb70bc78f986f3ea1583874890ab9`  
		Last Modified: Wed, 27 Nov 2019 00:23:09 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ff69bd4295999f971f59da66e0cb67f761d1db3358f084f96c60edeb6555ff92
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23760965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a9dc31c775488dfdd3f2b450ddabfcf6730b19064233060b75af12ae8eaf19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Nov 2019 00:17:16 GMT
ADD file:c9aef200b9be86f6df2e497769f58e5872a9aaba87c9c8b76daecc9c6d25cf79 in / 
# Wed, 27 Nov 2019 00:17:19 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 27 Nov 2019 00:17:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:17:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:17:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:448a2687ea9acf3392bf3e7d463178d8160382e5f881a890b9e717496fcfc96b`  
		Last Modified: Sun, 03 Nov 2019 10:06:07 GMT  
		Size: 23.7 MB (23729342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04092071780161878cd0083ec0a26123404b6389f38eb294074487f557b1e6c7`  
		Last Modified: Wed, 27 Nov 2019 00:19:36 GMT  
		Size: 30.6 KB (30587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a60f5aa5c62ffc8d0e972818974619be2434b1c4a301bff3ceca27c46c76118`  
		Last Modified: Wed, 27 Nov 2019 00:19:36 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fa2bbf618bd3a6a7a02eca57cf9267199a3efb36463c687259f8609d43096b`  
		Last Modified: Wed, 27 Nov 2019 00:19:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b1453de7a3075fe06b1c400e560e0c3dbabd845ae412130ab7c51ccd0464505d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26906664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447a33e68e810c1ac427bc7b6b78f0c060337fc66711cc48ec35b7d2dffc1793`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Nov 2019 23:50:36 GMT
ADD file:23ce21da58e3c58bbba513acc7816bb6398b19c94e0e93e3960d4b39187b8a6d in / 
# Tue, 26 Nov 2019 23:50:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 26 Nov 2019 23:50:43 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:50:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:50:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fff3e1c6a910106b907ae46a6aac6982f9e29a8730eec5eebb0758f9bb726578`  
		Last Modified: Sun, 03 Nov 2019 10:06:17 GMT  
		Size: 26.9 MB (26875211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c2b0017a4640c396a4ac77de3047cd7fc8b30af4005f81ade18db0075c204d`  
		Last Modified: Tue, 26 Nov 2019 23:52:28 GMT  
		Size: 30.4 KB (30418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ebb02f17e2bc538ccc8f1285c914b583b640495dcab330c66aa8574bd1f9b4`  
		Last Modified: Tue, 26 Nov 2019 23:52:28 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ea115211d254d4e8e75ea896007b87da838c5a356f391668502a389588f3b2`  
		Last Modified: Tue, 26 Nov 2019 23:52:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; 386

```console
$ docker pull ubuntu@sha256:34bd18af23fc4096f7144432a554e70830940583466e22bc4de4044e8a7513c8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29070450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea17b57c413af0290c95fac366fc955deef6ed6785d4dd01a7a08ff51facefc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Nov 2019 00:40:03 GMT
ADD file:4246474a00c04ec1953bc3df0a2b618d8c5e50a25406850e4ed25f0704d65af5 in / 
# Wed, 27 Nov 2019 00:40:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 27 Nov 2019 00:40:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:40:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:40:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cf5fbf1417c486b1f321f5de309a789cc06c2d4d2aa55a398ad9588358e44382`  
		Last Modified: Sun, 03 Nov 2019 10:06:27 GMT  
		Size: 29.0 MB (29038772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3c694acd44eec529539616f3a1a1642fd5ed0aba967fc3e9496f00f885a9eb`  
		Last Modified: Wed, 27 Nov 2019 00:41:13 GMT  
		Size: 30.7 KB (30672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e681846e27af440c687e65c91ab337609b9d2703cc00d72f24924edf966c60`  
		Last Modified: Wed, 27 Nov 2019 00:41:13 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e559d645f1976eead4fba9f7aa75f0766142d1db90c2c9d5a2eb659b78d94`  
		Last Modified: Wed, 27 Nov 2019 00:41:13 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f3dc5bfa18ff03bc2496b3033022aaaa53682d2848dfc8da6a4341f2b57e17e8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33035529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd69bdb48458c127a58ff3fa6084e2e3a4c72519f17a4edcc674383ed0b7668`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Nov 2019 00:29:49 GMT
ADD file:9290dea355f0fd25335e745c0fe627f8b84c72a2db761a35afb817face3ee003 in / 
# Wed, 27 Nov 2019 00:29:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 27 Nov 2019 00:30:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:30:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:30:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fc4809eaa3c749ba0c119eb0c3f29a7de548ed7a05a27f3598ae160446a29551`  
		Last Modified: Sun, 03 Nov 2019 10:07:13 GMT  
		Size: 33.0 MB (33004041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935dc1bdaba57b30e4b6843b5758929200af42948ecd4ae4ef66b2c317721d48`  
		Last Modified: Wed, 27 Nov 2019 00:34:19 GMT  
		Size: 30.4 KB (30446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e0233504c260871f64281e2ca8b6bdf25d225fa7dfb160804b28a149b80a76`  
		Last Modified: Wed, 27 Nov 2019 00:34:19 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6ccd5d5ba9643d7a6700d586dd042702c5aa7cc28754dcc9323651fdb3d980`  
		Last Modified: Wed, 27 Nov 2019 00:34:19 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:360242fcfdf4729cf72455869cc75dca203608729320d8265a16c4967be08471
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26714709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbecfe26dc1b63e9da4b01f4b37a9c3c380e7e581e550b8a32e937fb6abc1a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 01:19:15 GMT
ADD file:4c97153d4a7afc971d9aee338ce4f06a9fa3a64889b8f83bbf15781e664bab1c in / 
# Thu, 19 Dec 2019 01:19:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 01:19:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 01:19:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 01:19:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c33d195ae4c0866bde1a47e436c84fdb77b9679e6af4ba02f9e8fe4eaf85972`  
		Last Modified: Mon, 02 Dec 2019 15:36:38 GMT  
		Size: 26.7 MB (26682614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a41d4cb1d5afc1b8f4eae9e396114b62cf41ee529e6a8cfcc4e9e0544b367e2`  
		Last Modified: Thu, 19 Dec 2019 01:20:12 GMT  
		Size: 31.1 KB (31086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8358d099aa1117065a579db0fbe5d90d7155d19f7fd417351329550e1eb99bf4`  
		Last Modified: Thu, 19 Dec 2019 01:20:12 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d3bd335eb5fc325d2f62d526e7ab44b723439a5d4d8ae4fb0d64933d06bce2`  
		Last Modified: Thu, 19 Dec 2019 01:20:12 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

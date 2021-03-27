## `buildpack-deps:groovy-scm`

```console
$ docker pull buildpack-deps@sha256:b2dfaa570ef73604caa9df417746532dc9ca7ced01eb520f79fe13053c18c6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d21b88f1ce5c970ea5e4f55bd42cbe322f8220a8126ca4804979129203a5f6e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95889836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939842f68ab8ac08c409b4989fbdb1382d799cf7a8fb472729860a7ff8d964dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:18 GMT
ADD file:4aba1ec4c6317039d27ed2f8cdda90160c834d979269ba6253f4b8839e6a8c06 in / 
# Thu, 25 Mar 2021 22:33:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:21 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 10:42:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 10:43:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 10:43:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:67b8b51191f1c23048b4af7390755377b07b7033f43a5bc7a5bcf37f863f7adb`  
		Last Modified: Thu, 25 Mar 2021 22:35:06 GMT  
		Size: 31.3 MB (31348493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bee746ea8f946b8bb5dee1458e4bf97293706926511644fdfd4411b9bac5710`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014d36ded12e82e314bb890faf3e15c110c39688e938f9c8c8ba8ebda5cbcbb7`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9c37b96171571dc75418fdaead51ffde0478f656e8a8abba474da5f34e9982`  
		Last Modified: Fri, 26 Mar 2021 10:55:55 GMT  
		Size: 5.4 MB (5403819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126959169ae74465bee143ab20f409ffdbd10f26684b2284611d1380fda4ac47`  
		Last Modified: Fri, 26 Mar 2021 10:55:55 GMT  
		Size: 3.7 MB (3663037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f9f417ebd6fceb2f41c071071eb8113cbed20124275713383d643a00e3b3c4`  
		Last Modified: Fri, 26 Mar 2021 10:56:20 GMT  
		Size: 55.5 MB (55473449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4ffa36e9cfe200fe78d6e804a49f8011f544faeb2e5051aab5ef279e1d5d111a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84572609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fe00fccfbc1ce1f3a2fef57845bc309b57f6db033bd6c7687c0746ada8b233`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Mar 2021 09:14:55 GMT
ADD file:3f08cb88ecfb4ce1e2f7673073f544cac31372fed929da9dd2fa8cfc46284936 in / 
# Fri, 26 Mar 2021 09:15:11 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 26 Mar 2021 09:15:16 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 26 Mar 2021 09:15:20 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 26 Mar 2021 09:15:21 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 13:43:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:44:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 13:45:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3a8c187ab20e8ee012d9a5d214506d6fc30d3d08fd0e938ce628feaf2fa113b`  
		Last Modified: Fri, 26 Mar 2021 09:16:59 GMT  
		Size: 26.3 MB (26305201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa13ee74f81c6f477aef74be75c0ffbc9c88334a411b792d6d28ab528ebb38ff`  
		Last Modified: Fri, 26 Mar 2021 09:16:52 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937a0652ec2669b768054aa4c8c680013970c5af6606b3a30aa106f25bfc6655`  
		Last Modified: Fri, 26 Mar 2021 09:16:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4acf90e3d263bc628c8fe73964e5740f39607cef9d88c374679af243c6dae2`  
		Last Modified: Fri, 26 Mar 2021 14:00:22 GMT  
		Size: 4.8 MB (4839133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834b2c0fa6ee90c46fe708fef316364430187ba1cef0888e009c92c6d60b56d`  
		Last Modified: Fri, 26 Mar 2021 14:00:22 GMT  
		Size: 3.1 MB (3139633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9222f104a8f17d2b251ca2cc31626136f9e59af1581ef2d8881f8ed479840425`  
		Last Modified: Fri, 26 Mar 2021 14:00:50 GMT  
		Size: 50.3 MB (50287602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:49d4e3bf6662814798fb9f74c9edef89fad785d66e7b5a9a33df2617a9878054
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94340151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c807c6792380a394318ef1b2ae5ee2774b44358f54f7a2b67cf6c7fde3ce9702`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 23:23:37 GMT
ADD file:bc454d5161218f75993ebbdf481b33bcc8481d86df6a4ebebd1aa225f6ab1a6e in / 
# Thu, 25 Mar 2021 23:23:43 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:24:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:24:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:24:14 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 13:54:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:54:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 13:55:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2fbddb1214587c696bb31fede80842b3dbcd958c51046da66428aa707846d85`  
		Last Modified: Thu, 25 Mar 2021 23:28:41 GMT  
		Size: 29.9 MB (29879553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56199f788c6c3bfb7ce7f6df89f8bdba788bb47ffbe67536c9c9b5535230dfae`  
		Last Modified: Thu, 25 Mar 2021 23:28:33 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cee2f5c916ba34ced7d73891af1546061e319dd13b964641eb89838eb55a4f`  
		Last Modified: Thu, 25 Mar 2021 23:28:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b19d93e6232d632b3e7f17bcd095de0ecd7db1dad7260918146c8d37d87a8c`  
		Last Modified: Fri, 26 Mar 2021 14:02:06 GMT  
		Size: 5.4 MB (5371522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea1b4483b2919d2c2422397a25c5dd11fa7aa2a3d7983ce7520e57c521cd75`  
		Last Modified: Fri, 26 Mar 2021 14:02:05 GMT  
		Size: 3.6 MB (3634186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe075891276ff7551ce6750fa55d9795e5d43f0d05ee0483f2963ccf9f7668e`  
		Last Modified: Fri, 26 Mar 2021 14:02:28 GMT  
		Size: 55.5 MB (55453851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0814aebfb4d0a5da34693dfa51ab2985258b2de08ef2c445fe90951f63c556e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110846569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51993ed0f4f4ef45b3db81b3e4c0e7626cafd9de2e61426465636c1cc5f769bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 23:06:18 GMT
ADD file:e34a211f8389692e4244e58071f95e901c5b669a23e0bd2f42e5a0df9f3657ba in / 
# Thu, 25 Mar 2021 23:07:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:09:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:11:20 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:12:15 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 19:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 19:11:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 19:14:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:436fb29ec2596e4c355f1b6b28ce8845b13f5ad373b27d87372d9c298df4ef1c`  
		Last Modified: Thu, 25 Mar 2021 23:18:37 GMT  
		Size: 36.5 MB (36543260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd53feed846454ab651d6fd3a7c942ecf742ed6f3621f7dce883a32f449babd7`  
		Last Modified: Thu, 25 Mar 2021 23:18:30 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5673b7b9a679fb96367c8868e294e7898babfb273f90fc02c9188b52288cbe0`  
		Last Modified: Thu, 25 Mar 2021 23:18:30 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaad0b6865e4e1121408e3b5488fc03f1e5152e2530e144231612823b04fad33`  
		Last Modified: Fri, 26 Mar 2021 20:05:05 GMT  
		Size: 6.0 MB (6039462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1808b8250973d736b7bf9467649e91213a89e27345f352eeaa5b3cea8279b7`  
		Last Modified: Fri, 26 Mar 2021 20:04:56 GMT  
		Size: 4.5 MB (4520657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcdf928bd5ac7ceb7909f2fc51e5d299ba007c72977e41f79a1124937b30822`  
		Last Modified: Fri, 26 Mar 2021 20:06:45 GMT  
		Size: 63.7 MB (63742146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b496a6e62b75d870f2209e4918e19977b951c449787c2a4629e3dcca71f777e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101989889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6698f12e4f5221890b939962a47f6e96f7cbbe22246526becbb5a327291f7d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:53:51 GMT
ADD file:7945beb7b5ef4c133bdf7d9985c8bf01597f8529054f63bdd3248cc6f62898c6 in / 
# Thu, 25 Mar 2021 22:53:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:53:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:53:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:53:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:07:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 09:08:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff47e30c1aabcb1fb50a92bbf25aeb65010daab236491e40a6328f0d0837aedf`  
		Last Modified: Thu, 25 Mar 2021 22:54:56 GMT  
		Size: 31.6 MB (31555142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8d4f437f8df3327d0adb39cc03bee0f02236b2424230a1eb77593ae575e437`  
		Last Modified: Thu, 25 Mar 2021 22:54:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5ccf215f963aacb49a819b61b1f7658ff0d670b47ece9b0e8a8fa3ec074053`  
		Last Modified: Thu, 25 Mar 2021 22:54:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc20992cecbdf0269278df2147cd1afc47ee8194684c62516fb04e04cde2b94`  
		Last Modified: Fri, 26 Mar 2021 09:13:02 GMT  
		Size: 5.6 MB (5628850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83638988ee96c06d9bb6f2f756488c8f0c384f773c0f55bc6bf167d15486e8bf`  
		Last Modified: Fri, 26 Mar 2021 09:13:01 GMT  
		Size: 4.2 MB (4155848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e35596bd825564822fdd62bad760f3d970c85b41e25d6de3acb4e37cd3bcf1`  
		Last Modified: Fri, 26 Mar 2021 09:13:21 GMT  
		Size: 60.6 MB (60649009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

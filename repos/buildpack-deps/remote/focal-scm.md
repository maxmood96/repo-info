## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:57a162a545052301696ab53c56fac921a6bf3ef7b83b9a5356043ae96632528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2b175c6bbfadc97ed80b8fa4adbd5c59503c8465f50977806489187868bd8618
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99170165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53452d279028f2eb4290f13cb499912db3e47acf9510b8da649a6fc5753f66ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:46 GMT
ADD file:0ab26fb2f991568d8c593278d4713aed6f3962b7017e3e97e9e3f276031316b2 in / 
# Fri, 20 Mar 2020 19:20:47 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:49 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:52:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:52:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 20 Mar 2020 19:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:767fb6cc1b890aa8046de6d03522b32e23be0de28399261969d00d2666827988`  
		Last Modified: Fri, 20 Mar 2020 19:21:41 GMT  
		Size: 28.5 MB (28521801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c917d9c558a31b32c8cde71574bb4e5f32f55d211e9f0a24345b4b5cbb076dec`  
		Last Modified: Fri, 20 Mar 2020 19:21:37 GMT  
		Size: 31.6 KB (31643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fef7dab626401e4c58516546265cd18118fd3e9258278400e932c811e5d132c`  
		Last Modified: Fri, 20 Mar 2020 19:21:36 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7950fd118d3c2144a9737933f5ba06b35a0f4fab5667001c3f101f87a9cd09`  
		Last Modified: Fri, 20 Mar 2020 19:21:36 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffa145b61007d9318e97209cfefe9ba50ebd86732b5d616bf7778beed1ff0af`  
		Last Modified: Fri, 20 Mar 2020 19:57:49 GMT  
		Size: 6.9 MB (6859499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dec3ed7b85ac54f7c70e2acb445fd9a1c0f4f2d6d9730f689dc16a33f59c4f`  
		Last Modified: Fri, 20 Mar 2020 19:57:48 GMT  
		Size: 3.6 MB (3564924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec38c403de6c87df7e9259172c8c7d278c9b612ea94cbab8d6b45e60339c2595`  
		Last Modified: Fri, 20 Mar 2020 19:58:04 GMT  
		Size: 60.2 MB (60191285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bdf1ecb91b477875cc7e023b9be601a8a53788e637e56cb302e847b657736bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87624859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390e04580adc62c7b751d5463d9ff6203d2222da3cf214b407916ef524a961a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 01:01:57 GMT
ADD file:2d3ba051ed20fafa578680b18fbe731818ef6ab90ced4b0d6783816de70b6a6f in / 
# Thu, 16 Jan 2020 01:02:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:02:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:02:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:02:38 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:12:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 02:13:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:05:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc4316c8e9493de0b0e1b0cc1c1b9b1fb58750baed7140f2fd1d7d964c601fc3`  
		Last Modified: Thu, 16 Jan 2020 01:05:12 GMT  
		Size: 23.8 MB (23835040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21553c3db6ce4ac20d8a949658bc8bd42e4658e34d64017f3e117eb6da1c92`  
		Last Modified: Thu, 16 Jan 2020 01:05:06 GMT  
		Size: 30.6 KB (30569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2d0679b20cd11ff9c15f051b0c8be2781fdd2237f065c0be6336cfa58d0d9a`  
		Last Modified: Thu, 16 Jan 2020 01:05:06 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35042469e78e129ca9456d1cd736e5850df94ac632815d85a09777c32fb0082`  
		Last Modified: Thu, 16 Jan 2020 01:05:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5466c47a95ace9c543ced1eb1256ea7b8c427c0c022cca72e8cc24ffbb31f6`  
		Last Modified: Thu, 16 Jan 2020 02:25:43 GMT  
		Size: 5.9 MB (5871813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dff48eabde2f5a7ee75934543812cd750a9d08b78244571f77da78f6e588dde`  
		Last Modified: Thu, 16 Jan 2020 02:25:43 GMT  
		Size: 3.0 MB (3035891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad38e4ada26d1b355e20d9300eeec879d4d6ad6b351317ad2aa98c5b469b8e`  
		Last Modified: Sat, 01 Feb 2020 18:27:35 GMT  
		Size: 54.9 MB (54850512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c8a1fd41fb9fa7e3ade560f086b9c33cd4275be0bc870ccfd1d64cf17f28672d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97642270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bafaea40c6eda3e801934b7a45ebb31b80511ecb42cfca1bab40a1d3aff797`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:44:18 GMT
ADD file:627246f3025f0a9473866d1a3f837c7bc78c1bb64018aefa683ed63fd6b8affd in / 
# Fri, 20 Mar 2020 18:44:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:44:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:44:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:44:25 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:17:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:17:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 20 Mar 2020 19:18:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9806bdadc1314b3e8b4d5249399ac07348da8dfd86b71f450d4a8d5bd672df12`  
		Last Modified: Fri, 20 Mar 2020 18:45:35 GMT  
		Size: 27.1 MB (27127860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a0e1a95f5228adef261b8a421a32e0c6326702c2219757fd4c6ab176ae46d`  
		Last Modified: Fri, 20 Mar 2020 18:45:28 GMT  
		Size: 31.7 KB (31653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b08ae661b4f6495649f65df48cfe19cbbaada45e4c46064378e416fe5c68c11`  
		Last Modified: Fri, 20 Mar 2020 18:45:28 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e5fbabbfbbb4adc0246d014df57f1f8ed76e8f16b7cc3d313a1a7eafe628f7`  
		Last Modified: Fri, 20 Mar 2020 18:45:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da3d88749ec83ebe9d4c864674283cf8c82e033908fe57827b0fa550edadc6`  
		Last Modified: Fri, 20 Mar 2020 19:24:16 GMT  
		Size: 6.7 MB (6722069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4563cf360577e6079155b2b2a1d6538186dd007e8b140dfab33037ed16fd04ea`  
		Last Modified: Fri, 20 Mar 2020 19:24:15 GMT  
		Size: 3.5 MB (3541103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28870972fc030ebaf445ae2741c5e80b064fd4e8cf2b5895df590d064fd499b0`  
		Last Modified: Fri, 20 Mar 2020 19:24:40 GMT  
		Size: 60.2 MB (60218550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ced790a376f6ff81dd79321d673d7d7ebfebd7fe2f456f230498c08c594bd961
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114360563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c2ba547488a18a753c52ea8d44f1c4129420760173d24429caa48b8d3a3880`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:23:44 GMT
ADD file:aa6837ec5fc9aa5509004c5c2f8d9f4fca19beb57131babb5f3ab770ccb50cd1 in / 
# Fri, 20 Mar 2020 19:23:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:23:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:24:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:24:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:40:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 20 Mar 2020 20:42:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c60419ce4ad313deb007f5835ca7d2bd045778a693e50b3d2a66ddce1a36e995`  
		Last Modified: Fri, 20 Mar 2020 19:26:06 GMT  
		Size: 33.3 MB (33255285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d46f94aa4e6b2f9a3f0e7562389f25dc0ff07b147a0f5e369e09d220dab91a6`  
		Last Modified: Fri, 20 Mar 2020 19:25:59 GMT  
		Size: 31.5 KB (31500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95829298b5408a704109b7f54f06ba7180c2088d8b138b4069b0c0b72c989c36`  
		Last Modified: Fri, 20 Mar 2020 19:25:58 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4176ec2142d9c14ab633f5b3939c935d942d3af3ee9de948d70c8ea60146b05e`  
		Last Modified: Fri, 20 Mar 2020 19:25:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa00bbcfb61c4e0f2c416561c35902360fe4e9bf213bd33fe8ae03a6628e07`  
		Last Modified: Fri, 20 Mar 2020 20:54:32 GMT  
		Size: 7.8 MB (7811511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7d10881b5d3005f25cbe0c3d42ce03e8718d006eb0e29bfdeab6cc5c0a6449`  
		Last Modified: Fri, 20 Mar 2020 20:54:31 GMT  
		Size: 4.4 MB (4398695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef2e63ca39c690e45070891c81a9d590fd58519abf34d5381be86a75ff2ea1`  
		Last Modified: Fri, 20 Mar 2020 20:55:06 GMT  
		Size: 68.9 MB (68862529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:62b1f5e67303dd478d9e85fbbddbb46e363f16263a8f5fee026ca6773fda4093
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97292249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6387ba82230a3b281156da5dac5be30189bbeb845c0688016a35d3a4c91dfc15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:42:29 GMT
ADD file:420ba790b06c89e0e028fee491442a3d61a67bb27d8b548820ed00940f41abb8 in / 
# Fri, 20 Mar 2020 18:42:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:42:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:42:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:42:34 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:33:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:33:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 20 Mar 2020 19:34:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d55872e7f9efe88c9121c748ec231652e7bde16bce37c7d61bc808494cc99257`  
		Last Modified: Fri, 20 Mar 2020 18:43:16 GMT  
		Size: 27.2 MB (27204299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02987bfd1fe32596c731867a13d49a9152d762c34c69849dddaf97fb1704f27`  
		Last Modified: Fri, 20 Mar 2020 18:43:12 GMT  
		Size: 32.3 KB (32286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6459db5ba591c1c338d4d680ea401232e2def483b6e07db1bcf134e4df6bdbc2`  
		Last Modified: Fri, 20 Mar 2020 18:43:18 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6818c11522b95465a735052f0213a7a913b81557b6f5d42a7f21dbd25e0e36`  
		Last Modified: Fri, 20 Mar 2020 18:43:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b044e5f71f3bdc033d7327a10c3aaee1d7f55e6c78c658f0aaeb32811682c`  
		Last Modified: Fri, 20 Mar 2020 19:37:31 GMT  
		Size: 6.5 MB (6544443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3633d0d76dc022ba335bd391614cc3fa1235894789593a084330f6e0fd338707`  
		Last Modified: Fri, 20 Mar 2020 19:37:36 GMT  
		Size: 3.6 MB (3561525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c3e9641919cddf8854022bd67dd08fd3f2aee51db3dba78b1bd902448a3d8d`  
		Last Modified: Fri, 20 Mar 2020 19:37:50 GMT  
		Size: 59.9 MB (59948662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

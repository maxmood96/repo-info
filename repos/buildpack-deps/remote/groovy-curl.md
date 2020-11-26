## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:f0da2ac33bb506927e16e8bd06832d79c6b0ccaa542c60625c7306d976ae09ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7559c7ba6ec58498197fc483d23013e7715353e67c042cf48c5e692aff5a1873
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39441519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f4e556af339ed0a23a0d96d63d8cc7abd2b592e7990123bd49d86be3d48139`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 17:32:46 GMT
ADD file:6099585856c27a9f8dd40d7e679184a6d1bb58133acf73d5d3c9904932def005 in / 
# Fri, 23 Oct 2020 17:32:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 17:32:47 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 17:32:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 17:32:48 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 18:01:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:01:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7a14fb4cd302ea60d4b208f17bb50098b52a17183a2137c08299a3b915d7cbae`  
		Last Modified: Fri, 23 Oct 2020 17:33:40 GMT  
		Size: 31.3 MB (31337938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b1fecc905c746712dc231f73c5d630927892af991ce140673eb77dd9b697cd`  
		Last Modified: Fri, 23 Oct 2020 17:33:35 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac8019c9736cea870759cf87bf752344fd3fb2dbf7a3921e9c60e140213900`  
		Last Modified: Fri, 23 Oct 2020 17:33:35 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b137add616873c756cd3a60d7de3e8ac2ad471a32a8d7e7fba112082ac32f5`  
		Last Modified: Fri, 23 Oct 2020 18:08:23 GMT  
		Size: 4.5 MB (4515029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9baeffa76ee358acf2e9423b3bd03ff13ef4361cda101c57242f87268fc7e`  
		Last Modified: Fri, 23 Oct 2020 18:08:24 GMT  
		Size: 3.6 MB (3587545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9a28dc64b19c738c81d275eaec2cb2714e22e9cc9f572900e18ebe40c9f95c05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33307952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9ef23165fa8d02f3b92245632ccc23211564740f228f0924ed3718c93eec06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 23:00:02 GMT
ADD file:064c9cf96cc5a27a93d36df3f2590769d18b7ce2870d6fcfc9dc92137a6565b7 in / 
# Wed, 25 Nov 2020 23:00:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 23:00:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 23:00:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 23:00:10 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:47:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:47:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cf5d881b2b889e71fd32d9e0c3ba5c6da794e6e5afa2741a16d3fc09ae7beffc`  
		Last Modified: Wed, 25 Nov 2020 23:02:13 GMT  
		Size: 26.3 MB (26295207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb07a3af272cbbfd1fcc64d017f4fc7bae62fcb025cda21f621f2476bbf4589`  
		Last Modified: Wed, 25 Nov 2020 23:02:06 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2bd357c5c9ebe614fe49e864454ee6c2cc7bb576066d0d514483aed112ff05`  
		Last Modified: Wed, 25 Nov 2020 23:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7207a53d4c4a7708ce000c577926f3beb0dec788c12fd3fe7d2faf6d7c5633fd`  
		Last Modified: Wed, 25 Nov 2020 23:58:22 GMT  
		Size: 4.0 MB (3950065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f30892035840669548f54d04602e990b76625a1a2877362fc8aae8d308b813`  
		Last Modified: Wed, 25 Nov 2020 23:58:22 GMT  
		Size: 3.1 MB (3061644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c69ec2f4a050cdfde6ecc06060ce7be596c94837d3caf6179d6c690702a9ad2a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37946138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ea4f8a7f18ce3c819eed65b08be28bbaf85d8caf55a30522e60f6c46757394`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:43:30 GMT
ADD file:64620b7461f90248a314404599b9aa3b9b592786bcc8ed2cae9df8a7e1f15304 in / 
# Wed, 25 Nov 2020 22:43:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:43:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:38 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:08:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:08:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2769ac0e7b9ff64f87f3db82269939c4119f3e9b548bf84e398e068642e07624`  
		Last Modified: Wed, 25 Nov 2020 22:45:16 GMT  
		Size: 29.9 MB (29882425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b76975e3e10573aec5f323bc1d6dbc76af857b1dc3289a68a449dfb881dc2b6`  
		Last Modified: Wed, 25 Nov 2020 22:45:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958ead7f79658868738b309ef9d34e12c738ee519ace595275e35b3c7ea3a5c2`  
		Last Modified: Wed, 25 Nov 2020 22:45:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4213aae5ba683b357424fa2bea5c4e52825e7ea9b8b005dce568bef39c53401`  
		Last Modified: Wed, 25 Nov 2020 23:17:14 GMT  
		Size: 4.5 MB (4489528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9734172f17eb676dad8b6e9ebb6a0b12a5d362962c46d5b7b796b8f63ac368`  
		Last Modified: Wed, 25 Nov 2020 23:17:14 GMT  
		Size: 3.6 MB (3573150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:82e7e018fe1294cf8a03c316bc339371a20d53588837185f599aa236e9eb7e60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46149821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d939bbc61fa16e165f1d8fff8d751339b511bd495bcff62a00a1b67c5b1e3a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 19:27:22 GMT
ADD file:3cceb8288ea4091c4fb6670e395f7391741cb6aaa44a1f5e6a2085df56ecba62 in / 
# Fri, 23 Oct 2020 19:27:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:28:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:28:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:28:47 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 21:04:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 21:05:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a69afe95a22d68414fa1ac1b89258d7d482624063e15ae9202ea3fa7649709e8`  
		Last Modified: Fri, 23 Oct 2020 19:32:07 GMT  
		Size: 36.5 MB (36548485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80643583a935ac0edf00defeb0107c6483073a7c2dddd14e5dfad2a4699b178`  
		Last Modified: Fri, 23 Oct 2020 19:31:58 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49aeb38173a94db987f5d84e1a11177492fa369f214626d961156443b10f1571`  
		Last Modified: Fri, 23 Oct 2020 19:31:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26244204f484bf82c80adec639263fb4afb37e1c8a6aa041874a008251bea4a8`  
		Last Modified: Fri, 23 Oct 2020 21:53:01 GMT  
		Size: 5.2 MB (5151374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49940bb5dd8a122a071e1056de6bba9d7dd55b97adf0d169cae103878e2835b0`  
		Last Modified: Fri, 23 Oct 2020 21:53:02 GMT  
		Size: 4.4 MB (4448921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d5641bcde5d021f7a8a038aa8838600a749a7e9b423a8b2e123e3ee09bc3ec56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39754373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb7c83d70e4a2f6d5732231b15bf3dc00f8bc87a5d365a7082cc2e953ee4089`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:45:41 GMT
ADD file:af8181cb78887aa9e6aa7f7b33a8ef7b76b74cabc09f582883a8d3111c0fe9e9 in / 
# Wed, 25 Nov 2020 22:45:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:45:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:45:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:45:53 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:55:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:abd4319bb36506beca49a36e3151713760b1b1a72286ebd52ed6a0f8b037ef26`  
		Last Modified: Wed, 25 Nov 2020 22:47:37 GMT  
		Size: 31.5 MB (31461133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13be14e62d3b49d67b17ae821b83ac4bdfd2186f11cceaa27ea603582a04e6e6`  
		Last Modified: Wed, 25 Nov 2020 22:47:34 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f4745ab7467cbae8d29dc6729e2735cabc05177631c8eb03cfafa79c8bd58`  
		Last Modified: Wed, 25 Nov 2020 22:47:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eeebe396cfa22cf2fc2d0fd92c9dec59dbd2fe7726de52a00e2a081efc99c7b`  
		Last Modified: Thu, 26 Nov 2020 00:05:58 GMT  
		Size: 4.7 MB (4710202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd121be9c3aab14266f8b8785c0d3afe9508806816108bbdbc9185d242c3bae`  
		Last Modified: Thu, 26 Nov 2020 00:05:59 GMT  
		Size: 3.6 MB (3582006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

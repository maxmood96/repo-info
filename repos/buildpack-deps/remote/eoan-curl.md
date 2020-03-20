## `buildpack-deps:eoan-curl`

```console
$ docker pull buildpack-deps@sha256:16895f7c477feea99e246ed8cfae0ce6d9a2f53cf09b3141c45cfa2f13e9ddbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:eoan-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5ad44c8392491696d6e3fa16ecb308c14bdc3201ed2574bf89e58a11dfa69199
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38338393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe6177a1712075021ac46916b6c75989eb92721e9ff3ec5db690af123f96c1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:21:11 GMT
ADD file:49bd1c0bfe89a93a193774bfd334bc1151f0dca95849f81d1ac353673399585c in / 
# Fri, 21 Feb 2020 22:21:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:21:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:21:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:21:16 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:56:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a9c68053c4b2379a9ad5b7306236a13f469cfd18e727dd4e76470af366445b45`  
		Last Modified: Mon, 10 Feb 2020 15:41:51 GMT  
		Size: 28.3 MB (28276663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9c43fe7e5dcfee42adb18336072154126bc052cc1c578e64d27a8aeaabc97`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 30.6 KB (30633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90491034717d4c1d1e0b37a4bde4f3a0e26630af7d360b7c0248660ccbef59d5`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781c6270286751c77c20928c68fa3edd532f0d3d11108db32020c8840f0ea6cb`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73542a256b5ee66b5f38af9d7c37a2d5d03c3ed228335a54f0b9c4c556f2c45b`  
		Last Modified: Fri, 21 Feb 2020 23:04:21 GMT  
		Size: 6.5 MB (6512504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eaf9e73f3647faef689dc3183ba6ffe693631be3039058b42f3b7c177b97962`  
		Last Modified: Fri, 21 Feb 2020 23:04:21 GMT  
		Size: 3.5 MB (3517579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6ebe01c4e45709e77b552960fea4a9e9e7f68fafe801138934b1f5474242b8d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32282238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928dbef9bf075f0402464b85d375a8d69a40eb5f973f82ff010aeeb5b0ab16fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:58:53 GMT
ADD file:d5ea94843f1a1e0976b02f8e02c5256c148157dd51f492da5181ad8753622ab4 in / 
# Fri, 20 Mar 2020 18:58:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:58:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:58:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:58:59 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:21:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:21:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2ea86edd9db57be0bd75bed151c49e031bd6699fcbd94130c3a8a8ab459692de`  
		Last Modified: Mon, 16 Mar 2020 15:44:38 GMT  
		Size: 23.7 MB (23735633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6c62210e628371fc8ed38017e5360a6a15489b56acd8dba096dc79768da4ca`  
		Last Modified: Fri, 20 Mar 2020 19:00:28 GMT  
		Size: 30.6 KB (30613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8325644a644873d31f1108862c1ed632f57c3fbc43ebe7603f57c2c0d39a3665`  
		Last Modified: Fri, 20 Mar 2020 19:00:28 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c4a05bf433715cda695415ab43dfdcae3e89606057e6ab273703fa768f4a6d`  
		Last Modified: Fri, 20 Mar 2020 19:00:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5329b380082dac433270a0b1ad42ffe176511a6b4a4a7f6081c725d8a9772858`  
		Last Modified: Fri, 20 Mar 2020 19:26:53 GMT  
		Size: 5.5 MB (5532315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b02e6dbd45902d44e8810a3b6e246f1b3b62a3b0345c64c711bba978777b0d6`  
		Last Modified: Fri, 20 Mar 2020 19:26:53 GMT  
		Size: 3.0 MB (2982641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f422fc721b7d3c3b18b444a1e1a6e451280d6af20c42d64566197ebe3e99611b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36783227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08eb8bf2d1400d844f0ccdc17bb2163aba5ea310ca74d64804e4fc2212e2e91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:43:59 GMT
ADD file:908424aa468cb2a7000dd795511259c67a0f70d0bbafa4b05b405faf89be8a02 in / 
# Fri, 20 Mar 2020 18:44:01 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:44:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:44:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:44:06 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:14:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:20fe7914fb520387e59fda29e21ea64541bf9e7e95c9eef77a6ac68c18d23349`  
		Last Modified: Mon, 16 Mar 2020 15:44:48 GMT  
		Size: 26.9 MB (26869532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c6aa3850fcf8c6207823b79f1560303443a33d4fe996bf809b4dc7d00f7d35`  
		Last Modified: Fri, 20 Mar 2020 18:45:14 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02ac1bb4168bfb44e13693f63bd600c9230216a2443e5fb4839aedbb31635a2`  
		Last Modified: Fri, 20 Mar 2020 18:45:14 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1b98aacf49712db6881b4d4da724b4349964afa1b6e6b4e983b7465c028513`  
		Last Modified: Fri, 20 Mar 2020 18:45:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87bce95c870b3e429de8b2891d6e9fd55ff65194bb2c98b4dd1517d810be1ed`  
		Last Modified: Fri, 20 Mar 2020 19:23:03 GMT  
		Size: 6.4 MB (6370756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420f2437c57580d01b2aecf81116f84e3120a5062815f6ea05b18bac2f74e9f8`  
		Last Modified: Fri, 20 Mar 2020 19:23:02 GMT  
		Size: 3.5 MB (3511455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c06b85336cb8f09b72da13e3b0169a90ee4f6d58b86cd08c644c191a0bc565ec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39727859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430b9793bac54e8dece08e5b36af888f786d6c61b5a76697d8255f7f9429fc12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:39:08 GMT
ADD file:0e9faec03747f7230dbb61530a500027d8a504b2aa7edc19353d9d113a28b775 in / 
# Fri, 20 Mar 2020 18:39:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:39:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:39:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:39:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 18:59:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:00:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7ec2907f7e8e2aa58e6e8544a4c009b751bc4ffb0260097338c8af14584c359e`  
		Last Modified: Mon, 16 Mar 2020 15:45:02 GMT  
		Size: 29.0 MB (29044614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6611c39bb98f10485e66c9de26f541ea83047ec3a7c7c375b08960b001e976f7`  
		Last Modified: Fri, 20 Mar 2020 18:39:45 GMT  
		Size: 30.7 KB (30688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925c05ba7d1067bfcebc90f78d1d37877173cccaab5663827e1e19a564ae9064`  
		Last Modified: Fri, 20 Mar 2020 18:39:44 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de9c38a779a8dbacc0c634c58a8e8abbcb85229eac1910ff6d3fa00081dda86`  
		Last Modified: Fri, 20 Mar 2020 18:39:44 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f7f723694def9380e68a617edcb019578a85bcabb11c1c8314bfdf72d567c5`  
		Last Modified: Fri, 20 Mar 2020 19:05:20 GMT  
		Size: 6.8 MB (6841242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797bf372b91800946efda9e04e576b23d1a182a772d6dd22c10bc1b560de9e42`  
		Last Modified: Fri, 20 Mar 2020 19:05:20 GMT  
		Size: 3.8 MB (3810307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c03e944f856f61687fca0e5c163fd5756286da2b63016e5ea2f912061881e12e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44901138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10290a63f561b52fde0cc7c8d4624115bb72f1124f752fc8f7de921e0f7f5bdc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:31:25 GMT
ADD file:d3168601bc3d213abcd3bb57ad2824d9099de51d8775c8d356460e12d15a26a1 in / 
# Fri, 21 Feb 2020 22:31:31 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:31:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:31:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:31:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:03:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:051dbc8b8e4ed99bbd1a698a7e4bd348c280e0ddaf417786fbedd99ca22cb144`  
		Last Modified: Mon, 10 Feb 2020 15:43:20 GMT  
		Size: 33.0 MB (32986499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f53f3c55500976229df5bc71ead0d2723cda57b2c606b6e906de3b7b5c2ad80`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 30.5 KB (30477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8143f400347b6df364214d634dbcd1db12d526040a868183289501481e13f05`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6e204830d0f5b1439e36d1a6af90c8b04d96fb8b4bcacdd6f611706a97881`  
		Last Modified: Fri, 21 Feb 2020 22:33:33 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd064f9cfd83a46d8aefd85c1839261286088ce49c7ed0b6a49bc9f488ba789`  
		Last Modified: Fri, 21 Feb 2020 23:30:53 GMT  
		Size: 7.4 MB (7419981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74726e386bdfae67f0944edb98035484c91063bc63699525f6091848d0f79495`  
		Last Modified: Fri, 21 Feb 2020 23:30:52 GMT  
		Size: 4.5 MB (4463145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:444ac2f87074e3151ea1b2700ae4a2412dacd4d3c5c2bfd4787416510a92455f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36287738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfae3a948eff85621c77691aca8723e289a2c15fc4e28b116fc3ebc9e0d2214`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:42:18 GMT
ADD file:67b3704d37c528c5ff6a197ca57162dc6c474867b382ad39db7904ab7e226fc5 in / 
# Fri, 20 Mar 2020 18:42:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:42:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:42:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:42:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:32:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0517329801b2de345bcce817664cf86ae07c4024192a4284158da43c3122a418`  
		Last Modified: Mon, 16 Mar 2020 15:46:11 GMT  
		Size: 26.7 MB (26682375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511ae87888dfc4543789268e73d6a6615b85f3cf537675ca82cd56ccee47b8fd`  
		Last Modified: Fri, 20 Mar 2020 18:43:01 GMT  
		Size: 31.1 KB (31112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2492fa1c3c34d5a0666ea3189b225fbf28caa4aa29c30534274be8313a299c6a`  
		Last Modified: Fri, 20 Mar 2020 18:43:02 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad57e1baaa7aef9e2412ea570ae32f8973c10febade619f78326cd18c22eb6a`  
		Last Modified: Fri, 20 Mar 2020 18:43:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201e9590b4324aab4dfbd09eeab54089a6c9d7feb382d3a800ba7b871d578e5b`  
		Last Modified: Fri, 20 Mar 2020 19:36:46 GMT  
		Size: 6.1 MB (6139579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58616e43320d89facaf8f9003ae1495c9caff28193ed6c78f884ef4f56bda91`  
		Last Modified: Fri, 20 Mar 2020 19:36:51 GMT  
		Size: 3.4 MB (3433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.1.3`](#r-base413)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.1.3`

```console
$ docker pull r-base@sha256:01b2e0999328eb96f5bd08fcfaae8556fe28355a7ff0e6f3c1e5cd519468b245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `r-base:4.1.3` - linux; amd64

```console
$ docker pull r-base@sha256:2bc4b435dc278c9fd3f80835dee88a8c117cd7ca21c414696c879608e1b1d6db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333704428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7ea19c65d1b3ccec31a341db7ae56bd457f9406fc84940a55de6b07e0263d4`
-	Default Command: `["R"]`

```dockerfile
# Tue, 01 Mar 2022 02:16:21 GMT
ADD file:3bd81adfd714a4198480d282bb0361dcd321e2117c15e2fed68196a62ee3c209 in / 
# Tue, 01 Mar 2022 02:16:22 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 06:04:53 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 02 Mar 2022 06:04:54 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 02 Mar 2022 06:05:03 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 06:05:06 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 02 Mar 2022 06:05:06 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 02 Mar 2022 06:05:06 GMT
ENV LANG=en_US.UTF-8
# Wed, 02 Mar 2022 06:05:06 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 10 Mar 2022 22:19:50 GMT
ENV R_BASE_VERSION=4.1.3
# Thu, 10 Mar 2022 22:20:33 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Mar 2022 22:20:35 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b487f29e2f74d18c9e1d4ce1d18f5bc5c85ecf2dd3be54c2302e10505af8c8d6`  
		Last Modified: Tue, 01 Mar 2022 02:23:36 GMT  
		Size: 55.8 MB (55764029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059c826793480c91be73bd7c9e7242de79d68253a388bd7a5fc295253a70a55f`  
		Last Modified: Wed, 02 Mar 2022 06:06:11 GMT  
		Size: 2.0 KB (1974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a230dbf54f3392375a71368dd70115a17a139c56a37e9f9701b01535bb3396c`  
		Last Modified: Wed, 02 Mar 2022 06:06:11 GMT  
		Size: 25.8 MB (25846564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddb18afd468c4e249aedf8719e751877be45fa14ac0d479283809c26a3dfbd2`  
		Last Modified: Wed, 02 Mar 2022 06:06:09 GMT  
		Size: 864.6 KB (864596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f6687fec34825acae4943f5244aa04b9620598c589a4a0706382ca33293260`  
		Last Modified: Wed, 02 Mar 2022 06:06:08 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bf615cc2e292fe02f8ece568a342177350d5d3d6381ba4bdcf7c46fe097191`  
		Last Modified: Thu, 10 Mar 2022 22:21:11 GMT  
		Size: 251.2 MB (251226917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.1.3` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:22e732fa57daadc8c0a86a2f8e926df91874df87a0e8879e137218d3f573a3f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322860961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77804b141fe90681f3a9d1520f8b84e8673602746cb59a3740e3b04140f7ad79`
-	Default Command: `["R"]`

```dockerfile
# Tue, 01 Mar 2022 02:14:14 GMT
ADD file:cbb42efeafc90355fa8bb2f4086fc68a85686edc4a2fb940867860ea9f3797c6 in / 
# Tue, 01 Mar 2022 02:14:16 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:03:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 01 Mar 2022 22:03:06 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 01 Mar 2022 22:03:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:03:18 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 01 Mar 2022 22:03:19 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 01 Mar 2022 22:03:20 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Mar 2022 22:03:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 10 Mar 2022 22:41:43 GMT
ENV R_BASE_VERSION=4.1.3
# Thu, 10 Mar 2022 22:42:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Mar 2022 22:42:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3b9af4702f1c1636210e0d50f4406bf330b6072cdb5105da7e5e3217f6bfcf4f`  
		Last Modified: Tue, 01 Mar 2022 02:23:04 GMT  
		Size: 54.7 MB (54704462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4aefd52631f0f9ed4b226660f2e049936f3d6269418f5d5ce443f982425c30`  
		Last Modified: Tue, 01 Mar 2022 22:04:57 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b227c88136054f59a2d2f5237d59486e49b1965f40a0f3dd16e746fff35f6f7d`  
		Last Modified: Tue, 01 Mar 2022 22:04:58 GMT  
		Size: 25.8 MB (25834937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410de4a0e340d934dad5a056c596eaccaae7e9584593c1cbfcb300cea27c12d9`  
		Last Modified: Tue, 01 Mar 2022 22:04:55 GMT  
		Size: 864.6 KB (864613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03bcf6d57e24c9f6e5396b3f4c4b041229f13875c060e7b6000d059c8a4a28c`  
		Last Modified: Tue, 01 Mar 2022 22:04:55 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cadeaf2c5bb8964e1e12f8f814e9750b5c25028c3a8748abd84b482b2d75c1`  
		Last Modified: Thu, 10 Mar 2022 22:43:44 GMT  
		Size: 241.5 MB (241454741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:edd8c51e8bd9faafae457900c579569fe75f33cbbf50c74b8a520f2058c96735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:2bc4b435dc278c9fd3f80835dee88a8c117cd7ca21c414696c879608e1b1d6db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333704428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7ea19c65d1b3ccec31a341db7ae56bd457f9406fc84940a55de6b07e0263d4`
-	Default Command: `["R"]`

```dockerfile
# Tue, 01 Mar 2022 02:16:21 GMT
ADD file:3bd81adfd714a4198480d282bb0361dcd321e2117c15e2fed68196a62ee3c209 in / 
# Tue, 01 Mar 2022 02:16:22 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 06:04:53 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 02 Mar 2022 06:04:54 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 02 Mar 2022 06:05:03 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 06:05:06 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 02 Mar 2022 06:05:06 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 02 Mar 2022 06:05:06 GMT
ENV LANG=en_US.UTF-8
# Wed, 02 Mar 2022 06:05:06 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 10 Mar 2022 22:19:50 GMT
ENV R_BASE_VERSION=4.1.3
# Thu, 10 Mar 2022 22:20:33 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Mar 2022 22:20:35 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b487f29e2f74d18c9e1d4ce1d18f5bc5c85ecf2dd3be54c2302e10505af8c8d6`  
		Last Modified: Tue, 01 Mar 2022 02:23:36 GMT  
		Size: 55.8 MB (55764029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059c826793480c91be73bd7c9e7242de79d68253a388bd7a5fc295253a70a55f`  
		Last Modified: Wed, 02 Mar 2022 06:06:11 GMT  
		Size: 2.0 KB (1974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a230dbf54f3392375a71368dd70115a17a139c56a37e9f9701b01535bb3396c`  
		Last Modified: Wed, 02 Mar 2022 06:06:11 GMT  
		Size: 25.8 MB (25846564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddb18afd468c4e249aedf8719e751877be45fa14ac0d479283809c26a3dfbd2`  
		Last Modified: Wed, 02 Mar 2022 06:06:09 GMT  
		Size: 864.6 KB (864596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f6687fec34825acae4943f5244aa04b9620598c589a4a0706382ca33293260`  
		Last Modified: Wed, 02 Mar 2022 06:06:08 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bf615cc2e292fe02f8ece568a342177350d5d3d6381ba4bdcf7c46fe097191`  
		Last Modified: Thu, 10 Mar 2022 22:21:11 GMT  
		Size: 251.2 MB (251226917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:22e732fa57daadc8c0a86a2f8e926df91874df87a0e8879e137218d3f573a3f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322860961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77804b141fe90681f3a9d1520f8b84e8673602746cb59a3740e3b04140f7ad79`
-	Default Command: `["R"]`

```dockerfile
# Tue, 01 Mar 2022 02:14:14 GMT
ADD file:cbb42efeafc90355fa8bb2f4086fc68a85686edc4a2fb940867860ea9f3797c6 in / 
# Tue, 01 Mar 2022 02:14:16 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:03:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 01 Mar 2022 22:03:06 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 01 Mar 2022 22:03:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:03:18 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 01 Mar 2022 22:03:19 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 01 Mar 2022 22:03:20 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Mar 2022 22:03:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 10 Mar 2022 22:41:43 GMT
ENV R_BASE_VERSION=4.1.3
# Thu, 10 Mar 2022 22:42:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Mar 2022 22:42:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3b9af4702f1c1636210e0d50f4406bf330b6072cdb5105da7e5e3217f6bfcf4f`  
		Last Modified: Tue, 01 Mar 2022 02:23:04 GMT  
		Size: 54.7 MB (54704462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4aefd52631f0f9ed4b226660f2e049936f3d6269418f5d5ce443f982425c30`  
		Last Modified: Tue, 01 Mar 2022 22:04:57 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b227c88136054f59a2d2f5237d59486e49b1965f40a0f3dd16e746fff35f6f7d`  
		Last Modified: Tue, 01 Mar 2022 22:04:58 GMT  
		Size: 25.8 MB (25834937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410de4a0e340d934dad5a056c596eaccaae7e9584593c1cbfcb300cea27c12d9`  
		Last Modified: Tue, 01 Mar 2022 22:04:55 GMT  
		Size: 864.6 KB (864613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03bcf6d57e24c9f6e5396b3f4c4b041229f13875c060e7b6000d059c8a4a28c`  
		Last Modified: Tue, 01 Mar 2022 22:04:55 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cadeaf2c5bb8964e1e12f8f814e9750b5c25028c3a8748abd84b482b2d75c1`  
		Last Modified: Thu, 10 Mar 2022 22:43:44 GMT  
		Size: 241.5 MB (241454741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:f53da4aefd8b6b071c67be5aa546a00ac18ac0f0a5fd721306cc250b47791308
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331258562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38c6122bf106259ac425175bbd5be321ef5cc14bd8e9c211d0c50b5790ef839`
-	Default Command: `["R"]`

```dockerfile
# Wed, 26 Jan 2022 01:50:20 GMT
ADD file:38c73ba90be6f58e3639e5d4ebbb9b3f61fb845729ac0dca30389f1f8d2c32e2 in / 
# Wed, 26 Jan 2022 01:50:26 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 19:32:00 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 26 Jan 2022 19:32:16 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 26 Jan 2022 19:33:18 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 19:33:34 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 26 Jan 2022 19:33:37 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 26 Jan 2022 19:33:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 26 Jan 2022 19:33:50 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 26 Jan 2022 19:33:52 GMT
ENV R_BASE_VERSION=4.1.2
# Wed, 26 Jan 2022 19:33:56 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 26 Jan 2022 19:43:09 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 19:43:15 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:abb89d61badc571bdc7c4a161a7fc8463ac6b8eb973d6aeff716f76edb833ccf`  
		Last Modified: Wed, 26 Jan 2022 02:04:40 GMT  
		Size: 59.9 MB (59942294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f98cc64611d20b5b17e209530e22cb03248662a71c794504223ead272ae0c1`  
		Last Modified: Wed, 26 Jan 2022 19:43:34 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1633471432381a6ab516416379d1f7d161e5f46874e8919ff1f29d640b75e09a`  
		Last Modified: Wed, 26 Jan 2022 19:43:35 GMT  
		Size: 26.1 MB (26075299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbce397a55206c93376b1cfff032b1e6dc6bc7f3bccd99a288a51bdb6967fbf`  
		Last Modified: Wed, 26 Jan 2022 19:43:31 GMT  
		Size: 864.6 KB (864617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbf3d094059f2ed583df5aa6ba2ad42de8d6bde8411844bc1a4c1f6813b5b51`  
		Last Modified: Wed, 26 Jan 2022 19:43:31 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2441e84b7966f74f2c0460540d64df9e80cacb01c10ed22a1d548fc5173be9`  
		Last Modified: Wed, 26 Jan 2022 19:43:31 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc258d97a0498066c434f084a1e8b8174b0213328f71c9433e9b60c1a1a341a`  
		Last Modified: Wed, 26 Jan 2022 19:44:09 GMT  
		Size: 244.4 MB (244373822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:e53613fba064a29a8ae33b9c87bf7927bafc07eaa7877258a116e2e920d5b2e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297940226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a85192dada6cba43a8e652bd9ac5b8519890dd91d90bb70c7801f628d6be628`
-	Default Command: `["R"]`

```dockerfile
# Tue, 01 Mar 2022 02:04:00 GMT
ADD file:674969e6126779bfa143207845528923901c01711a6471c08e874b71260a2f41 in / 
# Tue, 01 Mar 2022 02:04:03 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 15:20:32 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 01 Mar 2022 15:20:33 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 01 Mar 2022 15:20:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 15:20:44 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 01 Mar 2022 15:20:44 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 01 Mar 2022 15:20:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Mar 2022 15:20:44 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 01 Mar 2022 15:20:45 GMT
ENV R_BASE_VERSION=4.1.2
# Tue, 01 Mar 2022 15:20:45 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Tue, 01 Mar 2022 15:21:27 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 15:21:34 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:fa3fc208bf283f64691e90f68e0932fa4d979c605b3bd3db327d9014d601764a`  
		Last Modified: Tue, 01 Mar 2022 02:09:32 GMT  
		Size: 54.0 MB (54006950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ecddba89851dad7a6e99dfaf31da88691f9223e2c307dbcbd6729c06b81539`  
		Last Modified: Tue, 01 Mar 2022 15:21:50 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248d2141b02ddf02d31a2993cc63718b51e58331562ce9e9587870d6b197cb02`  
		Last Modified: Tue, 01 Mar 2022 15:21:51 GMT  
		Size: 25.9 MB (25860360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34951adf2c32fb6697d4ed4cc302f3d64320f7bb32965f77ecc4b036700b1a7`  
		Last Modified: Tue, 01 Mar 2022 15:21:49 GMT  
		Size: 920.2 KB (920188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9160918a90c4210013a7129e046edc102c751e398bdd673b056bdc6db9b7bb`  
		Last Modified: Tue, 01 Mar 2022 15:21:49 GMT  
		Size: 346.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa78b755686ab914e647ddf9ced925687ff716035b4087f9fc794f42de06119`  
		Last Modified: Tue, 01 Mar 2022 15:21:49 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2aa72665267257acc2eddf512a0b4ed265ff8e5998e8440fc7adc7bc1a4874`  
		Last Modified: Tue, 01 Mar 2022 15:22:09 GMT  
		Size: 217.2 MB (217150112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

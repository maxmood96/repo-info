<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.1.3`](#r-base413)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.1.3`

```console
$ docker pull r-base@sha256:84a5e6036457d021b9dd9e4b19f921eae44d65b4a1c46e9d832ba7cff8a05191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

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

### `r-base:4.1.3` - linux; ppc64le

```console
$ docker pull r-base@sha256:5e6a72a06d3879561e8e2ce49f663c8e6fa6d9365feced6d12b750fa850d1ea6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332607075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cf81f4c2dacf4efb5118b43bb9a1a1b1674ae0221d1b1370c65e8f04711e0b`
-	Default Command: `["R"]`

```dockerfile
# Tue, 01 Mar 2022 02:09:22 GMT
ADD file:ecbae239a294b05483b5400d24edacdf29c149c700631f2b5532a4a4abb2b6ae in / 
# Tue, 01 Mar 2022 02:09:28 GMT
CMD ["bash"]
# Thu, 10 Mar 2022 23:21:53 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 10 Mar 2022 23:22:11 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Thu, 10 Mar 2022 23:23:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Mar 2022 23:23:29 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 10 Mar 2022 23:23:32 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 10 Mar 2022 23:23:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Mar 2022 23:23:45 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 10 Mar 2022 23:23:47 GMT
ENV R_BASE_VERSION=4.1.3
# Thu, 10 Mar 2022 23:28:27 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Mar 2022 23:28:30 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:91cc91972e5f07c31b49a5a17e3b7279431ecfbd12c3ad333e61d0c4e87d015b`  
		Last Modified: Tue, 01 Mar 2022 02:19:12 GMT  
		Size: 60.2 MB (60166284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a0955d2c2093b20b4c45852a4b0f829df51dcdeb5f834a7e7df11274002f6`  
		Last Modified: Thu, 10 Mar 2022 23:28:53 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5aa08a78211ead422ae45055878430a17d8b5d3d15a91c43e16c3ab5f3ffad`  
		Last Modified: Thu, 10 Mar 2022 23:28:57 GMT  
		Size: 26.1 MB (26072832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95885dc25aee61fe1033948bd912ec236a71398bb38ae94846a6325bdf6e5dea`  
		Last Modified: Thu, 10 Mar 2022 23:28:53 GMT  
		Size: 864.6 KB (864605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d032eb699f4c40bae8a1e40eff05983f8a771c8ba7901fb3498377390656d751`  
		Last Modified: Thu, 10 Mar 2022 23:28:53 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f14a07fcee751f93fa04fb18b559136faf2f928270f8cd206a61493911194e`  
		Last Modified: Thu, 10 Mar 2022 23:29:33 GMT  
		Size: 245.5 MB (245501014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.1.3` - linux; s390x

```console
$ docker pull r-base@sha256:ce2d80f672c847e92519298bd02359c527629a6868e266b085954ca53b4ce227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298336660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b391f34fecbb12836e367acb8f3930d845d13c09ec0dfadcddfbf2be90b580`
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
# Thu, 10 Mar 2022 22:43:27 GMT
ENV R_BASE_VERSION=4.1.3
# Fri, 11 Mar 2022 16:42:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Mar 2022 16:42:45 GMT
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
	-	`sha256:ca46d46c9a11106b2993b4768e86f4ac2ed91674f0f58a59b4a839eb03ce68fb`  
		Last Modified: Fri, 11 Mar 2022 16:43:26 GMT  
		Size: 217.5 MB (217546838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:84a5e6036457d021b9dd9e4b19f921eae44d65b4a1c46e9d832ba7cff8a05191
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
$ docker pull r-base@sha256:5e6a72a06d3879561e8e2ce49f663c8e6fa6d9365feced6d12b750fa850d1ea6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332607075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cf81f4c2dacf4efb5118b43bb9a1a1b1674ae0221d1b1370c65e8f04711e0b`
-	Default Command: `["R"]`

```dockerfile
# Tue, 01 Mar 2022 02:09:22 GMT
ADD file:ecbae239a294b05483b5400d24edacdf29c149c700631f2b5532a4a4abb2b6ae in / 
# Tue, 01 Mar 2022 02:09:28 GMT
CMD ["bash"]
# Thu, 10 Mar 2022 23:21:53 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 10 Mar 2022 23:22:11 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Thu, 10 Mar 2022 23:23:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Mar 2022 23:23:29 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 10 Mar 2022 23:23:32 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 10 Mar 2022 23:23:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Mar 2022 23:23:45 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 10 Mar 2022 23:23:47 GMT
ENV R_BASE_VERSION=4.1.3
# Thu, 10 Mar 2022 23:28:27 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Mar 2022 23:28:30 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:91cc91972e5f07c31b49a5a17e3b7279431ecfbd12c3ad333e61d0c4e87d015b`  
		Last Modified: Tue, 01 Mar 2022 02:19:12 GMT  
		Size: 60.2 MB (60166284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a0955d2c2093b20b4c45852a4b0f829df51dcdeb5f834a7e7df11274002f6`  
		Last Modified: Thu, 10 Mar 2022 23:28:53 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5aa08a78211ead422ae45055878430a17d8b5d3d15a91c43e16c3ab5f3ffad`  
		Last Modified: Thu, 10 Mar 2022 23:28:57 GMT  
		Size: 26.1 MB (26072832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95885dc25aee61fe1033948bd912ec236a71398bb38ae94846a6325bdf6e5dea`  
		Last Modified: Thu, 10 Mar 2022 23:28:53 GMT  
		Size: 864.6 KB (864605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d032eb699f4c40bae8a1e40eff05983f8a771c8ba7901fb3498377390656d751`  
		Last Modified: Thu, 10 Mar 2022 23:28:53 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f14a07fcee751f93fa04fb18b559136faf2f928270f8cd206a61493911194e`  
		Last Modified: Thu, 10 Mar 2022 23:29:33 GMT  
		Size: 245.5 MB (245501014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:ce2d80f672c847e92519298bd02359c527629a6868e266b085954ca53b4ce227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298336660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b391f34fecbb12836e367acb8f3930d845d13c09ec0dfadcddfbf2be90b580`
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
# Thu, 10 Mar 2022 22:43:27 GMT
ENV R_BASE_VERSION=4.1.3
# Fri, 11 Mar 2022 16:42:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Mar 2022 16:42:45 GMT
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
	-	`sha256:ca46d46c9a11106b2993b4768e86f4ac2ed91674f0f58a59b4a839eb03ce68fb`  
		Last Modified: Fri, 11 Mar 2022 16:43:26 GMT  
		Size: 217.5 MB (217546838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
